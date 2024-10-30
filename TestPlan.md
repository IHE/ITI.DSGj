This Test Plan page is a prototype. We expect the maturity of the content will improve over time. For now, we summarize high level testing scope and available tools. Comments are welcome.

## Introduction
The Document Digital Signature (DSG) Profile defines general purpose methods of digitally signing of documents for communication and persistence. The DSG test plan focuses on the conformance of the actors to the capabilities described in the profile.

## High-level Test Scope

### Content Creator
- The Content Creator is able to create a digitally signed document using one of the available options.

### Content Consumer
- The Content Consumer is able to validate the digitally signed document for integrity, authenticity, and authentication of the identity of the signer.

### Prerequisites
- Certificate Authority with certificates issued to Content Creator actors
- Timestamp authority (which may be external to the connectathon environment)

## Integration Test Procedure (Interoperability Testing)
This section defines test cases in the context of paired actors testing against each other. Integration testing is often limited by the capability of the actors which might support only a subset of the semantics REQUIRED. Full message semantics and failure-modes are generally more thoroughly exercises with unit (conformance) tests, not presently covered here.

### Content Creator Test Definition
- Option Tested: JSON Detached Signature
- GIVEN that the Content Creator is properly configured:
  - Certificate is issued based on an agreed trust
  - Timestamp server is configured on an agreed trustable timestamp server configuration
- THEN the Content Creator is able to successfully generate a JSON Detached Signature document using the test steps outlined
- AND communicated to a Content Consumer

#### Test Steps
  - Content Creator creates a DSG document according to the recommendations in Volume 3:5.10.3
  - The XDS Metadata is prepared according to Volume 3:5.10.6; which results in a new DocumentEntry holding the DSG, with association relationships to the signed document DocumentEntry
  - The content is published using a grouped Document Sharing Transport (e.g. XDS) and thus communicated to a Content Consumer



### Content Consumer Test Definitions

#### Test Case 1: JSON Detached Signature with valid JWS JSON object
- GIVEN that the Content Consumer is properly configured:
  - Trusts one or more Certificate Authorities, including the one the Content Creator used
  - Trusts one or more timestamp authorities, including the one that Content creator used
- WHEN the Content Creator shares a signed document 
- THEN the Content Consumer is able to validate the signed document using SHA256 and verifies that the JWS JSON object itself has integrity through verifying the signature

#### Test Case 2: JSON Detached Signature with a signer that is not authentic
- GIVEN that the Content Consumer is properly configured:
  - Trusts one or more Certificate Authorities, including the one the Content Creator used
  - Trusts one or more timestamp authorities, including the one that Content creator used
- WHEN the Content Creator shares a signed document 
- THEN the Content Consumer is able to validate the signer of the document was inauthentic as none of the public keys available to the consumer can be used to validate the signature

#### Test Case 3: JSON Detached Signature with a revoked public key
- GIVEN that the Content Consumer is properly configured:
  - Trusts one or more Certificate Authorities, including the one the Content Creator used
  - Trusts one or more timestamp authorities, including the one that Content creator used
- WHEN the Content Creator shares a signed document 
- THEN the Content Consumer is able to verify that the certificate used to sign the documents appears in CRL/OCSP responses as revoked

#### Test Case 4: JSON Detached Signature with contents that were modified post signature
- GIVEN that the Content Consumer is properly configured:
  - Trusts one or more Certificate Authorities, including the one the Content Creator used
  - Trusts one or more timestamp authorities, including the one that Content creator used
- WHEN the Content Creator shares a signed document 
- THEN the Content Consumer is able to validate that the hash of the documents doesn't match the hash of signed Documents received and that they were modified post signature
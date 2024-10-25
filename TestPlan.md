This Test Plan page is a prototype. We expect the maturity of the content will improve over time. For now, we summarize high level testing scope and available tools. Comments are welcome.

## Introduction
The Document Digital Signature (DSG) Profile defines general purpose methods of digitally signing of documents for communication and persistence. The DSG test plan focuses on the conformance of the actors to the capabilities described in the profile.

## High-level Test Scope

### Content Creator
- The Content Creator is able to create a digitally signed document using one of the available options.

### Content Consumer
- The Content Consumer is able to validate the digitally signed document for integrity, authenticity, and authentication of the identity of the signer.

## Integration Test Procedure (Interoperability Testing)
This section defines test cases in the context of paired actors testing against each other. Integration testing is often limited by the capability of the actors which might support only a subset of the semantics REQUIRED. Full message semantics and failure-modes are generally more thoroughly exercises with unit (conformance) tests, not presently covered here.

### Content Creator Test Definition
- Option Tested: JSON Detached Signature
- Given Test Data, the Content Creator is able to successfully generate a JSON Detached Signature document using the test steps outlined.
Test Steps
  - Using the following bundle as test data:  https://build.fhir.org/ig/HL7/fhir-ips/Bundle-IPS-examples-Bundle-01.json 
  - Prepare Payload content to be signed by calculating base64-urlencoded digest value of the payload using RS256
  - Preparing the JWS Protected Header as per 5.10.2.1 Protected Header
  - Preparing the input for Signature Value Computation as BASE64URL(UTF8(JWS Protected Header)) || '.' || ''
  - Computing the Signature Value using RS256
  - Creating an electronic timestamp with a timestamp authority
  - Creating an unprotected header that includes the timestamp token generated as 'sigTst'
  - Creating the final JWS JSON Object representation with protected, header and signature members

### Content Consumer Test Definition
- Option Tested: JSON Detached Signature
- Given a JWS JSON Object, the Content Consumer is able to validate the signed document using SHA256.
  - There are three levels of signature verification:
    - verifying that the JWS JSON object itself has integrity through verifying the signature,
    - confirming that the signer was authentic, not revoked, and appropriate to the signature purpose, and
    - confirming that the signed Documents of interest are unmodified using the hash algorithm
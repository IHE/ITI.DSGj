# ITI.DSGj

DSG with JSON signature

- Volume 1 changes to [1:37 Document Digital Signature (DSG)](ch-37.html)
- Volume 3 changes to [3:5.5 Document Digital Signature (DSG) Document Content](ch-5.5.html)

## Zulip Chat

Discussion on zulip chat stream - https://chat.fhir.org/#narrow/stream/179223-ihe/topic/IHE-DSG.20using.20JSON.20Signature

## Open Issues

#### 1. Notes about deviation from profile are not being stated in the DSGj profile.
It is presumed that the deviations from profile will yield implementations non conformant to this profile and that doesn't need to be explicitly stated. Repeated below are the comments that are removed from the chapter.

<p><strong>Removed Paragraph Content</strong></p>
   <span><i>
   "Note that Content Creators and Content Consumers should be capable of being configured to other conformance policies to support local policy. For example, some environments may choose a different <mark>JAdES</mark> profile, hashing algorithm, policy identifier, or signature purpose vocabulary. Content Creators would thus create Digital Signature blocks that are not conformant to this profile. Content Consumers can validate these Digital Signature blocks, and be capable of configured behavior according to the local policy. Deviations from these guidelines would need to be expressed in site policy and would be enumerated in the JWS-Signature block. For example, some environments may choose a different hashing algorithm, policy identifier, or signature purpose vocabulary. Some regions also require conformance to ISO 17090, which includes additional Certificate issuing, content, and validation rules."
   </i></span>

#### 2. Usage of DSG with MHDS would not be covered as DSG does not address signature for a FHIR Bundle

## Issues Identified in XML DSG chapter 5.5

#### 1. Notes about deviation from profile to be reviewed if they need to be present

#### 2. The requirement of "Shall use the canonicalization algorithm “Canonical XML 1.1 with Comments” ( http://www.w3.org/2006/12/xml-c14n11#WithComments )." needs to be reviewed
 <span>The JADES specification is proposing that the signature is applied across a bytestream and makes no assumptions about the canonicalization applied and that canonicalization recommendations are made consistent by PCC dev1</span>

#### 3. Table 5.5.2-1: Digital Signature Purposes from ASTM E1762-95(2013) to be replaced by FHIR Signature Type Value Set
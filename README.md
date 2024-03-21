# ITI.DSGj

DSG with JSON signature

- Volume 1 changes to [1:37 Document Digital Signature (DSG)](ch-37.html)
- Volume 3 changes to [3:5.5 Document Digital Signature (DSG) Document Content](ch-5.5.html)

## Zulip Chat

Discussion on zulip chat stream - https://chat.fhir.org/#narrow/stream/179223-ihe/topic/IHE-DSG.20using.20JSON.20Signature

## Open Issues

#### 1. Notes about deviation from profile are not being state in the DSGj profile.
It is presumed that the deviations from profile will yield implementations non conformant to this profile and that doesn't need to be explicitly stated. Repeated below are the comments that are removed from the chapter.

<p><strong>Removed Paragraph Content</strong></p>
   <span><i>
   "Note that Content Creators and Content Consumers should be capable of being configured to other conformance policies to support local policy. For example, some environments may choose a different <mark>JAdES</mark> profile, hashing algorithm, policy identifier, or signature purpose vocabulary. Content Creators would thus create Digital Signature blocks that are not conformant to this profile. Content Consumers can validate these Digital Signature blocks, and be capable of configured behavior according to the local policy. Deviations from these guidelines would need to be expressed in site policy and would be enumerated in the JWS-Signature block. For example, some environments may choose a different hashing algorithm, policy identifier, or signature purpose vocabulary. Some regions also require conformance to ISO 17090, which includes additional Certificate issuing, content, and validation rules."
   </i></span>


## Issues Identified XML DSG

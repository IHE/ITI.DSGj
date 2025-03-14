
**Integrating the Healthcare Enterprise**

**[IHE ITI](https://profiles.ihe.net/ITI)**

**Technical Framework Supplement**

**Document Digital Signature (DSG) addition of JSON Signature**

**Revision 2.1 - Trial Implementation**

Date: November 21, 2024

Author: ITI Technical Committee

Email: iti@ihe.net

**Please verify you have the most recent version of this document.** See [here](http://profiles.ihe.net/ITI) for Trial Implementation and Final Text versions and [here](https://profiles.ihe.net/ITI/#1.3) for Public Comment versions.

**Foreword**

This is a supplement to the IHE IT Infrastructure Technical Framework. Each supplement undergoes a process of public comment and trial implementation before being incorporated into the volumes of the Technical Frameworks.

This supplement is published on November 21, 2024 for trial implementation and may be available for testing at subsequent IHE Connectathons. The supplement may be amended based on the results of testing. Following successful testing it will be incorporated into the IT Infrastructure Technical Framework. Comments are invited and can be submitted using the [ITI Public Comment form](http://www.ihe.net/ITI_Public_Comments/) or by creating a [GitHub Issue](https://github.com/IHE/ITI.DSGj/issues/new?assignees=&labels=&template=public-comment-issue-template.md&title=). 

Discussion on [zulip chat stream: IHE DSG using JSON signature](https://chat.fhir.org/#narrow/stream/179223-ihe/topic/IHE-DSG.20using.20JSON.20Signature).

This supplement describes changes to the existing technical framework documents.

"Boxed" instructions like the sample below indicate to the Volume Editor how to integrate the relevant section(s) into the relevant Technical Framework volume.

| **Editor: Please amend Section X.X by the following** |
|------------------------------------------------------|

Where the amendment adds text, make the added text **<ins>bold underline</ins>**. Where the amendment removes text, make the removed text **~~bold strikethrough~~**. When entire new sections are added, introduce with editor's instructions to "add new text" or similar, which for readability are not bolded or underlined.

General information about IHE can be found at [http://www.ihe.net](http://www.ihe.net).

Information about the IHE IT Infrastructure domain can be found at [https://www.ihe.net/IHE_Domains](https://www.ihe.net/IHE_Domains/).

Information about the organization of IHE Technical Frameworks and Supplements and the process used to create them can be found at [https://www.ihe.net/resources/profiles](https://www.ihe.net/resources/profiles/) and [https://www.ihe.net/about_ihe/ihe_process](https://www.ihe.net/about_ihe/ihe_process/).

The current version of the IHE Technical Framework can be found at [https://profiles.ihe.net](https://profiles.ihe.net/).

# Introduction to This Supplement

## Problem Statement

This profile is motivated by customer requirements for Document Digital Signatures (DSG) to use signing technology using JSON encoding vs the XML-Signature currently supported in DSG profile.

# Open Issues and Questions

1. [Notes about deviation from profile are not being stated in the DSGj profile.](https://github.com/IHE/ITI.DSGj/issues/13)
1. [The usage of DSGj with MHD(ITI-105) is not covered by the DSGj chapter.](https://github.com/IHE/ITI.DSGj/issues/14)
1. [DSGj does not contain guidance around homeCommunityID](https://github.com/IHE/ITI.DSGj/issues/15)
1. [Provision of a JSON Schema file](https://github.com/IHE/ITI.DSGj/issues/31)

# Closed Issues

1. Will update the XML-Signature content module using a CP as some more clear descriptions have been written for the JSON Signature content module that would benefit the XML-Signature content module. These are not breaking changes.
1. Added examples after Public-Comment - [see ITI-Info DSG examples](https://github.com/IHE/ITI-Info/tree/master/examples/DSG)

# IHE Technical Frameworks General Introduction
The [IHE Technical Framework General Introduction](https://profiles.ihe.net/GeneralIntro/) is shared by all of the IHE domain technical frameworks. Each technical framework volume contains links to this document where appropriate.

## 9 Copyright Licenses
IHE technical documents refer to, and make use of, a number of standards developed and published by several standards development organizations. Please refer to the IHE Technical Frameworks General Introduction, [Section 9 - Copyright Licenses](https://profiles.ihe.net/GeneralIntro/ch-9.html) for copyright license information for frequently referenced base standards. Information pertaining to the use of IHE International copyrighted materials is also available there.

## 10 Trademark
IHE® and the IHE logo are trademarks of the Healthcare Information Management Systems Society in the United States and trademarks of IHE Europe in the European Community. Please refer to the IHE Technical Frameworks General Introduction, [Section 10 - Trademark](https://profiles.ihe.net/GeneralIntro/ch-10.html) for information on their use.

# IHE Technical Frameworks General Introduction Appendices
The [IHE Technical Framework General Introduction Appendices](https://profiles.ihe.net/GeneralIntro/) are components shared by all of the IHE domain technical frameworks. Each technical framework volume contains links to these documents where appropriate. 

| **Editor: Please update the following appendices to the General Introduction as indicated below. Note that these are not appendices to this domain's Technical Framework but rather, they are appendices to the IHE Technical Frameworks General Introduction located [here](https://profiles.ihe.net/GeneralIntro/index.html).**
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

## Appendix A - Actors

| **Editor: Please add the following new or modified actors to the [IHE Technical Frameworks General Introduction Appendix A](https://profiles.ihe.net/GeneralIntro/ch-A.html):** |
|-----------------------------------------------------------------------------------------------------------------------------|

&nbsp; 

| New or Modified Actor Name                                   | Definition                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------|
| No new actors          |                                                              |

&nbsp;

## Appendix B - Transactions

| **Editor: Please add the following new or modified transactions to the [IHE Technical Frameworks General Introduction Appendix B](https://profiles.ihe.net/GeneralIntro/ch-B.html):** |
|-----------------------------------------------------------------------------------------------------------------------------|

&nbsp;

|New or Modified Transaction Name and Number                                   | Definition                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------|
| No new transactions                           |                                                                                                    |

&nbsp;

## Appendix D - Glossary

| **Editor: Please add the following new or modified terms to the [IHE Technical Frameworks General Introduction Appendix D](https://profiles.ihe.net/GeneralIntro/ch-D.html):** |
|-----------------------------------------------------------------------------------------------------------------------------|

&nbsp;  

| Term                                   | Definition                                                                                         |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------|
| No new terms          |                                                              |

&nbsp;

# The DSG JSON Signature Changes

- Volume 1 changes to [1:37 Document Digital Signature (DSG)](./Volume1/ch-37.html)
- Volume 3 add [3:5.10 Document Digital Signature (DSG) JSON Signature Document Content](./Volume3/ch-5.10.html)
- Draft of a [Test Plan for JSON Signature option](https://github.com/IHE/ITI.DSGj/blob/main/TestPlan.md)

# IANA Considerations

IANA is requested to register the following in the “JSON Web Signature and Encryption Header Parameters” registry:

Header Parameter Name: iheSSId

Header Parameter Description: The iheSSId header parameter's value shall specify the SubmissionSet.uniqueId as per the https://profiles.ihe.net/ITI/TF/Volume3/ch-4.2.html#4.2.3.3.12.

Header Parameter Usage Location: JWS

Change Controller: IHE ITI

Specification document: https://profiles.ihe.net/ITI/DSGj/Volume3/ch-5.10.html#5.10

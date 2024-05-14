
**Integrating the Healthcare Enterprise**

**[IHE ITI](https://profiles.ihe.net/ITI)**

**Technical Framework Supplement**

**Document Digital Signature (DSG) addition of JSON Signature**

**Revision 2.0 - Draft for Public Comment**

Date: May 17, 2024

Author: ITI Technical Committee

Email: iti@ihe.net

**Please verify you have the most recent version of this document.** See [here](http://profiles.ihe.net/ITI) for Trial Implementation and Final Text versions and [here](https://profiles.ihe.net/ITI/#1.3) for Public Comment versions.

**Foreword**

This is a supplement to the IHE IT Infrastructure Technical Framework. Each supplement undergoes a process of public comment and trial implementation before being incorporated into the volumes of the Technical Frameworks.

This supplement is published on May 17, 2024 for public comment Comments are invited and can be submitted using the [ITI Public Comment form](http://www.ihe.net/ITI_Public_Comments/) or by creating a [GitHub Issue](https://github.com/IHE/ITI.DSGj/issues/new?assignees=&labels=&template=public-comment-issue-template.md&title=).

Discussion on [zulip chat stream: IHE DSG using JSON signature](https://chat.fhir.org/#narrow/stream/179223-ihe/topic/IHE-DSG.20using.20JSON.20Signature)

This supplement describes changes to the existing technical framework documents.

"Boxed" instructions like the sample below indicate to the Volume Editor how to integrate the relevant section(s) into the relevant Technical Framework volume.

| **Editor: Please amend Section X.X by the following** |
|------------------------------------------------------|

Where the amendment adds text, make the added text **<ins>bold underline</ins>**. Where the amendment removes text, make the removed text **~~bold strikethrough~~**. When entire new sections are added, introduce with editor's instructions to "add new text" or similar, which for readability are not bolded or underlined.

General information about IHE can be found at [http://www.ihe.net](http://www.ihe.net).

Information about the IHE IT Infrastructure domain can be found at [https://www.ihe.net/IHE_Domains](https://www.ihe.net/IHE_Domains/).

Information about the organization of IHE Technical Frameworks and Supplements and the process used to create them can be found at [https://www.ihe.net/resources/profiles](https://www.ihe.net/resources/profiles/) and [https://www.ihe.net/about_ihe/ihe_process](https://www.ihe.net/about_ihe/ihe_process/).

The current version of the IHE Technical Framework can be found at [https://profiles.ihe.net/](https://profiles.ihe.net/).

# Introduction to This Supplement

## Problem Statement

This profile is motivated by customer requirements for Document Digital Signatures (DSG) to use signing technology using JSON encoding vs the XML-Signature currently supported in DSG profile.

# Open Issues and Questions

1. [Notes about deviation from profile are not being stated in the DSGj profile.](https://github.com/IHE/ITI.DSGj/issues/13)
2. [The usage of DSGj with MHD(ITI-105) is not covered by the DSGj chapter.](https://github.com/IHE/ITI.DSGj/issues/14)
3. [DSGj does not contain guidance around homeCommunityID](https://github.com/IHE/ITI.DSGj/issues/15)
4. [Will add examples after Public-Comment](https://github.com/IHE/ITI.DSGj/issues/19) 

# Closed Issues

- Will update the XML-Signature content module using a CP as some more clear descriptions have been written for the JSON Signature content module that would benefit the XML-Signature content module. These are not breaking changes.

# IHE Technical Frameworks General Introduction
The [IHE Technical Framework General Introduction](https://profiles.ihe.net/GeneralIntro/) is shared by all of the IHE domain technical frameworks. Each technical framework volume contains links to this document where appropriate.

## 9 Copyright Licenses
IHE technical documents refer to, and make use of, a number of standards developed and published by several standards development organizations. Please refer to the IHE Technical Frameworks General Introduction, Section 9 - [Copyright Licenses](https://profiles.ihe.net/GeneralIntro/ch-9.html) for copyright license information for frequently referenced base standards. Information pertaining to the use of IHE International copyrighted materials is also available there.

## 10 Trademark
IHE® and the IHE logo are trademarks of the Healthcare Information Management Systems Society in the United States and trademarks of IHE Europe in the European Community. Please refer to the IHE Technical Frameworks General Introduction, Section 10 - [Trademark] (https://profiles.ihe.net/GeneralIntro/ch-10.html) for information on their use.

# IHE Technical Frameworks General Introduction Appendices
The [IHE Technical Framework General Introduction Appendices](https://profiles.ihe.net/GeneralIntro/) are components shared by all of the IHE domain technical frameworks. Each technical framework volume contains links to these documents where appropriate. 

| **Editor: Please update the following appendices to the General Introduction as indicated below. Note that these are not appendices to this domain's Technical Framework but rather, they are appendices to the IHE Technical Frameworks General Introduction located [here] (https://profiles.ihe.net/GeneralIntro/index.html.)**
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

## IHE Technical Framework General Introduction Appendix A: Actors

| **Editor: Please add the following new or modified actors to the [IHE Technical Frameworks General Introduction Appendix A](https://profiles.ihe.net/GeneralIntro/ch-A.html):** |

|-----------------------------------------------------------------------------------------------------------------------------|

| New or Modified Actor Name                                   | Definition                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------|
| No new actors          |                                                              |

## IHE Technical Framework General Introduction Appendix B: Transactions

| **Editor: Please add the following new or modified transactions to the [IHE Technical Frameworks General Introduction Appendix B](https://profiles.ihe.net/GeneralIntro/ch-B.html):** |
|-----------------------------------------------------------------------------------------------------------------------------|

|New or Modified Transaction Name and Number                                   | Definition                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------|
| No new transactions                           |                                                                                                    |

## IHE Technical Framework General Introduction Appendix D: Glossary

| **Editor: Please add the following new or modified terms to the [IHE Technical Frameworks General Introduction Appendix D](https://profiles.ihe.net/GeneralIntro/ch-D.html):** |
|-----------------------------------------------------------------------------------------------------------------------------|

&nbsp;  

| Term                                   | Definition                                                                                         |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------|
| No new terms          |                                                              |

&nbsp;

# The DSG JSON Signature changes

- Volume 1 changes to [1:37 Document Digital Signature (DSG)](./Volume1/ch-37.html)
- Volume 3 add [3:5.10 Document Digital Signature (DSG) JSON Signature Document Content](./Volume3/ch-5.10.html)


# EUDI Wallet Reference Implementation - Feature Map

A consolidated overview of the user functionality provided by the EUDI Wallet Reference Implementation, along with links to relevant functional and technical documentation. 


## Table of Contents
1. [Overview](#-overview)
2. [Standards, Protocols & Formats](#-standards-protocols-and-formats)
3. [Features](#-features)
4. [Supported Attestations](#-supported-attestations)
5. [Business Demos](#-business-demos)
6. [Releases](#-releases)  
 
## 🧭 Overview

The EUDI Wallet Reference Implementation, developed under the Architecture Reference Framework, showcases how citizens can securely identify, authenticate, and sign electronically using common EU standards. It is built on a modular design with reusable components that evolve over time and can support multiple projects. Below you can find an overview of the features and functionalities delivered by the EUDI Wallet Reference Implementation. 

## 📐 Standards, Protocols and Formats

The EUDI Wallet is supported by a defined set of standards and technical specifications considered essential for its implementation. These form the minimum foundation needed to ensure secure issuance, presentation, authentication, signing, and certification of digital identity credentials.

❗For a comprehensive set of standards and technical specifications (STS), you may visit the [Essential Standards and Technical Specifications (STS)](https://eu-digital-identity-wallet.github.io/eudi-doc-architecture-and-reference-framework/latest/technical-specifications/) section of the ARF.

In relation to credential formats, the following table indicates the formats supported by the EUDI Wallet Reference Implementation. 

| Format | Status | Description | 
|:-------|:-------|:------------|
| `mso_mdoc` | Published (ISO/IEC 18013-5) | Credential format based on ISO/IEC 18013-5 using a signed Mobile Security Object (MSO) to bind and protect data elements. Supports selective disclosure. | 
| `SD-JWT-VC` | Draft (IETF / OpenID Foundation) | Credential format extending JSON Web Tokens with selective disclosure for web-native verifiable credentials. | 


## 🧩 Features

The following table provides a high-level overview of the key user functionalities supported by the EUDI Wallet Reference Implementation.

| Features        | Description                                 | Status     | 
|:--------------------|:--------------------------------------------|:----------:|
| [**Issuance**](#issuance)            | Issuance of verifiable credentials          | In Progress|
| [**Presentation**](#presentation)        | Presentation of verifiable credentials       | In Progress|
| [**rQES**](#rqes) | Electronic signing with EUDI Wallet    | Completed |
| [**Transaction Logs**](#transaction-logs) | Log of historic transactions executed by the EUDI Wallet         | In Progress|
| [**Request data deletion from RPs**](#request-data-deletion-from-rps) | Users requesting data deletion from Relying Parties they have previously interacted with     |Planned |
| [**Report unlawful or suspicious requests to DPA(s)**](#report-unlawful-or-suspicious-requests) | Users reporting suspicious data requests to national Data Protection Authorities   |Planned |
| [**Attestation Revocation**](#attestation-revocation) | Revoking issued attestations         | Completed |
| [**Pseudonyms**](#pseudonyms)        | Using pseudonyms (i.e. passkeys) for authentication         | Planned |
| [**Wallet Revocation**](#wallet-revocation) | Revoking wallet instance         | Planned  |
| [**Wallet to Wallet interaction**](#wallet-to-wallet) | Enabling the exchange of PID/attestations between two EUDI Wallets       | Planned|
| [**Wallet Backup and Restore**](#wallet-backup-and-restore) | Supporting  procedures for backing up and restoring attestations of an EUDI Wallet       | Planned |
| [**Migrate to a different wallet**](#migrate-to-a-different-wallet) | Supporting  procedures for migrating attestations to a different EUDI Wallet      |Planned |
| [**Support for ZKP**](#support-for-zkp) | Supporting  Zero-Knowledge Proofs in EUDI Wallet interactions      |Planned|

You can explore the [EUDI Wallet Reference Implementation Roadmap](https://github.com/orgs/eu-digital-identity-wallet/projects/24) to explore further details in relation to the features and enhancements that are currently being developed or planned for future implementation.


The following sections elaborate on the detailed features supported by the EUDI Wallet Reference Implementation, grouped by functional area.

### _Issuance_ 

<details>
  <summary>Covers applicable issuance flows in alignment with OpenID4VCI. Expand to explore detailed functional specifications for the 'Issuance' capabilities.</summary>   

_The 'Issuance' functionality is aligned with the OpenID4VCI protocol and as such is being continuously updated in alignment with the [evolving standards and protocols](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/64)._


| Feature                         | Description                              |   Status     |
|:---------------------------------|:-------------------------------|:------------:|
| [Deferred Issuance](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/40) | Issue credentials with a deferred process            |  Completed |
| [Credential Offer](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/42)                  | Supporting issuer-initiated flows      |   Completed |
| [Pre-authorisation code flow](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/41)                  | Issuance decoupled from the user's authorisation, as it is performed outside of the issuance flow  |  Completed|
| [Batch Issuance](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/18)                  | Issuance of multiple instances of the same credential type     | Completed|
| [Attestation Re-Issuance](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/52)                  | Enabling the re-issuance of PID/attestation before its expiration.     | Planned|
| [Alignment to latest version of the standard](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/64)                  | Enhancements to issuance functionalities as detailed by the latest version of the OpenID4VCI standard.     | In Progress|
| [Alignment to latest version of the HAIP profile](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/69)                  | Enhancements to issuance, remote presentation and trust management as detailed by the HAIP v1.0 profile.  | Planned|


</details>

---
### _Presentation_

<details>
  <summary>Covers applicable presentation flows in alignment with OpenID4VP and ISO/IEC 18013-5. Expand to explore detailed functional specifications for the 'Presentation' capabilities.</summary>
  

_The 'Presentation' functionality is aligned with the OpenID4VP protocol (for remote presentation flows) and as such is being continuously updated in alignment with the [evolving standards and protocols](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/64)._

| Feature                         | Description                              |   Status     |
|:---------------------------------|:-------------------------------|:------------:|
| [Remote Same-device presentation](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/64)         | User uses a web browser or another application on the device on which the Wallet Unit is installed to share attestations to a requesting Relying Party         | Completed       |
| [Remote Cross-device presentation](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/64)         |  User uses a web browser on a device other than the device on which their Wallet Unit is installed to share attestations to a requesting Relying Party          |Completed       |
| [Proximity presentation](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/64)         | User and their device are physically near the Relying Party Instance, and PIDs and attestations are exchanged via proximity technologies (e.g., NFC, Bluetooth), either under human supervision (Supervised) or directly to a machine without supervision (Unsupervised)          |  Completed     |
| [Digital Credential API](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/34)         | The Digital Credentials API enables the secure presentation of attestations from the EUDI Wallet, leveraging the web browser for the presentation flow        |  Planned       |
| [Proximity Verifier](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/43)         | Implementation of an open source verifier application for Android, supporting stakeholders for developing their own proximity reader solutions       |  Completed       |
| [Alignment to latest version of the standard](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/64)                  | Enhancements to presentation functionalities as detailed by the latest version of the OpenID4VP standard (v1.0).     | Completed|

</details>

---
### _rQES_

<details>
  <summary>Covers scenarios for Remote qualified signatures. Expand to explore detailed functional specifications for the 'rQES' capabilities.</summary>

| Feature                         | Description                              |  Status     |
|:------------------------------|:--------------------------------|:------------:|
| [Wallet-Driven rQES (external SCA)](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/15)       | Remote qualified signatures in a Wallet-driven model, utilising an external 'Signature Creation Application'          | Completed       |
| [Wallet-Driven rQES (internal SCA)](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/27)        | Remote qualified signatures in a Wallet-driven model, utilising an internal (i.e. wallet component) 'Signature Creation Application'              | Completed       |
| [RP-Driven rQES (internal SCA)](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/16)       | Remote qualified signatures in a RP-driven model              | Completed      |
| [Document Retrieval (Wallet-Driven flows)](https://github.com/eu-digital-identity-wallet/eudi-doc-reference-implementation-architecture/issues/45)        | In a 'wallet-centric' model for rQES, a foreseen scenario includes the retrieval of the document to be signed from the corresponding Relying Party, instead of retrieving the document from the device's file system.             | Completed      |

</details>

---
### _Pseudonyms_

<details>
  <summary>Utilising passkeys through the EUDI Wallet for authentication purposes. Expand to explore detailed functional specifications for the 'Pseudonyms' capabilities.</summary>


| Feature                         | Description                              | Status     |
|:-----------------------------|:-------------------------------------|:------------:|
| [Pseudonym functionality](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/26)        | Pseudonyms allow EUDI Wallet users to be identified by service provider/relying parties without revealing any personal information.         |  Planned        |

</details>

---
### _Transaction Logs_

<details>
  <summary>EUDI Wallet Privacy Dashboard provides a record of transactions (i.e. data exchanges) executed through the EUDI Wallet. Expand to explore detailed functional specifications for the 'Transaction Logs (Privacy Dashboard)' capabilities.</summary>


| Feature                         | Description                              |  Status     |
|:-----------------------------|:------------------------------------|:-----------:|
| [Transaction Logs (Privacy Dashboard)](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/22) | EUDI Wallet Privacy Dashboard provides a record of transactions (i.e. data exchanges) executed through the EUDI Wallet. Transaction logs ensure a higher degree of transparency, privacy and control of the User over their personal data      | Completed       |


</details>

---

### _Request data deletion from RPs_

<details>
  <summary> Users requesting data deletion from Relying Parties they have previously interacted with. </summary>


| Feature                         | Description                              | Status     |
|:----------|:-------------------|:-------:|
|[Request Data Deletion](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/31)| Users request the deletion of their personal attributes from Relying Parties with which they have interacted through their Wallet Unit.  | Planned  |


</details>

---

### _Report unlawful or suspicious requests_

<details>
  <summary> Users report a Relying Party to the competent national Data Protection Authority where an allegedly unlawful or suspicious request for data is received. </summary>


| Feature                         | Description                              |Status     |
|:----------|:-------------------|:-------:|
|[Report unlawful or suspicious requests](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/32)| Users, through the Wallet Unit, report a Relying Party to the competent national Data Protection Authority where an allegedly unlawful or suspicious request for data is received.|Planned     |


</details>

---

### _Attestation Revocation_

<details>
  <summary>Attestations revoked by the issuer. Expand to explore detailed functional specifications for the 'Attestation Revocation' capabilities.</summary>

| Feature                         | Description                              |  Status     |
|:---------------------|:--------------------------|:------------:|
| [Handling attestation revocation](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/4)|  Attestation revocation support for the reference implementation including support from the issuer, verifier and wallet |   Completed       |

</details>

---
### _Wallet Revocation_

<details>
  <summary>Wallet instance revoked by the wallet provider. Expand to explore detailed functional specifications for the 'Wallet Revocation' capabilities.</summary>


| Feature                         | Description        |  Status     |
|:-------------|:--------------------|:------:|
| [Wallet instance revocation](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/28)| TBC          |  Planned   |

</details>

---

### _Wallet to Wallet_

<details>
  <summary> An EUDI Wallet User can request from another EUDI Wallet User to share an attestation of attributes using their EUDI Wallet Instances in proximity. Expand to explore detailed functional specifications for 'Wallet to Wallet' interaction capabilities.</summary>
  

| Feature                         | Description         | Status     |
|:--------------|:--------------|:----------:|
|[Wallet to Wallet](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/30)| An EUDI Wallet User can request from another EUDI Wallet User to share an attestation of attributes using their EUDI Wallet Instances in a proximity setting.   | Planned |


</details>

---
### _Wallet Backup and Restore_

<details>
  <summary> Backing up and restoring attestations of an EUDI Wallet. Expand to explore detailed functional specifications for 'Backup and Restore' interaction capabilities. </summary>


| Feature                         | Description                              | Status     |
|:-----------|:------------------|:--------:|
|[Wallet Backup & Restore](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/5)| Procedures for backing up the attestations a wallet unit contains.  | Planned   |

</details>

---
### _Migrate to a different wallet_

<details>
  <summary> Migrating attestations to a different EUDI Wallet. Expand to explore detailed functional specifications for 'Migration' capabilities. </summary>


| Feature                         | Description                              |  Status     |
|:----------|:-------------------|:-------:|
|[Migrate to a different wallet](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/33)| Procedures for migrating backed-up attestations of a wallet unit to a different Wallet Solution.   |  Planned |


</details>

---



### _Support for ZKP_

<details>
  <summary> Supporting Zero-Knowledge Proofs </summary>


| Feature                         | Description                              |  Status     |
|:----------|:-------------------|:-------:|
|[Support for Zero Knowledge Proof](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/56)| Supporting Zero-Knowledge Proofs in EUDI Wallet interactions| Planned  |


</details>

---

## 📂 Supported Attestations

The following table provides an overview of the key attestations supported by the EUDI Wallet Reference Implementation.

| Attestation                         | Description                              |  Status     |
|:-----------------------|:----------------------------|:-----------:|
| [PID](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/67) | Support for the 'Person Identification Data (PID)' in alignment with the [PID Rulebook](https://github.com/eu-digital-identity-wallet/eudi-doc-attestation-rulebooks-catalog/blob/main/rulebooks/pid/pid-rulebook.md) | Completed|
| [mDL](https://eu-digital-identity-wallet.github.io/eudi-doc-architecture-and-reference-framework/latest/annexes/annex-3/annex-3.02-mDL-rulebook/) | Support for the 'Mobile Driving License' in alignment with the [mDL Rulebook](https://github.com/eu-digital-identity-wallet/eudi-doc-attestation-rulebooks-catalog/blob/main/rulebooks/mdl/mdl-rulebook.md)         |  Completed       |
| [EHIC](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/45) | Support for the 'European Health Insurance Card'           |  Completed       |
| [PDA1](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/46) | Support for the 'Portable Document A1'           |  Completed       |

For further attestations supported by the EUDI Wallet Reference Implementation you can check our [Issuer](https://github.com/eu-digital-identity-wallet/eudi-srv-web-issuing-eudiw-py).

## 💼 Business Demos

### _Business Demos_

A set of demo implementations mocking business flows in different contexts are available, aiming to showcase the EUDI Wallet functionalities in real-life scenarios. 

| Business Scenario                         | Description                              |  Status     |
|:-----------|:-----------------|:---------:|
|[Travel](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/6)| A 'Travel Use Case’ implementation for the EUDI Wallet which showcases the utilization of the EUDI Wallet in a ‘Travel’ business scenario, where the EUDI Wallet is used for several purposes, such as presenting attestations (remotely and in proximity) as well as digitally signing documents.    | Completed       |
|[Cross-border recruitment](https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/issues/55)| A ‘Cross-Border Recruitment Use Case’ implementation for the EUDI Wallet which showcases the utilization of the EUDI Wallet in a ‘Cross-Border Recruitment’ business scenario, where the EUDI Wallet is used for several purposes, such as presenting attestations (remotely and in proximity) when applying/on-boarding for a job, as well as digitally signing job contract.       | In Progress       |

## 📦 Releases
The latest published versions of the key EUDI Wallet Reference Implementation components are summarised below:

| Component                | Release |
|:-------------------------|:-------:|
| EUDI Wallet app (Android) | [![Latest Android Wallet UI](https://img.shields.io/github/v/release/eu-digital-identity-wallet/eudi-app-android-wallet-ui?label=Latest%20Android%20Wallet%20UI)](https://github.com/eu-digital-identity-wallet/eudi-app-android-wallet-ui/releases) |
| EUDI Wallet app (iOS)     | [![Latest iOS Wallet UI](https://img.shields.io/github/v/release/eu-digital-identity-wallet/eudi-app-ios-wallet-ui?label=Latest%20iOS%20Wallet%20UI)](https://github.com/eu-digital-identity-wallet/eudi-app-ios-wallet-ui/releases) |
| Remote Verifier           | [![Latest Remote Verifier](https://img.shields.io/github/v/release/eu-digital-identity-wallet/eudi-web-verifier?label=Latest%20Remote%20Verifier)](https://github.com/eu-digital-identity-wallet/eudi-web-verifier/releases) |
| Issuer (Python)           | [![Latest Issuer Python](https://img.shields.io/github/v/release/eu-digital-identity-wallet/eudi-srv-web-issuing-eudiw-py?label=Latest%20Issuer%20Python)](https://github.com/eu-digital-identity-wallet/eudi-srv-web-issuing-eudiw-py/releases) |
| Issuer (Kotlin)           | [![Latest Issuer Kotlin](https://img.shields.io/github/v/release/eu-digital-identity-wallet/eudi-srv-pid-issuer?label=Latest%20Issuer%20Kotlin)](https://github.com/eu-digital-identity-wallet/eudi-srv-pid-issuer/releases) |
| Proximity Verifier        | [![Latest Proximity Verifier](https://img.shields.io/github/v/release/eu-digital-identity-wallet/eudi-app-multiplatform-verifier-ui?label=Latest%20Verifier%20UI)](https://github.com/eu-digital-identity-wallet/eudi-app-multiplatform-verifier-ui/releases) |



You can refer to the [EUDI Wallet Reference Implementation Roadmap](https://github.com/orgs/eu-digital-identity-wallet/projects/24) to view further details on the release roadmap.









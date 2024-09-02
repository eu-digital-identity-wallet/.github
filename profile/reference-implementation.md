:memo: [EUDI Wallet Reference Implementation](#eudi-wallet-reference-implementation) :question:[FAQ](#frequently-asked-questions) :computer: [Repositories](#repositories) :wrench:[How to Use](#how-to-use) :heavy_exclamation_mark: [Disclaimer](#disclaimer) :information_source:[About the project](#about-the-project)

![Reference Implementation for Digital Identity for all Europeans](https://raw.githubusercontent.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/main/docs/media/top-banner-ri.png)

# EUDI Wallet Reference Implementation 

## Overview

The EUDI Wallet Reference Implementation is built based on the [Architecture Reference Framework](https://github.com/eu-digital-identity-wallet/architecture-and-reference-framework) and aims at showcasing a robust and interoperable platform for digital identification, authentication and electronic signatures based on common standards across the European Union.

The EUDI Wallet Reference Implementation is based on a modular architecture composed of a set of business agnostic, re-usable components which will be evolved in incremental steps and can be re-used across multiple projects.
Specifically, as part of the EUDI Wallet Reference Implementation, the following set of components are being delivered:

- [Libraries and other software components needed to the framework](#libraries)
- [Demo EUDI Wallet mobile native applications for issuing, proximity and remote flows](#wallet-ui-app-and-demo-app-for-android-and-ios)
- [Verifier mobile native applications and web-services for proximity and remote flows](#verifier-apps-and-services)
- [Issuer applications and web-services](#issuing-apps-and-services)

Please refer to our documentation and repositories listed in the following sections for more detailed information on how to get started, contribute, and engage with the EUDI Wallet Reference Implementation.

## Functional Scope

The current scope of the EUDI Wallet Reference Implementation includes first iterations of key functionalities: Issuing, Sharing and Presenting Personal Identification Data (PID) and Mobile Driving License (mDL) in Remote and Proximity scenarios. Based on these functionalities, a broad set of Use Cases are supported as a minimum, such as:

- Mobile Driving License
- Accessing online public and private services
- Opening a bank account
- SIM registration
- Payment authorisation
- Authenticating a third-party service to sign documents
- Etc.

<Details open>
 <summary><i>Functional Scope Remarks </i></summary>

As of June 2024, the following remarks shall be considered in relation to the provided functionalities.

### Remote Presentation

- Same-device and cross-device flows for online authentication and authorization (OpenID4VP (draft 20) transferring mDoc for remote authentication and authorisation)
- Applicable platforms: Android, iOS

### Proximity Sharing

- Using QR/BLE proximity protocols
- NFC tag for device engagement support (static hand-over)
- Applicable platforms: Android, iOS

### Issuing

- An implementation of a credential issuing service, according to OpenId4VCI (draft 13) (provides test PID and mDL issuing service in mDoc and soon in SD-JWT-VC format)

</Details>

## Frequently Asked Questions

[Frequently Asked Questions](https://github.com/eu-digital-identity-wallet/.github/blob/main/profile/FAQ.md) about the EUDI Wallet Reference Implementation.


# Repositories

This section provides an overview of the key repositories of the EUDI Reference Implementation. The table below acts as navigation aid to find the information you are looking for. $\color{red}{\text{Red coloured repositories}}$ refer to both iOS and Android implementations, $\color{grey}{\text{grey coloured repositories}}$ refer to iOS implementation, and $\color{green}{\text{green coloured repositories}}$ refer to Android implementation.

## Libraries

### $\color{red}{\text{Wallet Core (Android) and Wallet Kit (iOS) Coordinator Libraries}}$

| Repository          | Description                                                                   | 
|---------------|-------------------------------------------------------------------------------|
| [Wallet Core (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-android-wallet-core) | Implementation of the EUDI Wallet Core library for Android that serves as a coordinator layer between the UI app and the Wallet libraries. Currently, coordinates issuing, proximity and remote presentation libraries.|
| [Wallet Kit (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-wallet-kit) | Implementation of the EUDI Wallet Kit library for iOS that serves as a coordinator layer between the UI app and the Wallet libraries. Currently coordinates issuing, proximity and remote presentation libraries.      |

### $\color{grey}{\text{Proximity Sharing iOS Libraries}}$

| Repository          | Description                                                                   | 
|---------------|-------------------------------------------------------------------------------|
| [mDoc Security (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-iso18013-security)      | Implementation of mDoc security mechanisms according to ISO/IEC 18013-5.       |
| [mDoc Data Transfer (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-iso18013-data-transfer) | Implementation of the mDoc data-transfer library according to ISO/IEC 18013-5. | 
| [mDoc Data Model (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-iso18013-data-model)    | Implementation of the mDoc data-model according to ISO/IEC 18013-5.           | 


### $\color{green}{\text{Proximity Sharing Android Libraries}}$

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [mDoc Data Transfer (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-android-iso18013-data-transfer) | This library provides a set of classes to manage the transfer of documents in an EUDI ISO 18013-5 Android Wallet. |

### $\color{grey}{\text{Remote Presentation iOS Libraries}}$

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [Presentation Exchange (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-presentation-exchange-swift)        | Implementation of DIF Presentation Exchange v2 specification in Swift.     | 
| [SIOPv2 & OpenID4VP protocols (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-siop-openid4vp-swift) | Implementation of SIOPv2 and OpenID4VP (draft 20) protocols (wallet's role) in Swift. |
| [SD-JWT (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-sdjwt-swift)                       | SD-JWT library for creating and verifying SD-JWT in JVM Swift.             | 


### $\color{green}{\text{Remote Presentation Android Libraries}}$

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [Presentation Exchange (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-presentation-exchange-kt)        | Implementation of DIF Presentation Exchange v2 specification in Kotlin.     |
| [SIOPv2 & OpenID4VP protocols (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-siop-openid4vp-kt) | Implementation of SIOPv2 and OpenID4VP (draft 20) protocols (wallet's role) in Kotlin. | 
| [SD-JWT (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-sdjwt-kt)                        | SD-JWT library for creating and verifying SD-JWT in JVM Kotlin.             | 

### $\color{grey}{\text{Ιssuing iOS Libraries}}$

| Repository          | Description                                                                   | 
|---------------|-------------------------------------------------------------------------------|
| [OpenId4VCI (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-openid4vci-swift) | Implementation of credential management supporting the OpenId4VCI (draft 13) protocol. | 

### $\color{green}{\text{Ιssuing Android Libraries}}$

| Repository          | Description                                                                   | 
|---------------|-------------------------------------------------------------------------------|
| [OpenId4VCI (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-jvm-openid4vci-kt)      | Implementation of credential management supporting the OpenId4VCI (draft 13) protocol.|

### $\color{grey}{\text{Wallet Data Storage and Cryptographic Management iOS Libraries}}$

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [mDoc Document Storage (iOS)](https://github.com/eu-digital-identity-wallet/eudi-lib-ios-wallet-storage) |  Storage for keys and wallet documents |

### $\color{green}{\text{Wallet Data Storage and Cryptographic Management Android Libraries}}$

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [mDoc Document Storage (Android)](https://github.com/eu-digital-identity-wallet/eudi-lib-android-wallet-document-manager)    | This library provides a set of classes to manage documents and their cryptographic keys in an EUDI Android Wallet. |

## $\color{red}{\text{Wallet UI App and demo App for Android and iOS}}$

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [UI / Demo App (Android)](https://github.com/eu-digital-identity-wallet/eudi-app-android-wallet-ui) | Implementation of wallet UI app for Android. Currently, it also includes Demo App, demonstrating the following capabilities: Proximity presentation, Same Device Online Authentication and issuing of PID and mDL.	 |
| [UI / Demo App (iOS)](https://github.com/eu-digital-identity-wallet/eudi-app-ios-wallet-ui) | Implementation of wallet UI app for iOS. Currently, it also includes Demo App, demonstrating the following capabilities: Proximity presentation, and Same Device Online Presentation and issuing of PID and mDL.| 

## Verifier Apps and Services

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [Web Verifier](https://github.com/eu-digital-identity-wallet/eudi-web-verifier)               | Demo Web Verifier UI application (Frontend) that acts as a Verifier/RP trusted end-point. Available at [https://verifier.eudiw.dev](https://verifier.eudiw.dev)  |  
| [Restful API (web-services)](https://github.com/eu-digital-identity-wallet/eudi-srv-web-verifier-endpoint-23220-4-kt)             | Demo Web Verifier application (Backend Restful service) that acts as a Verifier/RP trusted end-point.| 

## Issuing Apps and Services

| Repository          | Description                                                                   |
|---------------|-------------------------------------------------------------------------------|
| [OpenId4VCI issuer (Python)](https://github.com/eu-digital-identity-wallet/eudi-srv-web-issuing-eudiw-py)               | An implementation of a credential issuing service, according to OpenId4VCI (draft 13), in Python. Available at https://issuer.eudiw.dev/  |  
| [OpenId4VCI issuer (Kotlin)](https://github.com/eu-digital-identity-wallet/eudi-srv-pid-issuer)             | An implementation of a credential issuing service, according to OpenId4VCI (draft 13), in JVM Kotlin. Available at  https://issuer-backend.eudiw.dev/ | 

# Get started

<table><td>
<img src="https://raw.githubusercontent.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/main/docs/media/get-started.png" lat ="Get Started with Digital Identity for all Europeans"/>
</td>

<td>
Instructions for installing and using the applicable applications/libraries can be found in the corresponding 'ReadMe' files, i.e.:

- [Build your Demo App (Android)](https://github.com/eu-digital-identity-wallet/eudi-app-android-wallet-ui) assists on installing the mobile wallet application on Android phones. There is also information on how to actually start developing extensions on the Android platform implementation. 
- [Build your Demo App (iOS)](https://github.com/eu-digital-identity-wallet/eudi-app-ios-wallet-ui) assists on installing the mobile wallet application on iPhone. There is also information on how to actually start developing extensions on the iPhone platform implementation. 
- [Verifier for Remote Presentation](https://verifier.eudiw.dev/) assists on testing the wallet application using an online verifier. 
  - **Note:** external link to web verifier app
- [App Verifier for Proximity (Android)](https://install.appcenter.ms/orgs/eu-digital-identity-wallet/apps/mdoc-verifier-testing/distribution_groups/eudi%20verifier%20(testing)%20public) assists on installing a verifier application for testing proximity case on the wallet application.
  - **Note:** external link to APK download
- [Issuer Application](https://issuer.eudiw.dev/) assists on issuing attestations for the wallet application.
  - **Note:** external link to issuer app

</td></table>

# Disclaimer

The released software is a initial development release version: 

- The initial development release is an early endeavor reflecting the efforts of a short timeboxed period, and by no means can be considered as the final product.  
- The initial development release may be changed substantially over time, might introduce new features but also may change or remove existing ones, potentially breaking compatibility with your existing code.
- The initial development release is limited in functional scope.
- The initial development release may contain errors or design flaws and other problems that could cause system or other failures and data loss.
- The initial development release has reduced security, privacy, availability, and reliability standards relative to future releases. This could make the software slower, less reliable, or more vulnerable to attacks than mature software.
- The initial development release is not yet comprehensively documented. 
- Users of the software must perform sufficient engineering and additional testing in order to properly evaluate their application and determine whether any of the open-sourced components is suitable for use in that application.
- We strongly recommend not putting this version of the software into production use.
- Only the latest version of the software will be supported

# About the project

Links for additional information:  

- [Electronic Identification](https://digital-strategy.ec.europa.eu/en/policies/electronic-identification)  
- [Q&A Digital Identity Regulation Proposal](https://digital-strategy.ec.europa.eu/en/faqs/qa-digital-identity-regulation-proposal)  
- [European Digital Identity Wallet Toolbox Process](https://digital-strategy.ec.europa.eu/en/policies/eudi-wallet-toolbox)  
- [European Digital Identity Wallet Pilot implementation (Prototype and Large Scale Pilots)](https://digital-strategy.ec.europa.eu/en/policies/eudi-wallet-implementation)  

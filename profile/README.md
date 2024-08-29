
[Digital Strategy](https://digital-strategy.ec.europa.eu//en)> [Policies](https://digital-strategy.ec.europa.eu/en/policies)>[Electronic Identification](https://digital-strategy.ec.europa.eu//en/policies/electronic-identification)

![Digital Identity for all Europeans - A personal digital wallet for EU citizens and residents](https://raw.githubusercontent.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/main/docs/media/top-banner.png)

# EU Digital Identity Wallet 
## Digital Identity Regulation

Under the [Electronic Identification, Authentication and Trust Services (eIDAS) Regulation](https://digital-strategy.ec.europa.eu/en/policies/eidas-regulation), EU Member States may, on a voluntary basis, notify and recognise, national electronic identification schemes in their Member States. The recognition of notified electronic identification became mandatory in 2018.
Yet, there is no requirement for Member States to develop a national electronic identification and to make it interoperable with those in other Member States. This has led to discrepancies between countries.
The new Regulation on digital identity addresses shortcomings in eIDAS by improving the effectiveness of the framework and extending its benefits to the private sector.
Member States will offer citizens and businesses digital wallets that will be able to link various aspects of their national digital identities. These may be provided by public authorities or the private sector, if they are recognized by the Member States.

The EU Digital Identity Wallet will be:

* **made available to anyone who wants to use it**:  Any EU citizen, resident, and business in the EU who would like to make use of the EU Digital Identity will be able to do so.
* **used widely**: EU Digital Identity Wallets will be used as a way to identify users when providing them with access to public and private digital services across the EU.
* **controlled by users**: The EU Digital Identity Wallets will enable people to choose and keep track of their identity, data and certificates which they share with third parties. Anything which is not necessary to share will not be shared.

Consumers should also be able to access services online without having to use private platforms or unnecessarily sharing personal data. They will have full control of the data they share.

## Architecture and Reference Framework

On 3 June 2021, the European Commission adopted a Recommendation calling on Member States to work towards the development of a [a common toolbox](https://digital-strategy.ec.europa.eu/en/policies/eudi-wallet-toolbox) including a technical [Architecture and Reference Framework](https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/blob/main/docs/arf.md) a set of common standards and technical specifications and a set of common guidelines and best practices.

The new Regulation specifies that these outcomes will serve as a basis for the implementation of the proposal for a European Digital Identity Framework, without the process of developing the Toolbox interfering with, or prejudging the legislative process.

The new Regulation foresees that the Toolbox is developed by Member States’ experts in the eIDAS Expert Group  in close coordination with the Commission and, where relevant for the functioning of the European
Digital Identity (EUDI) Wallet infrastructure, other concerned public and private sector parties.

The current **authoritative version** is tagged as [release/tag in this repository](https://github.com/eu-digital-identity-wallet/architecture-and-reference-framework/releases).

The EUDI Wallet Reference Implementation below is built based on the [Architecture Reference Framework](https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/blob/main/docs/arf.md).

## ⭐Wallet Reference Implementation - Open Source Code

<img align="left" width="30%" src="https://raw.githubusercontent.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/main/docs/media/number1.png"/>

🚀 EUDI Wallet open source code is now available online. The journey has just started, [get started with your implementation](https://github.com/eu-digital-identity-wallet/.github/blob/main/profile/reference-implementation.md)! 

For further information on the repositories please [consult the list of repositories](https://github.com/orgs/eu-digital-identity-wallet/repositories).

Under the Digital Europe Programme, the Commission is facilitating [work to develop, implement and scale up the European Digital Identity framework](https://digital-strategy.ec.europa.eu/en/policies/eudi-wallet-implementation). The actions aim to arrive at a set of technical references, standards, components and solutions including an application of the EU Digital Identity Wallet to be made available to Member States.

The EUDI Wallet Reference Implementation aims at showcasing a robust and interoperable platform for digital identification, authentication and electronic signatures based on common standards across the European Union.

## High Level Overview

### Android Overview

A high level overview of the used repositories for the Android platform can be found in the below diagram. For further information please [consult the list of repositories](https://github.com/orgs/eu-digital-identity-wallet/repositories).

```mermaid
graph TD;
    A[eudi-app-android-wallet-ui]
    B[eudi-lib-android-wallet-core] -->  |Wallet Core|A 
    C[eudi-lib-android-wallet-document-manager] -->  |DocumentManager|B 
    D[eudi-lib-android-iso18013-data-transfer] --> |TransferManager|B 
    E[eudi-lib-jvm-openid4vci-kt] --> |OpenId4VciManager|B 
    F[eudi-lib-jvm-siop-openid4vp-kt] --> |OpenId4VpManager|B 
    G[com.android.identity:identity-credential-android] --> |SecureArea,StorageEngine|B 
    H --> D 
    I[eudi-lib-jvm-presentation-exchange] --> F 
```

### iOS Overview

A high level overview of the used repositories for the iOS platform can be found in the below diagram. For further information please [consult the list of repositories](https://github.com/orgs/eu-digital-identity-wallet/repositories).

```mermaid
graph TD;
    A[eudi-app-ios-wallet-ui]
    B[eudi-lib-ios-wallet-kit] -->  |Wallet Core|A 
    C[eudi-lib-ios-wallet-storage] -->  |Wallet Storage|B 
    D[eudi-lib-ios-iso18013-data-transfer] --> |Transfer Manager|B 
    E[eudi-lib-ios-openid4vci-swift] --> |OpenId4Vci Manager|B 
    F[eudi-lib-ios-siop-openid4vp-swift] --> |OpenId4Vp Manager|B 
    G[eudi-lib-ios-iso18013-security] --> |Mdoc Security|D 
    H[eudi-lib-ios-iso18013-data-model] --> |Mdoc Data Model|D 
    I[eudi-lib-ios-presentation-exchange-swift] --> F 
```

## Related Content

### Big Picture

[Electronic Identification](https://digital-strategy.ec.europa.eu//en/policies/electronic-identification)

Electronic identification (eID) is one of the tools to ensure secure access to online services and to carry out electronic transactions in a safer way.

[Q&A Digital Identity Regulation](https://digital-strategy.ec.europa.eu/en/faqs/qa-digital-identity-regulation-proposal)

Frequently Asked Question about the Digital Identity Regulation

#### Last update

26 July 2024

## About us

* [Privacy statement](https://digital-strategy.ec.europa.eu/en/pages/legal-notice#ecl-inpage-km0gfb8o)
* [Copyright notice ](https://digital-strategy.ec.europa.eu/en/pages/legal-notice#ecl-inpage-km0gezfs)
* [About Directorate-General CONNECT ](https://ec.europa.eu/info/departments/communications-networks-content-and-technology_en)
* [Language Policy ](https://digital-strategy.ec.europa.eu/en/pages/legal-notice#ecl-inpage-kyoexp6k)
* [Accessibility statement ](https://digital-strategy.ec.europa.eu/en/pages/accessibility)

## [European Commission website](https://commission.europa.eu/index_en)

* [Contact the European Commission](https://commission.europa.eu/about-european-commission/contact_en)
* [Follow the European Commission on social media ](https://european-union.europa.eu/contact-eu/social-media-channels_en#/search?page=0&institutions=european_commission)
* [Resources for partners](https://commission.europa.eu/resources-partners_en)
* [Language policy](https://commission.europa.eu/language-policy_en)
* [Cookies](https://commission.europa.eu/cookies_en)
* [Privacy policy](https://commission.europa.eu/privacy-policy_en)
* [Legal notice](https://commission.europa.eu/legal-notice_en)

❓[Frequently Asked Questions](#frequently-asked-questions) :email:[Contact Us](#contact-us) :information_source:[About the project](#about-the-project)

# EUDI Wallet Reference Implementation 
## Frequently Asked Questions

A list of frequently asked questions are consolidated in order to assist you with possible queries related to the EUDI Wallet Reference Implementation. Please refer to the [Architecture Reference Framework](https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/blob/main/README.md) for the corresponding technical specifications and the [EUDI Wallet Reference Implementation](https://github.com/eu-digital-identity-wallet/.github/blob/main/profile/reference-implementation.md) overview page for further information.

<Details>
 <summary>What are the specifications on which the Wallet Reference Implementation is based on?</summary> 
 
The Wallet Reference Implementation is based on the <a href="https://github.com/eu-digital-identity-wallet/architecture-and-reference-framework">Architecture Reference Framework</a>.
</Details>

<Details>
 <summary>What is the roadmap of the EUDI Wallet Reference Implementation?</summary> 

The roadmap of the EUDI Wallet reference implementation provides a transparent view of the features and enhancements that are currently being developed or planned to the future. Its purpose is to promote open communication and collaboration in our community. For further details check the <a href="https://github.com/orgs/eu-digital-identity-wallet/projects/24">Public Roadmap</a>.
</Details>

<Details>
 <summary>Is there a process allowing me to post my comments or contributions to the Wallet Reference Implementation?</summary> 

We encourage you to contribute or provide your feedback/suggestion for the EUDI Wallet Reference Implementation. Depending on the type of feedback you wish to provide, you may utilise one of the following channels:

- _Code contributions_:
Comments and contributions on the codebase of the EUDI Wallet Reference Implementation are welcomed through the corresponding Github space.
- _Roadmap suggestions_:
If you have any questions or comments about the features listed on the roadmap or wish to suggest new features, please reach out via the <a href="https://github.com/eu-digital-identity-wallet/eudi-wallet-reference-implementation-roadmap/discussions)">Discussions forum</a>.
- _Other feedback_:
A designated mailbox CNECT-EUDIW-SUPPORT@ec.europa.eu is available where any queries related to the Wallet Reference Implementation can be addressed.
</Details>

<Details>
 <summary>What are the programming languages that are being used?</summary> 
 
For Android it will mainly be Kotlin and for the iOS it will mainly be Swift (so it is the preferred native language of each platform). Other languages will also be used in the ecosystem of the EUDIW.
</Details>

<Details>
 <summary>What are the protocols supported for online – remote authentication?</summary> 
 
The baseline for the reference implementation is the ARF. Hence, we will be supporting OID4VP using the profile of ISO23220-4 Annex B.
</Details>

<Details>
 <summary>What are the protocols supported for proximity sharing?</summary> 
 
The baseline for the reference implementation is the ARF. Hence, we will be supporting ISO/IEC 18013-5.
</Details>

<Details>
 <summary>What are the protocols supported for issuing?</summary> 
 
The baseline for the reference implementation is the ARF. Hence, we will be supporting OpenId4VCI. For the currently supported version, please check the corresponding library.
</Details>

<Details>
 <summary>What are the formats that we will be using for Personal Identification Data (PID)?</summary> 
 
According to the ARF and the corresponding PID rulebook, we will be supporting both mDoc and SD-JWT format. At the momment, mDoc (CBOR) is supported. Alternative formats such as SD-JWT VC will be incorporated in a future release.
</Details>

<Details>
 <summary>What are the formats that we will be using for mDL, (Q)EAA?</summary> 
 
According to the ARF and the corresponding PID rulebook, we will be supporting both mDoc and SD-JWT format. At the momment, mDoc (CBOR) is supported. Alternative formats such as SD-JWT VC will be incorporated in a future release.
</Details>

<Details>
 <summary>What is the testing scope for the Wallet Reference Implementation?</summary> 
 
Security and units tests have been executed; details of the corresponding tests can be found in the corresponding repositories.
</Details>

## Contact Us

For any technical issues related with the code, please contact us through the “Issues” service of the corresponding GitHub Repository. For any other issues, please get in touch through: [CNECT-EUDIW-SUPPORT@ec.europa.eu](mailto:CNECT-EUDIW-SUPPORT@ec.europa.eu)

## About the project
[Read more about the project](https://ec.europa.eu/digital-building-blocks/sites/display/EUDIGITALIDENTITYWALLET)

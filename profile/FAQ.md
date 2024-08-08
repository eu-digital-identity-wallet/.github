❓ [Frequently Asked Questions](#frequently-asked-questions) :email:[Contact Us](#contact-us) :information_source:[About the project](#about-the-project)

# EUDI Wallet Reference Implementation 
## Frequently Asked Questions

A list of freqeuntly asked questions are consolidated in order to assist you with possible queries related to the EUDI Wallet Reference Implementation. Please refer to the [Architecture Reference Framework](https://github.com/eu-digital-identity-wallet/eudi-doc-architecture-and-reference-framework/blob/main/README.md) for the corresponding technical specifications and the [EUDI Wallet Reference Implementation](https://github.com/eu-digital-identity-wallet/.github/blob/main/profile/reference-implementation.md) overview page for further information.

<Details>
 <summary>**What are the specifications on which the Wallet Reference Implementation is based on?**</summary> 
 
The Wallet Reference Implementation is based on the <a href="https://github.com/eu-digital-identity-wallet/architecture-and-reference-framework">Architecture Reference Framework</a>.
</Details>

<Details>
 <summary>**Is there a process allowing me to post my comments or contributions to the Wallet Reference Implementation?**</summary> 
 
Comments and contributions on the codebase of the Wallet Reference Implementation are welcomed through the corresponding <a href="https://github.com/eu-digital-identity-wallet/architecture-and-reference-framework">Github space</a>. Additionally, a designated mailbox <a href="CNECT-EUDIW-SUPPORT@ec.europa.eu">CNECT-EUDIW-SUPPORT@ec.europa.eu</a> is available where any queries related to the Wallet Reference Implementation can be addressed.
</Details>

<Details>
 <summary>**What are the programming languages that are being used?**</summary> 
 
For Android it will mainly be Kotlin and for the iOS it will mainly be Swift (so it is the preferred native language of each platform). Other languages will also be used in the ecosystem of the EUDIW.
</Details>

<Details>
 <summary>**What are the protocols supported for online – remote authentication?** </summary> 
 
The baseline for the reference implementation is the ARF. Hence, we will be supporting OID4VP using the profile of ISO23220-4 Annex B.
</Details>

<Details>
 <summary>**What are the protocols supported for proximity sharing?** </summary> 
 
The baseline for the reference implementation is the ARF. Hence, we will be supporting ISO/IEC 18013-5.
</Details>

<Details>
 <summary>**What are the protocols supported for issuing?** </summary> 
 
The baseline for the reference implementation is the ARF. Hence, we will be supporting OpenId4VCI-draft 12.
</Details>

<Details>
 <summary>**What are the formats that we will be using for Personal Identification Data (PID)?**	</summary> 
 
According to the ARF and the corresponding PID rulebook, we will be supporting both mDoc and SD-JWT format. At the momment, mDoc (CBOR) is supported. Alternative formats such as SD-JWT VC will be incorporated in a future release end to end too.
</Details>

<Details>
 <summary>**What are the formats that we will be using for mDL, (Q)EAA?**	</summary> 
 
According to the ARF and the corresponding PID rulebook, we will be supporting both mDoc and SD-JWT format. At the momment, mDoc (CBOR) is supported. Alternative formats such as SD-JWT VC will be incorporated in a future release end to end too.
</Details>

<Details>
 <summary>**What is the testing scope for the Wallet Reference Implementation?**	</summary> 
 
Security and units tests have been executed; details of the corresponding tests can be found in the corresponding repositories.
</Details>

## Contact Us

For any technical issues related with the code, please contact us through the “Issues” service of the corresponding GitHub Repository. For any other issues, please get in touch through: [CNECT-EUDIW-SUPPORT@ec.europa.eu](mailto:CNECT-EUDIW-SUPPORT@ec.europa.eu)

## About the project
Links for additional information:  
-  [Electronic Identification](https://digital-strategy.ec.europa.eu/en/policies/electronic-identification)  
-  [Q&A Digital Identity Regulation Proposal](https://digital-strategy.ec.europa.eu/en/faqs/qa-digital-identity-regulation-proposal)  
-  [European Digital Identity Wallet Toolbox Process](https://digital-strategy.ec.europa.eu/en/policies/eudi-wallet-toolbox)  
-  [European Digital Identity Wallet Pilot implementation (Prototype and Large Scale Pilots)](https://digital-strategy.ec.europa.eu/en/policies/eudi-wallet-implementation)  

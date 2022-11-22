# Description
 
The PKI Consortium is managing a PQC Capabilities Matrix (PQCCM) of software applications, libraries and hardware that includes support for 
Post Quantum Cryptography, without endorsing their implementation or quality.

The list includes a wide variety of software applications, libraries, and hardware from different vendors. 
The list should be considered a living document and a starting point. Considering the rapid change in the area such things can vary from day to day and complete freshness of information can only be gathered from vendors directly. 

The PKI Consortium is actively working to promote the adoption of Post-Quantum Cryptography, and the capabilities matrix is a key part of that effort.

What the PQCCM do:
* collect and aggregate information on PQC capabilities across the cybersecurity landspace (vendors, software, hardware, etc..)

What the PQCCM don't do:
* review, vet, verify or test implementations or interoperability
* source code review, formal review of algorithms, etc.
* provide information, documentation or any recommended usage of Post Quantum Cryptography

No other activity besides what is listed under PQCCM DOs is under the purview of PKI Consortium (unless explicitly stated otherwise)".




# Capabilities
-----
The table lists information from vendors related to support for Post Quantum Cryptography.

| Vendor            | Capability | Date | Documentation                                                                                       | Notes |
| ----------------------- |:-----------|:-------|:----------------------------------------------------------------------------------------------------|:------|
|**HSMs**|
| Utimaco Crypto Server         |HMS, XMSS, XMSS-MT, Dilithium-128, Kyber-768, Kyber-1024| 2022-11-22   |TBD |Software simulator availabe, Dilithium in process of updated to round 3 version|
| Entrust nShield |FALCON, CRYSTALS-Dilithium, Rainbow, Picnic, SPHINCS+| 2022-11-22 | https://www.entrust.com/-/media/documentation/datasheets/entrust-pqc-option-pack-ds.pdf | The Entrust nShield Post-Quantum SDK enables post-quantum cryptographic applications for nShield HSMs with the CodeSafe SDK |
|**PKI Software**|
| Entrust PKIaaS | 	FALCON, CRYSTALS-Dilithium, SPHINCS+ | 2022-11-22 | https://www.entrust.com/digital-security/certificate-solutions/products/pki/managed-services/pki-as-a-service#:~:text=PKIaaS-,Post%2DQuantum,-Within%20the%20decade | The Entrust PKI as a Service (PKIaaS) for Post-Quantum Beta Program supports all three algorithms selected in round 3 of the NIST competition and can provide composite and pure quantum CA hierarchies |

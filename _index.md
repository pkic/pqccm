---
date: 2023-03-21T7:00:00Z
title: PQC Capabilities Matrix (PQCCM)

heroTitle: PQC Capabilities Matrix (PQCCM)
heroDescription: A list of software applications, libraries and hardware that includes support for Post Quantum Cryptography

tags:
- resource
---

The PKI Consortium is managing a PQC Capabilities Matrix (PQCCM) of software applications, libraries and hardware that includes support for 
Post Quantum Cryptography, without endorsing their implementation or quality.

The list includes a wide variety of software applications, libraries, and hardware from different vendors. 
The list should be considered a living document and a starting point. Considering the rapid change in the area such things can vary from day to day and complete freshness of information can only be gathered from vendors directly. 

The PKI Consortium is actively working to promote the adoption of Post-Quantum Cryptography, and the capabilities matrix is a key part of that effort.

**What the PQCCM does**:
* collects and aggregates information on PQC capabilities across the cybersecurity landspace (vendors, software, hardware, etc..)
* lists products that provide PQC functionality to the end user, not merely for example PQC enabled TLS access to a non PQC enabled service

No other activities besides those listed above are under the purview of PKI Consortium (unless explicitly stated otherwise).

**What the PQCCM doesn't do**:
* review, vet, verify or test implementations or interoperability
* perform source code review, formal review of algorithms, etc.
* provide information, documentation or any recommended usage of Post Quantum Cryptography

## Contribute

This list is a collaborative effort. To contribute please raise an issue or a PR on the [GitHub Repository](https://github.com/pkic/pqccm).

## Legend

|       Symbol       | Meaning                                                                | Comment                                                                                                                                                                                                                 |
| :----------------: | :--------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|        :x:         | The feature is currently not available                                 |                                                                                                                                                                                                                         |
| :heavy_check_mark: | The feature is available for usage/test now                            |                                                                                                                                                                                                                         |
|      :clock1:      | The feature is planned on the product roadmap in the coming six months | Roadmap items must not be added if they are not really scheduled to be implemented in the coming six month period. Roadmap items should be noted in the vendor section with a specific time, i.e. "Q2 2023" or similar. |

## Capabilities

The table lists information from vendors related to support for Post Quantum Cryptography.
The list below lista algorithms standardized by FIPS. The previous list listing support for draft algorithms can now be found in on the separate [draftalgorithms](draftalgorithms.md) page.

> The list is ordered alphabetically by vendor, there is no other meaning to the order.
{.callout-info}

| Vendor                                  | Product          | Category         | Last updated | [X.509 Hybrid certificates](#eferences) | [LMS](#references) | [XMSS](#references) | [ML-KEM/FIPS-203](#references) | [ML-DSA/FIPS-204](#references) | [SLH-DSA/FIPS-205](#references) |
| :-------------------------------------- | :--------------- | :--------------- | :----------- | :-------------------------------------: | :----------------: | :-----------------: | :-----------------: | :-------------------: | :----------------------: |
| [Botan](#botan)                         | Botan            | Software library |2025-02-27 |:x: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark:|
| [Bouncy Castle](#bouncy-castle)         | BC               | Software library |2025-02-27 |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark:|
| [Crypto4A](#crypto4a)                   | QxEDGE           | HSP              |2025-02-27 |:heavy_check_mark: |:heavy_check_mark:|:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |
| [Crypto4A](#crypto4a)                   | QxHSM            | HSM              |2025-02-27 |:heavy_check_mark: |:heavy_check_mark:|:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |
| [EVERTRUST](#evertrust)                 | STREAM/HORIZON   | PKI              |2025-03-03 |:heavy_check_mark:|:x:|:x:|:clock1:|:heavy_check_mark:|:clock1:|
| [Eviden](#eviden)                       | IDnomic PKI      | PKI              |2025-03-05 |:x:|:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:x:|
| [Eviden](#eviden)                     | Trustway Proteccio™ NetHSM | HSM      |2024-12-09 |:x:|:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|
| [Fortanix](#fortanix)                   | FX2200           | HSM              |2025-02-27 |:x: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |
| [InfoSec Global](#infosecglobal)        |AgileSec Analytics| Software         |2025-02-27 |:x: |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark: |
| [Keyfactor](#keyfactor)                 | SignServer       | Signing Software |2025-02-27 |:x: |:heavy_check_mark: |:x: |:x: |:heavy_check_mark: |:heavy_check_mark: |
| [Keyfactor](#keyfactor)                 | EJBCA            | PKI              |2025-02-27 |:heavy_check_mark: |:heavy_check_mark: |:x: |:heavy_check_mark: |:heavy_check_mark: |:clock1: |
| [Open Quantum Safe](#open-quantum-safe) | liboqs           | Software library |2025-02-27 |:x: |:x: |:x: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |
| [OpenSSL](#openssl) | libssl           | Software library |2025-04-15 |:x: |:x: |:x: |:heavy_check_mark: |:heavy_check_mark: |:x: |
| [Securosys](#securosys)                 | Primus HSM       | HSM              |2025-02-27 |:x: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |:heavy_check_mark: |

> **NOTE:** HSS and XMSS<sup>MT</sup> are the multi tree variants of LMS and XMSS. In the table both the simple and multi-tree versions may be supported if LMS/XMSS is checked.
{.callout-info}

## Botan
[Botan](https://github.com/randombit/botan) is a C++ cryptography library released under the permissive Simplified BSD license. It offers the tools necessary to implement a range of systems, such as TLS protocol, X.509 certificates, AEAD ciphers, PKCS#11 and TPM hardware support, password hashing, and post quantum crypto schemes.

## Bouncy Castle
Java and C# APIs with all NIST candidate support, and some older ones. [Available as open source software](https://www.bouncycastle.org/). All NIST standards are available in Java from version 1.79 and C# from version 3.0.0.

The [Bouncy Castle for kotlin](https://github.com/bcgit/bc-kotlin) open source package provides a script/command line interface for generating certificate chains with different algorithms, including hybrid certificates using X.509 section 9.8 alternative signatures. 

## Crypto4A

Crypto4A Technologies Inc. develops the crypto-agile and quantum-safe security products sold as the QxHSM™, a hardware security module (HSM) and the QxEDGE™, a hardware security platform (HSP). For more information about those products as well as the status of our FIPS 140-3 validation or CAVP algorithm list, please visit [www.crypto4a.com.

## EVERTRUST

[EVERTRUST Stream](https://evertrust.io/stream/) is a PKI CA/VA/TSA and [EVERTRUST Horizon](https://evertrust.io/horizon/) is a PKI RA and CLM software. Both products are currently able to issue and manage pure-PQC and hybrid backard-compatible certificates based on Dilithium/Falcon/Sphincs+ algorithms. Released versions have support for ML-DSA (with or without prehash), pure PQC certificates, and hybrid backward-compatible certificates as per ITU-T X.509 10/19. 
Other algorithms and some protocol support as well as PKCS#11 support is available in beta versions, as they depend on standards that are not yet published.

## Eviden
**IDnomic PKI**

The Eviden [IDnomic PKI](https://www.cryptovision.com/en/products/pki-solutions/idnomic-pki-3/) supports the published PQC algorithms standardized by NIST : ML-DSA and ML-KEM. Composite and pure quantum certificates hierarchies can be provided.

**Trustway Proteccio™ NetHSM**

The Eviden [Trustway Proteccio™ NetHSM](https://eviden.com/solutions/digital-security/data-encryption/trustway-proteccio-nethsm/) supports all common cryptographic algorithms including the PQC algorithms selected by NIST : ML-DSA, ML-KEM and SLH-DSA. 

## Fortanix

Fortanix DSM has LMS available and ML-DSA, ML-KEM and SLH-DSA on the roadmap for 2025. See [Algorithm Support](https://support.fortanix.com/hc/en-us/articles/360016160411-Algorithm-Support).

## Keyfactor
**SignServer**

SignServer performs server side signing and is capable of Post-Quantum signatures on CMS (RFC5662) messages as well as plain signatures. LMS, SLH-DSA and ML-DSA are supported from [SignServer 9.1](https://www.keyfactor.com/press-releases/keyfactor-makes-quantum-leap-with-post-quantum-pki-and-signing-capabilities/).

**EJBCA**

EJBCA PKI can create CAs and issue X.509 certificates signed using Post-Quantum algorithms. Available as open source software and containers with support for ML-DSA and ML-KEM from [EJBCA 9.1](https://www.keyfactor.com/press-releases/keyfactor-makes-quantum-leap-with-post-quantum-pki-and-signing-capabilities/).

## Open Quantum Safe

OQS is an open source software library that implements PQC [algorithms](https://openquantumsafe.org/liboqs/algorithms/), as well as integrations such as into OpenSSL.

## OpenSSL

[OpenSSL](https://openssl-library.org/) is an open source software library that implements PQC algorithms from version 3.5.

## Securosys

[Primus HSM](https://www.securosys.com/en/products/primus-hardware-security-modules-hsm), [Primus X Cyber Vault](https://www.securosys.com/en/hsm/cyber-vault) and [HSM as-a-service](https://www.securosys.com/cloud-security/cloudhsm-overview) supports all common cryptographic algorithms, blockchain procedures including the PQC algorithms selected by NIST.
Devices are under certification for FIPS140-3 Level 3 and CC EN 419221-5 (eIDAS protection profile).

## References

The following table contains references to the PQC capabilities and algorithms.

| Algorithm                                                     | Reference                                                                      |
| :------------------------------------------------------------ | :----------------------------------------------------------------------------- |
| FIPS 203 (ML-KEM)                                             | https://csrc.nist.gov/pubs/fips/203/ipd                                        |
| FIPS 204 (ML-DSA)                                             | https://csrc.nist.gov/pubs/fips/204/ipd                                        |
| FIPS 205 (SLH-DSA)                                            | https://csrc.nist.gov/pubs/fips/205/ipd                                        |
| Composite certificates                                        | https://datatracker.ietf.org/doc/draft-ounsworth-pq-composite-keys/            |
| Hybrid certificates                                           | https://datatracker.ietf.org/doc/html/draft-truskovsky-lamps-pq-hybrid-x509-01 |
| Chameleon certificates                                        | https://datatracker.ietf.org/doc/draft-bonnell-lamps-chameleon-certs/          |
| X.509 Alternative Signatures (section 9.8)                    | https://www.itu.int/rec/T-REC-X.509-201910-I                                   |
| LMS                                                           | https://www.rfc-editor.org/rfc/rfc8708.html                                    |
| XMSS                                                          | https://datatracker.ietf.org/doc/html/rfc8391                                  |
| Falcon                                                        | https://falcon-sign.info                                                       |
| Dilithium                                                     | https://pq-crystals.org/dilithium/resources.shtml                              |
| SPHINCS+                                                      | https://sphincs.org                                                            |
| Kyber                                                         | https://pq-crystals.org/kyber/index.shtml                                      |
| BIKE                                                          | https://bikesuite.org                                                          |
| McEliece                                                      | https://classic.mceliece.org                                                   |
| HQC                                                           | https://pqc-hqc.org                                                            |
| NIST Recommendation for Stateful Hash-Based Signature Schemes | [SP800-208](https://csrc.nist.gov/publications/detail/sp/800-208/final)        |

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

> The list is ordered alphabetically by vendor, there is no other meaning to the order.
{.callout-info}

| Vendor                                  | Product          | Category         | Last updated | [Composite certificates](#references) | [Hybrid certificates](#eferences) | [LMS](#references) | [XMSS](#references) | [Falcon](#references) | [Dilithium](#references) | [SPHINCS+](#references) | [Kyber](#references) | [BIKE](#references) | [McEliece](#references) | [HQC](#references) |
| :-------------------------------------- | :--------------- | :--------------- | :----------- | :-----------------------------------: | :--------------------------------: | :----------------: | :-----------------: | :-------------------: | :----------------------: | :---------------------: | :------------------: | :-----------------: | :---------------------: | :----------------: |
| [Botan](#botan)                         | Botan            | Software library | 2023-10-04   |                  :x:                  |                :x:                 |        :clock1:         | :heavy_check_mark:  |          :x:          |    :heavy_check_mark:    |           :heavy_check_mark:           |  :heavy_check_mark:  |         :x:         |   :clock1:    |        :x:         |
| [Bouncy Castle](#bouncy-castle)         | BC               | Software library | 2022-11-22   |          :heavy_check_mark:           |         :heavy_check_mark:         | :heavy_check_mark: | :heavy_check_mark:  |  :heavy_check_mark:   |    :heavy_check_mark:    |   :heavy_check_mark:    |  :heavy_check_mark:  | :heavy_check_mark:  |   :heavy_check_mark:    | :heavy_check_mark: |
| [Crypto4A](#crypto4a)                   | QxEDGE           | HSP              | 2022-12-04   |               :clock1:                |         :heavy_check_mark:         | :heavy_check_mark: | :heavy_check_mark:  |       :clock1:        |    :heavy_check_mark:    |   :heavy_check_mark:    |  :heavy_check_mark:  |         :x:         |   :heavy_check_mark:    |        :x:         |
| [Crypto4A](#crypto4a)                   | QxHSM            | HSM              | 2022-12-04   |               :clock1:                |         :heavy_check_mark:         | :heavy_check_mark: | :heavy_check_mark:  |       :clock1:        |    :heavy_check_mark:    |   :heavy_check_mark:    |  :heavy_check_mark:  |         :x:         |   :heavy_check_mark:    |        :x:         |
| [CZERTAINLY](#czertainly)               | CZERTAINLY       | Software         | 2023-02-19   |                  :x:                  |                :x:                 |        :x:         |         :x:         |  :heavy_check_mark:   |    :heavy_check_mark:    |   :heavy_check_mark:    |         :x:          |         :x:         |           :x:           |        :x:         |
| [Entrust](#entrust)                     | nShield          | HSM              | 2022-11-22   |                  :x:                  |                :x:                 |        :x:         |         :x:         |  :heavy_check_mark:   |    :heavy_check_mark:    |   :heavy_check_mark:    |         :x:          |         :x:         |           :x:           |        :x:         |
| [Entrust](#entrust)                     | PKIaaS           | PKI              | 2022-11-22   |          :heavy_check_mark:           |                :x:                 |        :x:         |         :x:         |  :heavy_check_mark:   |    :heavy_check_mark:    |   :heavy_check_mark:    |         :x:          |         :x:         |           :x:           |        :x:         |
| [EVERTRUST](#evertrust)                     | STREAM/HORIZON           | PKI              | 2023-09-07   |          :x:           |                :clock1:                 |        :x:         |         :x:         |  :clock1:   |    :clock1:    |   :clock1:    |         :x:          |         :x:         |           :x:           |        :x:         |
| [Fortanix](#fortanix)                   | FX2200           | HSM              | 2022-11-29   |                  :x:                  |                :x:                 | :heavy_check_mark: |         :x:         |       :clock1:        |         :clock1:         |        :clock1:         |         :x:          |         :x:         |           :x:           |        :x:         |
| [I4P](#i4p)                             | Trident          | HSM              | 2022-12-01   |                  :x:                  |                :x:                 |        :x:         |      :clock1:       |          :x:          |           :x:            |   :heavy_check_mark:    |  :heavy_check_mark:  |         :x:         |           :x:           |        :x:         |
| [IBM](#ibm)                             | 4769/CCA         | HSM              | 2023-01-11   |                  :x:                  |                :x:                 |        :x:         |         :x:         |          :x:          |    :heavy_check_mark:    |           :x:           |         :x:          |         :x:         |           :x:           |        :x:         |
| [IBM](#ibm)                             | Crypto Express 7S (CEX7S) / CCA/EP11| HSM              | 2023-01-22   |                  :x:                  |                :x:                 |        :x:         |         :x:         |          :x:          |    :heavy_check_mark:    |           :x:           |         :x:          |         :x:         |           :x:           |        :x:         |
| [IBM](#ibm)                             | Crypto Express 8S (CEX8S) / CCA/EP11| HSM              | 2023-01-22   |                  :x:                  |                :x:                 |        :x:         |         :x:         |          :x:          |    :heavy_check_mark:    |           :x:           |         :heavy_check_mark:      |         :x:         |           :x:           |        :x:         |
| [ISC](#isc)                             | CDK              | Software library | 2023-03-04   |                  :x:                  |                :x:                 | :heavy_check_mark: |         :x:         |  :heavy_check_mark:   |    :heavy_check_mark:    |   :heavy_check_mark:    |  :heavy_check_mark:  |         :x:         |   :heavy_check_mark:    |        :x:         |
| [ISC](#isc)                             | CertAgent        | PKI              | 2023-03-04   |                  :x:                  |                :x:                 |      :clock1:      |         :x:         |  :heavy_check_mark:   |    :heavy_check_mark:    |   :heavy_check_mark:    |  :heavy_check_mark:  |         :x:         |   :heavy_check_mark:    |        :x:         |
| [Keyfactor](#keyfactor)                 | SignServer       | Signing Software | 2022-12-19   |                  :x:                  |                :x:                 |        :heavy_check_mark:         |         :x:         |          :x:          |    :heavy_check_mark:    |   :heavy_check_mark:    |         :x:          |         :x:         |           :x:           |        :x:         |
| [Keyfactor](#keyfactor)                 | EJBCA            | PKI              | 2023-11-20   |                  :x:                  |                :clock1:          |        :x:         |         :x:         |  :heavy_check_mark:   |    :heavy_check_mark:    |           :x:           |         :x:          |         :x:         |           :x:           |        :x:         |
| [MTG AG](#mtg-ag)                       | Corporate PKI    | PKI              | 2023-09-25   |                  :x:                  |                :x:                 |        :x:         |         :x:         |  :heavy_check_mark:   |    :heavy_check_mark:    |   :heavy_check_mark:    |       :clock1:       |         :x:         |   :heavy_check_mark:    |        :x:         |
| [Open Quantum Safe](#open-quantum-safe) | liboqs           | Software library | 2022-11-30   |                  :x:                  |                :x:                 |        :x:         |         :x:         |  :heavy_check_mark:   |    :heavy_check_mark:    |   :heavy_check_mark:    |  :heavy_check_mark:  | :heavy_check_mark:  |   :heavy_check_mark:    | :heavy_check_mark: |
| [Securosys](#securosys)                 | Primus           | HSM              | 2022-11-28   |               :clock1:                |              :clock1:              |        :x:         |         :x:         |          :x:          |         :clock1:         |        :clock1:         |       :clock1:       |         :x:         |           :x:           |        :x:         |
| [Thales](#thales)                       | Luna             | HSM              | 2022-11-22   |                  :x:                  |                :x:                 | :heavy_check_mark: | :heavy_check_mark:  |          :x:          |    :heavy_check_mark:    |           :x:           |  :heavy_check_mark:  |         :x:         |           :x:           |        :x:         |
| [Utimaco](#utimaco)                     | Q-Safe           | HSM              | 2022-11-28   |                  :x:                  |                :x:                 | :heavy_check_mark: | :heavy_check_mark:  |          :x:          |    :heavy_check_mark:    |           :x:           |  :heavy_check_mark:  |         :x:         |           :x:           |        :x:         |
| [Utimaco](#utimaco)                     | u.trust Identify | PKI              | 2022-11-28   |          :heavy_check_mark:           |                :x:                 |        :x:         |         :x:         |  :heavy_check_mark:   |    :heavy_check_mark:    |   :heavy_check_mark:    |         :x:          |         :x:         |           :x:           |        :x:         |

> **NOTE:** HSS and XMSS<sup>MT</sup> are the multi tree variants of LMS and XMSS.
{.callout-info}

> **NOTE:** The table does not consider variants of algorithms, for example Dilithium has had many changes during the NIST rounds so a checkbox in the Dilithium column does not mean products are necessarily interoperable. Consult the vendor sections for details.
{.callout-info}

## Crypto4A

The QxEDGE is a Hybrid Security Platform (HSP) which combines the features of a Quantum-Ready HSM with Confidential Computing support. The QxHSM is a network attached HSM. Both products are built around the Crypto4A QASM FIPS 140, Level 3 validated module. All of the supported PQC algorithms are supported natively and available as part of the baseline product. The QASM also contains classic and PQC roots of trust that are used to validate firmware, code and configuration updates signed using dual signatures using HSS/LMS and ECDSA. The QASM also uses hybrid key management approach that combines Classic McEliece and ECDH for inter-HSM, C4A-to-HSM and long term external archiving security. An upcoming update (available as part of regular M&S) will also enable classic, PQC and Hybrid remote key attestation using already pre-loaded classic and PQC attestation keys.

## Securosys

[Primus HSM](https://www.securosys.com/en/products/primus-hardware-security-modules-hsm) manufactured by [Securosys](https://www.securosys.com/en/). The listed features are based on the roadmap for 2023 and are subject to change depending on market demand and industry research.

## Utimaco

uTrust Identify and Q-Safe firmware extension. Software simulator available, Dilithium in process of updated to round 3 version.

[Q-safe]https://utimaco.com/products/categories/further-solutions/q-safe)
[u.trust Identify](https://utimaco.com/products/categories/identity-management/utrust-identify)

## Thales

Functional module for Luna. Need functional modules enabled.

## Bouncy Castle
Java and C# APIs with all NIST candidate support, and some older ones. [Available as open source software](https://www.bouncycastle.org/). All NIST candidates available in Java from version 1.72 and C# from version 2.0.0.

The [Bouncy Castle for kotlin](https://github.com/bcgit/bc-kotlin) open source package provides a script/command line interface for generating certificate chains with different algorithms, including hybrid certificates using X.509 section 9.8 alternative signatures. 

## Entrust 
**nShield**

The [Entrust nShield Post-Quantum SDK](https://www.entrust.com/-/media/documentation/datasheets/entrust-pqc-option-pack-ds.pdf) enables post-quantum cryptographic applications for nShield HSMs with the CodeSafe SDK.

**PKIaaS**

The Entrust ]PKI as a Service (PKIaaS)](https://www.entrust.com/digital-security/certificate-solutions/products/pki/managed-services/pki-as-a-service) for Post-Quantum Beta Program supports all three algorithms selected in round 3 of the NIST competition and can provide composite and pure quantum CA hierarchies.

## EVERTRUST

EVERTRUST Stream is a PKI CA/VA/TSA and EVERTRUST Horizon is a PKI RA and CLM software. Both products are currently able to issue and manage pure-PQC and hybrid backard-compatible certificates based on Dilithium/Falcon/Sphincs+ algorithms. However the versions of the software that do so are yet unreleased. Release is planned upon completion of the standardization process.

## Keyfactor
**SignServer**

SignServer performs server side signing and is capable of Post-Quantum signatures on CMS (RFC5662) messages as well as plain signatures. SPHINCS+ and Dilithium are supported from [SignServer 6.0](https://www.keyfactor.com/press-releases/keyfactor-makes-quantum-leap-with-post-quantum-pki-and-signing-capabilities/).

**EJBCA**

EJBCA PKI can create CAs and issue X.509 certificates signed using Post-Quantum algorithms. Available as open source software and containers with support for Dilithium and Falcon from [EJBCA 8.0](https://www.keyfactor.com/press-releases/keyfactor-makes-quantum-leap-with-post-quantum-pki-and-signing-capabilities/).

## Fortanix

Fortanix DSM has LMS support, and NIST candidate signature algorithms on the roadmap for first half of 2023. See [Algorithm Support](https://support.fortanix.com/hc/en-us/articles/360016160411-Algorithm-Support)

## Open Quantum Safe

OQS is an open source software library that implements PQC [algorithms](https://openquantumsafe.org/liboqs/algorithms/), as well as integrations such as into OpenSSL.

## I4P
Trident HSM is a general purpose network HSM developed by [I4P](https://www.i4p.com/) that received the Common Criteria (CC) EAL4+ (EN 419221-5 as well as EN 419241-2) certification. 

Cryptographic applications are enabled to use Post-Quantum algorithms (SPHINCS+ and Kyber) even in the CC restricted mode that helps with using hybrid solutions and the transition to PQC.

## CZERTAINLY

Open source [CZERTAINLY](https://docs.czertainly.com/docs) platform implements experimental post-quantum cryptography algorithms support for certificate, cryptographic key, and digital signature lifecycle management and automation. The following PQC signature schemes are supported:
- FALCON
- CRYSTALS-Dilithium
- SPHINCS+

## IBM
The Crypto Express (CEX7S & CEX8S) cryptographic hardware security module products work with certain IBM Z® servers and the [Integrated Cryptographic Service Facility (ICSF)](https://www.ibm.com/docs/en/zos/3.1.0?topic=zos-cryptographic-services) to support post-quantum algorithms. Support is also available for [Linux on Z and LinuxONE](https://www.ibm.com/docs/en/linux-on-z?topic=hw-crypto-express-features). The 4769 cryptographic hardware security module product supports post-quantum algorithms using the [CCA](https://www.ibm.com/products/pcie-cryptographic-coprocessor) APIs on x64 and IBM Power® servers.

## MTG AG

[MTG Corporate PKI](https://www.mtg.de/en/public-key-infrastructures/corporate-pki/ ) consists of the two aligned product components MTG Certificate Authority (MTG CARA) and MTG Certificate Lifecycle Manager (CLM).
MTG CARA as been extended by the PQC algorithms ML-DSA (Dilithium), SLH-DSA (SPHINCS⁺), and Falcon.

Furthermore, we provide an online demo of a PQC CARA version supporting
the McEliece and SPHINCS⁺ post-quantum algorithms and a post quantum CA hierarchy that is available for private test at https://pqc-pki.mtg.de.



## ISC
ISC produces PKI/PQC-enabled applications (https://infoseccorp.com/pki/): CertAgent, a certificate authority; CSP<sup>id</sup>, a virtual smartcard with central repository for certificates and private keys; DAS, a webapp providing brokered encryption and authentication; SecretAgent, an encryption and digital signature utility; and cryptographic libraries that offer post-quantum algorithms.

## Botan
[Botan](https://github.com/randombit/botan) is a C++ cryptography library released under the permissive Simplified BSD license. It offers the tools necessary to implement a range of systems, such as TLS protocol, X.509 certificates, AEAD ciphers, PKCS#11 and TPM hardware support, password hashing, and post quantum crypto schemes.

## References

The following table contains references to the PQC capabilities and algorithms.

| Algorithm                                                     | Reference                                                                      |
| :------------------------------------------------------------ | :----------------------------------------------------------------------------- |
| FIPS drafts for comment                                       | https://csrc.nist.gov/News/2023/three-draft-fips-for-post-quantum-cryptography |
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

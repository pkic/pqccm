# Description
 
The PKI Consortium is managing a PQC Capabilities Matrix (PQCCM) of software applications, libraries and hardware that includes support for 
Post Quantum Cryptography, without endorsing their implementation or quality.

The list includes a wide variety of software applications, libraries, and hardware from different vendors. 
The list should be considered a living document and a starting point. Considering the rapid change in the area such things can vary from day to day and complete freshness of information can only be gathered from vendors directly. 

The PKI Consortium is actively working to promote the adoption of Post-Quantum Cryptography, and the capabilities matrix is a key part of that effort.

What the PQCCM do:
* collect and aggregate information on PQC capabilities across the cybersecurity landspace (vendors, software, hardware, etc..)

What the PQCCM doesn't do:
* review, vet, verify or test implementations or interoperability
* source code review, formal review of algorithms, etc.
* provide information, documentation or any recommended usage of Post Quantum Cryptography

No other activity besides what is listed under PQCCM DOs is under the purview of PKI Consortium (unless explicitly stated otherwise)".




# Capabilities

The table lists information from vendors related to support for Post Quantum Cryptography.
|Vendor|Product|Category|Last updated|[Composite certificates](#A)|[Hybrid certificates](#B)|[LMS](#C)|[XMSS](#D)|[Falcon](#E)|[Dilithium](#F)|[SPHINCS+](#G)|[Kyber](#H)|[BIKE](#I)|[McEliece](#J)|[HQC](#K)|
|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|
|[Securosys](#securosys)|Primus|HSM|2022-11-28|:clock1:|:clock1:|:x:|:x:|:x:|:clock1:|:clock1:|:clock1:|:x:|:x:|:x:|
|[Utimaco](#utimaco)|Q-Safe|HSM|2022-11-28|:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:x:|:heavy_check_mark:|:x:|:heavy_check_mark:|:x:|:x:|:x:|
|[Utimaco](#utimaco)|u.trust Identify|PKI|2022-11-28|:heavy_check_mark:|:x:|:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:x:|:x:|:x:|:x:|
|[Thales](#thales)|Luna|HSM |2022-11-22|:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:x:|:heavy_check_mark:|:x:|:heavy_check_mark:|:x:|:x:|:x:|
|[Entrust](#entrust)|nShield|HSM |2022-11-22|:x:|:x:|:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:x:|:x:|:x:|:x:|
|[Entrust](#entrust)|PKIaaS|PKI|2022-11-22|:heavy_check_mark:|:x:|:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:x:|:x:|:x:|:x:|
|[Bouncy Castle](#bouncy-castle)|BC|Software library|2022-11-22|:heavy_check_mark:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|
|[Keyfactor](#keyfactor)|SignServer|Signing Software|2022-11-22|:x:|:x:|:x:|:x:|:x:|:clock1:|:heavy_check_mark:|:x:|:x:|:x:|:x:|
|[Keyfactor](#keyfactor)|EJBCA|PKI|2022-11-22|:x:|:x:|:x:|:x:|:heavy_check_mark:|:clock1:|:x:|:x:|:x:|:x:|:x:|
|[Fortanix](#fortanix)|FX2200|HSM|2022-11-29|:x:|:x:|:heavy_check_mark:|:x:|:clock1:|:clock1:|:clock1:|:x:|:x:|:x:|:x:|


## Securosys
Primus HSM (https://www.securosys.com/en/products/primus-hardware-security-modules-hsm) manufactured by https://www.securosys.com/en/. The listed features are based on the roadmap for 2023 and are subject to change depending on market demand and industry research.

## Utimaco

uTrust Identify and Q-Safe firmware extension. Software simulator availabe, Dilithium in process of updated to round 3 version

## Thales

Functional module for Luna. Need functional modules enabled.

## Bouncy Castle
Java and C# APIs with all NIST candidate support, and some older ones. [Available as open source software](https://www.bouncycastle.org/). All NIST candidated available in Java from version 1.72 and C# from version 2.0.0.

The [Bouncy Castle for kotlin](https://github.com/bcgit/bc-kotlin) open source package provides a script/command line interface for generating certificate chains with different algorithms. 

## Entrust 
nShield

The Entrust nShield Post-Quantum SDK enables post-quantum cryptographic applications for nShield HSMs with the CodeSafe SDK.
https://www.entrust.com/-/media/documentation/datasheets/entrust-pqc-option-pack-ds.pdf

PKIaaS

The Entrust PKI as a Service (PKIaaS) for Post-Quantum Beta Program supports all three algorithms selected in round 3 of the NIST competition and can provide composite and pure quantum CA hierarchies.
https://www.entrust.com/digital-security/certificate-solutions/products/pki/managed-services/pki-as-a-service

## Keyfactor
SignServer

SignServer performs server side signing and is capable of Post-Quantum signatures on CMS (RFC5662) messages. Available as open source software from [SignServer Community v5.9.1](https://doc.primekey.com/signserver/signserver-release-information/signserver-release-notes/signserver-community-5-9-1-release-notes).

EJBCA

EJBCA PKI software can issue X.509 certificates supporting Post-Quantum algorithms. Available for private test.

## Fortanix

Fortanix DSM has NIST candidate signature algorithms on the roadmap for first half of 2023.

# References

The following table contains references to the PQC capabilities and algorithms.
|Algorithm|Reference|
|:--|:--|
|<span id="A">Composite certificates</span>|https://datatracker.ietf.org/doc/draft-ounsworth-pq-composite-keys/|
|<span id="B">Hybrid certificates</span>|https://datatracker.ietf.org/doc/html/draft-truskovsky-lamps-pq-hybrid-x509-01|
|<span id="C">LMS</span>|https://www.rfc-editor.org/rfc/rfc8708.html|
|<span id="D">XMSS</span>|https://datatracker.ietf.org/doc/html/rfc8391|
|<span id="E">Falcon</span>|https://falcon-sign.info|
|<span id="F">Dilithium</span>|https://pq-crystals.org/dilithium/resources.shtml|
|<span id="G">SPHINCS+</span>|https://sphincs.org|
|<span id="H">Kyber</span>|https://pq-crystals.org/kyber/index.shtml|
|<span id="I">BIKE</span>|https://bikesuite.org|
|<span id="J">McEliece</span>|https://classic.mceliece.org|
|<span id="K">HQC</span>|https://pqc-hqc.org|
|NIST Recommendation for Stateful Hash-Based Signature Schemes|[SP800-208](https://csrc.nist.gov/publications/detail/sp/800-208/final)|

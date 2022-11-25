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
| Vendor|Product     |Type|Last updated|X.509 Certs|Composite Certs|Hybrid Certs|HMS               |XMSS              |Falcon|Dilithium         |SPHINCS+|Kyber             |BIKE|McEliece|HQC|Other|
|:------|:-----------|:---|:---------|:----------|:--------------|:-----------|:-----------------|:-----------------|:-----|:-----------------|:-------|:-----------------|:---|:-------|:--|:---|
|[Utimaco](#utimaco)|CryptoServer|HSM |2022-11-22|:x:        |:x:            |:x:        |:heavy_check_mark:|:heavy_check_mark:|:x:   |:heavy_check_mark:|:x:     |:heavy_check_mark:|:x: |:x:     |:x:|:x:|
|[Thales](#thales)|Luna|HSM |2022-11-22|:x:        |:x:            |:x:        |:heavy_check_mark:|:heavy_check_mark:|:x:   |:heavy_check_mark:|:x:     |:heavy_check_mark:|:x: |:x:     |:x:|:x:|
|[Entrust](#entrust)|nShield|HSM |2022-11-22|:x:        |:x:            |:x:        |:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:x:|:x: |:x:     |:x:|:heavy_check_mark:|
|[Entrust](#entrust)|PKIaaS|PKI Software |2022-11-22|:heavy_check_mark:|:heavy_check_mark:|:x:        |:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:x:|:x: |:x:     |:x:|:x:|
|[Bouncy Castle](#bouncy-castle)|BC|API |2022-11-22|:heavy_check_mark:|:heavy_check_mark:|:x:        |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|
|[Keyfactor](#keyfactor)|SignServer|Signing Software|2022-11-22|:x:        |:x:            |:x:        |:x:|:x:|:x:   |:x:|:heavy_check_mark:     |:x:|:x: |:x:     |:x:|:x:|
|[Keyfactor](#keyfactor)|EJBCA|PKI Software|2022-11-22|:heavy_check_mark:        |:x:            |:x:        |:x:|:x:|:heavy_check_mark:|:x:|:x:     |:x:|:x: |:x:     |:x:|:x:|



## Utimaco

QSafe firmware extension. Software simulator availabe, Dilithium in process of updated to round 3 version

## Thales

Functional module for Lune. Need functional modules enabled.

## Bouncy Castle
Java and C# APIs with all NIST candidate support, and some older ones. Available as open source software.

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

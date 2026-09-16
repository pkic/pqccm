---
date: 2025-03-07T7:00:00Z
title: Quantum-Safe Features Matrix (QSFM)

heroTitle: Quantum-Safe Features Matrix (QSFM)
heroDescription: A list of hardware security modules that have built-in quantum-safe features.

tags:
- resource
---

The PKI Consortium is managing a Quantum-Safe Features Matrix (QSFM) of hardware security modules (HSMs) that include support for Quantum-Safe features beyond the mere implementation of Post Quantum Cyptography (PQC) capabilities (see [PQCCM](https://pkic.org/pqccm/)), without endorsing their implementation or quality.

The list includes a variety of HSMs from different vendors.
The list should be considered a living document and a starting point. Considering the rapid change in the area, such things can vary from day to day and complete freshness of information can only be gathered directly from the vendors.

The PKI Consortium is actively working to promote the adoption of Quantum-Safe infrastructures. PQC capabilities are obviously an important part of this effort, but what is often overlooked is that HSMs themselves are consumers of cryptography. Therefore, in order to have a Quantum-Safe infrastructure, it is important to use Quantum-Safe devices as foundational elements.

**What the QSFM does**:

* collects and aggregates information on Qantum-Safe features from different HSM vendors
* lists products that leverage Quantum-Safe mechanisms to enhance their own security

No other activities besides those listed above are under the purview of the PKI Consortium (unless explicitly stated otherwise).

**What the QSFM doesn't do**:

* review, vet, verify any of these claims, or validate them via testing
* perform source code review, formal review, etc.
* provide information, documentation or any recommended usage of the HSMs listed

## Contribute

This list is a collaborative effort. To contribute please raise an issue or a PR on the [GitHub Repository](https://github.com/pkic/pqccm).

## Legend

|       Symbol       | Meaning                                                                | Comment                                                                                                                                                                                                                 |
| :----------------: | :--------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|        :x:         | The feature is currently not available                                 |                                                                                                                                                                                                                         |
| :heavy_check_mark: | The feature is available for usage/test now                            |                                                                                                                                                                                                                         |
|      :clock1:      | The feature is planned on the product roadmap in the coming six months | Roadmap items must not be added if they are not really scheduled to be implemented in the coming six month period. Roadmap items should be noted in the vendor section with a specific time, i.e. "Q2 2023" or similar. |

## Definitions

This list provides definitions for each column used in the QSFM:

* **Quantum-Safe**: The corresponding feature leverages PQC algorithms for its security. If a mix of PQC and non-PQC algorithms is used, it is imperative that the PQC component(s) must be subjugated in order to attack the security of the underlying feature. For instance, if ECDSA and LMS are used to verify a F/W update, an invalid  LMS signature must yield the rejection of the F/W update, regardless of the validity of the ECDSA signature. Similarly, if RSA and ML-KEM are used to wrap sensitive material, an attacker with a Cryptographically Relevant Quantum Computer (CRQC) must not be able to obtain any sensitive information from breaking the RSA component.
* **Fully Quantum-Safe**: The device can operate completely without legacy algorithms with all features and protections being quantum-safe.
* **Hardware RoT Injected During Manufacturing**: PQC Roots of Trust (RoT) are injected into the device during the manufacturing process.
* **F/W Update**: The device's Firmware (F/W) update process is quantum-safe.
* **Secure Boot**: The device's secure-boot process is quantum-safe.
* **HSM-to-HSM Tunneling**: Transport mechanisms for communications of sensitive data between HSMs for load balancing, redundancy or disaster recovery are quantum-safe. Note that since those communication protocols may be proprietary, this category specifically refers to communication between HSMs of the same vendor.
* **User Key Storage & Management**: The device always uses quantum-safe mechanisms to protect all user keys during storage (internal and external). Internal storage refers to cryptographic material stored on disk within the HSM, while external storage refers to cryptographic material stored on a disk external to the HSM's security boundary. If the disk(s) were to be observed at any given time while the HSM is operational, it must be impossible to read sensitive data that isn't encrypted using PQC algorithms.
* **Backup and Archiving**: User key backup and archiving is quantum-safe, both in relation to the encryption of the material, and in the authentication methods used for key management functions. A backup refers to the set of information needed to restore the relevant cryptographic material on a new HSM from the same vendor. An archive is similar to a backup but it also contains sufficient information to be restored on any device from a third-party to prevent vendor lock-in, presuming that this third-party supports the relevant PQC algorithms to restore the sensitive material. 
* **HSM User Access Management**: User access management functionality of the HSM is quantum-safe. This includes user authentication to the module to perform security relevant operations.
* **Private Key Export**: User private key material exported outside of the HSM is secured using quantum-safe mechanisms.
* **Attestation Functionality**: Attestation capabilities of the module are quantum-safe.
* **HSM Audit Functionality**: Core security audit capabilities of the module as defined in FIPS 140-3 (ISO 24759 AS06.26) are quantum-safe.
* **NIST's CAVP PQC Certification**: Link to the module's CAVP certificate on NIST's website. You should review the [PQCCM](https://pkic.org/pqccm/) and the certificate to verify the mechanisms that are supported by the module.
* **FIPS 140-3 Validation Status of PQC-Capable Functionality**: The device's FIPS 140-3 validation status for a version that includes CAVP-certified PQC algorithms.
* **Crypto Agility**: The device is capable of being securely updated in the field using quantum-safe methods to add future PQC algorithms without requiring a hardware refresh.

## Quantum-Safe Features Matrix

The table lists information from vendors related to the Quantum-Safe features their product implements.

> The list is ordered alphabetically by vendor, there is no other meaning to the order.
{.callout-info}

| Vendor                | Product | Category | Last Updated | Fully Quantum-Safe | Hardware RoT Injected During Manufacturing | F/W Update  | Secure Boot              | HSM-to-HSM Tunneling | User Key Storage & Management | Backup and Archiving | HSM User Access Management | Private Key Export             | Attestation Functionality | HSM Audit Functionality | NIST's CAVP PQC Certification                                | FIPS 140-3 Validation Status of PQC-Capable Functionality | Crypto Agility |
| --------------------- | ------- | -------- | ------------ | ------------------------------------- | ----------------------- | ---------------------------- | ------------------------------------------ | ----------------------------------------- | ------------------------------------ | ------------------------------------------ | ------------------------------------- | ------------------------------------------------------------ | --------------------------------------------------------- | -------------- | -------------- | -------------- | -------------- |
| [Crypto4A](#crypto4a) | QxHSM   | HSM      | 2025-02-27   | :heavy_check_mark: | :heavy_check_mark:                    | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | MIP  | Yes |
| [Crypto4A](#crypto4a) | QxEDGE  | HSP      | 2025-02-27   | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | MIP | Yes |

> **NOTE:** Modules in the "MIP" status have been evaluated by a validation lab and are awaiting validation from NIST.
{.callout-info}

> **NOTE:** Modules in the “IUT” status have begun to be evaluated by an independent CMVP-accredited testing lab.
{.callout-info}

## Crypto4A

Crypto4A Technologies Inc. develops quantum-safe hardware security modules (HSMs) designed to meet the growing need for scalable, crypto-agile, and secure solutions in an increasingly complex digital landscape. With products like the QxHSM™ and the QxEDGE™, Crypto4A empowers organizations to prepare for the quantum computing era with confidence. For more information about the status of our FIPS 140-3 validation or CAVP algorithm list, please visit [www.crypto4a.com](http://www.crypto4a.com/).

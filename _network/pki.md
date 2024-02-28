---
title: all about PKI (Public Key Infrastructure)
---


**PKI (Public Key Infrastructure) in Relation to Easy-RSA:**

PKI, which stands for Public Key Infrastructure, is a system that manages digital certificates, public and private keys, and other cryptographic elements to secure communication over networks. In the context of Easy-RSA, a set of scripts built around OpenSSL for managing a PKI, PKI refers to the collection of files and associations between the Certificate Authority (CA), keypairs, certificate requests, and certificates[1].

Here are some key terms related to PKI in the context of Easy-RSA:

- **CA (Certificate Authority):** The CA is the "master cert" at the root of a PKI. It signs certificate requests to issue certificates.
- **Cert (Certificate):** A certificate is a request signed by a CA containing the public key, certificate details, and a digital signature from the CA.
- **Request:** A certificate request is sent to a CA for signing. It includes desired certificate information and a digital signature from the private key.
- **Keypair:** An asymmetric cryptographic pair consisting of public and private keys. The public key is included in requests and certificates.

Easy-RSA simplifies the process of setting up and managing a PKI by providing scripts that automate tasks like creating CAs, generating keypairs, signing certificates, and managing revocations. It allows users to establish their own PKI for various purposes such as securing VPN connections or web servers.

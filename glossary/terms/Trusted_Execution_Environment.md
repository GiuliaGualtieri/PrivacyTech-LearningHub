# Trusted Execution Environment

A **Trusted Execution Environment (TEE)** is a secure area within a device's main processor that isolates and protects sensitive data and code during execution. 
**TEEs** ensure that the data remains private and secure, even if the main operating system or other software layers are compromised. 
This makes TEEs particularly valuable in applications where privacy and data integrity are critical, such as finance, healthcare, and cloud computing.

**TEEs** allow the sensitive part of an application to run in an isolated and memory protected area (e.g., an Intel SGX enclave[^1]). 
Hence, one can deploy applications with **TEEs** in a potentially untrusted cloud environment. 
TEEs provide several properties: 
1. The confidentiality and integrity of an application. When an application is running, its memory is held in an isolated and protected area that no privileged processes/users can read nor tamper with. When an application transitions to a state of rest, it may choose to seal its state (encrypted with authenticated encryption) and recover it later.
2. The remote attestation feature guarantees that one can confirm that the code running in a TEE is the expected code and running on the legitimate hardware [^2]. 

### Examples of TEE :school_satchel:
- (**Intel Software Guard Extensions (SGX)**)[https://www.intel.com/content/www/us/en/products/docs/accelerator-engines/software-guard-extensions.html],
- (**ARM TrustZone**)[https://developer.arm.com/documentation/100690/0200/ARM-TrustZone-technology],
- (**AMD Secure Encrypted Virtualization (SEV)**)[https://www.amd.com/en/developer/sev.html], (github open source code)[https://github.com/AMDESE/AMDSEV].

### Relationship between TEEs and Confidential Computing :question:
**Trusted Execution Environments** are a key technology underlying the concept of **Confidential Computing**, but they are not exactly the same thing. 
Confidential Computing is a broader term referring to the set of technologies and solutions that protect data during processing, and TEEs are one of the main tools used to achieve this goal



[^1]: Matthew Hoekstra, Reshma Lal, Pradeep Pappachan, Vinay Phegade, and Juan Del Cuvillo. 2013. Using innovative instructions to create trustworthy software solutions. In Proceedings of the 2nd International Workshop on Hardware and Architectural Support for Security and Privacy. Article 11, 1 pages
[^2]: Victor Costan and Srinivas Devadas. 2016. Intel SGX explained. Cryptology ePrint Archive (2016).

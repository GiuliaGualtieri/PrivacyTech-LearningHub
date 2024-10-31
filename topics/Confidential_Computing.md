# Confidential Computing

Microsoft + NVIDIA [Unlocking secure, private AI with confidential computing](https://www.technologyreview.com/2024/07/12/1094838/unlocking-secure-private-ai-with-confidential-computing/)
> [!IMPORTANT]
> The fundamental steps of **Data Privacy** to properly preserve privacy are:
> - **At rest**
> - **In transit**
> - **In use**

For example, with **DP (Differential Privacy)**, we only cover point **3**. 
**Encryption**, on the other hand, can cover points **1** and **2**. 
In the section “Understanding Confidential Computing,” it clearly states that Encryption covers points 1 and 2 while leaving point 3 uncovered. 
Here, they propose Microsoft’s new technology: “**Confidential Computing**.”

The idea seems appealing: **a trusted execution environment (TEE)**, a physical “box” environment in which you work. 
If I understand correctly, the collaboration with NVIDIA has led to the **development of CPUs** and now **Tensor Core GPUs** to train powerful AI models, but with protected **access control keys**.

While studying for the **Azure Data Scientist Associate certification**, I came across **Azure Key Vault**, their key management solution. 
It manages passwords, tokens, certificates, API keys, encryption keys for data encryption, TLS, and SSL (Encryption in transit). 
From the article, it seems that they have also integrated **HSM (hardware security module)** key management.

Reading the phrase “**VM size that supports confidential computing capabilities**”, I realized that I’m not entirely clear on the difference between confidential and non-confidential hardware. 
The idea is quite simple: you control the OS that connects to the hardware via a protected key. 
However, what’s the difference between the old hardware and this new one? Why are they talking about VMs with sizes that can support this?

It seems to me that **cybersecurity issues persist regardless (multi-party access)**. 

“_So, in these multi-party computation scenarios, or 'data clean rooms' multiple parties can merge their data sets, and no single party gets access to the combined data set. Only the code that is authorized will get access._"

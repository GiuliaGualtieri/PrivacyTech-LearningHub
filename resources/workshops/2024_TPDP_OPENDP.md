# TPDP + OpenDP 
https://tpdp.journalprivacyconfidentiality.org
## Key Take Aways (Part 1)
- **Adding randomness helps privacy guarantees**.
- **The notion of DP aims to guarantee privacy even in the worst case**. It aims to protect the privacy of a single record even when the model trained and all the other records participating in the training are colluding to the leak information about this one record.
- **Releasing a final trained model is assumed to leak as much as information as releasing an intermediate step.**
- **Generate data with DP**: the deploy of the models is hard
- **Epsilon budget**: after a certain value it does not make any sense
- Keep in mind to always **ensure transparency of the user**
- **Tuning**: how do we should consider the privacy cost? Tuning on public data -> privacy cost is zero, while on private date we have to sell a privacy end-to-end solution.
- **With DP** it’s possible to release information concerning “blocked” dataset (for now), **we can release more refined dataset**.
- DP’s motto: “give privacy to everyone!”
- **Memorization** is necessary whenever the distribution of subpopulation frequencies is long tailed. There is general tendency to memorize the labels of the training data, and it’s necessary. BUT: (of course) Memorization of the training data presents significant privacy risks when the training data contains sensitive personal information and thus it is important to understand whether such memorization is necessary for accurate learning.
- **Data Curation** does not care about privacy at all. Nowadays curating data has become very important to training state of the art models. However, there is limited investigation of the implications and opportunities of data curation for privacy. (Data curation = select best dataset for your model)
- **Data Deduplication** is super common nowadays. Basically, all foundation models do it. Part of the reason is due to the data memorization. Diffusion models, regurgitate images that they have seen most. Deduplication on private data -> you must be careful, as deduplication on private training data can lead to adaptive privacy attacks.
- When analyzing Differentially Private (DP) machine learning pipelines, the potential privacy cost of data-dependent pre-processing is frequently overlooked in privacy accounting -> new techniques: Smooth DP, Bounded DP (?)
- **Privacy Semantics**: alternative privacy. **Access-control** topic, rather than aggregate statistics. Models like LLMs: do they preserve contextual integrity?
- **RAG** (retrieval-augmented generation,  input -> access to datastore -> return output). Example: Google Search Generative Experience. Search mechanism = google, Datastore = Internet. training data attribution.
- Public model: trained on public data. Take it and **retrain on private date**.

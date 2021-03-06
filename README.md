# ImmuneConstrainedVAE
Dozens of vaccines protecting against SARS-CoV-2 have now been approved for public use, yet there remains a high risk that the virus evolves to escape vaccine protection. This motivates the need for a new generation of vaccines that can protect against a wider gamut of a virus’s evolutionary accessible states, not just the currently circulating strains. Computational methods such as sequence generative models can play a critical role in mapping out this state space. In particular, they can be used to screen thousands of examples of viral proteins that might pose a high risk of vaccine escape.  

In this work, we take steps towards such a computational method by designing and evaluating a conditional Variational Autoencoder (VAE) capable of selectively generating SARS-CoV-2 spike proteins with low immune visibility. The model is trained on 65,000 of the most common wild-type SARS-CoV-2 sequences and uses NetMHCpan to estimate levels of exposure to human T cell immunity. The model's generated sequences are compared with those derived from two simpler generative models; a random-mutator and an 11-gram language model. We discover that although all three models are able to generate stable, structurally valid sequences, only the VAE model can generate low immunogenicity sequences sampled from a distribution that interpolates smoothly along the principal variance directions of natural sequences.

## Folder structure

- VAEmodel: includes the jupyter notebook used for training the VAE
- evaluation: scripts to run DDGun and the rest of the evaluation pipeline
- RandomAndLanguageModel: script to run random mutator and 11gram VAE
- visualisation: pipeline to produce tSNE embeddings visualisations of protein sequences

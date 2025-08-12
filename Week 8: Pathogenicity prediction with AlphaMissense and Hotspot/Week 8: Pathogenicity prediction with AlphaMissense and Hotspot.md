## Workshop assignment 

## 🏠 Take-home points

- AlphaMissense was built on AF2 protein structure database, integrating structural, evolutionary, and variant frequency information.

- It assigns each variant a pathogenicity score (0–1) and classifies it as likely benign, likely pathogenic, or uncertain.

- It provides information about the functional or structural importance of specific regions on protein structure, for example by revealing clusters with a high pathogenicity profile.

- Hotspot calculates the average profile of pathonecity and highlights the protein regions where variants are predicted to be highly pathogenic, mapping these "hotspot" regions onto AF2-predicted structures for functional and structural insight.

- If a cluster contains mostly variants with benign characteristics, it does not necessarily mean that all variants within it will have benign-like effects.

- Similarly, if a cluster contains variants with pathogenic characteristics, certain substitutions may still be compensated for and exhibit benign-like effects.

## Summary 

In this section, we will talk about AlphaMissense which is a deep learning model developed by Google DeepMind to predict the pathogenicity of missense variants. Built upon the structural database of AF2, it uses AF2-predicted protein structures alongside evolutionary conservation patterns and variant frequency data to assess the potential impact of these variants on protein stability and function. Trained on a massive dataset covering nearly 71 million possible human variants, AlphaMissense assigns each variant a pathogenicity score between 0 to 1, classifying them as likely benign, likely pathogenic, or uncertain. It provides a valuable resource for researchers and clinicians to prioritize variants for further study. 

Link to the AlphaMissense paper: https://www.science.org/doi/10.1126/science.adg7492

➡️ Link for the try yourself section: https://alphafold.ebi.ac.uk/entry/Q9UQ13?activeTab=summary

Link to the AlphaMissense database: https://alphamissense.hegelab.org/search

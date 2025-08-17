## 📝 Workshop report (The deadline is 12:00 a.m. on the same day) (5 pts)

- In the second half of this section, you will evaluate the AlphaMissense scores of the proteins and variants analyzed in the previous week. Compare the AlphaMissense scores with the free energy change scores obtained in the previous week. Provide a brief comparative discussion linking the free energy scores to the observed variant characteristics. (0.5 pts)

- For the previously selected variant positions, assess their tendency to be pathogenic or benign according to AlphaMissense, taking into account their structural and functional importance. Please consider all substitutions within the selected variant positions. Additionally, extract all variant information for these positions or neighboring positions from UniProt or gnomAD, and provide supportive or enhanced classification for these reported variants using AlphaMissense scores. (1.5 pts)

- Evaluate the structural environment (heatmaps) of the variant positions to identify clusters with pathogenic-like or benign-like profiles. (1 pts)

- Evaluate the hotspots in your protein and determine whether the selected variants are located within these regions. Provide a discussion on the average pathogenicity and the identified hotspots. (1 pts)

- Why is it important to use multiple complementary methods to assess the impact of a variant on a protein’s structure and function? How can we decide which predictive method is the most reliable for assessing a protein variant’s impact in a desired research context? (1 pts)


## 🏠 Take-home points

- AlphaMissense was built on AF2 protein structure database, integrating structural, evolutionary, and variant frequency information.

- It assigns each variant a pathogenicity score (0–1) and classifies it as likely benign, likely pathogenic, or uncertain.

- It provides information about the functional or structural importance of specific regions on protein structure, for example by revealing clusters with a high pathogenicity profile.

- Hotspot calculates the average profile of pathonecity and highlights the protein regions where variants are predicted to be highly pathogenic, mapping these "hotspot" regions onto AF2-predicted structures for functional and structural insight.

- If a cluster contains mostly variants with benign characteristics, it does not necessarily mean that all variants within it will have benign-like effects.

- Similarly, if a cluster contains variants with pathogenic characteristics, certain substitutions may still be compensated for and exhibit benign-like effects.

## Summary 

In this section, we will talk about AlphaMissense which is a deep learning model developed by Google DeepMind to predict the pathogenicity of missense variants. Built upon the structural database of AF2, it uses AF2-predicted protein structures alongside evolutionary conservation patterns and variant frequency data to assess the potential impact of these variants on protein stability and function. Trained on a massive dataset covering nearly 71 million possible human variants, AlphaMissense assigns each variant a pathogenicity score between 0 to 1, classifying them as likely benign, likely pathogenic, or uncertain. It provides a valuable resource for researchers and clinicians to prioritize variants for further study. 

<img width="1241" height="714" alt="Screenshot 2025-08-13 at 04 31 12" src="https://github.com/user-attachments/assets/91f1db88-ae6f-4fdc-a8dc-aab2af772bb7" />
from Google DeepMind

## References

Link to the AlphaMissense paper: https://www.science.org/doi/10.1126/science.adg7492

➡️ Link for the try yourself section: https://alphafold.ebi.ac.uk/entry/Q9UQ13?activeTab=summary

Link to the AlphaMissense database: https://alphamissense.hegelab.org/search

## Slides

https://docs.google.com/presentation/d/10h39rGs_Ny3c_DKLXtgdAg39RXoml9EL7uRERrGHQto/edit?usp=sharing

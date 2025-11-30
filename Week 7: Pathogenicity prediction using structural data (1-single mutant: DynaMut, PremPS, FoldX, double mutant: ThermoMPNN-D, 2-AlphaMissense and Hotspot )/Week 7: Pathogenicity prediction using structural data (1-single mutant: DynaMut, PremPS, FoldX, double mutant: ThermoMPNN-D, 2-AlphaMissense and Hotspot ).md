## 🚨 Attention: pre-course action

In the first half of this section, we will discuss various structure-based pathogenicity prediction tools, and then we will perform free energy calculations on our target proteins to assess the effects of mutations. Therefore, before coming to class, please select a human protein from the PDB or UniProt that you are interested in, preferably in a monomeric form for simplicity (If your structure is a dimer or tetramer, don't worry, we can manipulate it to extract the monomeric form before starting the calculations). Download the corresponding PDB structure (in .pdb format) and record the entry ID. You are also expected to select three different variants of your target protein, classified as pathogenic, of uncertain significance, and benign. To choose these variants, you can use the "Variant Viewer" available under the "Disease & Variants" section in UniProt. You can also extract variant information from gnomAD. Additionally, it is recommended to select variants that are located within the same 3D environment, such as being in close proximity within a specific domain of the protein. 

In the second half of this section, you will evaluate the AlphaMissense scores of the proteins and variants analyzed in the first section.

👍 Make sure to review the FoldX set-up tutorials below. 

👇 Below is an example for variant selection:

IL37, with the monomeric form extracted from the dimeric PDB structure with ID 5hn1, is an anti-inflammatory cytokine consisting of a single domain with  β-trefoil fold. Side chains of three amino acid residues N76, R152, and I177 were displayed. (gnomAD: N76S VUS, R152W benign, I177T pathogenic)

<img width="799" height="678" alt="image1" src="https://github.com/user-attachments/assets/636ea167-e871-4ef9-84d9-665e417cd9b8" />

## 📝 Workshop report (The deadline is 2025-11-18 at 11.59 pm, −2 points for each day late, up to a maximum of 3 days) (5 pts)

Tools: FoldX, DynaMut2, PremPS, ThermoMPNN (Tamarind Bio)

- Perform ΔΔG calculations for three selected variants of your protein structure using four different methods discussed in the class. (2 pts, 0.5 pts for each method)

- Report the ΔΔG values in a table and provide a comparative discussion of the methods. (1 pts)

- Rationalize why some mutations tend to be pathogenic while others are benign. In this discussion, consider factors such as secondary structure, relative solvent-accessible surface area (rSASA), B-factor, hydrophobicity, and electrostatic charges. (2 pts)

## 📝 Workshop report (The deadline is 2025-11-18 at 11.59 pm, −2 points for each day late, up to a maximum of 3 days) (5 pts)

- Compare the AlphaMissense scores with the free energy change scores obtained in the previous section. Provide a brief comparative discussion linking the free energy scores to the observed variant characteristics. (0.5 pts)

- For the previously selected variant positions, assess their tendency to be pathogenic or benign according to AlphaMissense, taking into account their structural and functional importance. Please consider all substitutions within the selected variant positions. Additionally, extract all variant information for these positions or neighboring positions from UniProt or gnomAD, and provide supportive or enhanced classification for these reported variants using AlphaMissense scores. (1.5 pts)

- Evaluate the structural environment (heatmaps) of the variant positions to identify clusters with pathogenic-like or benign-like profiles. (1 pts)

- Evaluate the hotspots in your protein and determine whether the selected variants are located within these regions. Provide a discussion on the average pathogenicity and the identified hotspots. (1 pts)

- Why is it important to use multiple complementary methods to assess the impact of a variant on a protein’s structure and function? How can we decide which predictive method is the most reliable for assessing a protein variant’s impact in a desired research context? (1 pts)

## 🏠 Take-home points 

1st part:

- FoldX is a physics-based method that calculates changes in free energy (ΔΔG) upon mutation using an empirical force field, offering fast and relatively accurate predictions, particularly for point mutations.

- DynaMut combines normal mode analysis with statistical potentials to assess both structural stability and changes in protein dynamics, providing insights into flexibility changes caused by mutations.

- PremPS employs a hybrid approach integrating structural, energetic, and evolutionary features through machine learning to predict ΔΔG values with improved accuracy, particularly for missense variants.

- ThermoMPNN is a deep learning-based method that uses graph neural networks trained on massive mutational data to predict effects of mutations on protein stability, including single and double mutants, and can infer potential pathogenicity by modeling ΔΔG landscapes. 

2nd part: 

- AlphaMissense was built on AF2 protein structure database, integrating structural, evolutionary, and variant frequency information.

- It assigns each variant a pathogenicity score (0–1) and classifies it as likely benign, likely pathogenic, or uncertain.

- It provides information about the functional or structural importance of specific regions on protein structure, for example by revealing clusters with a high pathogenicity profile.

- Hotspot calculates the average profile of pathonecity and highlights the protein regions where variants are predicted to be highly pathogenic, mapping these "hotspot" regions onto AF2-predicted structures for functional and structural insight.

- If a cluster contains mostly variants with benign characteristics, it does not necessarily mean that all variants within it will have benign-like effects.

- Similarly, if a cluster contains variants with pathogenic characteristics, certain substitutions may still be compensated for and exhibit benign-like effects.


## Summary
1st part:

In this section, we will explore pathogenicity prediction tools that utilize the structural data of proteins. FoldX, DynaMut, PremPS, and ThermoMPNN are widely used computational tools for predicting the pathogenicity of protein mutations by estimating changes in protein stability. Each method has its own underlying architecture, offering distinct advantages and limitations. To improve reliability, it is often necessary to cross-validate the outputs of these tools. Collectively, they enable us to prioritize potentially pathogenic mutations by quantifying their thermodynamic impact on protein structure and function.

![science adj8672-f1](https://github.com/user-attachments/assets/a602ca69-b6d2-4e9d-a93f-44ee2415024b) from Science Journal

2nd part:

In this section, we will talk about AlphaMissense which is a deep learning model developed by Google DeepMind to predict the pathogenicity of missense variants. Built upon the structural database of AF2, it uses AF2-predicted protein structures alongside evolutionary conservation patterns and variant frequency data to assess the potential impact of these variants on protein stability and function. Trained on a massive dataset covering nearly 71 million possible human variants, AlphaMissense assigns each variant a pathogenicity score between 0 to 1, classifying them as likely benign, likely pathogenic, or uncertain. It provides a valuable resource for researchers and clinicians to prioritize variants for further study.

<img width="1012" height="579" alt="Screenshot 2025-09-10 at 12 12 54" src="https://github.com/user-attachments/assets/7aa70786-fd8b-4839-a000-31e8e7c7e3ea" /> from Google DeepMind

![1-s2 0-S2001037024001247-gr006_lrg](https://github.com/user-attachments/assets/ba2c8082-cce7-44f8-829b-2b55123fb4af)
Sardag, Inci, et al., 2024

## Software downlaod

🔑 You are required to register for the FoldX server under the academic license, which is free of charge.

To register, please follow this link: https://foldxsuite.crg.eu/academic-license-info

❗️ There are two tutorial videos, one for Mac and one for Windows, on how to install FoldX locally on your computer. You are expected to install FoldX before coming to class by following these tutorials, as there will be no time to do so during the session. If you are having issues, do not hesitate to contact me!

❗️❗️ Please try to download FoldX at least three days in advance of the class so that we can solve any potential issues and avoid delays in obtaining the academic license. I will not be able to assist with installation issues on the day of the class.

## References

1st part:

Link to the FoldX paper: https://academic.oup.com/nar/article/33/suppl_2/W382/2505499

Link to the DynaMut paper: https://academic.oup.com/nar/article/46/W1/W350/4990022?login=false

Link to the PremPS paper: https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008543

Link to the ThermoMPNN paper: https://www.science.org/doi/10.1126/science.add2187

Tool access:

➡️ Link to the DynaMut server: https://biosig.lab.uq.edu.au/dynamut/

➡️ Link to the PremPS server: https://lilab.jysw.suda.edu.cn/research/PremPS/research/PremPS/

➡️ Link to the ThermoMPNN Colab: https://colab.research.google.com/drive/1OcT4eYwzxUFNlHNPk9_5uvxGNMVg3CFA

2nd part: 

Link to the AlphaMissense paper: https://www.science.org/doi/10.1126/science.adg7492

➡️ Link for the try yourself section: https://alphafold.ebi.ac.uk/entry/Q9UQ13?activeTab=summary

Link to the AlphaMissense database: https://alphamissense.hegelab.org/search

## Slides

1st part:

https://docs.google.com/presentation/d/1DyIXaXer8BrBsRzPI62I9Tl4_k4rsK4JK6lR7Qz7M1w/edit?usp=sharing

2nd part:

https://docs.google.com/presentation/d/10h39rGs_Ny3c_DKLXtgdAg39RXoml9EL7uRERrGHQto/edit?usp=sharing

See the video in week 7 for FoldX installation for mac.

See the following video for FoldX installation for windows: https://www.youtube.com/watch?v=ZatwVMnswA4😎

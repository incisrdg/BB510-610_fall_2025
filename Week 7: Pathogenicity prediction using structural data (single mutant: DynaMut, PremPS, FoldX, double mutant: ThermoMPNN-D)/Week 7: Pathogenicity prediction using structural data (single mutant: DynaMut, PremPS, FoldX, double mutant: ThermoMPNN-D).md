## 🚨 Attention: pre-course action

In the first half of this section, we will discuss various structure-based pathogenicity prediction tools, and in the second half, we will perform free energy calculations on our target proteins to assess the effects of mutations. Therefore, before coming to class, please select a human protein from the PDB or UniProt that you are interested in, preferably in a monomeric form for simplicity (If your structure is a dimer or tetramer, don't worry, we can manipulate it to extract the monomeric form before starting the calculations). Download the corresponding PDB structure (in .pdb format) and record the entry ID. You are also expected to select three different variants of your target protein, classified as pathogenic, of uncertain significance, and benign. To choose these variants, you can use the "Variant Viewer" available under the "Disease & Variants" section in UniProt. You can also extract variant information from gnomAD. Additionally, it is recommended to select variants that are located within the same 3D environment, such as being in close proximity within a specific domain of the protein. 

👍 Make sure to review the FoldX set-up tutorials below. 

👇 Below is an example for variant selection:

IL37, with the monomeric form extracted from the dimeric PDB structure with ID 5hn1, is an anti-inflammatory cytokine consisting of a single domain with  β-trefoil fold. Side chains of three amino acid residues N76, R152, and I177 were displayed. (gnomAD: N76S VUS, R152W benign, I177T pathogenic)

<img width="799" height="678" alt="image1" src="https://github.com/user-attachments/assets/636ea167-e871-4ef9-84d9-665e417cd9b8" />

## 📝 Workshop report (The deadline is 12:00 a.m. on the same day) (5 pts)

- Perform ΔΔG calculations for three selected variants of your protein structure using four different methods discussed in the class. (2 pts, 0.5 pts for each method)

- Report the ΔΔG values in a table and provide a comparative discussion of the methods. (1 pts)


- Rationalize why some mutations tend to be pathogenic while others are benign. In this discussion, consider factors such as secondary structure, relative solvent-accessible surface area (rASA), B-factor, hydrophobicity, and electrostatic charges. (2 pts)

## 🏠 Take-home points 

- FoldX is a physics-based method that calculates changes in free energy (ΔΔG) upon mutation using an empirical force field, offering fast and relatively accurate predictions, particularly for point mutations.

- DynaMut combines normal mode analysis with statistical potentials to assess both structural stability and changes in protein dynamics, providing insights into flexibility changes caused by mutations.

- PremPS employs a hybrid approach integrating structural, energetic, and evolutionary features through machine learning to predict ΔΔG values with improved accuracy, particularly for missense variants.

- ThermoMPNN is a deep learning-based method that uses graph neural networks trained on massive mutational data to predict effects of mutations on protein stability, including single and double mutants, and can infer potential pathogenicity by modeling ΔΔG landscapes. 

## Summary

In this section, we will explore pathogenicity prediction tools that utilize the structural data of proteins. FoldX, DynaMut, PremPS, and ThermoMPNN are widely used computational tools for predicting the pathogenicity of protein mutations by estimating changes in protein stability. Each method has its own underlying architecture, offering distinct advantages and limitations. To improve reliability, it is often necessary to cross-validate the outputs of these tools. Collectively, they enable us to prioritize potentially pathogenic mutations by quantifying their thermodynamic impact on protein structure and function.

![science adj8672-f1](https://github.com/user-attachments/assets/a602ca69-b6d2-4e9d-a93f-44ee2415024b) from Science Journal

## Software downlaod

🔑 You are required to register for the FoldX server under the academic license, which is free of charge.

To register, please follow this link: https://foldxsuite.crg.eu/academic-license-info

❗️ There are two tutorial videos, one for Mac and one for Windows, on how to install FoldX locally on your computer. You are expected to install FoldX before coming to class by following these tutorials, as there will be no time to do so during the session. If you are having issues, do not hesitate to contact me!

❗️❗️ Please try to download FoldX at least three days in advance of the class so that we can solve any potential issues and avoid delays in obtaining the academic license. I will not be able to assist with installation issues on the day of the class.

## References

Link to the FoldX paper: https://academic.oup.com/nar/article/33/suppl_2/W382/2505499

Link to the DynaMut paper: https://academic.oup.com/nar/article/46/W1/W350/4990022?login=false

Link to the PremPS paper: https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008543

Link to the ThermoMPNN paper: https://www.science.org/doi/10.1126/science.add2187

Tool access:

➡️ Link to the DynaMut server: https://biosig.lab.uq.edu.au/dynamut/

➡️ Link to the PremPS server: https://lilab.jysw.suda.edu.cn/research/PremPS/research/PremPS/

➡️ Link to the ThermoMPNN Colab: https://colab.research.google.com/drive/1OcT4eYwzxUFNlHNPk9_5uvxGNMVg3CFA

## Slides

https://docs.google.com/presentation/d/1DyIXaXer8BrBsRzPI62I9Tl4_k4rsK4JK6lR7Qz7M1w/edit?usp=sharing

## 🚨 Attention: pre-course action

In the first half of this section, we will discuss various structure-based pathogenicity prediction tools, and in the second half, we will perform free energy calculations on our target proteins to assess the effects of mutations. Therefore, before coming to class, please select a human protein from the PDB or UniProt that you are interested in, preferably in a monomeric form for simplicity. Download the corresponding PDB structure (in .pdb format) and record the entry ID. You are also expected to select three different variants of your target protein, classified as pathogenic, of uncertain significance, and benign. To choose these variants, you can use the "Variant Viewer" available under the "Disease & Variants" section in UniProt. You can also extract variant information from gnomAD. Additionally, it is recommended to select variants that are located within the same 3D environment, such as being in close proximity within a specific domain of the protein. 


## 🏠 Take-home points 

- FoldX is a physics-based method that calculates changes in free energy (ΔΔG) upon mutation using an empirical force field, offering fast and relatively accurate predictions, particularly for point mutations.

- DynaMut combines normal mode analysis with statistical potentials to assess both structural stability and changes in protein dynamics, providing insights into flexibility alterations caused by mutations.

- PremPS employs a hybrid approach integrating structural, energetic, and evolutionary features through machine learning to predict ΔΔG values with improved accuracy, particularly for missense variants.

- ThermoMPNN is a deep learning-based method that uses graph neural networks trained on massive mutational datasets to predict mutation effects on protein stability, including single and double mutants, and can infer potential pathogenicity by modeling ΔΔG landscapes. 

## Summary

In this section, we will explore pathogenicity prediction tools that utilize the structural data of proteins. FoldX, DynaMut, PremPS, and ThermoMPNN are widely used computational tools for predicting the pathogenicity of protein mutations by estimating changes in protein stability. Each method has its own underlying architecture, offering distinct advantages and limitations. To improve reliability, it is often necessary to cross-validate the outputs of these tools. Collectively, they enable us to prioritize potentially pathogenic mutations by quantifying their thermodynamic impact on protein structure and function.

![science adj8672-f1](https://github.com/user-attachments/assets/a602ca69-b6d2-4e9d-a93f-44ee2415024b) Science


## References

Link to the FoldX paper: https://academic.oup.com/nar/article/33/suppl_2/W382/2505499

Link to the DynaMut paper: https://academic.oup.com/nar/article/46/W1/W350/4990022?login=false

Link to the PremPS paper: https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1008543

Link to the ThermoMPNN paper: https://www.science.org/doi/10.1126/science.add2187

Tool access:

➡️ Link to the DynaMut server: https://biosig.lab.uq.edu.au/dynamut/

➡️ Link to the PremPS server: https://lilab.jysw.suda.edu.cn/research/PremPS/research/PremPS/

➡️ Link to the ThermoMPNN Colab: https://colab.research.google.com/drive/1OcT4eYwzxUFNlHNPk9_5uvxGNMVg3CFA

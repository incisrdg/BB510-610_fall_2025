## 🏠 Take-home points

- Protein-protein interaction (PPI) prediction problem is the challenge of predicting whether and how two proteins interact, often from sequence or structural information, given the complexity and variability of biological interfaces.

- Rigid-body docking assumes proteins remain structurally rigid and searches for the best geometric and physicochemical fit between their surfaces.

- Flexible-docking allows conformational changes, typically in side chains or loops, to better capture realistic protein–protein interactions.

- Ensemble-docking uses multiple conformations of proteins (from experiments or simulations) to account for structural flexibility during docking.

- Machine learning approaches learn interaction patterns directly from large datasets of protein sequences and structures, enabling end-to-end prediction of binding likelihoods and interfaces.

## Summary

In this section, we will discuss various protein–protein docking methods, their theoretical foundations, and applications. Protein–protein docking is a computational strategy used to predict the structures of protein complexes from known subunits and represents an upper-level challenge built on protein structure prediction. The field has evolved over several decades, beginning with rigid-body docking in the 1970s–1980s, which relied on surface complementarity, advancing to scoring-based and flexible docking in the 1990s–2000s to account for side-chain and backbone motions, and later to ensemble docking, which incorporates conformational variability. Most recently, deep learning–based methods such as AlphaFold-Multimer have achieved unprecedented accuracy by leveraging large-scale sequence and structure datasets.

![ProteinComplexStructure-2](https://github.com/user-attachments/assets/c42dcaed-9135-4031-be60-9a4edab16670)

from Stony Brook University

## Softwares

Link to the ClusPro server: https://cluspro.bu.edu/home.php

Link to the HADDOCK web server: https://rascar.science.uu.nl/haddock2.4/submit/1

Link to the Tamarind Bio server: https://www.tamarind.bio/

## References

Link to the paper Machine learning to predict de novo protein–protein interactions: https://www.cell.com/trends/biotechnology/fulltext/S0167-7799%2825%2900158-1

Link to the paper Modulation of p53 binding to MDM2: computational studies reveal important roles of Tyr100: https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-10-S15-S6#Sec9

Link to the paper Calcium Signalling in Heart and Vessels: Role of Calmodulin and Downstream Calmodulin-Dependent Protein Kinases: https://www.mdpi.com/1422-0067/23/24/16139

Link to the paper of Elucidation of protein function using computational docking and hotspot analysis by ClusPro and FTMap: https://journals.iucr.org/d/issues/2022/06/00/qg5007/qg5007fig1.html

Link to the active and passive residue selection in HADDOCK: https://www.bonvinlab.org/haddock-restraints/active_passive.html

Link to the paper on Modeling Protein–Glycan Interactions with HADDOCK: https://pubs.acs.org/doi/10.1021/acs.jcim.4c01372

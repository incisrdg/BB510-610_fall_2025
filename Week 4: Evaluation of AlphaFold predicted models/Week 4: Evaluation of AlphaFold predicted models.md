## 📝 Take-home work (10 pts) ❗️(The deadline is 2025-11-11 at 12 pm)❗️

After this section, you will be given a take-home assignment in which you will evaluate six AF2-predicted structures based on the metrics (pLDDT, PAE, pTM) discussed in the course. For each structure, please briefly explain the results of the scores and discuss their effects and interpretation in the context of the protein’s structure. You can retrieve the structures from the AlphaFold database using the following entry names:

1) AF-Q8W3K0-F1-v4, AF-Q5VSL9-F1-v4 (0.5 + 0.5 pts)
2) AF-Q9UPX6-F1-v4 (1 pts)
3) IL37-IL18R1_complex (2 pts)            
4) AF-Q9P0S9-F1-v4 (3 pts)
5) AF-Q99972-F1-v4 (3 pts)

The naming convention follows this structure: “AF” denotes an AlphaFold prediction, “Q8W3K0” represents the corresponding UniProt accession code, “F1” indicates the first segment of the predicted sequence (as AlphaFold divides structures exceeding 1,400 aas into segments), and “v4” specifies the version of the model. When searching in the AlphaFold database, you must use either the protein’s name or its UniProt accession code, entering the full identifier (e.g., “AF-Q8W3K0-F1-v4”) will not return any results! 

❓ Take-home assignment guidline:

- For the two entries listed in the first section, evaluate the structures based on their pLDDT and PAE scores, examine the TED domains, and provide a detailed discussion of the annotated domain’s function. (max 4 lines for each entry)

- For the second entry, assess the structures with respect to their pLDDT, PAE, and TED domains, and provide a detailed discussion on disorders. (max 4 lines)

- For the third entry, evaluate the given protein complex in terms of its pLDDT, ipLDDT, PAE, iPAE, pTM, ipTM, and TED domains, and provide an in-depth discussion of the interface. (Prediction is provided in the week 4 materials.) (max 6 lines)
   - To identify the interface, please use the Python script provided in the week 4 section.
   - Once the interface has been identified, calculate the ipLDDT, iPAE, and ipTM values by averaging the scores corresponding to the interface residues (You can do averaging using a short Python script or simply in Excel).
  
- For the fourth entry, assess the structures with respect to their pLDDT, PAE, and TED domains and consider the TmAlphaFold database to provide a discussion of the results with respect to membrane localization. Compare the structural differences between the AF2-predicted structure and the ground truth (PDB ID: 2LOS_A) by calculating the RMSD after structural alignment. Taking into account the pLDDT and PAE scores, as well as the ground truth structure, discuss the prediction accuracy of the AF2-generated model. Based on the structural accuracy, provide a discussion on the membrane localization. (max 6 lines)
  
- For the fifth entry, assess the structures with respect to their pLDDT, PAE, and TED domains, and survey the human myocilin "fragments" deposited in the PDB and compare them with the AlphaFold2-predicted model, highlighting any global structural differences (Please pay attention that the olfactomedin domain is the C-terminal fragment of the myocilin). Then check the UniProt database to determine the protein’s function, and use this information to rationalize the structural differences observed between the computationally predicted model and the experimental structures. 
   - In one of the PDB entries, one of the side helices differs from the others. Identify and report that structure, compare its motif to the AF2-predicted model, and discuss what this local structural deviation might suggest about the protein’s evolutionary history and importance of that structural motif. (max 8 lines)

🌄 You may also include score plots, structural visualizations, and comparative graphs of the proteins to support and strengthen your discussion.
  
## 🏠 Take-home Points

- AlphaFold provides several confidence metrics such as pLDDT, ipLDDT, PAE, iPAE, pTM, and ipTM to help assess the quality and reliability of its accuracy of predicted protein structures.

- The pLDDT score provides local (per-residue) confidence, reflecting the accuracy of predicted secondary structures, while ipLDDT offers an analogous measure for interface regions.

          - pLDDT>90: very high
          - 70<pLDDT<90: confident
          - 50<pLDDT<70: low
          - pLDDT<50: very low
  

- The PAE (Predicted Aligned Error) score, a continuous metric, reflects the confidence in the relative positioning between pairs of residues (with iPAE used for interface regions). It is particularly informative for domain–domain positioning, multimer interface orientation, flexible or hinge regions.

- The pTM (predicted TM-score) provides an estimate of the global structural accuracy of a predicted model, evaluating the correctness of the overall protein fold .
  
          - pTM>0.5: similar fold
          - pTM<0.5: wrong fold

  - TmAlphaFold database TmAlphaFold database provides open access to the membrane orientation of alpha-helical transmembrane protein's structure predicted by AlphaFold together with the evaluation of the predicted structures.

## Summary
Deep learning methods such as AlphaFold and RoseTTAFold have dramatically advanced ability to predict the structures of proteins and protein–protein complexes. However, accurately evaluating the confidence and accuracy of these predictions is equally important, especially for guiding experimental validation or downstream applications like drug design and variant analysis. Confidence metrics such as pLDDT and PAE, generated by the models themselves, provide residue-level and inter-residue/inter-domain error estimates. For protein complexes, additional scores like the predicted TM-score (pTM), interface predicted TM-score (ipTM) help assess global and interface-specific accuracy. Therefore, thorough assessment of both global and local predicted structural motifs is critical for accurately interpreting and validating deep learning–based structural predictions. This is one of the most important sections of the course, and it is crucial to develop a fundamental understanding of these confidence scores. Do not worry, we will discuss them extensively and work through various cases to become familiar with their use and implementation. Despite its importance and the effort it takes to understand, I believe this is the most enjoyable week of the course! 🥳


<img width="583" height="533" alt="rra1_rra1_plddt" src="https://github.com/user-attachments/assets/d8cdc415-c2e4-437c-b3d2-b172810edbc6" /> 

AlphaFold2 precition of RRA1-RRA1 dimer

## Databases

Link to the AlphaFold database: https://alphafold.ebi.ac.uk/

Link to the TmAlphaFold database: https://tmalphafold.ttk.hu/

Link to the TmDet server: https://tmdet.unitmp.org/

Link to the CCTOP server: https://cctop.ttk.hu/job/submit

## References

Link to the paper on lDDT metric: https://academic.oup.com/bioinformatics/article/29/21/2722/195896?login=true

Link to the paper of ColabFold: https://www.nature.com/articles/s41592-022-01488-1

Link to the paper of TmAlphaFold: https://academic.oup.com/nar/article/51/D1/D517/6786192?login=false

pLDDT score:

   ➡️ Link to the AF2 structure AF-Q8IZS7-F1: https://alphafold.ebi.ac.uk/entry/Q8IZS7

   ➡️ Link to the AF2 structure AF-Q3S2X4-F1: https://alphafold.ebi.ac.uk/entry/Q3S2X4

   ➡️ Link to the AF2 structure AF-P36883-F1: https://alphafold.ebi.ac.uk/entry/P36883

PAE score:

   ➡️ Link to the AF2 structure AF-Q9NRI5-F1: https://alphafold.ebi.ac.uk/entry/Q9NRI5

   ➡️ Link to the AF2 structure AF-P9WNQ7-F1: https://alphafold.ebi.ac.uk/entry/P9WNQ7

   ➡️ Link to the AF2 structure AF-O15121-F1: https://alphafold.ebi.ac.uk/entry/O15121

Link to the paper "How significant is a protein structure similarity with TM-score = 0.5?" : https://academic.oup.com/bioinformatics/article/26/7/889/213219
   
Link to the paper "Scoring function for automated assessment of protein structure template quality": https://onlinelibrary.wiley.com/doi/full/10.1002/prot.20264?casa_token=hX_5at8e3FsAAAAA%3AKUNF1hwKQIVYIOGv2noTxnulTMCVb5ut5vLXkZ-eIuajcLKghchnCjsD97mN91Qw2Y6HQocFjxEU0x5P

Link to the paper "Interrogation and validation of the interactome of neuronal Munc18-interacting Mint proteins with AlphaFold2": https://www.biorxiv.org/lookup/doi/10.1101/2023.02.20.529329

## Slides

https://docs.google.com/presentation/d/1xrgTU-YrxNIb44ym3nXpIGljJDZzavWqU8Lh6kGjZdk/edit?usp=sharing

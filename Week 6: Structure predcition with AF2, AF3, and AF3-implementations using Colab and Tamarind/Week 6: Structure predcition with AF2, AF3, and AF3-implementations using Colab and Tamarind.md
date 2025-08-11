## 🚨 Attention: pre-course action

In this section, we will perform protein structure predictions using ColabFold (for AF2), AF3 server, and Tamarinde Bio server (for Boltz-2 and Chai-1). Please create accounts for the servers in advance of the session via the links provided on the README page.

❗️ You are also expected to select a monomeric and a dimeric (hetero-/homo-dimer) human protein and extract the corresponding FASTA sequence from the UniProt. Avoid structures larger than 500 aas to save time. Verify the PDB entries to obtain the ground truth structures/complexes. (Make sure that your structures/complexes have ground truths, in other words experimentally resolved structures, available in the PDB.)

🤓 Here are some suggestions: 

- IL37 and IL18Rα

- PDB ID: 7x2l

- Human Nars1 protein

- Drosophila Sep2 and Sep5 

## 🏠 Take-home points

- Adding lipids can help support the correct orientation of membrane-embedded proteins.

- Adding salts can help proteins fold into the native conformation.

- Natural ligands can provide structural information that guides the positioning of specific ligand backbones.

- Be aware of hallucinations when predicting structures of larger protein sequences.

- Multiple copies may superimpose during the prediction of higher-order oligomeric assemblies.

- 1/20 seeds got confident prediction scores.

## Summary

This section focuses on structure predictions using four different methods: AF2, AF3, Boltz-2,
and Chai-1. The goal is to evaluate how various parameters such as model type, number of recycles, number of seeds, presence of ions, presence of lipids, and the introduction of pocket and contact restraints affect the prediction outcomes. We will also discuss practical hacks and warnings to consider during protein structure prediction.

<img width="672" height="367" alt="Screenshot 2025-08-06 at 08 25 01" src="https://github.com/user-attachments/assets/90fc4ece-9bf8-48fc-9658-6fd830207281" />
 from Sergey Ovchinnikov’s slides

## References

Sergey Ovchinnikov’s slides

## Slides

https://docs.google.com/presentation/d/1MeapGNPZwZcQyvFA1ts-XJdXpp9gv7b2nevZYu8CEAc/edit?usp=sharing

## 🚨 Attention: pre-course action

In this section, we will perform protein structure predictions using Colab multimer (for AF2), AF3 server, and Tamarinde Bio (for Boltz-2 and Chai-1). Please create accounts for the servers in advance of the session through the links provided on the README page. We will commence the predictions during the workshop session of the course.

##  📝 Take-home work

This workshop presents a case study in which we will perform structure predictions over an antibody–antigen (Ab–Ag) complexe that was entirely blind by all these prediction methods, in other words, the complex was released after the training cut-off of these methods.

- Our candidate, PDB ID 7ZK1, is the crystal structure of cystinosin, a proton-driven cystine transporter, bound to both a sybody and a nanobody. Here what it looks like:

  <img width="250" height="371" alt="image1-2" src="https://github.com/user-attachments/assets/b822be23-8672-4e5e-89bb-221ef7bfc4f4" />

- For simplicity, let's assume that we are only interested in interaction between the synthetic nanobody (sybody) and the transporter.

1) Please retrieve the structure from the PDB along with the FASTA sequences for all chains.

2) Perform complex prediction with AF2 via Colab
   - Employ multimer_v3 model 
   - Adjust # of recycles to 6. (Attention: Only one prediction can be run at a time in Colab.)

3) Perform complex predictions with AF3 via AF3 server
   - Adjust # of seeds to 1 and 20, respectively. (2 different predicitons will be obtained)

4) Perform complex predictions with Chai-1 via Tamarind Bio
   - Adjust # of seeds to 1 and # of recycles to 20
   - Apply a pocket restraint to the antibody
   - Please assign unique job names in Tamarind Bio, as jobs with identical names will be overwritten.

5) Perform complex predictions with Boltz-2 via Tamarind Bio
   - Adjust # of seeds to 1 and # of recycles to 20
   - Apply a contacts restraint to the antibody
   - Please assign unique job names in Tamarind Bio, as jobs with identical names will be overwritten.


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

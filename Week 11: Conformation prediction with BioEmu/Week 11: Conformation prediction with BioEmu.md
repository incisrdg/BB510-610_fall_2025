## 📝 Workshop report (The deadline is 12:00 a.m. on the same day) (8 pts)

The second half of this course will be a workshop session. For the desired protein, please perform conformation prediction with BioEmu using the following parameters: num_samples=20, model_name=bioemu-v1.1, n_write_samples=-1, and enable the options reconstruct_sidechains, run_md, and one_per_cluster. Set the md_protocol to local minimization. 

- Superimpose the predicted conformations and upload a snapshot of the aligned structures. (1 pt)

- Extract the experimental structure of the target protein from the PDB (if available) and the AF2-predicted structure from the AF2 database. Calculate the RMSD of the BioEmu-predicted conformations by aligning them to the experimental structure and the AF2-predicted structure, respectively. (3 pts)

- Using experimental structural data or other experimental evidence available in the literature, assess the BioEmu-predicted structures and discuss how successfully it captured different conformations. If BioEmu failed to capture different conformations, discuss possible reasons behind this limitation. Additionally, discuss the structural differences between the AF2-predicted and BioEmu-predicted models, explaining the underlying reasons for these differences. (4 pts)


## 🏠 Take-home points

- BioEmu generates protein ensembles, not a single static structure, providing rapid insights into conformational diversity and stability shifts that are critical for understanding protein function.

- It learns an energy-based scoring function to approximate the Boltzmann distribution of protein conformations, enabling accurate sampling of equilibrium ensembles.

- It selects structures from the learned distribution and refines them through diffusion to produce realistic conformational states much faster than MD. 

## Summary
So far, we have discussed various protein structure prediction methods. However, understanding a protein’s function often requires more than a single static structure. BioEmu is a generative AI model that rapidly produces accurate structural ensembles, achieving results comparable to long molecular dynamics (MD) simulations but within hours on a single GPU. Trained on AlphaFold structures, MD trajectories, and experimental stability measurements, it captures conformational diversity and stability shifts that are valuable for drug design and protein engineering.

![BioEmu-1-TWLIFB-1200x627-2](https://github.com/user-attachments/assets/2dd0c9bb-d0e6-418e-95d3-b711464f5ff5)

Microsoft research

## References

Link to the preprint of BioEmu: https://www.biorxiv.org/content/10.1101/2024.12.05.626885v2.full

Link to the paper of BioEmu: https://www.science.org/doi/10.1126/science.adv9817

Link to the BioEmu Colab notebook: https://colab.research.google.com/github/sokrypton/ColabFold/blob/main/BioEmu.ipynb

## Slides 

https://docs.google.com/presentation/d/1V6P8oMm3ujYXSQmNXnVrqyHzTePNntoS5J5__87bu2E/edit?usp=sharing




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

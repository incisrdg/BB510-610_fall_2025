## ❗️Attention: 

This section covers the theoretical and computational background of deep learning models on protein structure prediction. For ease of understanding, you are expected to read the first two papers in the reference section, which focus on the architectures of AF2 and AF3.

## 🏠 Take-home points:

**AF2 architecture**

Input representation module:
- Input: protein sequence + multiple sequence alignments (MSAs) + optional templates
- Output: MSA representation (N sequences × L residues), pair representation (L × L contact map prior)

Evoformer module:    
- Input: MSA representation + pairwise representation
- Transformer-based blocks: row attention → column attention → transition → out-product mean → triangle representation
- Output: learned MSA representation + pairwise representation

Structure module:    
- IPA → backbone fitting → side chain placement

##

**AF3 architecture**

Input representation module:
- Input: protein sequence + multiple sequence alignments (MSAs) ( optional templates) + nucleis acid sequences/small molecules/ions/water (optional docking poses)
- Output: single representation (N sequences × L residues), pair representation (L × L contact map prior) [no MSA representation]

Pairformer module:    
- Input: single representation + pair representation
- Pairformer block: single attention → pair attention → single-pair communication [no triangle representation]
- Output: refined single and pair embeddings

Geometric module
- Pairwise distances
- Orientations
- Angular/geometric features

Structure module:
- Diffusion module → denoising

##

## Summary

AlphaFold2 (AF2) introduced a groundbreaking architecture combining a pair representation (capturing residue-residue interactions) and a MSA representation (capturing evolutionary information) through iterative attention-based modules called Evoformer blocks. It outputs 3D structures via a structure module using invariant point attention and backbone torsion angle prediction. AlphaFold3 (AF3) extends this by unifying the architecture to handle diverse biomolecular inputs including proteins, nucleic acids, and small molecules through a multimodal tokenization and attention mechanism. Instead of separate MSA and pair inputs, AF3 uses a general-purpose architecture inspired by diffusion and generative models, incorporating explicit geometric representations and a diffusion-based structure sampling strategy. Open-source AF3-implementations like Boltz and Chai replicate AF3’s architecture with slight variations: Boltz-1 implements a deep learning model refining the AF3 framework with improved input processing, architectural adjustments, and a redesigned confidence while Chai-1, with the same model architecture and training strategy with AF3, supports experimental restraints for enhanced accuracy and can function without MSAs.

![gr9_lrg](https://github.com/user-attachments/assets/71bff1b7-713f-4f27-9f95-3832132e92fb)
(AF2, ESMFold, AF3, respectively.) 
Pratt, Olivia S., et al., 2025

## References

Link to the paper of AF2: https://www.nature.com/articles/s41586-021-03819-2

Link to the paper of AF3: https://www.nature.com/articles/s41586-024-07487-w

Link to the paper on "Assessing the Performance of AF2 and AF3-Implementations on Antibody-Antigen Complexes": https://www.biorxiv.org/content/10.1101/2025.07.25.666870v1.abstract

Link to the paper of Boltz-1: https://www.biorxiv.org/content/10.1101/2024.11.19.624167v1.full

Link to the paper of Chai-1: https://www.google.com/search?client=safari&rls=en&q=chai-1&ie=UTF-8&oe=UTF-8

## Slides

https://docs.google.com/presentation/d/1C6mlZ-NunWhLkgmeJsuTbuPWF2K-Dnvji4RLWvaEyOY/edit?usp=sharing

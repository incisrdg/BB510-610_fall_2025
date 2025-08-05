## ❗️Attention: 

This section covers the theoretical and computational background of deep learning models on protein structure prediction. For ease of understanding, you are expected to read the first two papers in the reference section, which focus on the architectures of AF2 and AF3.

## Take-home points:

AF2 architecture

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

AF3 architecture

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

## References

Link to the paper of AF2: https://www.nature.com/articles/s41586-021-03819-2

Link to the paper of AF3: https://www.nature.com/articles/s41586-024-07487-w

Link to the paper on "Assessing the Performance of AF2 and AF3-Implementations on Antibody-Antigen Complexes": https://www.biorxiv.org/content/10.1101/2025.07.25.666870v1.abstract

Link to the paper of Boltz-1: https://www.biorxiv.org/content/10.1101/2024.11.19.624167v1.full

Link to the paper of Chai-1: https://www.google.com/search?client=safari&rls=en&q=chai-1&ie=UTF-8&oe=UTF-8

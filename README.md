# MIT Sports Analytics Paper Competition

## Overview
This repository accompanies the abstract submission for the MIT Sports Analytics Paper Competition. As discussed with Kelly Condon (MIT responsible for the competition), due to the high volume of submissions, abstracts may be submitted with a placeholder GitHub link. The full implementation and code will be provided at the full paper deadline.

## Repository Structure (to be updated)
project/

├── data/ # Placeholder for public datasets

├── src/ # Core algorithms (to be released with full paper)

├── notebooks/ # Reproducibility workflows

└── README.md # Project documentation

## Data
- **Current submission**: uses synthetic/public placeholders.  
- **Full paper version**: will include adapted pipelines with publicly available data.  

## Instructions
For now, no runnable code is attached.  
Once the full paper is requested, this repository will be updated with:

- Preprocessing scripts  
- Core algorithm implementation  
- Reproducibility instructions  

---

## Abstract
Football clubs face a persistent challenge: when a key player departs or suffers injury, the disruption to tactical systems and team performance is immediate — yet effective replacements are often neither instant nor data-informed. The scouting process remains largely intuition-driven, struggling to deliver timely and context-aware decisions at the speed modern football demands (Rein & Memmert, 2016; Güllich et al., 2022).

This paper introduces a scalable, data-driven framework for modeling player similarity and tactical fit. Built on over 750 million data points collected from multi-source providers, the system processes 400+ variables per player, unified through a normalized PostgreSQL–TimescaleDB architecture optimized for high-frequency querying and temporal analysis (Junqueira et al., 2021).

The core of the similarity engine is a multi-stage pipeline:
- Dimensionality Reduction via PCA, tailored per position and league, to isolate the most relevant statistical components (Jolliffe & Cadima, 2016).
- Cluster Modeling using K-Means and silhouette scoring, defining sub-profiles within each player role (e.g., creative midfielders, ball-playing centre-backs) (Bunker & Thabtah, 2019).
- Feature Selection based on inter-cluster variance, ensuring that similarity is grounded in the most discriminative metrics for each context.
- Similarity Search using Euclidean and cosine distance functions on reduced spaces, returning top-N matches by profile fit (Decroos et al., 2019).
- Context Filters allow clubs to constrain searches by salary range, development stage, league pace, or tactical role.

The resulting engine enables clubs to:
- Instantly identify stylistic replacements grounded in tactical and economic reality.
- Benchmark youth players against elite-level role models based on developmental curves (Liu et al., 2022).
- Discover undervalued talents with near-identical statistical footprints to high-value players.

This paper argues that scouting should not rely on memory, anecdote, or highlight reels, but rather on mathematical proximity, tactical embeddings, and contextualized role modeling. In a game increasingly shaped by marginal gains and short transfer windows, a universal language of similarity may be the foundation for more intelligent, reactive football strategy.

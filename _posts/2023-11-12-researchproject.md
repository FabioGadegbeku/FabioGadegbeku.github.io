---
layout: post
title: Similarity Based Constraint Score for Feature Selection
author: Fabio
tags:
date: 2023-11-12 13:56 +0800
last_modified_at: 10-04-2024
---
Master 1 research project about implementing a new constraint score. This score is crafted upon the foundation of similarity matrices constructed within a lower-dimensional subspace, offering the unique capability to evaluate the relevance of all features simultaneously. You can find the full report here :[Constraint Scores](https://jmp.sh/s/2toaZNCVRbycgtyos5Nf) (Or click on the title for more details)
{: .message }

# Similarity-Based-CS
This project addresses the curse of dimensionality in feature selection methods, with a focus on supervised and semi-supervised learning. It introduces a novel constraint score that evaluates the relevance of feature subsets in a lower-dimensional subspace, taking into account correlations between features and avoiding high-dimensional original feature spaces.

## Key Components :

- Curse of Dimensionality: The project tackles the challenges associated with high-dimensional data and the impact on machine learning tasks.

- Feature Selection: Describes the process of selecting a subset of relevant features to improve model efficiency and effectiveness.

- Constraint Scores: Explains the use of must-link and cannot-link constraints and their limitations when evaluating individual features.

- Correlations Between Features: Highlights the importance of considering feature interactions and dependencies in real-world data.

- High-Dimensional Original Feature Space: Discusses the issues associated with working in high-dimensional spaces and its impact on similarity computation.

- New Constraint Score: Introduces the primary focus of the project, which is the development of a novel constraint score that operates on feature subsets in a lower-dimensional subspace.


## How To Use :

- Information and descriptions of the state of the art constraint scores and our new similarity based constraint score can be found in the report pdf.

- To use the implementations of these scores clone the repository and the scores can be found in the c_scores.py file inside the sim_based_cs folder.

- In c_scores.py you'll also find functions for preprocessing your data, plotting results, and computing the rank matrix.

- In the notebook you can find the results obtained by my implementations.

If there's any problem or questions don't hesitate to contact me !

Link to the projects github : [Similarity-Based-CS](https://github.com/FabioGadegbeku/Similarity-Based-CS).

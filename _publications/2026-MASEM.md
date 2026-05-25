---
title: "Manifold Sampling via Entropy Maximization"
collection: publications
category: underReview
authors:
    - Cornelius V. Braun*
    - <strong>Tilman Burghoff*</strong>
    - Marc Toussaint
preview_image: /images/masem_grid_mp_htcol.svg
excerpt: 'Sampling points from disconnected Manifolds by using a entropy-maximizing resampling strategy.'
date: 2026-05-12
venue: 'Under Review'
links: '[arXiv](https://arxiv.org/abs/2605.12338) | [Bibtex](/files/braun2026manifold.bib)'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
Scaling up datasets is highly effective in improving the performance of deep learning models, including in the field of robot learning. However, data collection still proves to be a bottleneck. Approaches relying on collecting human demonstrations are labor-intensive and inherently limited: they tend to be narrow, task-specific, and fail to adequately explore the full space of feasible states. Synthetic data generation could remedy this, but current techniques mostly rely on local trajectory optimization and fail to find diverse solutions. In this work, we propose a novel method capable of finding diverse long-horizon manipulations through black-box simulation. We achieve this by combining an RRT-style search with sampling-based MPC, together with a novel sampling scheme that guides the exploration toward stable configurations. Specifically, we sample from a manifold of stable states while growing a search tree directly through simulation, without restricting the planner to purely stable motions. We demonstrate the method's ability to discover diverse manipulation strategies, including pushing, grasping, pivoting, throwing, and tool use, across different robot morphologies, without task-specific guidance. 
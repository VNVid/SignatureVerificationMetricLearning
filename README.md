# Methods for Signature Verification using Metric Learning

This repository contains the code and documentation for my bachelor thesis, titled **"Methods for Signature Verification using Metric Learning."** The work focuses on exploring various loss functions for signature verification tasks using metric learning.

## Abstract

Handwritten signatures are a critical component of identity verification in financial and commercial contexts. While convolutional neural networks have been widely used in signature verification, recent research highlights metric learning as a promising approach. This thesis investigates the impact of different loss functions on the performance of neural networks trained for signature verification using metric learning.

## Key Contributions

1. **Comparison of Loss Functions**:
   - Analyzed the performance of two popular loss functions: **contrastive loss** and **triplet loss**.
   - Proposed a novel **modified loss function** combining the strengths of contrastive and triplet loss.

2. **Experimental Setup**:
   - Model architecture: ResNet18 without pretraining.
   - Dataset: SigComp2011 (Dutch).
   - Vector dimensionality: 128.
   - Distance metric: Euclidean distance.

3. **Findings**:
   - **Triplet loss** achieved the best overall performance by avoiding overfitting.
   - The **modified loss function** improved certain metrics compared to contrastive loss but underperformed compared to triplet loss on unseen data.


## Loss Functions Overview

### Contrastive Loss
Encourages similar signatures to cluster tightly while pushing apart dissimilar ones beyond a margin.

### Triplet Loss
Uses anchor, positive, and negative samples to ensure that genuine signatures are closer to the anchor than forged ones by a defined margin.

### Modified Loss
Combines triplet loss with a relaxed version of contrastive loss to mitigate excessive clustering of genuine signatures.

## Results

   - Contrastive Loss: Overfitting on training data; poor generalization.
   - Triplet Loss: Balanced training and testing performance.
   - Modified Loss: Moderate improvement over contrastive loss on some metrics but did not outperform triplet loss overall.

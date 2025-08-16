# Do Sparse Subnetworks Exhibit Cognitively Aligned Attention? Effects of Pruning on Saliency Map Fidelity, Sparsity, and Concept Purity

Submitted to **CogInterp: Interpreting Cognition in Deep Learning Models, NeurIPS Workshop 2025**.

Prior works have shown that neural networks can be heavily pruned while preserving performance, but the impact of pruning on interpretability remains unclear. In this work, we investigate how magnitude-based pruning followed by fine-tuning affects both low-level saliency maps and high-level concept representations. Using a ResNet-18 trained on ImageNette, we compare post-hoc explanations from Vanilla Gradients (VG) and Integrated Gradients (IG) across pruning levels, evaluating sparsity and faithfulness. We further apply CRAFT-based concept extraction to track changes in semantic coherence of learned concepts.

Our results show that light to moderate pruning improves saliency map focus and reliability while retaining distinct, semantically meaningful concepts. In contrast, aggressive pruning merges heterogeneous features, reducing concept purity despite maintaining accuracy. These findings suggest that judicious pruning can guide internal representations toward more human-aligned attention patterns, while excessive pruning undermines interpretability.

## Requirements
- kornia (for applying filters to feature-maps)
- captum (for saliency maps)
- quantus (for computing several metrics for saliency maps)
- Ranger Optimizer (for optimizing ResNet model during training)
- craft-xai (for concept explainability)


## Structure
    - craft: This folder contains the craft.ipynb file to measure concept importance for the models. There are two more folders "collected_images" and "concept_visualization" which consists of images used to measure the importance and the outputs respectively. The code has been derived from this github link: https://github.com/deel-ai/Craft
    - explanations: This folder consists of all the quanlitative explanations produced by the RESNET models.
    - models: This folder contains the trained normal and pruned models.
    - plots: This folder consists of roadplots and other comparision plots for the models.
    - calculate_road.ipynb: Code to measure ROAD metrics for the models.
    - calculate_sparsity.ipynb: Code to measure sparsity of models.
    - generate_plots.ipynb:Code to geenrate various plots shown in the paper.
    - lottery_ticket.ipynb: This file consists of code to train normal and pruned networks using lottery hypothesis method.
    - metrics.ipynb: Implementation of helper functions related to explanation metrics.
    - resnet_18.py: Implementation of ResNet 18 model.
    - saliency_maps.ipynb : Code to generate saliency maps for models using various explanation methods.
    - utils.ipynb: Helper functions.

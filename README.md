# Do Sparse Subnetworks Exhibit Cognitively Aligned Attention? Effects of Pruning on Saliency Map Fidelity, Sparsity, and Concept Purity

Repository for the paper "Do Sparse Subnetworks Exhibit Cognitively Aligned Attention? Effects of Pruning on Saliency Map Fidelity, Sparsity, and Concept Purity", submitted on CogInterp: Interpreting Cognition in Deep Learning Models, NeurIPS Workshop 2025.

This paper provides our implementation of building efficient and interpretable models using various deep learning model Pruning strategies.

## Requirement
- kornia (for applying filters to feature-maps)
- captum (for saliency maps)
- quantus (for computing several metrics for saliency maps)
- Ranger Optimizer (for optimizing ResNet model during training)
- craft-xai (for concept explaianbility)


## Structure
    - craft: This folder contains the craft.ipynb file to measure concept importance for the models. There are two more folders "collected_images" and "concept_visualization" which consists of images used to measure the importance and the outputs respectively.
    - explanations: This folder consists of all the quanlitative explanations produced by the RESNET models.
    - models: This folder contains the trained normal and pruned models.
    - plots: This folder consists of roadplots and other comparision plots for the models.
    - calculate_road.ipynb: Code to measure ROAD metrics for the models.
    - calculate_sparsity.ipynb: Code to measure sparsity of models.
    - generate_plots.ipynb:Code to geenrate various plots shown in the paper.
    - lottery_ticket.ipynb: This file consists of code to train normal and pruned networks using lottery hypothesis method.
    - metrics.ipynb: Implementation of helper functions related to explanation metrics.
    - resnet_18.py: Implementation of ResNet 18 model.
    - saliency_maps.ipynb : Code to genrate saliency maps for models using various explantion methods.
    - utils.ipynb: Helper functions.

# Challenge 17: Hybrid Machine Learning Approaches for Land–Atmosphere Flux Modelling

Author: Xu Shan, Sujan Koirala, and Nuno Carvalhais

This repo is a forked repo from [SindbadTutorials.jl](https://github.com/LandEcosystems/SindbadTutorials.jl) for the Challenge 17 of the AI4PEX winter school at Athens in 2026. The original repo is developed by the team of Model-Data Integration Group at Max Planck Institute of Biogeochemistry. The tutorials are designed to be run in a `terminal` or in a `Colab` notebook, and they will guide you through the process of building hybrid by exploring different ML architectures for biogeochemical processes (for example, GPP sensitivity to air temperature) to improve the generalizability of the hybrid models across different locations and time scales.

The installation of the tutorial is found here: [Tutorials](https://github.com/LandEcosystems/SindbadTutorials.jl/tree/main?tab=readme-ov-file#sindbadtutorialsjl), and the specific challenge we will be tackling is found here: [Hybrid process learning](https://github.com/LandEcosystems/SindbadTutorials.jl/blob/main/tutorials/hybrid_process_learning/Task_Process.md#task-02-build-a-hybrid-model-for-gpp-sensitivity-to-air-temperature)

## Description

Land–atmosphere exchanges of carbon, water, and energy regulate the interactions between terrestrial ecosystems and the climate system. Accurately representing these fluxes in land surface models remains challenging due to complex ecosystem responses to environmental drivers such as temperature, radiation, and moisture availability. Traditional process-based models rely on simplified parameterizations of these relationships, which may not fully capture the variability observed across ecosystems and climatic conditions.

Hybrid modelling approaches offer a promising solution by integrating machine learning (ML) components with process-based models. In this framework, data-driven models can learn relationships from observational datasets and inform parameterizations within mechanistic modelling systems. This allows researchers to leverage the strengths of both approaches: the physical consistency of process-based models and the flexibility of machine learning.

In this challenge, participants will explore hybrid ML–process model workflows within the **SINDBAD modelling framework**. Using observational datasets, ML models will be trained to learn relationships between environmental drivers and ecosystem responses, and then integrated into the modelling framework to evaluate their impact on simulated land–atmosphere fluxes.

The tutorial demonstrates a workflow in which machine learning models are trained offline and then incorporated into the modelling system to influence process parameterizations. While the exercise focuses on learning the sensitivity of Gross Primary Production (GPP) to air temperature as an example, the workflow is general and can be applied to other ecosystem processes and environmental controls.

---

## Motivation

Understanding and predicting land–atmosphere fluxes is essential for assessing ecosystem responses to climate variability and long-term climate change. Process-based models provide a structured representation of ecosystem processes, but they often rely on empirical parameterizations that may not generalize well across sites or environmental conditions.

Machine learning approaches can leverage large observational datasets to infer complex relationships between environmental drivers and ecosystem processes. However, purely data-driven models lack the interpretability and physical constraints provided by mechanistic models.

Hybrid modelling approaches bridge this gap by combining process-based models with data-driven components. This allows ML models to learn relationships from data while maintaining the structure of existing modelling frameworks.

This challenge introduces participants to these hybrid workflows by demonstrating how an ML model trained on observational data can be integrated into the SINDBAD modelling system to improve representations of ecosystem processes affecting land–atmosphere fluxes.

---

## Challenge Objectives

The main objectives of this challenge are to:

1. Develop an understanding of hybrid ML–process model workflows within the SINDBAD modelling framework.
2. Train machine learning models using observational environmental datasets to learn relationships relevant to ecosystem processes.
3. Integrate trained ML models into the modelling framework to inform parameterizations that influence simulated land–atmosphere fluxes.
4. Evaluate the strengths, limitations, and computational trade-offs of hybrid modelling approaches.

---

## Two Valid Tasks

### Task 1: Offline Learning of Environmental Controls on Ecosystem Processes

Participants will train a machine learning model using observational datasets to learn relationships between environmental variables and ecosystem responses.  
As an example, the tutorial focuses on learning the sensitivity of **Gross Primary Production (GPP)** to **air temperature**, though the workflow is applicable to other drivers and processes.

Participants may explore different ML architectures, such as:

- Feedforward neural networks
- Recurrent neural networks
- Other machine learning approaches

The goal is to understand how ML models can learn relationships from environmental data that are typically represented through simplified parameterizations in process-based models.

---

### Task 2: Integration of ML Models into the SINDBAD Framework

Participants will integrate the trained ML model into the SINDBAD modelling framework by:

1. Adding a new model approach representing the learned process relationship.
2. Linking the trained ML model to the modelling workflow.
3. Evaluating its impact on simulated ecosystem fluxes.

Two integration approaches will be explored:

- **Lookup Table Integration**  
  Precompute ML predictions and store them as lookup tables used during simulation.

- **Direct Model Inference**  
  Call the ML model directly during model computation.

Participants will evaluate the trade-offs between computational efficiency and model flexibility when using these approaches.

---


## Getting the repo

The following command will install the tutorial files and SINDBAD itself. First of all, go to `colab` (or use `colab` extension if you are using VSCode), then go to `Tools` -> `Command Palette` -> `show terminal` to open a terminal in `colab`. Then mount your Google Drive by:
```bash
from google.colab import drive
drive.mount('/content/drive')
```
Then, run the following command in the terminal to clone the repo:

```bash
cd /content/drive/MyDrive
git clone https://github.com/WinterSchool2026/WinterSchool2026-ch17-Hybrid-land-atmosphere.git
```

or 
```bash
git clone https://github.com/LandEcosystems/SindbadTutorials.jl
```


# Tutorials
The tutorial files are stored in the `tutorials` subdirectory, and organised by topic or summer school or other event. The current tutorials are:
- hybrid_parameter_learning
- hybrid_process_learning
- insitu_inversion
- global_inversion


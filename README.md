# Advanced Machine Learning for Spatiotemporal PM₂.₅ Concentration Prediction in Urban Environments

[cite\_start]This repository contains the datasets and KNIME workflows for the research paper: **"Advanced Machine Learning for Spatiotemporal PM₂.₅ Concentration Prediction in Urban Environments: A Methodological Framework and Preliminary Evaluation"**[cite: 462].

[cite\_start]**Authors:** Saliha Çelikcan BİLGİN¹\*, Turgay Tugay BİLGİN², Hüseyin TOROS³ [cite: 463]  
[cite\_start]¹ *Department of Energy Systems Engineering, Bursa Technical University, Bursa, Türkiye* [cite: 464]  
[cite\_start]² *Department of Computer Engineering, Bursa Technical University, Bursa, Türkiye* [cite: 465, 466]  
[cite\_start]³ *Department of Meteorological Engineering, Istanbul Technical University, Istanbul, Türkiye* [cite: 467]

## Abstract

[cite\_start]Fine particulate matter (PM₂.₅) is a critical air pollutant, but its monitoring is often inadequate[cite: 470]. [cite\_start]This study proposes and evaluates a novel machine learning framework to reconstruct high-resolution PM₂.₅ concentrations at monitoring stations that lack direct measurements[cite: 471]. [cite\_start]The methodology uses optimized Gradient Boosting (GB) and Multilayer Perceptron (MLP) models, integrating pollutant data (PM₁₀, NO₂) with meteorological parameters from the ECMWF ERA5 dataset[cite: 472]. [cite\_start]The framework was developed using data from Bursa, Turkey[cite: 473]. [cite\_start]As direct validation was not possible, a preliminary evaluation was conducted via an indirect assessment strategy: using the predicted PM₂.₅ as a feature to forecast PM₁₀[cite: 473, 474]. [cite\_start]The high correlation achieved suggests the PM₂.₅ predictions are physically consistent, demonstrating the framework's potential to enhance the spatial resolution of air quality monitoring networks[cite: 475, 477].

## Repository Contents

This repository is organized as follows:

  - **/data/**: Contains the datasets used for training and evaluating the models. (Bu klasörü sizin oluşturmanız beklenmektedir).
  - **/workflows/**: Contains the KNIME workflows used to implement the methodologies described in the paper.
      - `Saliha_tez_workflow_V2.knwf`: The KNIME workflow for the **Gradient Boosting (GB)** models.
      - `Saliha_tez_workflow_MLP.knwf`: The KNIME workflow for the **Multilayer Perceptron (MLP)** models.
  - `README.md`: This file.

## Reproducibility Guide

[cite\_start]The models described in the paper were developed using the open-source KNIME Analytics Platform[cite: 526, 665, 699]. To reproduce our results, please follow these steps:

1.  **Install KNIME:** Download and install the free [KNIME Analytics Platform](https://www.knime.com/downloads) (the workflows were developed with version 4.7.x).
2.  **Clone the Repository:** Clone or download this repository to your local machine.
    ```bash
    git clone https://github.com/ttbilgin/pm2.5_prediction_paper_dataset.git
    ```
3.  **Import Workflow:** In the KNIME Analytics Platform, go to `File > Import KNIME Workflow...`.
4.  **Select Workflow:** Navigate to the `/workflows` directory in the cloned repository and select either the GB or MLP workflow (`.knwf` file).
5.  **Configure Data Paths:** Before executing the workflow, you may need to reconfigure the paths in the `Excel Reader` nodes to point to the correct location of the data files (in the `/data` directory) on your local system.

## Data Sources

The data used in this study were obtained from the following sources:

  - [cite\_start]**Air Quality Data:** Provided by the Republic of Turkey Ministry of Environment, Urbanization, and Climate Change, via the National Air Quality Monitoring Network (NAQMN)[cite: 554, 876].
  - [cite\_start]**Meteorological Data:** Sourced from the ECMWF ERA5 reanalysis dataset, accessed through the Copernicus Climate Data Store[cite: 591, 877].

-----

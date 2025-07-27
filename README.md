# Advanced Machine Learning for Spatiotemporal PM₂.₅ Concentration Prediction in Urban Environments

This repository contains the datasets and KNIME workflows for the research paper: **"Advanced Machine Learning for Spatiotemporal PM₂.₅ Concentration Prediction in Urban Environments: A Methodological Framework and Preliminary Evaluation"**.

## Repository Contents

This repository is organized as follows:

  - **/data/**: Contains the datasets used for training and evaluating the models. (Bu klasörü sizin oluşturmanız beklenmektedir).
  - **/workflows/**: Contains the KNIME workflows used to implement the methodologies described in the paper.
      - `Saliha_tez_workflow_V2.knwf`: The KNIME workflow for the **Gradient Boosting (GB)** models.
      - `Saliha_tez_workflow_MLP.knwf`: The KNIME workflow for the **Multilayer Perceptron (MLP)** models.
  - `README.md`: This file.

## Reproducibility Guide

The models described in the paper were developed using the open-source KNIME Analytics Platform. To reproduce our results, please follow these steps:

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

  - **Air Quality Data:** Provided by the Republic of Turkey Ministry of Environment, Urbanization, and Climate Change, via the National Air Quality Monitoring Network (NAQMN).
  - **Meteorological Data:** Sourced from the ECMWF ERA5 reanalysis dataset, accessed through the Copernicus Climate Data Store.

-----

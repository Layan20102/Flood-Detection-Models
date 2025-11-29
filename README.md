
This project aims to implement a robust and automated solution for **binary flood classification** (Flood vs. Non-Flood) using Synthetic Aperture Radar (SAR) imagery from the **Sentinel-1** mission, leveraging the **SEN12FLOOD** dataset.

 **Task (T):**
The task is to enable the machine learning model to detect and predict flooded areas from satellite imagery.

**Why SAR?**  
- **VV** emphasizes reflections from smooth surfaces (water, infrastructure).  
- **VH** emphasizes cross-polarized scattering from vegetation and rough terrain.  
Together, they provide complementary flood cues even under clouds or night conditions.

 **Our Approach:**

We employ a comprehensive machine learning pipeline, culminating in a **Convolutional Neural Network (CNN) classifier**, built on the following key technical steps:

1.  **Preprocessing & Feature Engineering:** We convert raw VV/VH backscatter data to the $\text{dB}$ scale, apply the **Lee speckle filter** for noise reduction, and generate a set of **six advanced SAR features** (including polarization ratios and differences) for enhanced discrimination between water and land.
2.  **Data Preparation:** The image tiles are meticulously processed, split into Train/Validation/Test sets, and carefully **balanced** to ensure the model trains effectively on both flood and non-flood scenarios.
3.  **Model Training:** A  CNN architecture is trained to accurately classify 256x256 image tiles, addressing the critical challenge of rapid and reliable flood mapping.


 **Dataset Source:**
SEN12-FLOOD — Sentinel-1 Synthetic Aperture Radar (SAR) with flood annotations in GeoJSON.  
https://www.kaggle.com/datasets/virajkadam/sen12flood


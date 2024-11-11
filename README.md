# <h1 align="center">  <b>sKwanda_V2: OpenGeoAI-Dataset | Optical Imagery Training Set</b><br></h1>

![image](https://github.com/user-attachments/assets/cfaba4c7-0114-4548-bba2-9c6328daeee2)

### Repository Overview
The sKwanda_V2: OpenGeoAI-Dataset is a high-resolution optical imagery dataset, designed to support advanced research in geospatial machine learning applications, such as semantic segmentation, land cover classification, and spatial analysis. The dataset provides geospatially referenced image patches that are derived from airborne remote sensing data. The images in this dataset are organized into three subsets—training, validation, and test—each consisting of 512 × 512 pixel patches along with their corresponding ground truth (GT) labels. This dataset is specifically curated for use in supervised learning tasks, enabling the development and evaluation of cutting-edge models in the field of geospatial AI.

The dataset comes with additional metadata, including georeferencing information, spectral bands, and spatial resolution parameters, which enable temporal, spectral, and spatial analysis. The data structure is designed to facilitate the preservation of spatial integrity and temporal consistency, ensuring that model training is aligned with real-world geographic contexts.

#### Key Features
High-Resolution Imagery: The dataset contains 512 × 512 pixel patches, suitable for fine-grained analysis of land cover and spatial features.
Geospatial Referencing: All images are georeferenced using the NAD83 / UTM Zone 18N coordinate system (EPSG: 26918). This provides the necessary geospatial accuracy for tasks requiring precise mapping and location-based analysis.
Spectral Bands: The dataset includes multiple spectral bands, providing valuable information for advanced remote sensing applications such as multispectral classification and vegetation analysis.
Ground Truth Labels: Each image patch is paired with corresponding ground truth labels that define the land cover classes (e.g., water, vegetation, urban, etc.) for supervised classification tasks.
Open Source: The dataset is made publicly available for non-commercial research purposes, contributing to the advancement of geospatial AI for social good and environmental monitoring.
##### Dataset Structure
The dataset is organized into three subsets:

Training Set: This subset includes images used to train machine learning models. It contains a diverse set of image patches with labeled ground truth.
Validation Set: This subset is used to tune model hyperparameters and validate the performance during the model development phase.
Test Set: This subset is used to evaluate the final performance of the trained model, providing an unbiased evaluation on unseen data.
Each image patch is 512 × 512 pixels, and the dataset contains several spectral bands, typically including Red, Green, Blue, and Near-Infrared (NIR) bands.
For the sKwanda-V1 dataset, clip the images to 512 × 512 patches. Please, respect the following structure:



The .aux file accompanying the dataset provides essential metadata such as the spatial reference system (SRS), geotransformation matrix, and band-specific information. This metadata ensures that spatial and spectral integrity is maintained throughout any preprocessing or transformation of the data.

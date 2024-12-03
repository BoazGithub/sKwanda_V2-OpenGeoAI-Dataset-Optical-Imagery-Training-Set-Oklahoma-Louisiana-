# <h1 align="center">  <b>sKwanda_V2: OpenGeoAI-Dataset | Optical Imagery Training Set</b><br></h1>


<h2 align="left">Data Engineering team:Authors <br></h2>

[![Author](https://img.shields.io/badge/Boaz-MWUBAHIMANA-orange.svg)](https://github.com/BoazGithub) 
[![Author](https://img.shields.io/badge/YAN-Jianguo-orange.svg)](http://www.lmars.whu.edu.cn/enjianguo-yan/) 
[![Author](https://img.shields.io/badge/Swalpa-KumarRoy-orange.svg)](https://ieeexplore.ieee.org/author/37086689617) 
[![Author](https://img.shields.io/badge/Maurice-Mugabowindekwe-orange.svg)](https://researchprofiles.ku.dk/en/persons/maurice-mugabowindekwe) 
[![Author](https://img.shields.io/badge/Xiao-Huang-orange.svg)](https://envs.emory.edu/people/bios/Huang-Xiao%20.html) 
[![Author](https://img.shields.io/badge/Elias-Nyandwi-orange.svg)](https://cst.ur.ac.rw/?Dr-Elias-Nyandwi-723) 
[![Author](https://img.shields.io/badge/Eric-Habineza-orange.svg)](https://www.linkedin.com/in/eric-habineza-79559519b/?originalSubdomain=rw) 
[![Author](https://img.shields.io/badge/Fidele-Mwizerwa-orange.svg)](https://cst.ur.ac.rw/?Mrs-Fidele-MWIZERWA) 
[![Author](https://img.shields.io/badge/Joseph-Tuyishimire-orange.svg)](https://cst.ur.ac.rw/?Mr-Joseph-Tuyishimire) 
[![Author](https://img.shields.io/badge/Dingruibo-Miao-orange.svg)](https://ieeexplore.ieee.org/author/37089315877) 

### Dataset Overview
The sKwanda_V2: OpenGeoAI-Dataset is a high-resolution optical imagery dataset, designed to support advanced research in geospatial machine learning applications, such as semantic segmentation, land cover classification, and spatial analysis. The dataset provides geospatially referenced image patches that are derived from airborne remote sensing data. The images in this dataset are organized into three subsets—training, validation, and test—each consisting of 512 × 512 pixel patches along with their corresponding ground truth (GT) labels. This dataset is specifically curated for use in supervised learning tasks, enabling the development and evaluation of cutting-edge models in the field of geospatial AI.VHF_ParaNet Model and sKwanda_V2_(Bugesera_Rwamagana{Rwanda}) and Oklahoma{USA} dataset can be downloaded [[here](https://drive.google.com/drive/folders/1h9T6w84P8b2xyD81at4JMn30VekAS53E?usp=drive_link)], [[here](https://drive.google.com/file/d/1X_Fz7LQIeix3rV3K29FBfKiU1WMdROe-/view?usp=drive_link)]  respectively.


# <h1 align="center">  <b>![image](https://github.com/user-attachments/assets/cfaba4c7-0114-4548-bba2-9c6328daeee2)</b><br></h1>
The dataset comes with additional metadata, including georeferencing information, spectral bands, and spatial resolution parameters, which enable temporal, spectral, and spatial analysis. The data structure is designed to facilitate the preservation of spatial integrity and temporal consistency, ensuring that model training is aligned with real-world geographic contexts.

#### Key Features
High-Resolution Imagery: The dataset contains 512 × 512 pixel patches, suitable for fine-grained analysis of land cover and spatial features.
Geospatial Referencing: All images are georeferenced using the NAD83 / UTM Zone 18N coordinate system (EPSG: 26918). This provides the necessary geospatial accuracy for tasks requiring precise mapping and location-based analysis.
Spectral Bands: The dataset includes multiple spectral bands, providing valuable information for advanced remote sensing applications such as multispectral classification and vegetation analysis.
Ground Truth Labels: Each image patch is paired with corresponding ground truth labels that define the land cover classes (e.g., water, vegetation, urban, etc.) for supervised classification tasks.
Open Source: The dataset is made publicly available for non-commercial research purposes, contributing to the advancement of geospatial AI for social good and environmental monitoring.
##### 👉 Dataset Structure
The dataset is organized into three subsets:

Training Set: This subset includes images used to train machine learning models. It contains a diverse set of image patches with labeled ground truth.
Validation Set: This subset is used to tune model hyperparameters and validate the performance during the model development phase.
Test Set: This subset is used to evaluate the final performance of the trained model, providing an unbiased evaluation on unseen data.
Each image patch is 512 × 512 pixels, and the dataset contains several spectral bands, typically including Red, Green, Blue, and Near-Infrared (NIR) bands.
For the sKwanda-V1 dataset, clip the images to 512 × 512 patches. Please, respect the following structure:
# <h1 align="center">  <b>![image](https://github.com/user-attachments/assets/0a1974ca-ed0d-4bfb-b622-2db015faccfa)</b><br></h1>

The .aux file accompanying the dataset provides essential metadata such as the spatial reference system (SRS), geotransformation matrix, and band-specific information. This metadata ensures that spatial and spectral integrity is maintained throughout any preprocessing or transformation of the data.

## 💬 Geospatial Metadata
The .aux file contains detailed information on the coordinate system, geotransformation, and image bands. The key elements include:

Coordinate System (PROJCS): The dataset is georeferenced using NAD83 / UTM Zone 18N (EPSG: 26918), ensuring compatibility with geospatial software and accurate mapping in the Transverse Mercator projection.
GeoTransform: Defines how pixel coordinates are mapped to real-world coordinates, maintaining the spatial integrity when tiles are extracted from large images.
Spectral Bands: Each image contains four bands, including Red, Green, Blue, and Near-Infrared (NIR). The metadata ensures that each band’s NoData values and source indexes are recorded correctly.

🔭 Example of GeoTIFF Metadata
<SRS dataAxisToSRSAxisMapping="1,2">PROJCS["NAD83 / UTM zone 18N", ...]</SRS>
<GeoTransform> 3.2114759999999998e+05, 5.9999999999999998e-01, 0.0000000000000000e+00, 4.3120584000000004e+06, 0.0000000000000000e+00, -5.9999999999999998e-01</GeoTransform>
<PAMRasterBand band="1">
    <NoDataValue>2.55000000000000E+02</NoDataValue>
</PAMRasterBand>
## Dataset acquisition locations
sKwanda_V2 dataset are acquired over Nyagatare, and Rwamagana{top-left-corner at red A}, and migration was made over the National Agriculture imagery program{top-left-corner at red B} and CheasaBay land cover products

![3MVH_ParaNetl_2024](https://github.com/user-attachments/assets/6dbddb6a-6101-4944-84c6-b59101ff4345)

### Usage
##### Installation
To begin using the dataset, you can download it via Google Drive (link provided in the repository).

###### Preprocessing and Patch Extraction
1. Patch Extraction: The dataset’s large airborne images have been split into smaller 512 × 512 pixel tiles. This process ensures that the data is manageable and ready for training deep learning models, such as Convolutional Neural Networks (CNNs) and Transformer-based models (ViT).
2. Geospatial Integrity: When splitting the images, it is crucial to retain the GeoTIFF metadata, including GeoTransform and projection system information, ensuring that each extracted tile maintains its spatial reference.
##### Training Models
The dataset is ideal for supervised learning tasks, particularly in the context of land cover classification and semantic segmentation. Researchers can train deep learning models using this dataset, ensuring that the model learns spatial patterns and global features with geospatial awareness. Models such as CNNs, Fully Convolutional Networks (FCNs), and Vision Transformers (ViT) are particularly well-suited for this task.

### Some Results made on sKwanda_V2 Dataset are illustrates below:

#### Quantitative Results:

![image](https://github.com/user-attachments/assets/23bb198f-e35c-4de1-983c-7a36b8ccbd41)


#### Qualitative Results:

![image](https://github.com/user-attachments/assets/def8aca1-0957-4249-a1ed-16bc3dac649f)


#### State_of_the_Art_Dataset&Methods (SoA): 

1. ![image](https://github.com/user-attachments/assets/35db271b-8d92-480d-9f36-24ea08ad41ec)



2. ![VHF_Para_Dataset_correlation_heatmap5_page-0001](https://github.com/user-attachments/assets/5d3040cb-7e4c-4cde-8b5d-b7b244091aa6)

###### Evaluation
Once the model is trained, the test set can be used to evaluate its performance in an unbiased manner. Metrics such as accuracy, IoU (Intersection over Union), and F1-score can be used to assess model efficacy.

![nyagate_multimodel_performance_metrics_histograms_with_lines_and_unique_colormap_page-0001](https://github.com/user-attachments/assets/9c1c3e94-46a5-4a65-b35a-229156094ea0)

### License and Citation
License: The dataset is released under a non-commercial license for academic and research purposes only. For commercial use, please contact the authors.


### :truck: Datasets and model <a name="dataset"></a>

The full train and test code will be released soon. You can download our novel public sKwanda_V2 dataset through the following link:

- [x] [sKwabda-V2][Google drive](https://drive.google.com/drive/folders/1D7HpbORsItR4IQtyxlpAGm_KFXNlIc1E?usp=drive_link).

- [x] [C2FNet: Weak supervision learning strategy][Google drive](https://drive.google.com/drive/u/2/folders/1aBNy1f0MCCerNpvHZgLrW3yE059xalg8).

###### Citation: If you use this dataset in your research, please cite the following:
```bibtex
📃 makefile
Copy code
@article{Mwubahimana2024sKwanda,
title={sKwanda V2: OpenGeoAI Dataset for Optical Imagery Training},
author={Boaz Mwubahimana},
year={2024},
journal={IEEE Journal of Geospatial AI},
volume={XX},
number={YY},
pages={ZZ-ZZ},
```

#### Acknowledgments
This dataset was created with the support of the Planetary Science Group at the State Key Laboratory of Information Engineering in Surveying, Mapping, and Remote Sensing of Wuhan University. 

Special thanks to the :
1. Google Earth
2. L2HNet,
3. Sentinel Hub, and
4.  ESRI for their tools and resources, which were instrumental in dataset creation.

#### Contact Information
For any inquiries or collaboration opportunities, please contact Boaz Mwubahimana at aiboaz1896@gmail.com.

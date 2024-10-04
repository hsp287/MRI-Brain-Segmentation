## Description:
This repository is for the EL-GY 6123 Final Project from Spring 2023. 
Three different U-net architectures (2D using FLAIR, 2D using FLAIR + T1 weighted + T2 weighted, and 3D using FLAIR) are tested and compared.
We utilize the MICCAI 2016 dataset on brain lesion segmentation available at: https://shanoir.irisa.fr/shanoir-ng/welcome
This dataset contains both raw and pre-processed MRI scans.
We also utilize the tool volBrain for masking out the skull region from raw MRI: https://volbrain.net/services/volBrain

There are 4 notebook files:
1) MRI_preprocessing: contains some data pre-processing steps for raw MRI scans (de-noising, skull-stripping)
2) Unet_Segmentation_2D: contains the data loading and training of the 2D Unet model.
3) Unet_Segmentation_2D_multi: contains the data loading and training of the 2D multi-MRI Unet model.
4) Unet_Segmentation_3D: contains the data loading and training of the 3D Unet model.

Basic data normalization and cropping are employed to keep inputs.
For the 2D data inputs, random flips and rotations are applied. For the 3D data inputs, only random flips are applied.

## Model architectures:

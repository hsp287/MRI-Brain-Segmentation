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
(a) 2D Unet (Flair only)  (b) 2D Unet (Multiple MRI types)  (c) 3D Unet (FLAIR only)
<img src="Images/unet_all3.png" width="50%" margin-left="auto" margin-right="auto">

## Results:

|Loss and DICE curves|Segmentation Results|
|---------------|-----------|
|<img src="Images/loss_dice.png" width="100%">|<img src="Images/2d_results.png" width="100%"><img src="Images/3d_results.png" width="67%">|


## GIF of 3D segmentation results:
Yellow: Overlap
Green: Error
<img src="Images/3D_segmentation.gif" width="100%" margin-left="auto" margin-right="auto">

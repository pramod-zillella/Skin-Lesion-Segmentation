# Skin-Lesion-Segmentation

## Background
Automatic skin lesion segmentation on dermoscopic images is an essential step in computer-aided diagnosis of melanoma. However, this task is challenging due to significant
variations of lesion appearances across different patients.Clinical treatment of skin lesion is primarily dependent on timely detection and delimitation
of lesion boundaries for accurate cancerous region localization.

## Introduction
We present a fully automated architecture for accurately detecting border and segmenting the skin lesion by coupling a deep learning model with the Berkeley wavelet transform map derived from the specific kernel filters. Our proposed method effectively combines the Berkeley wavelet transform feature maps into a deep learning U-Net model trained in an end-to-end manner, which results in the reduction of the number of trainable parameters. The model was trained on [HAM10000](https://www.nature.com/articles/s41591-020-0942-0) and [ISIC training data](https://ieeexplore.ieee.org/document/8363547) and test on [PH2](https://ieeexplore.ieee.org/document/6610779) and ISIC Validation data.

## Preprocessing
The dermoscopic images are pre-processed using [Berkeley wavelet transform](https://direct.mit.edu/neco/article/20/6/1537/7305/The-Berkeley-Wavelet-Transform-A-Biologically) by applying the 8 mother wavelets on the dermoscopic images to form the berkeley wavelet decomposed image. 
<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118661413-b9210780-b80c-11eb-8896-c551c1877c8c.png" width="700">             
</p>


## Network architecture
![Network](https://user-images.githubusercontent.com/63542593/118666798-13bc6280-b811-11eb-93b7-697e7237b031.png)

## Quantitative Segmentation Results

<p align="center">
  
| Dataset  | Sensitivity | Accuracy | Dice | Jaccard Similarity | 
| :---: | :---: | :---: | :---: | :---: |
|    [PH2](https://ieeexplore.ieee.org/document/6610779)    | 96.44  | 96.89  | 96.42  | 93.11  |
| [ISIC 2017](https://challenge.isic-archive.com/landing/2017) | 92.46  | 95.64  | 88.20  | 78.89  |

</p>

## Segmentation Visualization Results

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118668023-1ec3c280-b812-11eb-831a-03903d6ef51e.png" width="900">             
</p>

&nbsp; Dermoscopic Image &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  BWT Feature Map &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Ground Truth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Predicted Mask &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  lesion boundary

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118668035-208d8600-b812-11eb-8725-2d96d71d727b.png" width="900">             
</p>

&nbsp; Dermoscopic Image &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  BWT Feature Map &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Ground Truth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Predicted Mask &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  lesion boundary

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118668047-24210d00-b812-11eb-83d0-967f9f1e5e7f.png" width="900">             
</p>

&nbsp; Dermoscopic Image &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  BWT Feature Map &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Ground Truth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Predicted Mask &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  lesion boundary

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118668646-b0cbcb00-b812-11eb-82f9-5961a7cb45cd.png" width="900">             
</p>


&nbsp; Dermoscopic Image &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  BWT Feature Map &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Ground Truth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Predicted Mask &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  lesion boundary

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118668649-b2958e80-b812-11eb-8d54-5c52eb34ee68.png" width="900">             
</p>


&nbsp; Dermoscopic Image &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  BWT Feature Map &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Ground Truth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Predicted Mask &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  lesion boundary

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118668661-b45f5200-b812-11eb-8c17-90c878a57924.png" width="900">             
</p>


&nbsp; Dermoscopic Image &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  BWT Feature Map &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Ground Truth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Predicted Mask &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  lesion boundary

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118668808-d0fb8a00-b812-11eb-9011-7f83e5d6d7db.png" width="900">             
</p>


&nbsp; Dermoscopic Image &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  BWT Feature Map &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Ground Truth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Predicted Mask &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  lesion boundary

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118668813-d22cb700-b812-11eb-9206-75ca129394fb.png" width="900">             
</p>


&nbsp; Dermoscopic Image &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  BWT Feature Map &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Ground Truth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Predicted Mask &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  lesion boundary

<p align="center">
<img src="https://user-images.githubusercontent.com/63542593/118668845-da84f200-b812-11eb-83be-00eea0286c92.png" width="900">             
</p>

&nbsp; Dermoscopic Image &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  BWT Feature Map &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Ground Truth &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   Predicted Mask &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  lesion boundary

# Conclusion
The Use of inexpensive Berkeley wavelet transform helps in enhancing the minutiae details of the skin lesion that helped in achieving an improved algorithm for accurate and automatic skin lesion segmentation. Furthermore, the model is computationally efficient with 1.2 Million parameters, and only takes 0.0625 seconds to segment the lesion from the dermoscopic image, making it extremely useful in clinical settings.

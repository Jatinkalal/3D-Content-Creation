# 3D-Content-Creation
This repository focuses on generating diverse 3D point clouds from single-view 2D RGB images. The project utilizes a pretrained architecture known as 3D Attribute Flow to achieve this.
## Introduction 
In this approach, we perform interpolation in the latent space between a source and a target, enabling the generation of a wide range of 3D point clouds. This method leverages the capabilities of the pretrained model to produce diverse and visually appealing 3D content from 2D inputs.

## System Architecture
![Archi]()
In this apporach we take two images, one as source and one as target, we perform feature extraction by leveraging pretrained resnet-18 architecture, then in the obtained feature vector we perform interpolation (cosine as well as linear) and pass this feature vector to the pretrained 3D Attribute Flow which reconstructs 3D point clouds, thereby generating diverse 3D point clouds from single view 2D RGB images.

## Results from Inter-class interpolation.
![inter]()
Source is car and target is plane, dataset used was shapenet rendered images.


## Results from Intra-class interpolation.
![intra]()
Source is car type1 and target is cartype2, dataset used was shapenet rendered images.






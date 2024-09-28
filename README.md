# 3D-Content-Creation
This repository focuses on generating diverse 3D point clouds from single-view 2D RGB images. The project utilizes a pretrained architecture known as ![3DAttributeFlow](https://github.com/junshengzhou/3DAttriFlow) to achieve this.
## Introduction 
In this approach, we perform interpolation in the latent space between a source and a target, enabling the generation of a wide range of 3D point clouds. This method leverages the capabilities of the pretrained model to produce diverse and visually appealing 3D content from 2D inputs.

## System Architecture
![Archi](https://github.com/Jatinkalal/3D-Content-Creation/blob/main/Images/%E2%80%8Efinal_block_diagram.%E2%80%8E001.jpeg)
In this apporach we take two images, one as source and one as target, we perform feature extraction by leveraging pretrained resnet-18 architecture, then in the obtained feature vector we perform interpolation (cosine as well as linear) and pass this feature vector to the pretrained 3D Attribute Flow which reconstructs 3D point clouds, thereby generating diverse 3D point clouds from single view 2D RGB images.

## Results from Inter-class interpolation.
![inter](https://github.com/Jatinkalal/3D-Content-Creation/blob/main/Images/Plane2car.002.jpeg)
Source is car and target is plane, dataset used was shapenet rendered images.

## Results from Intra-class interpolation.
![intra](https://github.com/Jatinkalal/3D-Content-Creation/blob/main/Images/1.gif)
Source is car type1 and target is cartype2, dataset used was shapenet rendered images.

## Results from varying parameters of latent vector
![len](https://github.com/Jatinkalal/3D-Content-Creation/blob/main/Images/PlaneLen.png)
Here we vary 5th dimension of the latent vector to observe change in the length of the wings, Red one represents no varied parameter hence no change in the length of the wings, while blue one is with  5th parameter varied to observe change in the length of its wings.











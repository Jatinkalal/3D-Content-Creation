# 3D Point Cloud Content Creation
This repository focuses on generating diverse 3D point clouds from single-view 2D RGB images. The project utilizes a pretrained architecture known as [3DAttributeFlow](https://github.com/junshengzhou/3DAttriFlow) to achieve this.
## Introduction 
In this approach, we perform interpolation in the latent space between a source and a target, enabling the generation of a wide range of 3D point clouds. This method leverages the capabilities of the pretrained model to produce diverse and visually appealing 3D content from 2D inputs.

## System Architecture
![Archi](https://github.com/Jatinkalal/3D-Content-Creation/blob/main/Images/%E2%80%8Efinal_block_diagram.%E2%80%8E001.jpeg)
In this apporach we take two images, one as source and one as target, we perform feature extraction by leveraging pretrained resnet-18 architecture, then in the obtained feature vector we perform interpolation (cosine as well as linear) and pass this feature vector to the pretrained 3D Attribute Flow which reconstructs 3D point clouds, thereby generating diverse 3D point clouds from single view 2D RGB images.

## Results from Inter-class interpolation.
![inter](https://github.com/Jatinkalal/3D-Content-Creation/blob/main/Images/Plane2car.002.jpeg)
Source is plane and target is car and intermediate point clouds represent output from that interpolation step, dataset used was shapenet rendered images.

## Results from Intra-class interpolation.
![intra](https://github.com/Jatinkalal/3D-Content-Creation/blob/main/Images/car2car.001.jpeg)
Source is car type1 and target is car type2 and intermediate point clouds represent output from that interpolation step,  dataset used was shapenet rendered images.

## Results from combining geometric style and semantic attributes.
![combine](https://github.com/Jatinkalal/3D-Content-Creation/blob/main/Images/chair_combined2.001.jpeg)
Here we combine the geomtric style from chair 1 along with semantic attributes of chair 2 to generate a 3D point cloud with overall geometry as chair 1 and having semantics of chair 2.



## Results from varying parameters of latent vector
![len](https://github.com/Jatinkalal/3D-Content-Creation/blob/main/Images/PlaneLen.png)
Here we vary the 5th dimension of the latent vector to observe changes in the length of the wings. **(Red one)** represents no varied parameter, hence no change in the length of the wings, while **(Blue one)** is with the 5th parameter varied to observe the change in the length of its wings.











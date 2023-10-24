# Lane Detection Using Deep Learing
The aim is to build a machine learning model to distinguish the drivable lane road from the obstacles and background in the active road image.
###### (This is the link for Pretrained Model https://drive.google.com/file/d/1-LCbdwhTEUE2J2jj31Q-n83xA__QuvVE/view?usp=share_link<br>
###### and dataset is https://drive.google.com/file/d/1MJy2X3qSKVx125iG23Zd0vli0ewdGP-F/view?usp=share_link)
### Dataset
BDD100K dataset is used as reference (BDD100K -https://bdd-data.berkeley.edu/). The label images of BDD100K dataset were modified  in
such a way that, there are only three colors (pink,blue and black) in the label representing lane area,obstacles and background respectively.
### Library Used
TensorFlow<br>
PyTorch<br>
Matplotlib<br>
Numpy<br>
Pandas<br>
## Unet Model Architecture
The architecture consists of two main parts: the contracting path and the expanding path.<br>
The contracting path is a series of convolutional and pooling layers that gradually reduce the spatial resolution of the input image while increasing the number of feature channels.<br>
Once the contracting path has extracted the features, the expanding path uses a series of upsampling and convolutional layers to restore the spatial resolution of the image while decreasing the number of feature channels.<br>
In addition to the contracting and expanding paths, UNet also includes skip connections that directly connect the corresponding feature maps from the contracting and expanding paths. These skip connections allow the network to preserve spatial information from the contracting path, which can be important for accurate segmentation.
![image](https://github.com/Sagar2inf/Lane_detection_model/assets/108271916/6b963587-727a-445e-a477-88588218c78a)

# Raspberry Pi 4 DNN image
![output image]( https://qengineering.eu/images/Water6.webp )<br/>
## A Raspberry Pi 4 64-OS image with deep learning examples
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
Regularly, we get the question if we have an image of our Raspberry Pi with some frameworks and [our deep-learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html). We are happy to comply with this request.

------------

## Installation.

- Get a 16 GB SD-card which will hold the image. 
- Download the image (4 GByte!) from our [Mega](https://mega.nz/file/x4gSVYIR#fgPrbITp8K2wCtH8SHdzLA_fRyI_PvmyT9ieSy5qXoc) site.
- Unzip the 7z file.
- Flash the image on the SD-card with the [Imager](https://www.raspberrypi.org/software/) or [balenaEtcher](https://www.balena.io/etcher/).
- Insert the SD-card in your Raspberry Pi 4 and enjoy.
- No WiFi installed. Password: ***3.14***

------------

## Tips.

* You can [overclock the Raspberry Pi](https://qengineering.eu/overclocking-the-raspberry-pi-4.html) if your SD-card is not too worn out. 1800 MHz is no problem. Most deep learning examples even work at 1950 MHz.<br/>
* If you are in need of extra space, you can delete the opencv and the opencv_contrib folder from the SD-card. There are no longer needed since all libraries are placed in the /usr/local directory.
* Use a tool like [GParted](https://gparted.org/) `sudo apt-get install gparted` to expand the 16 GB image to larger SD-cards.

------------

## Contents.

- [OpenCV](https://github.com/Qengineering/OpenCV-Livecam-Raspberry-Pi)
- [Classification](https://github.com/Qengineering/TensorFlow_Lite_Classification_RPi_64-bits)
- [SSD](https://github.com/Qengineering/TensorFlow_Lite_SSD_RPi_64-bits)
- [Segmentation](https://github.com/Qengineering/TensorFlow_Lite_Segmentation_RPi_64-bit)
- [Segmentation Yolact](https://github.com/Qengineering/Yolact-ncnn-Raspberry-Pi-4)
- [Pose](https://github.com/Qengineering/TensorFlow_Lite_Pose_RPi_64-bits)
- [Face detection](https://github.com/Qengineering/Face-detection-Raspberry-Pi-32-64-bits)
- [Face mask detection Paddle](https://github.com/Qengineering/Face-Mask-Detection-Raspberry-Pi-64-bits)
- [Face mask detection TensorFlow](https://github.com/Qengineering/TensorFlow_Lite_Face_Mask_RPi_64-bits)
- [Face recognition](https://github.com/Qengineering/Face-Recognition-Raspberry-Pi-64-bits)

------------

## Pre-installed frameworks.

- [OpenCV](https://qengineering.eu/deep-learning-with-opencv-on-raspberry-pi-4.html) 4.5.1
- [ncnn](https://qengineering.eu/install-ncnn-on-raspberry-pi-4.html) 20210124
- [MNN](https://qengineering.eu/install-mnn-on-raspberry-pi-4.html) 1.1.0
- [Paddle-Lite](https://qengineering.eu/install-paddle-lite-on-raspberry-pi-4.html) 2.7
- [TensorFlow-Lite](https://qengineering.eu/install-tensorflow-2-lite-on-raspberry-64-os.html) 2.4.1
- [TensorFLow](https://qengineering.eu/install-tensorflow-2.4.0-on-raspberry-64-os.html) 2.4.1
- [TensorFlow Addons](https://qengineering.eu/install-tensorflow-2.4.0-on-raspberry-64-os.html) 0.13.0-dev
- [Pytorch](https://qengineering.eu/install-pytorch-on-raspberry-pi-4.html) 1.8.0
- [TorchVision](https://qengineering.eu/install-pytorch-on-raspberry-pi-4.html) 0.9.0

![output image](https://qengineering.eu/images/SD_frameworks.png)<br/>

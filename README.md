# Raspberry Pi 4 DNN image
![output image]( https://qengineering.eu/images/Water6.webp )<br/>
## A Raspberry Pi 4 64-OS image with deep learning examples
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
We are regularly asked if we don't have an image of our Raspberry Pi with the [deep learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html) on it. We are happy to comply with this request.

------------

## Installation.

- Get a 16 GB SD-card which will hold the image. 
- Download the image (4 GByte!) [Mega link](https://mega.nz/file/Yg5V1aRZ#Si0Uv2Aof4EPT4WMMHIGUhEDZrqy7sX8DTseLGv7Sg8)
- Unzip the 7z file
- Flash the image on the SD-card with the [Imager](https://www.raspberrypi.org/software/) or [balenaEtcher](https://www.balena.io/etcher/)
- Insert the SD-card in your Raspberry Pi 4 and enjoy.
- No WiFi installed. Password: ***3.14***

------------

## Tips.

* You can [overclock the Raspberry Pi](https://qengineering.eu/overclocking-the-raspberry-pi-4.html) if your SD-card is not to weared out. 1800 MHz is no problem. Most deep learning examples even work at 1950 MHz.<br/>
* If you are in need of extra space, you can delete the opencv and the opencv_contrib folder from the SD-card. There are no longer needed since all libraries are placed in the /usr/local directory.

------------

## Contents.

- [Classification](https://github.com/Qengineering/TensorFlow_Lite_Classification_RPi_64-bits)
- [SSD](https://github.com/Qengineering/TensorFlow_Lite_SSD_RPi_64-bits)
- [Segmentation](https://github.com/Qengineering/TensorFlow_Lite_Segmentation_RPi_64-bit)
- [Pose](https://github.com/Qengineering/TensorFlow_Lite_Pose_RPi_64-bits)
- [Face detection](https://github.com/Qengineering/Face-detection-Raspberry-Pi-32-64-bits)
- [Face mask detection Paddle](https://github.com/Qengineering/Face-Mask-Detection-Raspberry-Pi-64-bits)
- [Face mask detection TensorFlow](https://github.com/Qengineering/TensorFlow_Lite_Face_Mask_RPi_64-bits)
- [Face recognition](https://github.com/Qengineering/Face-Recognition-Raspberry-Pi-64-bits)


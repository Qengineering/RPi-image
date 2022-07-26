# Raspberry Pi 4 DNN image
![output image]( https://qengineering.eu/images/Water6.webp )<br/>
## A Raspberry Pi 4 64-OS image with deep learning examples
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
### February 19, 2022
Use [PiShrink](https://github.com/Drewsif/PiShrink) to support of different SD sizes. Reduced the file from 4.83 to 2.68 GByte <br/>

### January 24, 2022
Updated and upgraded to the latest Debian 10 **Buster** release.<br/>

Regularly, we get the question if we have an image of our Raspberry Pi with some frameworks and [our deep-learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html). We are happy to comply with this request.

------------

## Installation.

- Get a 16 GB SD-card which will hold the image. 
- Download the image RPi_64OS_DNN.xz (2.68 GByte!) from our [Gdrive](https://drive.google.com/file/d/1s8ulI44O96qmVPmWyz8yw3lzamh-32gN/view?usp=sharing) or mirror [Gdrive](https://drive.google.com/file/d/1Ae2mj06bVnej0igNd8N0pmsKZSbXgDZH/view?usp=sharing) or [Mirror](https://ln5.sync.com/dl/8dc06d210/x5e7vpik-3sr4jjub-z2vckx8a-p732jfdj) site.
- Flash the image on the SD-card with the [Imager](https://www.raspberrypi.org/software/) or [balenaEtcher](https://www.balena.io/etcher/).
- Insert the SD-card in your Raspberry Pi 4.
- Wait a few minutes, while the image will expand to the full size of your SD card.
- No WiFi installed. Password: ***3.14***
- RPi_64OS_DNN.xz md5sum: c4c7b4e6571f690d4f6c156ca5df9444

------------

## Tips.

* You can [overclock the Raspberry Pi](https://qengineering.eu/overclocking-the-raspberry-pi-4.html) if your SD-card is not too worn out. 1800 MHz is no problem. Most deep learning examples even work at 1950 MHz.<br/>
* If you are in need of extra space, you can delete the opencv and the opencv_contrib folder from the SD-card. There are no longer needed since all libraries are placed in the /usr/local directory.

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

![output image](https://qengineering.eu/images/SD_frameworks.png)

------------

## WiFi.

Since everyone has a unique password on their WiFi connection, we have not activated the WiFi.<br/>
To enable the wireless LAN follow the next steps:<br/>

1) Left click on the Ethernet symbol.<br/><br/>
![image](https://user-images.githubusercontent.com/44409029/124445112-8eb8e880-dd7f-11eb-80e6-121dc31fd0b8.png)<br/><br/>
2) Click "Turn on wireless LAN", and wait a few seconds. Your RPi will scan for available networks.<br/><br/>
![image](https://user-images.githubusercontent.com/44409029/124445876-39310b80-dd80-11eb-97ff-1ef8f8c477e8.png)<br/><br/>
3) Left click again on the Ethernet symbol and choose your network.<br/><br/>
![image](https://user-images.githubusercontent.com/44409029/124446101-64b3f600-dd80-11eb-9385-eee4fd730268.png)<br/><br/>
4) Give your key, and wait a couple of seconds to let the RPi establish the connection.<br/><br/>
![image](https://user-images.githubusercontent.com/44409029/124447227-74800a00-dd81-11eb-9c47-bee6b2b84bc1.png)<br/><br/>
5) Success! <br/><br/>
![image](https://user-images.githubusercontent.com/44409029/124446775-063b4780-dd81-11eb-9fd8-2d597ad31cee.png)

------------

## OpenCV + TensorFlow.

Importing both TensorFlow and OpenCV in Python can throw the error: _cannot allocate memory in static TLS block_.<br/>
This behaviour only occurs on an aarch64 system and is caused by the OpenMP memory requirements not being met.<br/>
For more information, see GitHub ticket [#14884](https://github.com/opencv/opencv/issues/14884).<br/>

![output image](https://qengineering.eu/images/SwapImportOpenCVRPi.png)

There are a few solutions. The easiest is to import OpenCV at the beginning, as shown above.<br/>
The other is disabling OpenMP by setting the -DBUILD_OPENMP and -DWITH_OPENMP flags OFF.<br/>
Where possible, OpenCV will now use the default pthread or the TBB engine for parallelization.<br/>
We don't recommend it. Not all OpenCV algorithms automatically switch to pthread.<br/>
Our advice is to import OpenCV into Python first before anything else.<br/>

------------

[![paypal](https://qengineering.eu/images/TipJarSmall4.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CPZTM5BB3FCYL) 


# YoloV4-with-Nvidia-Tesla-T4-on-Ubuntu-18.04-server
Those steps for setup a YoloV4 with 2 Nvidia graphic cards (NVIDIA Tesla T4) on Ubuntu 18.04 server.

Cuda setup were pain in the neck, more like a shitshow task to do. 
We were 3 “IT professional” trying to make Yolov4 works on ubuntu server for one week (full time) and finally it has worked.
I want to share what we did to make it easier for you :), Because Nvidia did not.

#### I will gather the references of the steps in the end, and thanks for those out there sharing their knowledge and this what helped us make this machine works.

## Install Ubuntu:
- Clean up your old machine from the dust ^^.
- install ubuntu 18.04 Server with the proper confugration for the server (access to ports and on...)

## install the necessary drivers:
- always update your system befor any install:
  - `$ sudo apt update`
  - `$ sudo apt upgrade`
  
- If you want to find out info about your GPU card :
  - ` $ sudo lshw -C display `
  
- Find the proper driver for the graphic cards and other PCI Devices (in our case we had just the graphic cards):
  - ` apt search nvidia-driver `
  
- You will get a list of different drivers (Choose the recommended one or not).
  - If you don't want to choose the driver (wants the recommended ) : `$ sudo ubuntu-drivers autoinstall `
  - In case you want some specific driver like the driver for nvidia and version 460 (on the list): `$ sudo apt install nvidia-driver-460`
  
- Reboot your system, you have to.
  - ` $ sudo reboot `
.
.
.

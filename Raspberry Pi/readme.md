# CZ3004 MDP RPi
Nanyang Technological University School of Computer Science and Engineering

Academic Year 2020-2021 Semester 2

source code for CZ3004 Multi-Disciplinary Project - Raspberry Pi

Group: 15

## RPi (Communications)
### Set Up on Raspberry Pi

- Working on Raspbian Jessie (2016-02-26), with Python version 3.4.2. Ensure that OpenCV 3.3.0 is installed as well.
- Ensure that `picamera` version is at 1.1.0 (`sudo pip3 install "picamera[array]" == 1.1.0`)  
- Ensure that `at-spi2-core` is installed (`sudo apt-get install at-spi2-core`)  
 
### To run RPi
- Change directory: `cd rpi`  
- Main Program: `sudo python3 -m main`
  - optional argument:  `-i <name>`
  - where `name` is your name if your computer is being used as the image processing server
  - default: no image recognition

Begins a multithread session that will establish communications with N7 Tablet, Arduino and PC.

### Connecting a new bluetooth device

- `sudo hciconfig hci0 piscan`
- `hcitool scan`

### Miscellaneous
- to shut down RPi: [`sudo shutdown -h now`](https://raspberrypi.stackexchange.com/a/383)
- [additional reference for installing OpenCV](https://www.pyimagesearch.com/2018/09/26/install-opencv-4-on-your-raspberry-pi/)
- bluetooth [`sudo systemctl enable rfcomm`]
- for rpi to take a photo: [`raspistill -w 1920 -h 1080 -q 100 -o cam2.jpg`]

x11 forward use xauth list and xauth add in sudo su  

[reference code](https://github.com/Elelightning/MDP_Integrated)

## Image Processing Server
For details, please refer to image processing server's README (https://github.com/michaelTJC96/MDP_Group15/blob/main/Raspberry%20Pi/image_processing_server/README.md).

## directory structure
- image_processing_server: code to be ran on our computer for image recognition
- mock_pc: a mock-up of algorithm (movement via commands that are entered manually)
- rpi: code to be ran on RPi

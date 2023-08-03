# ALPR_YOLOv8 : Automatic License Plate Recognition (ALPR) using YOLOv8

This project aims to provide an Automatic License Plate Recognition (ALPR) system using the YOLOv8 model. With this system, you can detect license plates in images and videos.

## Getting Started

Follow these steps to get started with the project:

### Clone the Repository

Use the following git command to clone the repository to your local machine:

`git clone https://github.com/Elmehdidebug/ALPR_YOLOv8.git`


### Download Sample Video

Download a sample video from Google Drive using the following link:

[Download Sample Video](https://drive.google.com/uc?id=1P-oVR0J35Dw40lzw47sE19oADSW-tyb1&confirm=t)

### License Plate Detection

To perform license plate detection, execute the following command:

`yolo task=detect mode=predict model={HOME}/runs/detect/train/weights/best.pt conf=0.25 source="demo.mp4" save=True`

After running the command, you will see the path to the results in the last line of the execution, for example:

`Results saved to runs/detect/predict`



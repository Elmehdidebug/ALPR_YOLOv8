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

or use 

`gdown "https://drive.google.com/uc?id=1P-oVR0J35Dw40lzw47sE19oADSW-tyb1&confirm=t"`

### License Plate Detection

To perform license plate detection, execute the following command:

`yolo task=detect mode=predict model={HOME}/runs/detect/train/weights/best.pt conf=0.25 source="demo.mp4" save=True`

After running the command, you will see the path to the results in the last line of the execution, for example:

`Results saved to runs/detect/predict`


## Fine-tuning the Model

If you wish to fine-tune the ALPR YOLOv8 model on your own dataset, follow these steps:

1. Access the dataset's Universe home page: [License Plates Dataset](https://universe.roboflow.com/samrat-sahoo/license-plates-f8vsn/dataset/5).

2. On the dataset page, click the "Download this Dataset" button and choose "YOLO v8 text format." You will be prompted with a code snippet similar to the one below, which includes your API key:

   ```python
   # Example code for downloading dataset
   api_key = "YOUR_API_KEY"
   from roboflow import Roboflow
   rf = Roboflow(api_key=api_key)
   project = rf.workspace("samrat-sahoo").project("license-plates-f8vsn")
   dataset = project.version(5).download("yolov8")

3. Copy the code snippet and paste it into the ALPR_yolov8.ipynb notebook. Execute the code to download the dataset.

4. With the dataset at your disposal, you can fine-tune the YOLOv8 model using your own parameters and training settings. The notebook provides a step-by-step guide and explanatory comments to help you through the process.


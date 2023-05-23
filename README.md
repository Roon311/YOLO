# YOLO Object Detection

This repository contains code for performing object detection using YOLO (You Only Look Once) algorithm. The project utilizes the Darknet framework and pre-trained weights on the COCO dataset.

## Requirements

Make sure you have the following dependencies installed:

- OpenCV
- CUDA (if using GPU)
- cuDNN (if using GPU)

## Setup

1. Clone the YOLO repository:

   ```bash
   git clone https://github.com/Roon311/YOLO.git
   ```

2. Navigate to the project directory:

   ```bash
   cd YOLO
   ```

3. Build the Darknet framework:

   ```bash
   make
   ```

4. Download the pre-trained weights for YOLO:

   ```bash
   wget https://pjreddie.com/media/files/yolov3.weights
   ```

## Usage

1. Run object detection using YOLO:

   ```bash
   ./darknet detect cfg/yolov3.cfg yolov3.weights data/person.jpg
   ```

   This command will perform object detection on the provided image `data/person.jpg` using the YOLOv3 model and display the detected objects.

2. Modify the Darknet configuration file `cfg/yolov3.cfg` to customize the model architecture, such as adjusting the confidence threshold or selecting different anchor sizes.

## Evaluation

To evaluate the YOLO model on the COCO dataset or other custom datasets, follow these steps:

1. Download the COCO dataset or prepare your custom dataset.

2. Modify the Darknet configuration file `cfg/yolov3.cfg` and update the `cfg/coco.data` file to specify the dataset paths and other relevant settings.

3. Run evaluation using Darknet:

   ```bash
   ./darknet detector test cfg/coco.data cfg/yolov3.cfg yolov3.weights
   ```

   This command will perform evaluation on the specified dataset using the trained YOLOv3 model.

## Results

After running the object detection using Darknet, the following results were obtained:

- Detection Time (GPU): 11.29 seconds
- Total Number of Objects Detected: 3069 objects

## Contact

For any questions or inquiries, please contact s-noureldin.hamedo@zewailcity.edu.eg.

Good luck with your YOLO object detection project!

# YOLO Object Detection

This GitHub repository contains code and models for performing object detection using different versions of the YOLO (You Only Look Once) algorithm, including YOLOv3, YOLOv5, and YOLOv8. The project utilizes the Ultralytics YOLOv3 implementation, as well as the Darknet framework for YOLOv3.

## Features

- YOLOv3: This implementation uses the Ultralytics YOLOv3 model, which is trained on the COCO dataset and provides accurate object detection across multiple classes.
- YOLOv5: The repository also includes variants of YOLOv5, which is a newer version of the YOLO algorithm. YOLOv5 offers improved performance and flexibility, with options for different model sizes and configurations.
- YOLOv8: Additionally, the project includes YOLOv8, an experimental version of the YOLO algorithm that incorporates advanced techniques and architectural enhancements.


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

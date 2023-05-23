YOLO Object Detection
This repository contains code for performing object detection using YOLO (You Only Look Once) algorithm. The project utilizes the Darknet framework and pre-trained weights on the COCO dataset.

Requirements
Make sure you have the following dependencies installed:

OpenCV
CUDA (if using GPU)
cuDNN (if using GPU)
Setup
Clone the YOLO repository:

bash
Copy code
git clone https://github.com/Roon311/YOLO.git
Navigate to the project directory:

bash
Copy code
cd YOLO
Build the Darknet framework:

bash
Copy code
make
Download the pre-trained weights for YOLO:

bash
Copy code
wget https://pjreddie.com/media/files/yolov3.weights
Usage
Run object detection using YOLO:

bash
Copy code
./darknet detect cfg/yolov3.cfg yolov3.weights data/person.jpg
This command will perform object detection on the provided image data/person.jpg using the YOLOv3 model and display the detected objects.

Modify the Darknet configuration file cfg/yolov3.cfg to customize the model architecture, such as adjusting the confidence threshold or selecting different anchor sizes.

Evaluation
To evaluate the YOLO model on the COCO dataset or other custom datasets, follow these steps:

Download the COCO dataset or prepare your custom dataset.

Modify the Darknet configuration file cfg/yolov3.cfg and update the cfg/coco.data file to specify the dataset paths and other relevant settings.

Run evaluation using Darknet:

bash
Copy code
./darknet detector test cfg/coco.data cfg/yolov3.cfg yolov3.weights
This command will perform evaluation on the specified dataset using the trained YOLOv3 model.

Results
After running the object detection using Darknet, the following results were obtained:

Detection Time (GPU): 11.29 seconds
Total Number of Objects Detected: 3069 objects
Include any additional relevant information about the performance, insights, or limitations of the model here.

Contact
For any questions or inquiries, please contact s-noureldin.hamedo@zewailcity.edu.eg.

Good luck with your YOLO object detection project!

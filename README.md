# Grocery Product Detection and Counting

This repository includes detecting products from grocery shops shelves images and calculating total count of products in a shelf.

Object detection is a computer vision technique that works to identify and locate objects within an image or video. Specifically, object detection draws bounding boxes around these detected objects, which allow us to locate where said objects are in (or how they move through) a given scene.

# Yolov5

YOLO an acronym for 'You only look once', is an object detection algorithm that divides images into a grid system. Each cell in the grid is responsible for detecting objects within itself. Best option for real time object detection with respect to speed and accuracy.

Shortly after the release of YOLOv4, Glenn Jocher introduced YOLOv5 using the Pytorch framework with models pre-trained on COCO dataset. And its also called YOLOP(You Only Look Once Pytorch). 

![image](https://user-images.githubusercontent.com/71822090/136696222-a4a15e2d-90c8-4e8c-9e75-72801f2f3b28.png)

Compared to Efficient net yolov5 performs better in speed and accuracy.

# Dataset

The grocery dataset is an image dataset with 355 images(284 in training and 71 in testing set). Collected from ~40 groceries, with 4 cameras.
Downloaded from https://github.com/gulvarol/grocerydataset.

The images were annoted in YOLO supporting format using LabelImg(https://github.com/tzutalin/labelImg).
Only one class 'product' is defined.

After annotation and resizing, dataset is zipped and saved in Google drive.

# Network Architecture

![network architecture](https://user-images.githubusercontent.com/71822090/136700132-8d213f26-68d2-43af-b70f-a1752d50883d.JPG)

# Training

The model is trained for 150 epochs with batch size 16 and image size 640.

# Results

![C3_P03_N3_S3_1](https://user-images.githubusercontent.com/71822090/136700304-bb714e28-f730-4c04-a865-f6dfc023bcae.jpg)

![C1_P02_N2_S2_1](https://user-images.githubusercontent.com/71822090/136700332-82137331-1e63-43b5-a957-f6e2df55e4d2.jpg)

# Output

Evaluation output with Precision, Recall and mAP on testing set is generated as metrics.json file

![output1](https://user-images.githubusercontent.com/71822090/136700564-228f786d-2aae-4d97-9747-28c607cf51ae.JPG)

Total number of products in a shelves are generated as image2products.json file

![output2](https://user-images.githubusercontent.com/71822090/136700585-34667677-f10a-47b0-9e45-180e4eedccf7.JPG)

# Reference

https://docs.ultralytics.com/#what-is-yolov5

# Conclusion

In real time scenarios for product management in retail shops, this model is very helpful. And it can be further improved by working on video dataset and further automation for product filling and counting in shops will be the real time application.








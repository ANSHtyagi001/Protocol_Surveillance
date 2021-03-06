Protocol Surveillance for Communicable Diseases using YOLO

This is a project to perform fall detection, vehicle crash detection and social distancing detection from CCTV cameras in real-time.

## How YOLO works ?

![Alt text](https://cdn-images-1.medium.com/max/1024/1*bSLNlG7crv-p-m4LVYYk3Q.png)

YOLO stands for You Only Look Once. It is used for object detection
To perform object detection on an image it looks at an image only once in a very clever way unlike R-CNN which takes several instances of the same image to perform detection. 

YOLO divides an image into a grid and several bounding boxes are formed. Then a confidence score is taken for each boundary box to see whether an bounding box contains any object within it. The confidence score is high if the object inside the box matches the pre-trained YOLO dataset ( [COCO Dataset](https://cocodataset.org/) ). The higher the confidence score, the higher the probability that a bounding box contains an object. Now several bounding boxes will intersect with each other. More the bounding boxes intersect, more is the probability that there is an object inside that box. Now we only keep those bounding boxes whose confidence score is more than threshold value lets say 30%. Now we match these bounding boxes with already known features of an object like person, car and classify them.

The good thing about YOLO is that all the predictions in the boxes are made at the same time i.e. the neural networks just ran only once.
And that is why YOLO is powerful and fast.

## Installation

### Softwares Required
* Python: Language in which code is written
* CMake: For compiling openCV
* Visual Studio Code: For building openCV and darknet code
* Nvidia GPU Driver: For faster GPU performance
* CUDA: For parallel computing using GPU
* CuDNN: A GPU-accelerated library of primitives for deep neural networks
* OpenCV: For working on images/videos in python
* Darknet: Neural network framework for YOLO
### Installation of above softwares
You can follow the two part YouTube videos of [Augmented Startups](https://www.youtube.com/watch?v=5pYh1rFnNZs&ab_channel=AugmentedStartups)
#### [Note-1: Darknet library gets updated daily so this code won't work for future versions of darknet. This code works for May 2020 - June 2020 version of [Darknet](https://github.com/AlexeyAB/darknet). So download that version of darknet otherwise you will get a lot of errors which would be very difficult to remove.]
#### [Note-2: If you face some errors check the comments of the video of [Augmented Startups](https://www.youtube.com/watch?v=5pYh1rFnNZs&ab_channel=AugmentedStartups). You will get the solutions for most of them there. Also download only that versions of the software that has been told in the video.]
### Usage
After the above installation work is done and darknet libraries are working, place the python files inside [YOLO\darknet\build\darknet\x64]() folder.

There are four ways to perform detection on videos:
1. Video from Web Cam
2. Local Stored Video
3. YouTube video
4. Video from Mobile Camera ( [DroidCam](https://www.dev47apps.com/) )

See the code of the program and uncomment the line from which you want to take the  video to perform detection.

You can take the video from Sample dataset to perform detection.
#### [Note: If you want to perform the detection on a locally stored video then make sure that the video is stored inside the [YOLO\darknet\build\darknet\x64]() folder along with the python script]

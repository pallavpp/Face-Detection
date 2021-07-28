# Face Detection System
This code detects faces in live video using YOLO algorithm and Harr-Cascade classifier.

It uses Keras framework along with OpenCV and Pillow library.


## Requirements
- [TensorFlow](https://pypi.org/project/tensorflow/)
- [Keras](https://pypi.org/project/keras/)
- [OpenCV](https://pypi.org/project/opencv-python/)
- [Pillow](https://pypi.org/project/Pillow/)
- YOLOv3 Weights: Can be downloaded from [here](https://pjreddie.com/media/files/yolov3.weights) or [here](https://drive.google.com/file/d/1yF29HmHUQFsIhODzshj49zPg_gXZVENe/view?usp=sharing).
- Haar-Cascade Classifier: Can be found [here](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml) on the OpenCV GitHub repo, and can be downloaded from [here](https://drive.google.com/file/d/1M1MiTZRXeP3y5h06dtbpNhH5fGQyYoDy/view?usp=sharing).


## Working
- Harr-Cascade classifier by itself is not that accurate and often returns false-positives (As seen in the following examples):

  <img width="200" height="200" alt="haar_image3" src="https://user-images.githubusercontent.com/62967830/127311964-5bc0593c-cab5-44d6-9200-a467adb94ef7.jpg">
  <img width="200" height="200" alt="haar_image8" src="https://user-images.githubusercontent.com/62967830/127312030-cc275e9c-c952-41a8-8f50-2a4d44fb5a51.jpg">
- Detection of full body in image/frame by YOLOv3 (Very Accurate):

  <img width="200" height="200" alt="yolo_image3" src="https://user-images.githubusercontent.com/62967830/127311574-09e55d95-ce6b-47bd-9403-5feec6eb09f2.jpg">
  <img width="200" height="200" alt="yolo_image8" src="https://user-images.githubusercontent.com/62967830/127311654-36d10a04-31e8-4893-a8ed-85afd05525c4.jpg">

- Implementing Haar-Cascade classifier inside regions detected by YOLOv3 gives much more accurate results:

  <img width="200" height="200" alt="final_image3" src="https://user-images.githubusercontent.com/62967830/127312234-20d4a145-3ac4-41f8-873f-1f0ec2f0dd6f.jpg">
  <img width="200" height="200" alt="final_image8" src="https://user-images.githubusercontent.com/62967830/127312287-fc78bd36-82eb-4492-8b80-f16feaed3ac2.jpg">

# Face Detection System
This code detects faces in live video using YOLO algorithm and Harr-Cascade classifier.

Uses Keras framework along with OpenCV and Pillow library.


## Requirements
- [TensorFlow](https://pypi.org/project/tensorflow/)
- [Keras](https://pypi.org/project/keras/)
- [OpenCV](https://pypi.org/project/opencv-python/)
- [Pillow](https://pypi.org/project/Pillow/)
- YOLOv3 Weights: Can be downloaded from [here](https://pjreddie.com/media/files/yolov3.weights) or [here](https://drive.google.com/file/d/1yF29HmHUQFsIhODzshj49zPg_gXZVENe/view?usp=sharing).
- Haar-Cascade Classifier: Can be found [here](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml) on the OpenCV GitHub repo, and can be downloaded from [here](https://drive.google.com/file/d/1M1MiTZRXeP3y5h06dtbpNhH5fGQyYoDy/view?usp=sharing).


## Working
Detection of full body in image/frame by YOLOv3:
Harr-Cascade classifier by itself is not that accurate and often returns false-positives:
Implementing it inside regions detected by YOLOv3 gives much more accurate results:

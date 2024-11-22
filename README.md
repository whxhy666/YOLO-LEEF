# YOLO-LEEF
 YOLO-LFFE: A Lightweight Fish Detection Model  Based on Feature Enhanced Fusion

# This is the code for the official yolov8
 https://github.com/ultralytics/ultralytics/blob/main/ultralytics/cfg/models/v8/yolov8.yaml

# How to use
1.Install
 Pip install the ultralytics package including all requirements in a Python>=3.8 environment with PyTorch>=1.8.
2.PYTHON
from ultralytics import YOLO
if __name__ == '__main__':
    model = YOLO("ultralytics/cfg/cfg/yolo-LFFE.yaml")
    model.train(data='/home/zdy/hh/ultralytics/ultralytics-main/dataset/deepfish.yaml',
                cache=False,
                imgsz=640,
                epochs=300,
                batch=32,
                close_mosaic=0,
                workers=4,
                device=[0,1],
                optimizer='SGD',
                project='train',
                name='exp',
                )
    model.val()

# lemons-vs-apples-object-detection
What would you do if life gives you lemons? easy, make a photo session for some lemons and apples then see if a YOLOv8 and Faster-RCNN will be able to detect lemons from sweet-sweet apples.


## 1. Dataset Collection
- There were two lemons and two apples, a green one and a red one in my humble fridge. so I took a 100 picture of them collectively. I made sure to take them under different light conditions and using different backgrounds
- <img src="https://user-images.githubusercontent.com/36730799/223129385-48e43120-95f6-4de5-a9b7-cf509ec9a52c.png" width=25% height=25%> <img src="https://user-images.githubusercontent.com/36730799/223129324-8f483327-38a3-43ca-b481-15382c466d4f.png" width=25% height=25%>
- Then annonated the pictures using Roboflow 
- Applied resizing and rotation for data preprocessing and agumentation

## 2. Model Training and Inference 
I used Faster-RCNN and YOLOV8 for this object detection task. 

### 2.1 Faster-RCNN
You can find my notebook [here](https://github.com/mariammaher550/lemons-vs-apples-object-detection/blob/main/train_fast_rcnn_on_custom_dataset_detectron2.ipynb) for the source code. 
#### Training, Inference and Metrics
- I used detectron2 to load and train Faster-RCNN from detectron2 model zoo. You could find their official repo [here](https://github.com/facebookresearch/detectron2) also, this [article](https://towardsdatascience.com/object-detection-in-6-steps-using-detectron2-705b92575578) was helfpul too
- The training has taken 23 minutes with 300 epochs and 16 batch size
- Metrics :
-  <img src= "https://user-images.githubusercontent.com/36730799/223133762-4e2587b0-95b3-479a-b098-700c1fef5390.png" width=60% height=60% >
- Samples detected : 
- <img src="https://user-images.githubusercontent.com/36730799/223135212-9f9d87d1-25e1-4e89-886d-3dcdc41ca3bc.png" width=20% height=20%>  <img src="https://user-images.githubusercontent.com/36730799/223135653-807d3433-3030-4b95-a6dd-ea21cb08ad3b.png" width=20% height=20%> 

### 2.2 YOLOv8
You can find my notebook [here](https://github.com/mariammaher550/lemons-vs-apples-object-detection/blob/main/train_yolov8_on_custom_dataset.ipynb) for the source code
#### Training, Inference and Metrics
- I closely followed this [article](https://blog.roboflow.com/how-to-train-yolov8-on-a-custom-dataset/) from roboflow.Inwhich 
- The training has taken less than 2 minutes with 25 epochs 
- Metrics :
-

-  <img src= "https://user-images.githubusercontent.com/36730799/223138424-9886497a-fbf7-4687-9566-995027200607.png" width=80% height=80% >  <img src= "https://user-images.githubusercontent.com/36730799/223139129-b76a4486-fbdc-40f9-a472-15c7ed2b7794.png" width=70% height=70% > 
- Samples detected : 
- <img src="https://user-images.githubusercontent.com/36730799/223139717-64a675a6-af8f-4db3-bfbc-f1ec8e84bea9.png" width=50% height=50%>  

# Ship-Detection---Object-Detection



# YOLOv8 Model Training

This repository contains the steps  to train the YOLOv8 object detection model , the results acquired.

## Overview

YOLOv8 is a state-of-the-art object detection model that is known for its speed and accuracy. 

## Requirements

- Python 3.x
- PyTorch
- CUDA (optional, for GPU acceleration)
- Other dependencies as required

## Steps Performed to train the model

1. **Data Collection:** Gathered images and corresponding annotations for dataset.

2. **Data Preprocessing:**  formated annotations ( converted coco.json  to YOLO format),
3. splited dataset into train/validation sets  in the ratio 80:20
4. Create a YAML configuration file (data.yaml) specifying details about the dataset(train&validation folder paths , Number of classes, class names
5.  Yolov8 model 
  - yolo.yaml -- initialize a YOLOv8N model object based on the specifications provided in the datayaml file.
  - Trained for 100  epochs with an early stopping criteria of patience=5
  - saved the models in [Weights](weights)
  - Acquired results , stored in [Results](Results)
6. Predictions are done by loading the best.pt model  from weights for the validation set , stored in [Predictions](Predictions)

7. Jupyter notebook - [notebook](Yolov8.ipynb)


        
##  Metric Results

Metrics                 | Value
---------------------- | -------------
mAP50                  | 0.83948713 
mAP50-95               | 0.55158244
precision              | 0.89090876
recall                 | 0.73130703



# Results
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/935f4b80-6876-428f-8bed-a2b97b50c8cf" width="450px">
      <br>
    </td>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/bfc4bf49-2247-4791-81b8-af027943e52a" width="450px">
      <br>
    </td>
      </tr>
</table>
    <table>
  <tr>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/704f5a20-408c-4a3b-aeb5-a5af21545281" width="450px">
      <br>
    </td>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/139507f5-f976-4454-b24d-982ba744e712" width="450px">
      <br>
    </td>
  </tr>
</table>

# Visualization Results on test dataset

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/3412810a-44a6-4d37-ac20-0e912b5d4117" width="400px">
      <br>
    </td>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/0ac0c0a1-6864-4e92-8852-c0bbf7789936" width="400px">
      <br>
    </td>
  </tr>
</table>


<table>
  <tr>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/a897945d-a1e4-4fd9-b36d-770ee0dba0c1" width="400px">
      <br>
    </td>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/01c1e418-7ee0-479b-a11c-0485055b0882" width="400px">
      <br>
    </td>
  </tr>
</table>




<table>
  <tr>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/9e50a70c-e3c7-44b0-9002-100479bf6468" width="400px">
      <br>
    </td>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/e95286a7-71ce-459e-8e79-87f323cef751" width="400px">
      <br>
    </td>
  </tr>
</table>




<table>
  <tr>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/694df7fa-0214-45c6-850e-f0d59732d166" width="400px">
      <br>
    </td>
    <td align="center">
      <img src="https://github.com/kasamrohith02/Ship-Detection---Object-Detection/assets/143547473/112ab72a-7f82-4296-8279-f3506a082c0f" width="400px">
      <br>
    </td>
  </tr>
</table>




- The results.csv file captures a comprehensive snapshot of my experiments, tracking performance metrics across epochs  
 [click me to view <b>"results.csv"</b>](Results/results.csv)

- Predict folder contains predictions of ships(unseen data) made by the trained YOLOv8 model  
 [click me to view <b>"Predictions"</b>](Predictions)




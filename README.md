## GBH-YOLOv5: Ghost convolution with BottleneckCSP and tiny target prediction Head incorporating YOLOv5 for PV panel defect detection
---
## Contents
1. [Project description](#Project)
2. [Required environment](#Required)
3. [Training](#Training)
4. [Testing](#Testing)
5. [Acknowledgements](#Acknowledgements)

## Citations
@article{Li2023,<br>
  title = {GBH-YOLOv5: Ghost Convolution with BottleneckCSP and Tiny Target Prediction Head Incorporating YOLOv5 for PV Panel Defect Detection},<br>
      shorttitle = {GBH-YOLOv5},<br>
      author = {Li, Longlong and Wang, Zhifeng and Zhang, Tingting},<br>
      year = {2023},<br>
      month = jan,<br>
      journal = {Electronics},<br>
      volume = {12},<br>
      number = {3},<br>
      pages = {1--15},<br>
      publisher = {Multidisciplinary Digital Publishing Institute},<br>
      issn = {2079-9292},<br>
      doi = {10.3390/electronics12030561},<br>
      copyright = {http://creativecommons.org/licenses/by/3.0/},<br>
      }<br>


## Project description
This project is based on the improved and optimized model of YOLOv5s, and its task is to detect defects on the surface of photovoltaic panels. In this study, the YOLOv5 model was improved to achieve 97.8% performance on PV Multi-Defect dataset. Research work based on this project has been submitted to 'Electronics', and the manuscript is titled "GBH-YOLOv5: Ghost convolution with BottleneckCSP and tiny target prediction Head incorporating YOLOv5 for PV paneldefect detection"

## Required environment

Pytorch == 1.8.1  
python == 3.8  
Cuda == 11.1

### Install the project environment
```python
pip install -r requirements.txt
```

### Check whether the dependent environment is normal.
```python
python detect.py --source ./data/images/ --weights weights/yolov5s.pt
```

## Training

### Data preparation
Download PV Multi-Defect images (train, val) and labels. Link: https://github.com/CCNUZFW/PV-Multi-Defect.  
Download weights. Link: https://pan.baidu.com/s/1ApCScpr1CZ_AeVJH7crgCw Extraction code: lmn8   

### Start training
```python
python train.py
```

## Testing
The optimal weight obtained from the training was used for the test.
```python
python detect.py --source ./testfiles/img1.jpg --weights runs/train/exp/weights/best.pt
```


## Acknowledgements
https://github.com/ultralytics/yolov5  
https://github.com/robintzeng/Pytorch-CSPNet

If you have any question, please feel free to contact us through zfwang@ccnu.edu.cn.

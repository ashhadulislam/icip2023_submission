# Algorithm Submission
## _Automatic Detection of Mosquito Breeding Grounds_



- Project details
- Execution Instructions

## Project details

The models used were different sizes of yolov8 models.
Generally yolov8 models can be downloaded pre-trained on the COCO-128 dataset.
In our case, we have used the architecture of the yolov8 models but trained them from scratch on the given data.
As the given images are taken by UAVs the dimension of the objects to be detected are low. Hence we believed that it would be better to train the models from scratch.
For more details on using yolov8 models please refer to https://github.com/ultralytics/ultralytics
We are sharing the weights so that they can be downloaded and cross checked.

| Class | Model | Class | Model | Class | Model |
| ------ | ------ | ------ | ------ | ------ | ------ |
| bottles | [yolov8n](https://drive.google.com/file/d/1qdbawRmvPYFye68nr-LeydtBa-U2VCt9/view?usp=share_link) | 30 | 0.37408 | 0.26071 | 0.307271 |
| buckets | [yolov8n](https://drive.google.com/file/d/19znjmcKp8rS0b-0kJ_IcJorbaXmP_ZzL/view?usp=share_link) | 30 | 0.95153 | 0.81167 | 0.871791 |
| pools | [yolov8l](https://drive.google.com/file/d/1uUalZcfUWo-8CbfrJ5KniODbh3dc7mez/view?usp=share_link) | 30 | 0.98845 | 0.98154 | 0.984983 |
| puddles | [yolov8n](https://drive.google.com/file/d/16FpR3aNoHckaL8TMOm020uvKMNbYajak/view?usp=share_link) | 30 | 1.0 | 0.99821 | 0.999104 |
| tires | [yolov8n](https://drive.google.com/file/d/1NauZ6pdH44Cfe_HJaztJ5p0CdjKhCSI6/view?usp=share_link) | 30 | 0.21349 | 0.27741 | 0.241288 |
| watertanks | [yolov8l](https://drive.google.com/file/d/1bJAlNBn8rL0Mqak9dSoMrYG8nvyQy9KR/view?usp=share_link) | 30 | 0.22078 | 0.23787 | 0.229007 |


Data Preprocessing and training steps can be followed by following the below notebooks

[01_CreateAnnotationsYOLOv8-all0s.ipynb](https://drive.google.com/file/d/1GbZfzOL60qHz5g7_Y-X5AKy4oiszfs2O/view?usp=share_link) 
This piece of code creates the annotations for every individual class which will be used later.

[02_ArrangeFiles-0ForAllClasses.ipynb](https://drive.google.com/file/d/1p4VM6GHAbwGu_uLgM2Ad4ebvIfWZ2AkY/view?usp=share_link)
This piece of code separates data per class and stores corresponding images and annotations in separate folders.

[03_SplitArrangedFiles.ipynb](https://drive.google.com/file/d/1AYySG0eYn1t3uCcyfk9pHj5qHjGhLevM/view?usp=sharing)
This piece of code splits the data per class into train and test

[04_CreateYAMLFiles.ipynb](https://drive.google.com/file/d/15cazAX4eY0ujd98COamvtUaKUTWXJH4y/view?usp=share_link)
This notebook creates the yml files necessary for each class to train models for each class

[05_yolov8Train.ipynb](https://drive.google.com/file/d/16-Uv26feVWlLc2kO88i3n8Pcz5LWDPvn/view?usp=share_link)
This notebook is for training the yolo models on different classes of data


Contacts:
Najla Fahad (nbfx95@gmail.com)
Ashhadul Islam (ashhadulislam@gmail.com(

## License
MIT

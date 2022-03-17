# Epi-Stroma Model (Python-DL)
DL model for segmentation on H&E-stained digitized images of Epithelium-Stroma tissue segments.

## Pre-requisites

- Linux (Tested on windows10, CUDA10.2)
- NVIDIA GPU (Tested on Nvidia TianX 1080 x 12 on local workstations)
- Python (3.5+), matplotlib (3.1.1), numpy (1.17.3), opencv-python (4.1.1.26), pillow (6.2.1), PyTorch (1.4+), scikit-learn (0.22.1), scipy (1.3.1), torchvision (0.4.2), tensorboardx (optional)

## How to run
Run Python train.py to train a epithelium vs stroma model. Specify the dataset and mask argument by:
'''python
python train.py --dataset <dataset name> --arch NestedUNet --img_ext .png --mask_ext .png
'''
To directly predict the epithelium and generate the segmentation mask, run
'''
python pred.py
'''
Specify the model snapshot by --name arguments, the default folder containing the images for predict is called input.

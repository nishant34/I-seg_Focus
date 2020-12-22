# I-seg_Focus

* This repository contains the results of an attention based Deep neural Network Architecture applied to MICCAI I-seg challenge for MRI scans of 6 month infants and decent results were observed. 
* The architecture was derived from Focusnet (state of the art architectures for 3D segmentation). 
* This architecture has been extended to 3D segmentaion of voxel based scans.
* Decent Results were observed for the metric(DSC score, which was proposed by MICCAI for the challenge).

# Dataset Description
The challenge Details can be found [here](http://iseg2017.web.unc.edu/rules/results/)
* It required 3 evaluation metrics DSC,MHD and ASD score for 3 categories: CSF,WM,GM.
* There are 10 T1 and T2 weighted scans provided for the challenge for training in the 
* The test set contains 23 cases and results have to be submitted in appropriate format.
* The scans are provided in .hdr and .img format.
* Each case has 256x256x144 MRI scan of vioxel base representation. 
* Annotations into 4 categories are also provided for the train set.

# Code_structure
* To bring the data in .h5 format run the following code:
```javascript
python prepare_hdf5_cutedge.py 
```
Also maintain the directory structure as the orignal provided by MICCAI and adjust path value in above file.

The .h5 format data extracted from this code can be found [here](https://drive.google.com/drive/u/1/folders/1C8O432hWpzUFD8z71KsFzJNdq_Ed8oSe).

* dataloader.py: a dataloader to load the h5 dataset.
* metrics.py : Code for the metrics defined by MICCAI for this challenge.
* There are 2 variants of the model so adjust the file while training.
* model train files have the training code and val files have the validation code along with the model structure.

The training can also be seen in the follwing [link](https://colab.research.google.com/drive/1FJ0bH1ry91Ei5dQYuhEpcY0zIrrI_vnG).
The train val split ratio is 9:1.
The validation can also be seen in the following [link](https://colab.research.google.com/drive/1matFu0UsngJmhKSnnoLIOndzC-PdcHPT).
Further description along with the model image can be seen in the following [doc](https://docs.google.com/document/d/16WZNNuNzkmpq01fxrwKnV0zsz3hc9kAt/edit).
These wer the final validation result ona single scan:
```javascript
| Note              | class1| class2|class3| Avg.|
| 20000_weights1000 | 94.53 | 90.83 | 89.60 | 91.65 |
```
The model :
![alt text](https://drive.google.com/file/d/1c3tN6dO-Sfvn0JzIemVBCyzyQxDizBmG/view?usp=sharing)




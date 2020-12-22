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




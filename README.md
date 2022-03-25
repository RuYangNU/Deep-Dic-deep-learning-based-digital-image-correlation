# Deep DIC: Deep Learning-Based Digital Image Correlation for End-to-End Displacement and Strain Measurement
 
Note: We are still working on uploading more dataset. <br/>

Digital image correlation (DIC) has become an industry standard to retrieve accurate displacement and strain measurement in tensile testing and other material characterization. Though traditional DIC offers a high precision estimation of deformation for general tensile testing cases, the prediction becomes unstable at large deformation or when the speckle patterns start to tear. In addition, traditional DIC requires a long computation time and often produces a low spatial resolution output affected by filtering and speckle pattern quality. To address these challenges, we propose a new deep learning-based DIC approach – Deep DIC, in which two convolutional neural networks, DisplacementNet and StrainNet, are designed to work together for end-to-end prediction of displacements and strains. DisplacementNet predicts the displacement field and adaptively tracks the region of interest. StrainNet predicts the strain field directly from the image input without relying on the displacement prediction, which significantly improves the strain prediction accuracy. A new dataset generation method is developed to synthesize a realistic and comprehensive dataset, including generation of speckle patterns and deformation of the speckle image with synthetic displacement field. Though trained on synthetic dataset only, Deep DIC is tested on both simulated and experimental data. Deep DIC gives highly consistent and comparable predictions of displacement and strain with those obtained from commercial DIC software, while it outperforms commercial software with very robust strain prediction even at large and localized deformation and varied pattern qualities. In addition, Deep DIC is capable of real-time prediction of deformation with a calculation time down to milliseconds.<br/>
Please refer to our paper: https://www.sciencedirect.com/science/article/pii/S092401362100434<br/>
and https://arxiv.org/ftp/arxiv/papers/2110/2110.13720.pdf

## Citation
If you find this code or the provided data useful in your research, please consider cite:<br/>
@article{yang2022deep,<br/>
title={Deep DIC: Deep learning-based digital image correlation for end-to-end displacement and strain measurement},<br/>
author={Yang, Ru and Li, Yang and Zeng, Danielle and Guo, Ping},<br/>
journal={Journal of Materials Processing Technology},<br/>
volume={302},<br/>
pages={117474},<br/>
year={2022},<br/>
publisher={Elsevier}<br/>
}

## Dependencies
Deep-DIC is implemented in [PyTorch](https://pytorch.org/) and tested with Ubuntu 20.04, please install PyTorch first following the official instruction. 
- Python 3.7 
- PyTorch (version = 1.16)
- Torchvision (version = 0.7.0)
- Pillow (version = 7.2)
- numpy
- scipy
- CUDA

## Overview
We provide:
- Datasets: training dataset, validation dataset and test dataset.
      https://drive.google.com/drive/folders/1B2JLnd0Jn5kwrqkbHT9R6MUC-NROJ3C0?usp=sharing
- Pre-trained models:
      https://drive.google.com/drive/folders/1n2axHsJ3flHxk_edceY6eOfiX7GjW_d6?usp=sharing
    - DisplacementNet
    - StrainNet
- Code to test with pair of speckle images.
- Code to train the two CNNs with dataset.

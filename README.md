# U-Finger: Multi-Scale Dilated Convolutional Network for Fingerprint Image Denoising and Inpainting

## Introduction
This paper studies the challenging problem of fingerprint
image denoising and inpainting. To tackle the challenge of suppressing
complicated artifacts (blur, brightness, contrast, elastic transformation,
occlusion, scratch, resolution, rotation, and so on) while preserving fine
textures, we develop a multi-scale convolutional network, termed as U-
Finger. Based on the domain expertise, we show that the usage of dilated
convolutions as well as the removal of padding have important positive
impacts on the final restoration performance, in addition to multi-scale
cascaded feature modules. Our model achieves the overall ranking of
No.2 in the ECCV 2018 Chalearn LAP Inpainting Competition Track 3
(Fingerprint Denoising and Inpainting). Among all participating teams,
we obtain the MSE of 0.0231 (rank 2), PSNR 16.9688 dB (rank 2), and
SSIM 0.8093 (rank 3), on the hold-out testing set.

This code repository is built on top of [DeepLab v2](https://bitbucket.org/aquariusjay/deeplab-public-ver2).

For more details, please refer to our [paper](https://arxiv.org/abs/1807.10993).


## Converting the colored images to gray
- `cd Testing`
- Use processimage.py to generate gray images

### Models
- `cd Testing`

### Training
- `cd exper`
- Run `main_train_denoise.sh` to train the denoising network seperately.
- Need to have an txt file where all the image names are listed and its location needs to updated in main_train_denoise.sh

### Testing
- `cd Testing`
- Use the dia_mean.ipynb file to generate images for testing
- The trained model and its deploy files are also located in the same folder
- Use conv.ipynb to remove the noise on the edges 

## Citation
Please cite the paper in your publications if it helps your research:

    @inproceedings{rgsl888,
      author = {Ramakrishna Prabhu, Xiaojing Yu, Zhangyang Wang, Ding Liu, Anxiao Jiang},
      title = {U-Finger: Multi-Scale Dilated Convolutional Network for Fingerprint Image Denoising and Inpainting},
      year = {2018},
      journal={arXiv preprint arXiv:1807.10993}
      }
      

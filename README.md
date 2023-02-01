# RGINP: Reference Guided Image Inpainting <br> using Facial Attributes

This repository is a official Pytorch implementation of RGINP.

<br>

![Teaser Image](imgs/main_img.jpg)

## [Paper](https://arxiv.org/abs/2301.08044)
>**"Reference Guided Image Inpainting using Facial Attributes"** <br>
>Dongsik Yoon, Jeong-gi Kwak, Yuanming Li, David K Han, Youngsaeng Jin and Hanseok Ko<br>
>**British Machine Vision Conference (BMVC), 2021** <br>

## Architecture
![Architecture](imgs/architecture.jpg)

$I_{masked}$ and $M$ are the input of Enc, we omit $M$ in this figure to express clearly our framework. For the test stage (red line), the user extract desired attributes using our attributes extractor to a reference image.

## Dependencies
- pytorch
- numpy
- Python3
- munch
- Pillow

## **Preparing datasets**
We utilize all the experiments in this paper using [CelebA-HQ dataset](https://github.com/tkarras/progressive_growing_of_gans/tree/original-theano-version) and [Quick Draw Irregular Mask dataset](https://github.com/karfly/qd-imd).
Please download the datasets and then construct them as shown below.
If you want to train or evaluate different images you have yo change 
If you want to learn and evaluate different images you have to change `dataloader.py`.

```
    --data
      --train
        --CelebA_HQ
          --0.jpg
            ⋮
          --27999.jpg
      --test
        --CelebA_HQ
          --28000.jpg
            ⋮
          --29999.jpg
      --masks
        --traian
            --00000_train.png
              ⋮
        --test
            --00000_test.png
              ⋮
        
    --RGINP
        ⋮
```


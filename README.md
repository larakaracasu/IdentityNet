# IdentityNet: A Platform for Facial Anti-Spoofing Detection

Facial spoofing poses a significant challenge in cyber security. This paper introduces IdentityNet, a web platform designed to (1) differentiate genuine faces from spoofed faces and (2) identify the type of presentation attack. IdentityNet allows users to easily select a model, upload their own photo, and receive a prediction for whether the image is live or spoofed, as well as the spoof type classification. Our approach uses a variety of model architectures, including binary and multiclass convolutional neural networks (CNNs), unimodal and multimodal Vision Transformers (ViTs), and Generative Adversarial Networks (GANs). The performance of these models was evaluated with the following metrics: loss, accuracy, precision, recall, and F1 score. Ultimately, we find that the model performance greatly varied. While the multiclass CNN achieved the highest accuracy at 0.9760, our GAN-driven CNN achieved the lowest recall at 0.9560. We also discuss model validation mechanisms including data leakage investigations, fairness testing using additional dataset for more diverse demographics, and model explainability analysis. Overall, this paper addresses the development, training, and evaluation of the aforementioned models, their performances, validation and the creation of the IdentityNet platform.
For this, we used the Celeb-A Spoof For Face Anti-Spoofing (Kaggle 2020) dataset of 47,248 spoof images and 19,924 live images.

### Binary CNN
* Binary classifier with CNN: [model.pth](https://drive.google.com/file/d/1vxKYC-lTgIN_uPRxgROswtFvvE083ftW/view?usp=sharing)
* Binary classifier with CNN (leakage addressed): [model.pth](https://drive.google.com/file/d/1CJpca6ajSydwS17waEwbSIE4OaT2Ew09/view?usp=sharing)

### Multiclass CNN
* 5-class classifier with CNN: [multiclass_cnn.pth](https://drive.google.com/file/d/1E8ZP-Tbbi1x-EZNz3FpBmI_x9WPzsbjK/view?usp=sharing)
* 5-class classifier with CNN (V2): [multiclass_cnn_2.pth](https://drive.google.com/file/d/1n4KGSxFkg9gGQ6QptdzCC8AYWAaEXj_j/view?usp=sharing)
* Enhanced 5-class classifier with CNN (downsampled spoof images from original dataset + lives images from another dataset, grouped by gender and age): [enhanced_multiclass_cnn.pth](https://drive.google.com/file/d/1eapCHekVgl7QrSaYzXn5PBSK1umcq5-O/view?usp=sharing)

### GAN:
 - Generator: [generator_model.pth](https://drive.google.com/file/d/1KfKjb-qCuZpc5LuDAqsRtsY1uEeJ86RA/view?usp=sharing)
 - Discriminator: [discriminator_model.pth](https://drive.google.com/file/d/1aRgL1uWnqfajiyTGuFOIDN7ev09oMibz/view?usp=sharing)
 - simple CNN on pretrained model using GAN generated images: [gan_simple_cnn.pth](https://drive.google.com/file/d/1Mk_UEo-uKuE6fvTJXZYwdL8sgwq_Ilbn/view?usp=sharing)

### ViT:
  - ViT Multiclass Image Only: [vit_multiclass.pth](https://drive.google.com/file/d/1fISEKMOm9RFfOd-wumcMCOiBmXqFVtlc/view?usp=share_link)
  - ViT Multiclass Concatenation Model: [vit_multiclass_concat.pth](https://drive.google.com/file/d/1-jfPuQnttVrBNkoX_uTu_jCyg5LJm7Qg/view?usp=share_link)
  - ViT Multiclass Contenation with Neural Network Model: [vit_multiclass_concat_with_nn.pth](https://drive.google.com/file/d/1eB4Y1foTljMby35R9VUt_CeWs22yEE9n/view?usp=share_link)


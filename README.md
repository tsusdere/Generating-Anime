# Generating-Anime
Use GANs in order to generate anime faces
## Purpose
The purpose of this project was to gain an understaing on how Generative Adversarial Networks (GAN) work in order to generate images from noise.
The theme of this project was 'anime' this was chose as many GAN examples inolve generating human faces or attributes and there is not much research or
projects involving 2D characters. It will also add some fun to the project.
## Datasets
The datasets provided are the [**Anime Faces**](https://www.kaggle.com/soumikrakshit/anime-faces) & [**selfie2anime**](https://www.kaggle.com/arnaud58/selfie2anime) datasets. The first dataset contains 64x64 RGB anime faces with a white background and simple features as opposed to the second dataset. The second dataset **selfie2anime** involves 
## Methodology
* Create a DCGAN model by incorporating a generator and discriminator network.
* The generator network will attempt to generate images from noise to create 64x64 RGB anime face image.
* Disciminator network will determine if the images are 'rea' or 'fake' depending on the ground truth provided
* Update the generator and the weights based on the discriminator's choice and generated new images to attempt to 'fool' the discriminator.
## Results
The generator started to stall in improving the quality of the images that are generated around the 2,000th epoch. This is attributed to the generator being to 'fool' the discriminator easily and thus the discriminator marks all the images from that point on as 'real' with a high accuracy. This causes an extremely high FID score which when training another dataset and comparing to other models the proposed model is out classed as it contains the highest FID score out of all. 
From the FID scores quantitatively the  model did not hold on to the same caliber as the other models which can be found talked about in the [**AniGan**](https://arxiv.org/abs/2102.12593) paper which dives deeper into each individual architecture of the models. Qualitatively the images seem to be pretty decent when comparing it to the ground truth images that have been used to train the model. <br />
<p align="center">
  <img width="543" height="232" src="https://github.com/tsusdere/Generating-Anime/blob/main/results/FID%20table.JPG">
</p><br />

## Image Results
<p align="center">
  <img width="543" height="232" src="https://github.com/tsusdere/Generating-Anime/blob/main/results/Animated%20GIF.gif">
</p><br />

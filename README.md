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
Below is a GIF created by compiling all the images that have been generated to demonstrate how the generator progresses as it generates images. As mentioned diminishing returns seems to apply as the generator seems to stop improving in the quality and just generate radom images of the same quality. The model was able to generate images that are qualitatively close to those that it was being trained on when the model was trained on the Anime Faces dataset. The difference being some distortion in the faces as it seemed the generated images was attempting to blend two faces poorly. The FID score was also high when comparing a generated image to a ground truth images meaning the model still needs improvements, primarily in training the discriminator as the generator was able to ‘fool’ it easily. When the model was trained on the selfie2anime dataset the disparity of the FID score demonstrates how the proposed model is outclasses by models that are of higher caliber. Overall, though the results are not on par with state-of-the-art cases the results are good for the objective of this project, learning about GANs.

<p align="center">
  <img width="480" height="480" src="https://github.com/tsusdere/Generating-Anime/blob/main/results/Animated%20GIF.gif">
</p><br />

## Keypoints
* DCGAN was able to generate anime images from noise vectors but with a high FID score.
* Generated images appeared to have some distortion almost seemed like a weak blend of two different faces.
* Improvement stalled after the 2,000-epoch meaning we need to train the discriminator and lock the generator.
* Data generated could be used to attempt adversarial training with neural networks to attempt to protect from attacks with random distorted images.
* Improving on state-of-the-art models such as a StyleGAN will allow for open-source improvement on the generated images.


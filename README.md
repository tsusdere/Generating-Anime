# Generating-Anime
Use GANs in order to generate anime faces
## Purpose
The purpose of this project was to gain an understaing on how Generative Adversarial Networks (GAN) work in order to generate images from noise.
The theme of this project was 'anime' this was chose as many GAN examples inolve generating human faces or attributes and there is not much research or
projects involving 2D characters. It will also add some fun to the project.
## Datasets
The datasets provided are the [**Anime Faces**]{https://www.kaggle.com/soumikrakshit/anime-faces} & [**selfie2anime**]{https://www.kaggle.com/arnaud58/selfie2anime} datasets. The first dataset contains 64x64 RGB anime faces with a white background and simple features as opposed to the second dataset. The second dataset **selfie2anime** involves 
## Methodology
* Create a DCGAN model by incorporating a generator and discriminator network.
* The generator network will attempt to generate images from noise to create 64x64 RGB anime face image.
* Disciminator network will determine if the images are 'rea' or 'fake' depending on the ground truth provided
* Update the generator and the weights based on the discriminator's choice and generated new images to attempt to 'fool' the discriminator.

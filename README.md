# AI-Clothing: AI Powered Clothing Design Generator
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kailasds/mj-project/blob/master/AI-Clothing.ipynb)



![teaser](clothing-gan-thumbnail.gif)



## Inspiration
GAN or Generative Adversarial Network is a generative model that enables us to generate images by learning the probability distribution of a large image dataset. GAN enables us to generate high-quality arts or design even without the technical or artistic skill in drawing. Recently, many face editing demonstrations on GAN has been made, but never seen semantic manipulation in other datasets. Hence,  we created AI-Clothing, an application where you can collaboratively design clothes without high technical expertise.

## What it does
AI-Clothing enables us to generate clothing images and mix these images. While mixing, you can control which structure or style that you want the clothing to copy. Additionally, you can edit the generated clothing with several given attributes such as dark color, jacket, dress, or coat.

## How to build 
We trained StyleGAN2-ADA on a subset of the Lookbook dataset. The total images we trained it on are 8,726 clothing images with a clean background.

After finishing training the GAN, We proceeded to use GANSpace method to find important directions in the latent space. Then, we tried to guess what these directions represent and labeled them accordingly. The reason we used GANSpace is that it is unsupervised and does not need an attribute classifier.

Finally, we created a UI with Gradio UI library. All the development is done on Collab. Gradio made deployment very easy. We can directly deploy the UI from Collab where Gradio will create a proxy from the Collab server to their domain and the given URL.


## Challenges 
One of the challenges we faced was uploading the dataset to Google Drive. As the file size was large a direct access to the dataset was denied. Temporarily we uploaded the dataset to Mega to rectify the issues. Once solved we uploaded it back to the Google Drive.

## Learning
We discovered Gradio UI, a library that makes ML deployment very easy. There were also other alternatives such as StreamLit or Dash, but found Gradio as the easiest to work with. One shortcoming is that it's quite inflexible in terms of customization.

## What's next 
There is a lot of potential for the project. Some features that can be added are appearance transfer, image inversion (uploading & editing real image), generating the fashion model itself, etc.
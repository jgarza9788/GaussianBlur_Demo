GaussianBlur_PPM
-------------------------------------
[Asset Store Link](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!-- vscode-markdown-toc -->
* [Table of Contents](#TableofContents)
* [Description Features](#DescriptionFeatures)
* [How To Use GaussianBlur_PPM](#HowToUseGaussianBlur_PPM)
	* [Intro](#Intro)
		* [BlurEffect.cs](#BlurEffect.cs)
		* [Postprocessing Layer and Postprocessing Volume](#PostprocessingLayerandPostprocessingVolume)

<!-- vscode-markdown-toc-config
	numbering=false
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc --> 

## Description Features

This is a blur effect that is achieved using Unity's Post Processing Method.

Since this uses the Post Processing Method it should be compatable with Unity's High Definition Render Pipeline (HDRP) and the Lightweight Render Pipeline (LWRP), however this is currently untested.

## How To Use GaussianBlur_PPM

### Intro

a gameObject will be set up with a special #C script that will create a texture that our camera will use to know which pixels it will need to blur.

This is how the demo looks

![Imgur](https://i.imgur.com/fuX6Fj9.png)

#### BlurEffect.cs
Attach this script to objects that you want to be blurred. 

This Script will create a texture where the pixels that should be blurred are more white then the pixels that should not be blurred.

![Imgur](https://i.imgur.com/Hs9cWUN.png)

#### Postprocessing Layer and Postprocessing Volume

Now we need to attach the Post Processing Layer and the Post Processing Volumne to our camera.

Then add the GaussianBlur_PPM to your Post Processing Profile.

![Imgur](https://i.imgur.com/Mvcr3WC.png)

> Note: if you don't have Post Processing installed you can get it from the menu (i.e. Window -> Package Manager -> Post Processing)



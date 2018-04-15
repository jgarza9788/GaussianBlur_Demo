 GaussianBlur_RenderBlur
-------------------------------------
[Asset Store Link](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!-- TOC -->

- [Table of Contents](#table-of-contents)
- [Description Features](#description-features)
- [How To Use GaussianBlur_RenderBlur](#how-to-use-gaussianblur_renderblur)
    - [Preface](#preface)
        - [BlurRenderer.cs](#blurrenderercs)
        - [GaussianBlur_RenderBlur.shader](#gaussianblur_renderblurshader)
    - [Troubleshooting](#troubleshooting)
        - [It's Blocky?](#its-blocky)
        - [I've got a ton of Errors!](#ive-got-a-ton-of-errors)
        - [Doesn't Do WorldSpace](#doesnt-do-worldspace)
        - [Jumpy Update](#jumpy-update)

<!-- /TOC -->


## Description Features

A GaussianBlur_RenderBlur effect for UI Components.

* Render a blurred texture(s) once and reuse it/them
* Adjust Blur and Lightness using C# or JS
* Add alpha mask for different shapes!
* Adjust Quality for mobile/low-end hardware
* Unity Free friendly.
* Fully commented C# code.
* Awesome demos!


>**WARNING!**  
I plan to rewrite this assset (or replace it with GaussianBlur_Mobile).  
Therefore, you will get an obsolete message when using this blur.

## How To Use GaussianBlur_RenderBlur

### Preface

**GaussianBlur_RenderBlur** (folder)  
Contains a Gaussian Blur shader(s), and script(s), that updates global textures when called on.
Call this "Render on Demand". This can be used for low-end devices when you don't need to update the blur every frame, or if you just want to be battery friendly.


#### BlurRenderer.cs

Below is a ScreenShot of the BlurRenderer.cs Script.

**MaxBlur**: the maxium blur used to make the global textures.  
**Quality**: the quality of the blur (the lower the better for mobile)  
**TextureCnt**: the number of global textures generated (5 max)  
**DownRes**: lowering the resolution of the image that is captured from the camera. (the highter the better for mobile).  
**RenderNow**: a trigger mostly used for debugging in the unity editor.  

![Imgur](http://i.imgur.com/QqZl5No.png)

#### GaussianBlur_RenderBlur.shader

Uses properties and the global textures to generate a blurred effect on the screen.

**_Lightnesss**: multiplies the color of the image to make it lighter, or darker.  
**_BlurSize**: A number between 0 and 1, in order to blender between each of the global textures (_Blur#).  
**_AlphaAsBlurSize**: Alpha in your image will be used to calculate the BlurSize.  

![Imgur](http://i.imgur.com/8h4rLRm.png)

Below is a diagram to convery how BlurSize is calculated.

* If BlurRenderer generated 5 textures.
	* If your BlurSize is 1, then _Blur4 will be used.
	* If your BlurSize is 0.5 then the shader will use a mix of _Blur1 and _Blur2.
	* If your BlurSize is 0.1 then the shader will used _Blur0 with an alpha of 0.5.

![Imgur](http://i.imgur.com/Tlrsep0m.png)


### Troubleshooting

#### It's Blocky?  
If the Shader seems blocky (like in the image below), increase the Quality value in the shader.

![Imgur](http://i.imgur.com/5xclyZ4m.png)

#### I've got a ton of Errors!

The Shaders written in Unity get recompiled into 8 different shaders for each rendering engine. Unfortunately  this shader doesn't work with DirectX9 (D3D9), therefore please disable it in the inspector.

![Imgur](http://i.imgur.com/weoBIhh.png)

If compiling for windows you can choose the graphical API in PlayerSettings
![Imgur](http://i.imgur.com/V909vba.png)

#### Doesn't Do WorldSpace

Sorry, but this method doesn't support WorldSpace canvasses.
*Please let me know if you want this and I will do my best.*

#### Jumpy Update

The blur effect will seem to jump a bit when the texture(s) are updated. (i.e. not a smooth update)
This is something i will be working on in the next few months.
*Let me know if this is a priotity*

>**WARNING!**  
In order to accomplish a fix for this this i might need to render more textures
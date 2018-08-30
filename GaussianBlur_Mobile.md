 GaussianBlur_Mobile
-------------------------------------
[Asset Store Link](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!-- TOC -->

- [Table of Contents](#table-of-contents)
- [Description Features](#description-features)
- [How To Use GaussianBlur_Mobile](#how-to-use-gaussianblur_mobile)
    - [Intro](#intro)
    - [Create or Update the Global Texture](#create-or-update-the-global-texture)
    - [Use the Global Texture](#use-the-global-texture)
- [Troubleshooting](#troubleshooting)
    - [Doesn't Do WorldSpace](#doesnt-do-worldspace)
    - [Jumpy Update](#jumpy-update)
    - [Blurring Other UI](#blurring-other-ui)

<!-- /TOC -->

## Description Features

A GaussianBlur effect for UI Components.

* Mobile Friendly
* Adjust Blur and Lightness using C# or JS
* Add alpha mask for different shapes!
* Unity Free friendly.
* Fully commented C# code.
* Awesome demos!

## How To Use GaussianBlur_Mobile

### Intro

**GaussianBlur_Mobile** (folder)  
Contains a Gaussian Blur shader(s), and script(s), that updates global textures when called on.  

Therefore there are two parts:  
1. a Script that creates or updates the global texture.
2. a Shader to use that global texture.


### Create or Update the Global Texture

You can set up the BlurRenderer using the Create() method. (Example below) 
~~~cs
//make sure to use GaussianBlur_Mobile
using GaussianBlur_Mobile;

public BlurRenderer BRM;

void Start()
{
	BR = BlurRenderer.Create();

	////or Add to the camera of your choice 
	//BR = BlurRenderer.Create(ThisCamera);
}

void Update() 
{
	//...

	//change how many Iterations
	BR.Iterations = (int)Iterations.value;

	//change DownRes number
	BR.DownRes = (int)DownRes.value;

	//turn UpdateBlur on or off
	BR.UpdateBlur = UpdateBlur.isOn;

	//change the update rate
	BR.UpdateRate = UpdateRate.value;

	/*NEW*/
	//you can now choose to use the gametime (i.e. deltaTime) or real time (i.e. unscaled time)
	BR.updateUsingGameTime = true

	//...
}

~~~

See **/Assets/GaussianBlur/GaussianBlur_Mobile/Demo/Scripts/DemoSliderControl.cs** for a more complete example.

An alternative method would be to add the BlurRenderer.cs to your main camera.

### Use the Global Texture

To use the global texture a material will be set up.  
One is already set up for the Demo. (i.e. DemoBlur.mat)  

1. You can create a new material by **Assets > Create > Material**  
2. And using the **Custom/GaussianBlur_Mobile** Shader.  
3. And Add this Material to your UI Image.

![Imgur](https://i.imgur.com/5aJb2D4m.png)  

![Imgur](https://i.imgur.com/bpOggyxm.png)

![Imgur](https://i.imgur.com/pB5K7Y4m.png)



## Troubleshooting

### Doesn't Do WorldSpace

Sorry, but this method doesn't support WorldSpace canvasses.
*Please let me know if you want this and I will do my best.*

### Jumpy Update

You might want to decrease the UpdateRate, or Lower the DownRes.  

### Blurring Other UI

Blurring other UI can be tricky.
The UI that should be blurred should be in the worldspace.
If this UI is transparent, please use the Sprites-Default material.
_See **Demo_OtherUI.scene** for example_
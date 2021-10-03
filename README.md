 GaussianBlur_URP
-------------------------------------
[Asset Store Link](http://u3d.as/1wQD)  
[HRP version](http://u3d.as/1EMR)  
[non-ShaderGraph version](http://u3d.as/yJk)  

© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)


## Table of Contents

<!-- TOC -->

- [GaussianBlur_URP](#gaussianblur_urp)
- [Table of Contents](#table-of-contents)
- [Contact](#contact)
- [Description Features](#description-features)
- [Set Up](#set-up)
- [GaussianBlur_IU](#gaussianblur_iu)
- [GaussianBlur_IUEffect](#gaussianblur_iueffect)
- [GaussianBlur_WS](#gaussianblur_ws)
- [Videos](#videos)
- [Terms of Use](#terms-of-use)
- [FAQs](#faqs)
    - [it's just GREY!](#its-just-grey)
    - [incorrect importing](#incorrect-importing)

<!-- /TOC -->

## Contact

Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [jgarza9788 - UnityPortfolio](https://github.com/jgarza9788/UnityPortfolio)  


## Description Features

* Alpha Mask
* Mobile Friendly
* Adjust Blur, Lightness, Saturation, and TintColor 
* Built on URP
* easily modifiable/editable Shader Graph
* 3 Shaders
    * GaussianBlur_IU
    * GaussianBlur_IUEffect
    * GaussianBlur_WS (WorldSpace, or Objects)

## Set Up
Use the URP_Asset  
it's in ***\GaussianBlur_URP\Assets\URP**

note: this will do several things.
1. Allow us to use _CameraOpaqueTexture (our default texture for blurring)
    1. a custom texture can be used (i.e. a render texture or any 2D texture)
2. Enable Custom rendering for WorldSpaced objects we want blurred.

![Imgur](https://i.imgur.com/B7s0p8Ls.png)

## GaussianBlur_IU
To use the shader on the UI, just use the material.  
(or create you're own material and use my shader)

CustomTexture:  
pass in any texture you'd like (i.e. a Render Texture or 2D Texture)

useCameraOpaqueTexture:  
this will be used as a default texture for blurring.  
note: this will not render transparent objects (you might want to use a Render Texture)

BlurScale:  
This is how much to blur the texture.  
(This will automatically adjust two other variables)

Lightness:  
how light or dark the UI should be.

Tint:  
a color tint to be applied to the UI.

Saturation:  
adjusts the saturation (color) of the UI.

![Imgur](https://i.imgur.com/CPsRJI8s.png)


## GaussianBlur_IUEffect
This will use the Source Image.
So you can fade the blur depending on where it is on the screen.

note:  
edges will be blurred, but less in the center  
![Imgur](https://i.imgur.com/vZ7FJoNs.png)

## GaussianBlur_WS
This is for Objects in the WorldSpace.

note: The Layer should be set to BlurObject.

Metallic & Smoothness:  
these are used to adjust the shinny-ness of the object.  

if this is not working we might want to double check our custom-renderer.
it's in ***\GaussianBlur_URP\Assets\URP**

![Imgur](https://i.imgur.com/X4vxYgks.png)  
![Imgur](https://i.imgur.com/isubyX3s.png)


## Videos
[GaussianBlur_UI](https://youtu.be/v11TBFgPKDE)  
[GaussianBlur_WS](https://youtu.be/lwK_AaKw4kc)    
[GaussianBlur_UIEffect](https://youtu.be/2delOzh9Wt8)

## Terms of Use

Required:
please follow [Unity's EULA](https://unity3d.com/legal/as_terms) 

Suggestion/Optional:
please put my name in the credits, or in the special thanks section. :)  

## FAQs

### it's just GREY!
Please delete the **Settings** folder from the default URP project.  
For some reason this causes an error in the URP_Asset i have included in the project

### incorrect importing 

I have receieved emails about the materials folder not being imported within the assets folder.

![Imgur](https://i.imgur.com/a7dzmU9.png)

### better performance from mobile 

1. use Vulkan 
    * this should be in the PlayerSettings, Other Settings, Rendering.

2. Increase the **Update Rate** in the BlurRenderer.cs script
    * this will update the blur less frequently, however if you are on a pause menu (or something similar) this will cut down on how often your blur is updating. 

3. Lower the quality toggle within the material settings.
    * this will change how it renders, however it should be lighter. 

 
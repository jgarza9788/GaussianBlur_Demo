 GaussianBlur
-------------------------------------
[Asset Store Link](http://u3d.as/yJk)  
[GaussianBlur+](http://u3d.as/1wQD)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)


## Table of Contents

 * [Table of Contents](#table-of-contents)
 * [Contact](#contact)
 * [Description Features](#description-features)
 * [Terms of Use](#terms-of-use)
 * [FAQs](#FAQs)

## Contact

Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.info/contact](http://justingarza.info/contact/)  
Alternate Website: [jgarza9788 - UnityPortfolio](https://github.com/jgarza9788/UnityPortfolio)  


## Description Features

1. [GaussianBlur_Live](https://github.com/jgarza9788/GaussianBlur_Demo/blob/master/GaussianBlur_Live.md)
	* Layered Blur
	* WorldSpace
	* Alpha Mask
	* Adjust Blur and Lightness
	* Quality setting (to use less resources)
	* Unity Free friendly
	* Fully commented C# code
	* Awesome demo
	* NOTE: This will not work with Scriptable Render Pipelines (LWRP/HDRP)
2. [GaussianBlur_Mobile](https://github.com/jgarza9788/GaussianBlur_Demo/blob/master/GaussianBlur_Mobile.md)
	* Alpha Mask
	* Mobile Friendly 
	* Adjust Blur, Lightness, Saturation, and TintColor
	* Works in ScreenSpace-Camera Mode 
	* Unity Free friendly
	* Fully commented C# code
	* Awesome demo
    * Additional DEMOS!  
        * Drop Glow
        * Drop Shadow
        * Pause/Play 
        * ScreenSpace Camera
        * Use with ScrollView
    * NOTE: This will not work with Scriptable Render Pipelines (LWRP/HDRP)
3. [GaussianBlur_CamTransition](https://github.com/jgarza9788/GaussianBlur_Demo/blob/master/GaussianBlur_CamTransition.md)
    * Blur and Transition between two Cameras
    * NOTE: This will not work with Scriptable Render Pipelines (LWRP/HDRP)
4. [GaussianBlur_PPM](https://github.com/jgarza9788/GaussianBlur_Demo/blob/master/GaussianBlur_PPM.md)
	* Alpha Mask
	* Mobile Friendly 
	* Adjust Blur, Lightness, Saturation, and TintColor
    * Layered Blur
    * WorldSpace
    * uses Unity's Post Processing Method
    * NOTE: This will not work with Scriptable Render Pipelines (LWRP/HDRP)
5. [GaussianBlur_SRP](https://github.com/jgarza9788/GaussianBlur_Demo/blob/master/GaussianBlur_SRP.md)
   * **(only in GaussianBlur+)**
   * Alpha Mask
   * Mobile Friendly 
   * Adjust Blur, Lightness, Saturation, and TintColor 
   * Compatable with Unity's Scriptable Rendering Pipelines 



## Terms of Use

You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section.  
please do not re-distribute.  

## FAQs
### better performance from mobile 

1. use Vulkan 
    * this should be in the PlayerSettings, Other Settings, Rendering.

2. Increase the **Update Rate** in the BlurRenderer.cs script
    * this will update the blur less frequently, however if you are on a pause menu (or something similar) this will cut down on how often your blur is updating. 

3. Lower the quality toggle within the material settings.
    * this will change how it renders, however it should be lighter. 


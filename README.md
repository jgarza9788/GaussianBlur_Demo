GaussianBlur
-------------------------------------
[Asset Store Link](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

Contact  
-------------------------------------
Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.net/contact](http://justingarza.net/contact/)
  
Description/Features
-------------------------------------
A GaussianBlur effect for UI Components.* Adjust Blur and Lightness using C# or JS
* Add alpha mask for different shapes!
* Adjust Quality for mobile/low-end hardware* Unity Free friendly.
* Fully commented C# code.
* Awesome demos!
Terms of Use
-------------------------------------
You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section. :)  
please do not re-distribute.  

Table of Contents 
-------------------------------------
1. How to Use
	* Create Material
	* Use Material
	* Change Material via Script
2. F.A.Q.s
	* What is edge smear? 
	* Why are there two shaders?
	* Why is it black?
	* Why is it blocky?


How to Use
-------------------------------------
####Create Material
Create a new material, name it as needed.  
Assign the GaussianBlur shader to it.

![Imgur](http://i.imgur.com/FFtSIYlm.png)

####Use Material
Assign the new material to an image within your canvas.

![Imgur](http://i.imgur.com/XIshcrMm.png)

Note: if you used GaussianBlurV2.shader make sure to add SyncCoordinates.cs to the same image in your canvas.

####Change Material via Script
This Shader has 5 properties.  

1. _Color  
 * This is the Tint Color of the shader.
 * For best uses maintain a low alpha.  
2. _BlurSize  
 * Amount of Blur
3. _Lightness  
 * How light/dark the material should be.
4. _Quality  
 * the Quality of the blur.
 * Use low number for mobile/low-end devices
5. _Reprocess
 * Reprocess the blur
 * (does not exist on GaussianBlurV2.shader)



**Examples:**

~~~cs  
//set the color
ScreenBlurLayer.SetColor("_Color",Color.red);
        
//set the BlurSize
ScreenBlurLayer.SetFloat("_BlurSize",30f);
     
//Set the Lightness   
ScreenBlurLayer.SetFloat("_Lightness",0.2f);

//Set the Quality
ScreenBlurLayer.SetFloat("_Quality",4.0f);

//Reprocess the Blur...true/false
ScreenBlurLayer.SetFloat("_Reprocess",1f); //true
ScreenBlurLayer.SetFloat("_Reprocess",0f); //false
~~~
 

Please see the DemoSliderControl.cs script for more information.

For more information about materials please see
https://docs.unity3d.com/ScriptReference/Material.html


F.A.Q.s
-------------------------------------
####What is edge smear?   
Edge Smear is the name of an issue where objects outside of the UI get smeared in from the edge and effect the blur. 

Edge Smear only occurs if you decided to use the GaussianBlurV1.shader

![Imgur](http://i.imgur.com/OGPs9vFm.png)

####Why are there two shaders? 

GaussianBlurV1.shader:  
Is my first attempt at this shader.
However, it suffers from the Edge Smear.

GaussianBlurV2.shader:  
Is my second attempt at this shader.
It doesn't suffer from the Edge Smear, however it needs more information to render properly. (see SyncCoordinates.cs for more info) 

![Imgur](http://i.imgur.com/kwOaR5Gm.png)

####Why is it black?
If GaussianBlurV2.shader is being used and the values like ScreenWidth, ScreenHeight, PanelWidth, PanelHeight..etc are not correct than the shader might render as black.

####Why is it blocky?  
If the Shader seems blocky (like in the image below), increase the Quality value in the shader.

![Imgur](http://i.imgur.com/5xclyZ4m.png)

####Still Not Working Correctly?
I have tested this script on the OSes and devices listed below.  

* IOS iPhone6s
* Android Nexus9
* OSX Macbook Pro
* Windows7(bootcamp) Macbook Pro 

Please understand that I couldn't test every graphics card, so if you have an error please feel free to reach out to me so we can try to solve it.




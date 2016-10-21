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
  
How to Use
-------------------------------------
####Create Material
Create a new material, name it as needed.  
Assign the GaussianBlur shader to it.

![Imgur](http://i.imgur.com/FFtSIYl.png)

####Use Material
Assign the new material to an image within your canvas.

![Imgur](http://i.imgur.com/XIshcrM.png)


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



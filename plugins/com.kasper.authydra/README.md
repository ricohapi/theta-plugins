English(US) | [日本語](README.ja.md)

# Authydra
Kasper Oerlemans  
[Privacy Policy](../../README.md#privacy-policy) | [Terms of Services](../../README.md#terms-of-services)

<div align="center">
 <img src="1.png">

 <table>
  <tr>
   <td><img src="2.png"></td>
   <td><img src="3.png"></td>
   <td><img src="4.png"></td>
   <td><img src="5.png"></td>
  </tr>
 </table>
</div>

[![Install on THETA](https://assets.ricoh360.com/image/upload/v1/front/theta/install-button.svg?)](https://link.ricoh360.com/plugins/com.kasper.authydra/apk)

***

## Description
VFX automatic HDR capture plugin  
  
A plugin for the RICOH THETA V and Z1 to make one HDR exr file. Main use would be for on set VFX HDR capture. With a simple web interface one can set the capture settings and download the EXR file (and original pictures if desired)  
  
One can choose the number of pictures taken, the number of pictures taken on each exposure to reduce noise and the exposure difference between each bracket (stop jumps, this can also be set to auto).  
  
There are enough HDR apps. What makes this one different?  
  
It measures the on set lighting and bases it bracketing on that lighting situation. It takes 1 auto exposed picture to determine basic exposure settings. Based on that it set the lowest iso and then starts taking pictures. Unfortunately very bright lights (like the sun) are still visible with lowest shutter times and iso. This maybe can be fixed on the Z1 with higher aperture.  
  
It automatically merges these pictures into one EXR file ready to be used in NUKE, MAYA etc. (this is done through OpenCV hdr libraries.)  
  
How to use?  
  
On the THETA V, make sure to set the plugin as the default plugin to use.  
  
Start the plugin by holding down the mode button for 2 seconds. The little led will turn white. And the wifi logo will turn Magenta.  
  
Put the camera on chosen location (use a tripod, shooting handheld will lead to crappy pictures) Now either push the photo button. You have 5 seconds to run away and hide, else you are in the picture. Or connect you phone/laptop/tablet/... to the wifi of the ricoh theta and goto http://192.168.1.1:8888 and choose your setting and press the take picture button.  
  
The Wifi logo turns greens and the theta makes pictures and optionally makes sounds. When using the webinterface you are taken to a page that shows the progress of the process, also there is a low res version of the pictures you are taking.  
  
After the picture taking the wifi logo will blink red and blue. You can now move or pick up the camera. It is busy merging the pictures. This takes about one or two minutes. When it is done it makes a sound and the wifi logo turn magenta again. The webinterface will return to the settings page.  
  
Use the web interface to download (and or delete) the pictures. You can view the jpg of picture in 360 by pressing the filename in the file manage menu.  
  
Good to know It tries to keep the iso as low as possible but also the the exposure time, when exposure gets above 1 sec, it increases iso (until it runs out of iso and then increases exposure time again ;-) .) This version works with OpenCV 3.4.4 I ran into to some problems with 4.0 which I couldn't fix right away. It also generates a tonemapped jpg, just for fun. Haven't been able to get this jpg to show up in the theta ios app. Don't know why maybe someone can help? If you want to build it for yourself make sure to change the file paths in the Android.mk file (in the app folder).  
  
Known Problems  
  
The black hole sun error. When there is a very bright element in your picture. That is still over exposed in the darkest picture this will give a black hole in the final EXR. I am looking into this problem. One would be to fix it as post compositing problem. Another onw would be to look better into the HDR merge algorithm and see what is happening there.  
Credits  
  
The picture taking part is largely based on the work of Ichi Hirota’s dual-fisheye plug-in https://github.com/theta360developers/original-dual-fisheye-plugin  
The integration of OpenCV is a combination of https://community.theta360.guide/t/ricoh-blog-post-running-opencv-in-your-ricoh-theta/4084 and https://www.learn2crack.com/2016/03/setup-opencv-sdk-android-studio.html and a lot of trail and error!  
The HDR part is based on https://www.learnopencv.com/high-dynamic-range-hdr-imaging-using-opencv-cpp-python/  
The view in 360 is done using the great kaleidoscope library https://github.com/thiagopnts/kaleidoscope by Thiago Pontes  
The hydra logo is from the free clipart site: https://publicdomainvectors.org/en/free-clipart/Hydra-dragon-vector-silhouette/75432.html  
The mergeHDR option is added by Zachary Burke  
Feel free to change, improve and of course use!  
  
Let me know what you think and run into!  
  
TODO v2.2  
fix black hole sun (either by comp or in merge function)  
z1 -> raw processing * ?dng support -> split in two exposures  
raw stichting with opencv  
z1 -> do something with display  
z1 -> aperture support  
z1 dng remove from zip??  
TODO ideas  
export default python script to recreate hdri offline?  
support opencv 4  
support tonemapped jpg in theta default app  
sRGB-> lin  
whitepoint  
total time calculator  
set auto off to 10 min  
  
  
## Information
  * Updated：2020/7/30
  * Version：2.1.1
  * Requires：
    * RICOH THETA Z1 (Firmware version 1.40.1)
    * RICOH THETA V (Firmware version 3.30.1)
  * Support：[Partner Plugins](https://community.theta360.guide/t/hdr-plugin-to-automatically-create-exr-file-for-vfx-use/4132/9)
  * Age Restriction：No

* The [RICOH THETA](https://theta360.com/ja/about/application/pc.html#app-detail-01) basic app for computer is required to install plugins

English(US) | [日本語](README.ja.md)

# Burst-IBL-Shooter
CGSLAB  
[Privacy Policy](../../README.md#privacy-policy) | [Terms of Services](../../README.md#terms-of-services)

<div align="center">
 <img src="1.png">

 <table>
  <tr>
   <td><img src="2.png"></td>
   <td><img src="3.png"></td>
   <td><img src="../../resources/common/img/noimg.png"></td>
   <td><img src="../../resources/common/img/noimg.png"></td>
  </tr>
 </table>
</div>

[![Install on THETA](https://assets.ricoh360.com/image/upload/v1/front/theta/install-button.svg?)](https://link.ricoh360.com/plugins/info.cgslab.burstiblshooter/apk)

***

## Description
Burst Capture Mode of Camera API is used.  
Seven shots are taken in ±3EV steps based on a -5EV offset from the auto exposure.  
Bracketed shots can be taken properly from dark indoors to bright outdoors.  
  
Pressing the Mode/Fn Button allows you to select between instant shooting and self-timer mode.  
Mode 1: Now Shoot: The picture is taken immediately.  
Mode 2: (3Sec)Sound SelfTimer: The picture will be taken after 3 seconds of self-timer sound. →♪P-P-P-PP>Shooting  
Mode 3: (7Sec)Sound SelfTimer: The picture will be taken after 7 seconds of self-timer sound. →♪P-P-P-P-P-P-P-P-P-P-P-P-P-P>Shooting  
  
Only RAW data (DNG) will be saved.  
After shooting, it takes about 20 seconds to write the image, but you can move the camera.  
At this time, the text "WRITEING .DNG FILE. CAN MOVE THETA. | Dont Shoot!"  
After writing is complete, the text "BURST-IBL-SHOOTER V1.1 | CAN SHOOT!" will be displayed and a write completion sound will sound, allowing the camera to resume shooting.  
*The state of the photo mode was taken just before.  
  
The data is saved in the Burst_IBL_Shooter folder, organized by date and time for easy data management.  
Depending on the shooting environment, duplicate images may be generated.  
  
Remote shooting is possible with the compatible Bluetooth Remote Control when used with the official remote control plug-in.  
  
There are no plans to internally convert to HDRI due to quality and processing time issues. See here for an ACES-compliant HDRI creation method. (JapaneseOnry)  
https://cgworld.jp/feature/202006-cgw262t1-tips02.html  

## What's New
1,Addition of self-timer mode.  
1-1. 4 types of self-timer functions have been added: 3 or 7 seconds + with or without self-timer sound.  
1-2. Press Mode/Fn Button to move to the next Mode.  
Mode 1: Now Shoot: The picture is taken immediately.  
Mode 2: (3Sec)Sound SelfTimer: The picture is taken after 3 seconds of self-timer sound. → ♪P-P-PP>Shoot  
Mode 3: (7Sec)Sound SelfTimer: The picture is taken after 7 seconds of self-timer sound. → ♪P-P-P-P-P-P-PP>Shoot  
*For the lowest value, it will go around. ex)1←→3  
  
2,Error Shooting prevention function.  
"DONT SHOOT!" will be displayed in the write status after shooting, and mode change and shooting button operation will be disabled.
When the camera moves to the state where "CAN SHOOT." is displayed after writing is completed, the camera can be operated again.  
  
3,Addition of writing completion sound.  
A completion sound is now emitted when writing is complete after shooting in all modes.  
When the shutter volume of THETA Z1 is turned off, the self-timer sound, shutter sound, and writing completion sound will be silent in all modes.  
  
4,Deprecation of remote controllers.  
The following problems may occur when using a Bluetooth remote controller.  
The self-timer count sound may not be generated when shooting.  
When shooting with the self-timer in mode 2 or 3, the connection with the Bluetooth remote controller is disconnected after shooting.  

## Information
  * Updated：2022/6/3
  * Version：1.1.0
  * Requires：
    * RICOH THETA Z1 (Firmware version 2.00.1)
  * Support：[Partner Plugins](http://site.cgslab.info/archives/929)
  * Age Restriction：No

* The [RICOH THETA](https://theta360.com/ja/about/application/pc.html#app-detail-01) basic app for computer is required to install plugins

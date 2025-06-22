English(US) | [日本語](README.ja.md)

# HDRI

Ricoh Company, Ltd.  
[Terms of Use](https://www.ricoh360.com/terms/plugins/)

<div align="center"><img src="./1.png"><table><tr><td><img src="./2.png"></td><td><img src="./3.png"></td><td><img src="./4.png"></td><td><img src="./5.png"></td></tr></table></div>

[![Install on THETA](https://assets.ricoh360.com/image/upload/v1/front/theta/install-button.svg?)](https://link.ricoh360.com/plugins/com.theta360.hdri/apk)

## Description

<div id="plugin-description">

This plug-in will create high dynamic range images (EXR) in the camera after bracket shooting.  
"Normally, to create high dynamic range images (EXR), it was necessary to perform the lengthy process of shooting an image with the camera and then editing it on a PC before creating EXR data. The HDRI plug-in enables you to use only THETA to simply press the shutter button once to perform the process from shooting to image editing.  
Created high dynamic range images contain information with a wide range of brightness difference. This allows you to use them for ambient lighting when creating CG and rendering, which enables you to reproduce shades of light so that it feels as though you are actually in the space where the image was taken."  
You can also shoot while watching the live preview on the smartphone.  

[How to operate the plug-in]  

- Starting the plug-in  

1. Set "HDRI" as an active plug-in from "Settings" - "Camera settings"- "Plug-in” in "RICOH THETA" basic app for the smartphone.
2. Press and hold the Mode button to activate the plug-in."


- Making shooting settings  

Seven types of settings can be made by the following operations.  
＜Camera operation＞  

* Pressing the WLAN button briefly: Sets the number of shots for bracket shooting. Each time the button is pressed, the setting value switches in the order of [7], [9], [11], and [13].  

* Pressing and holding the WLAN button: Sets whether to save RAW images. Each time the button is pressed and held, the setting switches between “Without RAW image saving” and “With RAW image saving”.  

* Pressing the Fn button briefly: Sets the EV step. Each time the button is pressed, the setting value switches in the order of [0.3], [0.7], [1.0], [1.3], [1.7], [2.0], [2.3], [2.7], and [3.0].  

* Pressing and holding the Fn button: Sets the shutter speed upper limit. Each time the button is pressed and held, the setting value switches in the order of [1/2], [1], [2], [4], [8], [15], [30], and [60].  

* Pressing the Mode button briefly: Sets the self-timer to save. Each time the button is pressed, the setting value switches in the order of [OFF], [2], [5], [10], and [15].  
  
＜WebUI setting screen＞  

Burst capture mode：[ON], and [OFF] can be selected.  

HDR file format：[OpenEXR(.exr)], [Radiance HDR(.hdr)] can be selected.  

* When burst capture is ON, the maximum number of shots is 9, and RAW saving is OFF. Burst capture is ON by default.  
* WebUI is the screen displayed on the browser when starting from the basic app for smartphone. Tap the gear icon in the upper right to display the settings screen.  
  

- Live preview display  

In the basic app for smartphone, select "Settings" - "Camera settings" - "Plug-in" - "HDRI", then tap the icon displayed next to "Starting plug-in".  
The browser is launched and the live preview is displayed.  

- Shooting  
Press the shutter button on the smartphone screen or the shutter button on the camera to start shooting.  
After “WAIT” is displayed, the set number of bracket shots are taken, and “MERGE” is displayed. When “MERGE” disappears, the data is saved.  

* When using Remote Control TR-1, activate the remote control before using this plug-in
* If the shutter upper limit (variable by setting) or lower limit (1/25000 seconds) is reached with the bracket, the set number of shots may not be reached.

- Retrieving shooting data  
Connect the camera to a computer with a USB cable, and retrieve each data from the following folders.  
  
[.exr file]  
DCIM/HDRI/YYYYMMDD_HHMMSS.exr  
  
[.hdr file]  
DCIM/HDRI/YYYYMMDD_HHMMSS.hdr  
  
[Bracket shooting result (original data of .exr file)]  
DCIM/HDRI/Bracket/YYYYMMDD_HHMMSS/YYYYMMDD_HHMMSS_N.JPG  
DCIM/HDRI/Bracket/YYYYMMDD_HHMMSS/YYYYMMDD_HHMMSS_N.DNG  

</div>

## What's New

<div id="plugin-whats-new">

* Speeding up image processing (merge processing)

* Fixed the problem that top/bottom correction does not work.

</div>

## Information

- Updated: 2023/7/25
- Version: 1.3.0
- Requires:
  - RICOH THETA Z1 (v2.11.1, v2.20.3, v2.30.1)
- Support: [RICOH Plugins](https://support.theta360.com/en/)
- Age Restriction: No

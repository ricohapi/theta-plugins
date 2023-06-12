[English(US)](README.md) | 日本語

# HDR2EXR
Kasper Oerlemans  
[プライバシーポリシー](../../README.ja.md#%E3%83%97%E3%83%A9%E3%82%A4%E3%83%90%E3%82%B7%E3%83%BC%E3%83%9D%E3%83%AA%E3%82%B7%E3%83%BC) | [利用規約](../../README.ja.md#%E5%88%A9%E7%94%A8%E8%A6%8F%E7%B4%84)

<div align="center">
 <img src="1.png">
 <table>
  <tr>
   <td><img src="../../resources/common/img/noimg.png"></td>
   <td><img src="../../resources/common/img/noimg.png"></td>
   <td><img src="../../resources/common/img/noimg.png"></td>
   <td><img src="../../resources/common/img/noimg.png"></td>
  </tr>
 </table>
</div>

[![Install on THETA](https://assets.ricoh360.com/image/upload/v1/front/theta/install-button.svg?)](https://link.ricoh360.com/plugins/com.kasper.hdr2exr/apk)

***

## 説明
HDR2EXR is a plug-in for RICOH THETA V to help visual special effects professionally easily grab lighting conditions on-set. Just by pressing the shutter button once, the HDR2EXR plug-in will take 11 bracketed pictures and merge them to one HDR file. The main use is intended for on-set VFX HDR capture.  
  
Details  
HDR2EXR measures on-set lighting conditions and bases bracketing on that specific lighting situation. It first takes 1 auto exposed picture to determine basic exposure settings. Based on that information, it sets the lowest ISO and then starts taking pictures.
For each bracket it takes 3 pictures and averages them together to reduce noise. It takes 11 brackets with a 2.5 stop increase. This should be enough to capture almost every lighting situation. Unfortunately, very bright light (like the sun) is still visible with lowest shutter times and ISO. This maybe can be fixed on the new RICOH THETA Z1 with higher aperture settings. This version of the HDR2EXR plug-in does not work with the Z1.  
Finally, HDR2EXR automatically merges those 11 pictures into one EXR file ready to be used in NUKE, MAYA, etc. Creation of the EXR file is done by utilizing OpenCV HDR libraries.  
  
  
How to use?  
Make sure to set the plugin as the default plugin to use.  
  
Start the plug-in by holding down the Mode button for 2 seconds. The little LED will turn white. And the Wi-Fi LED will turn Magenta.
Place the camera in the chosen location (use a tripod, shooting handheld will lead to crappy pictures) and push the shutter button. You have 5 seconds to run away and hide, else you are in the picture.  
The Wi-Fi LED will turn green and the THETA will make picture taking sounds. It takes 34 pictures (1 to measure lighting and 3 times 11 brackets).  
After the picture taking the Wi-Fi LED will blink red and blue. You can now move or pick up the camera. It is busy merging the pictures. This takes about 1-2 minutes. When it is done it will make a sound and the Wi-Fi LED will turn Magenta again.
Connect the THETA to a computer to download the pictures.  
  
Good to Know  
After running the plug-in, you may need to reboot your camera. The new files may not show up properly on Windows or Mac without rebooting.  
  
In order to be copied and moved over to Windows, the EXR file is first created with a .JPG extension. It comes in this format: “EXRFILER05071408_removethis.JPG”. On Windows, using File Manager, copy over to your computer and then change the extension to .EXR. On a Mac, use the app Image Capture. Both the EXR file and the “EXRFILER05071408_removethis.JPG” will be available to copy over.  
The default sleep setting for THETA is often 3 minutes. You should use the RICOH THETA mobile app to set sleep to OFF.  
HDR2EXR tries to keep the ISO as low as possible but also the exposure time. When exposure gets above 1 sec, it increases the ISO until it runs out of ISO and then increases exposure time again. ;-)  
This version works with OpenCV 3.4.4. I ran into to some problems with 4.0 which I couldn't fix right away. It also generates a tonemapped jpg, just for fun. I haven't been able to get this jpg to show up in the THETA iOS app. Don't know why, maybe someone can help?
If you want to build it for yourself make sure to change the file paths in the Android.mk file (in the app folder).  
  
Credits  
The picture taking part is largely based on the work of Ichi Hirota’s dual-fisheye plug-in https://github.com/theta360developers/original-dual-fisheye-plugin  
The integration of OpenCV is a combination of https://community.theta360.guide/t/ricoh-blog-post-running-opencv-in-your-ricoh-theta/4084 and https://www.learn2crack.com/2016/03/setup-opencv-sdk-android-studio.html and a lot of trail and error!  
The HDR part is based on https://www.learnopencv.com/high-dynamic-range-hdr-imaging-using-opencv-cpp-python/  
Feel free to change, improve and of course use!  
Let me know what you think and run into!  
  
  
## 新機能
Supports RICOH THETA V firmware 3.00.1

## 情報
  * 更新日：2019/6/14
  * バージョン：1.0.2
  * 要件：
    * RICOH THETA V （ファームウェア バージョン 2.50.1,3.00.1）
  * サポート：[Partner Plugins](https://community.theta360.guide/t/hdr-plugin-to-automatically-create-exr-file-for-vfx-use/4132)
  * 年齢制限：なし

* プラグインをインストールするにはパソコン用基本アプリ [RICOH THETA](https://theta360.com/ja/about/application/pc.html#app-detail-01) が必要です

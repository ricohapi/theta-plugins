[English(US)](README.md) | 日本語

# HDRI
Ricoh Company, Ltd.  
[利用規約](https://theta360.com/en/legal/terms_of_use_plugins/)

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

[![Install on THETA](https://assets.ricoh360.com/image/upload/v1/front/theta/install-button.svg?)](https://link.ricoh360.com/plugins/com.theta360.hdri/apk)

***

## 説明
本プラグインはブラケット撮影後にカメラ内で高ダイナミックレンジ画像（EXR）を生成します。  
通常、高ダイナミックレンジ画像（EXR）を生成するには、カメラで撮影した後、PCで画像編集し、EXRデータを生成するという手間がかかるものでした。HDRIプラグインでは1回シャッターを切っただけで、撮影から画像編集まで、THETA単体で行うことができます。生成された高ダイナミックレンジ画像は幅広い輝度差の情報を持っているので、CGやレンダリング作成時の環境光としてご活用いただくと、まるでその空間にいるかのような光の陰影を再現することができます。  
なお、スマートフォンからライブプリビューを見ながら撮影することもできます。  
  

[操作方法]  
- 起動  
スマートフォン用基本アプリから「設定」-「カメラ設定」-「プラグイン」で「HDRI」を選択。「プラグインを起動」ボタンを押す。  
または  
スマートフォン用基本アプリでプラグインを「HDRI」に選択した後、THETA本体のModeボタン長押しする。  

- 撮影設定  
以下の操作で、7種類の設定が行えます。  

＜カメラ本体操作＞  
* 無線LANボタン短押し：ブラケット枚数を指定します。操作するたびに[7,9,11,13]と順に設定が切り替わります。
* 無線LANボタン長押し：RAW保存の有無を指定します。操作するたびに、RAW保存なしとRAW保存ありの設定が切り替わります。
* Fnボタン短押し：EVステップを指定します。操作するたびに[0.3, 0.7, 1.0, 1.3, 1.7, 2.0, 2.3, 2.7, 3.0]と順に設定が切り替わります。
* Fnボタン長押し：シャッター速度上限を指定します。操作するたびに[1/2, 1, 2, 4, 8, 10, 30, 60]と順に設定が切り替わります。
* Modeボタン短押し：セルフタイマー設定を指定します。操作するたびに[OFF, 2, 5, 10, 15]と順に設定が切り替わります。

＜WebUIの設定画面＞
Burst capture mode：[ON/OFF]を選択できます。  

HDR file format：[OpenEXR(.exr)/Radiance HDR(.hdr)]を選択できます。  

* バースト撮影がONの場合、撮影枚数は最大9枚、Raw保存はOffになります。初期値はバースト撮影ONです。
* WebUIはスマートフォン用基本アプリから起動した時に、ブラウザに表示される画面です。 右上の歯車マークをタップすると設定画面が表示されます。
  

- ライブプリビュー表示

スマートフォン用基本アプリから「設定」 -「カメラ設定」-「プラグイン」で「HDRI」を選択後、「プラグイン起動中」の横に表示されているアイコンをタップ。  
ブラウザが起動し、ライブプリビューが表示される。  

- 撮影
スマートフォン画面、または、カメラのシャッターボタンを押すと撮影が開始されます。  
「WAIT」の表示のあと、指定した回数のブラケット撮影が行われ、「MERGE」の表示が消えるとデータが保存されます。  

* リモートコントロールTR-1をご利用の際には、本プラグインを起動前にペアリングを済ませてください。
* ブラケットでシャッター上限（設定で可変）もしくは下限（1/25000秒）に達した場合は指定した撮影回数にならない場合があります。

- 撮影データの取り出し  
カメラをUSBケーブルでPCに接続し、以下のフォルダから各データを取り出してください。  

[.exrファイル]  
DCIM/HDRI/YYYYMMDD_HHMMSS.exr  
  
[.hdrファイル]  
DCIM/HDRI/YYYYMMDD_HHMMSS.hdr  
  
[ブラケット撮影結果(.exrの元データ)]  
DCIM/HDRI/Bracket/YYYYMMDD_HHMMSS/YYYYMMDD_HHMMSS_N.JPG  
DCIM/HDRI/Bracket/YYYYMMDD_HHMMSS/YYYYMMDD_HHMMSS_N.DNG  

## 新機能
* バースト撮影に対応  
ただし、バースト撮影時は最大9枚、Raw保存はOffになります。初期値はバースト撮影ONとなります。

* 画像処理（マージ処理）の高速化

* WebUIに以下項目の設定画面を追加
  * バースト撮影 [ON/OFF]
  * HDRファイル形式 [OpenEXR(.exr)/Radiance HDR(.hdr)]

* Modeボタンで設定できる項目を、「HDRファイル形式設定」から「セルフタイマー設定」に変更

* 設定値の記憶に対応

* シャッター速度上限に15, 30, 60秒を追加

* EXRファイルの保存形式を以下のように変更  
RGB 16ビット 圧縮なし（V1.1以前は32ビット 圧縮あり）

* EVのステップ幅を広げた際にノイズ（赤、青、白など）が発生する問題を修正

## 情報
  * 更新日：2023/4/10
  * バージョン：1.2.0
  * 要件：
    * RICOH THETA Z1 （ファームウェア バージョン 2.11.1）
  * サポート：[RICOH Plugins](https://support.theta360.com/ja/)
  * 年齢制限：なし

* プラグインをインストールするにはパソコン用基本アプリ [RICOH THETA](https://theta360.com/ja/about/application/pc.html#app-detail-01) が必要です

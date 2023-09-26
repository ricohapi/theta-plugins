[English(US)](README.md) | 日本語

# HDRI-X
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

[![Install on THETA](https://assets.ricoh360.com/image/upload/v1/front/theta/install-button.svg?)](https://link.ricoh360.com/plugins/com.theta360.hdri_x/apk)

***

## 説明
本プラグインはTHETA X用のプラグインです。THETA Z1用のプラグインは以下URLになります。  
https://github.com/ricohapi/theta-plugins/blob/main/plugins/com.theta360.hdri/README.ja.md  
  

本プラグインはブラケット撮影後にカメラ内で高ダイナミックレンジ画像（EXR）を生成します。  
通常、高ダイナミックレンジ画像（EXR）を生成するには、カメラで撮影した後、PCで画像編集し、EXRデータを生成するという手間がかかるものでした。HDRIプラグインでは1回シャッターを切っただけで、撮影から画像編集まで、THETA単体で行うことができます。生成された高ダイナミックレンジ画像は幅広い輝度差の情報を持っているので、CGやレンダリング作成時の環境光としてご活用いただくと、まるでその空間にいるかのような光の陰影を再現することができます。  
なお、スマートフォンからライブプリビューを見ながら撮影することもできます。  
  

[操作方法]  
- 起動  
スマートフォン用基本アプリから「設定」-「カメラ設定」-「プラグイン」で「HDRI-X」を選択。  
または  
カメラの撮影画面で左方向にスワイプしてプラグイン選択画面を表示し、「HDRI-X」をタップします。  

- 撮影設定  
カメラの画面に表示されているメニューから5種類の設定が行えます。  
  
  BRAKET : ブラケット枚数を指定します。[7,9,11,13]を選択できます。  
EV STEP : EVステップを指定します。[0.3, 0.7, 1.0, 1.3, 1.7, 2.0, 2.3, 2.7, 3.0]を選択できます。  
ST : セルフタイマー設定を指定します。[OFF, 2, 5, 10, 15]を選択できます。  
SS<= : シャッター速度上限を指定します。[0.5, 1.0, 2.0, 4.0, 8.0, 15.0, 30.0, 60.0]を選択できます。  
FORMAT : HDR file formatを指定します。[EXR, HDR]を選択できます。  
  
  *THETA Xは、RAW保存、バースト撮影に対応していません。 
  

- スマートフォンへのライブプリビュー表示  
スマートフォン用基本アプリから「設定」 -「カメラ設定」-「プラグイン」で「HDRI」を選択後、「プラグイン起動中」の横に表示されているアイコンをタップ。  
ブラウザが起動し、ライブプリビューが表示される。  

- 撮影  
スマートフォン画面、または、カメラのシャッターボタンを押すと撮影が開始されます。  
「wait」の表示のあと、指定した回数のブラケット撮影が行われ、「merge」の表示が消えるとデータが保存されます。  
  
  *リモートコントロールTR-1をご利用の際には、本プラグインを起動前にペアリングを済ませてください。  
*ブラケットでシャッター上限（設定で可変）もしくは下限（1/16000秒）に達した場合は指定した撮影回数にならない場合があります。
  
- 撮影データの取り出し  
microSDXCカードを抜いた状態で、カメラをUSBケーブルでPCに接続し、以下のフォルダから各データを取り出してください。  
  
  *本プラグインはmicroSDXCカードへの保存に対応していません。microSDXCを挿入した状態で撮影しても、画像は全て内蔵メモリに保存されます。  
  
[.exrファイル]  
DCIM/HDRI/YYYYMMDD_HHMMSS.exr  
  
[.hdrファイル]  
DCIM/HDRI/YYYYMMDD_HHMMSS.hdr  
  
[ブラケット撮影結果(.exrの元データ)]  
DCIM/HDRI/Bracket/YYYYMMDD_HHMMSS/YYYYMMDD_HHMMSS_N.JPG  

## 情報
  * 更新日：2023/9/25
  * バージョン：1.0.0
  * 要件：
    * RICOH THETA X （ファームウェア バージョン 2.20.1,2.21.0）
  * サポート：[RICOH Plugins](https://support.theta360.com/ja/)
  * 年齢制限：なし

* プラグインをインストールするにはパソコン用基本アプリ [RICOH THETA](https://theta360.com/ja/about/application/pc.html#app-detail-01) が必要です

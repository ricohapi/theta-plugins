[English(US)](README.md) | 日本語

# Burst-IBL-Shooter
CGSLAB  
[利用規約](http://site.cgslab.info/archives/929)

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

## 説明
このプラグインは、VFXで使用するIBL(HDRI)作成用のブラケット撮影を1秒未満で行なえます。  
設定不要でほぼ全てのライティング環境に対応でき、明るい環境では、手持ち撮影も可能です。  
  
Camera APIのBurst Capture Modeを使用してます。  
自動露出から-5EVオフセットを基準に±3EVステップで7枚撮影されます。  
暗い屋内から明るい屋外まで、ブラケット撮影を適切に行うことができます。  
  
Mode/Fn Buttonを押すことで即撮影とセルフタイマーモードを選択できます。  
モード1：Now Shoot：即座に撮影が行われます。  
モード2：(3Sec)Sound SelfTimer：3秒間のセルフタイマー音の後に撮影されます。→♪P-P-PP>撮影  
モード3：(7Sec)Sound SelfTimer：7秒間のセルフタイマー音の後に撮影されます。→♪P-P-P-P-P-P-PP>撮影  
  
RAWデータ(DNG)のみの保存となります。  
撮影後、画像の書き込みに20秒程度かかりますが、カメラを動かしても問題ありません。  
この際に「WRITEING .DNG FILE. CAN MOVE THETA. | Dont Shoot!」の文章が表示されます。  
書き込み完了後に「BURST-IBL-SHOOTER V1.1 | CAN SHOOT!」の文章が表示され書き込み完了音が鳴り再撮影が可能になります。  
※直前の撮影モードの状態になっています。  
  
Burst_IBL_Shooterフォルダに日時でフォルダ分けして保存されるためデータの管理が行いやすいです。  
撮影環境によって重複設定で撮影された画像が生成される場合があります。  
  
公式のリモートコントロールプラグインとの併用で対応のBluetooth Remote Controlで遠隔撮影が可能です。  
  
品質や処理時間の問題から、内部でHDRIに変換する予定はありません。ACESに準拠したHDRIの作成方法はこちらをご覧ください。(日本語のみ)  
https://cgworld.jp/feature/202006-cgw262t1-tips02.html


## 新機能
1.セルフタイマーモードの追加。
1-1. 3または7秒＋セルフタイマーサウンド有無の4種類のセルフタイマー機能が追加されました。  
1-2. Mode/Fn Buttonを押すことで次のModeへ移行します。  
モード1：Now Shoot：即座に撮影が行われます。  
モード2：(3Sec)Sound SelfTimer：3秒間のセルフタイマー音の後に撮影されます。→♪P-P-PP>Shoot  
モード3：(7Sec)Sound SelfTimer：7秒間のセルフタイマー音の後に撮影されます。→♪P-P-P-P-P-P-PP>Shoot  
※最上下値の場合、一周します。1←→3  
   
2.誤撮影防止機能。  
撮影後の書き込み状態では「DONT SHOOT!」が表示され、モード変更及び撮影ボタンの操作は無効になります。  
書き込み完了後の「CAN SHOOT.」が表示された状態に移行した場合、再度操作可能になります。  
  
3.書き込み完了音の追加。  
すべてのモードでの撮影後の書き込みが完了時、書き込み完了音が鳴るようになりました。  
THETA Z1のシャッター音量をOFFにしている場合はすべてのモードでセルフタイマー音、シャッター音、書き込み完了音は無音となります。  
  
4.リモートコントローラの非推奨  
Bluetoothリモートコントローラを使用した場合に以下の問題が発生する場合があるため非推奨とします。  
・撮影時にセルフタイマーのカウント音が発生しない場合がある。  
・モード2/3でのセルフタイマー撮影をした場合、Bluetoothリモートコントローラとの接続が撮影後に切断される。  

## 情報
  * 更新日：2022/6/3
  * バージョン：1.1.0
  * 要件：
    * RICOH THETA Z1 （ファームウェア バージョン 2.00.1）
  * サポート：[Partner Plugins](http://site.cgslab.info/archives/929)
  * 年齢制限：なし

* プラグインをインストールするにはパソコン用基本アプリ [RICOH THETA](https://theta360.com/ja/about/application/pc.html#app-detail-01) が必要です

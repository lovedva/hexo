---
title: Install OS
---
## Install OS
2017.10.26  

### #1 公式サイトでOSファイルをダウンロードする
デスクトップ付けのZIPフィルをダウンロードする：  
https://www.raspberrypi.org/downloads/raspbian/  
![](/assets/2/20171026-8d0ba183.png)   

7-Zip（圧縮・解凍ソフト）Download：  
https://sevenzip.osdn.jp/
### #2 Win32 Disk Imagerをインストールする
Win32 Disk Imager[^1] このプログラムは、RAWディスクイメージをリムーバブルデバイスに書き込むか、もしくはリムーバブルデバイスをRAWイメージディスクにバックアップすることに設計されています。  

Download：  
https://sourceforge.net/projects/win32diskimager/
### #3 OSファイルをSDカードに書き込む
##### 1.ZIPファイルを解凍する
解凍ソフトがない場合は「7-Zip」をインストールしてください。  
ZIPファイルを解凍して、OSのディスクイメージファイル[^2]（IMGファイル）を得る。  
![](/assets/2/20171026-15b75cf2.png)  

##### 2.OSファイルをSDカードに書き込む
Win32 Disk Imagerを使ってイメージファイルを書き込む。  
![](/assets/2/20171101-f3539aac.png)　　

イメージファイルとSDカードのドライブを選択して、「Write」をクリックすると書き込みが開始される。  
![](/assets/2/20171101-c5219866.png)  
書き込みが終わったら、OSのインストールが完了する。

[^1]:Win32 Disk Imagerの説明： https://ja.osdn.net/projects/sfnet_win32diskimager/    
[^2]:イメージファイルとは　 https://www.gigafree.net/faq/word/imgfile.html

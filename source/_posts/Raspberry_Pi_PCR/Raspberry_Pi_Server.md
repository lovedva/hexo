---
title: Raspberry Pi Serverの説明
---
[TOC]
## RasPiのAP/NATとサーバーの構築(RasPiをアクセスポイント/NATとして使う)
#### 1．アクセスポイント（Wireless LAN access point）とは
ノートパソコン・スマートフォンなどの無線LANクライアント（無線端末）を、相互に接続したり、他のネットワーク（有線LAN等）に接続する無線機の一種。   
有線LANに接続すると，無線WiFiを作ること(シェア)ができます。  

#### 2．NAT（Network Address Translation）とは
インターネットプロトコルによって構築されたコンピュータネットワークにおいて、パケットヘッダに含まれるIPアドレスを、別のIPアドレスに変換する技術である。   
ルーターから割り当てもらったIPアドレスを他のIPアドレスを変換する。  
メリットは，異なるIPアドレスが割り当てられても，RasPiが作ったWiFiに接続するクライアント設備に対して，RasPiのIPアドレスは変わらない。  
#### 3．RasPi Server
** Wifiに接続 --> RasPiサーバーをアクセス(固定IP) --> ホームページでRasPiの情報が見える。 **    
RasPiを有線LANに接続するとホットスポットとして使う可能。  
スタンドアロンネットワーク(Local Network)でも動く。  
RasPi自体がLANケーブルが差し込まれていなくても，Wifi信号を送信する。ただしこの場合は，このWifiに接続する設備はインターネットには繋がってない。RasPiを中心で作られたローカルネットワークの中で，RasPiサーバーをアクセスして，ホームページを見ることができる。  

#### 4.RasPiのAPに接続
```
SSID：Pi-Server  
Password：12345678
```

#### 5.RasPiのサーバーをアクセス
次のIPをブラウザーで開く  
```
192.168.4.1:5000
```
HelloWorldが出たら成功。

## このページを快速アクセス
#### 本ページのURL：
` https://tiger-dog.coding.me/wiki/RaspberryPiの初期設定と使い方%20←/Raspberry_Pi_Server/ `

#### 快速アクセス：

1．`https://lovedva.github.io` にアクセス。    

<img src="http://q48hgww4y.bkt.clouddn.com/markdown-img-paste-20200123234746879.png"  align='left' />
  <br>
　<br> 　<br>

2．左側の「Raspberry_Pi_PCR←」を選択。  

<img src="http://q48hgww4y.bkt.clouddn.com/markdown-img-paste-20200123235112504.png" align='left'/>   　


3．「Raspberry Pi Serverの説明」を選ぶ。  

<img src="http://q48hgww4y.bkt.clouddn.com/markdown-img-paste-20200123235214715.png"  style='left'/>  　　

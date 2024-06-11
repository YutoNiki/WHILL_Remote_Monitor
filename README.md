# WHILL_Remote_Monitor
位置情報をなんやかんやするやつ

## 依存関係

- ハードウェア
  - [Raspberry Pi 4 Model B](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/)
  - [SANWA SUPPLY CMS-V53BK ウェブカメラ](https://www.sanwa.co.jp/product/syohin?code=CMS-V53BK)
- ソフトウェア
  - [WebRTC Native Client Momo](https://github.com/shiguredo/momo)

## 導入手順

### 0 注意事項

1. Raspberry Pi に Raspberry Pi OS はインストール済みとします。
2. Raspberry Pi のローカル IP アドレスは「192.168.255.10」が割り当てられていることを前提としています。  
   （研究室で立てたローカルのAPです。）

### 1 WebRTC Native Client Momo の導入

次の 2 つの公式ドキュメントに従って、WebRTC Native Client Momo を Raspberry Pi に導入・動作確認します。

- [Raspberry Pi (Raspberry-Pi-OS) で Momo を使ってみる](https://github.com/shiguredo/momo/blob/develop/doc/SETUP_RASPBERRY_PI.md)
- [テストモードを利用して Momo を動かしてみる](https://github.com/shiguredo/momo/blob/develop/doc/USE_TEST.md)

WebRTC Native Client Momo のバイナリおよび関連ファイルは /home/pi/mimamori 下に展開しておきます。


## 使い方

Raspberry Pi と同じローカルエリアネットワークに接続されているデバイスから http://192.168.0.100:8080/html/mimamori.html にアクセスします。  
画面右上「接続」ボタンを押して、ストリーミングを開始します。  
また、画面右上「昼モード」、「夜モード」ボタンを押して、カメラの設定を切り替えます。  
さらに、画面右上「画面キャプチャ」ボタンを押して、Web カメラの画像を指定した LINE のトークルームに送信します。

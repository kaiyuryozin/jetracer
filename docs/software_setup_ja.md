
# ソフトウェア設定

これらのステップを終えた後、あなたはすべてJetRacerをプログラムする準備ができているでしょう。終了したら、 [例に沿って](examples_ja.md)実行してください。

## ステップ1  - フラッシュマイクロSDカード
1.  JetCard SDカードのイメージ[jetcard_v0p0p0.img](https://drive.google.com/open?id=1wXD1CwtxiH5Mz4uSmIZ76fd78zDQltW_)をWindows、Linux、またはMacのデスクトップマシンにダウンロードします。

> あなたはこの[md5sum](https://drive.google.com/open?id=1356ZBrYUWaTgbV50UMB1uCfWrNcd6PEF)に対してそれをチェックすることができます

1. デスクトップマシンに32GB + SDカードを挿入してください
1. 使用する[エッチング装置は、](https://www.balena.io/etcher/)選択`jetcard_v0p0p0.img`し、SDカードにそれをフラッシュ
1. デスクトップマシンからSDカードを取り出す

> あらかじめ作成されたSDカードのパスワードは`jetson`

## ステップ2  - 電源を入れてUSB経由で接続する
1. 設定したSDカードをJetson Nanoモジュールに挿入します
1.  USBバレルプラグアダプターをUSBバッテリーパックに差し込んで電源を入れる
1.  Windows、Linux、またはMacマシンをマイクロUSB経由でJetson Nanoに接続します。
1.  Windows、Linux、またはMacマシンでブラウザを開き、 `192.168.55.1:8888`移動します。
1. デフォルトのパスワード`jetson`を使ってサインインする

## ステップ2  -  JetRacerをWiFiに接続する
1.  Jupyter Labで`File` - > `New` - > `Terminal`クリックしてターミナルを開き`File`
1. 端末で、次のコマンドを入力して利用可能なWiFiネットワークを一覧表示し、ネットワークの`ssid_name`を見つけます。

```
sudo nmcli device wifi list
```

1. 選択したWiFiネットワークに接続する

>それはあなたがからウェブプログラミングされるのと同じネットワーク上にあるべきです

```
sudo nmcli device wifi connect <ssid_name> password <password>
```

1. 次のコマンドで返されたWiFiインタフェース`wlan0`のWiFi IPアドレス（ `inet` ）を書き留めます。これを`jetson_ip_address`と呼びます。

```
ifconfig
```

## ステップ4  -  WiFi経由でJetRacerに接続する
1. マイクロUSBケーブルをJetson Nanoから取り外します
1. 前のJupyter Labブラウザタブを閉じます
1. 新しいブラウザタブを開き、 `http://<jetson_ip_address>:8888`移動し`http://<jetson_ip_address>:8888`
1. パスワード`jetson`サインイン

## ステップ5  -  Pythonパッケージをインストールする

>  Jetson Nanoがインターネットに接続されていることを確認してください

1. ターミナルを開き、以下を呼び出して[JetCam](http://github.com/NVIDIA-AI-IOT/jetcam) Pythonパッケージをインストールして[ください](http://github.com/NVIDIA-AI-IOT/jetcam) 。

```
cd $HOME git clone https://github.com/NVIDIA-AI-IOT/jetcam
cd jetcam sudo python3 setup.py install
```

1. 以下のコマンドを実行して、 [torch2trt](http://github.com/NVIDIA-AI-IOT/torch2trt) Pythonパッケージをインストールして[ください。](http://github.com/NVIDIA-AI-IOT/torch2trt)

```
cd $HOME git clone https://github.com/NVIDIA-AI-IOT/torch2trt
cd torch2trt sudo python3 setup.py install
```

1. ターミナルで以下を実行して[JetRacer](http://github.com/NVIDIA-AI-IOT/jetracer)パッケージをインストールして[ください。](http://github.com/NVIDIA-AI-IOT/jetracer)

```
cd $HOME git clone https://github.com/NVIDIA-AI-IOT/jetracer
cd jetracer sudo python3 setup.py install
```

## ステップ6  -  Jetson Nanoを5Wモードに設定する

 Jetson Nanoがバッテリーが供給できるよりも多くの電力を引き出すのを防ぐために、5Wモードに設定します。
1. 端末を開き、以下を呼び出して5Wモードを設定します

```
sudo nvpmodel -m1
```

## 次

次に、 [例を](examples.md)実行していきます。

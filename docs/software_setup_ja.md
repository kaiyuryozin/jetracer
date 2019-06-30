
# ソフトウェア設定

このステップを終えたら、JetRacerをプログラムする準備は万端です。完了したら、次は[制作例](examples_ja.md)に沿って進めてください。

## ステップ1  - マイクロSDカードの書き込み
1.  JetCard SDカードのイメージ[jetcard_v0p0p0.img](https://drive.google.com/open?id=1wXD1CwtxiH5Mz4uSmIZ76fd78zDQltW_)をWindows、Linux、またはMacのデスクトップマシンにダウンロードする

> [md5sum](https://drive.google.com/open?id=1356ZBrYUWaTgbV50UMB1uCfWrNcd6PEF)を確認できます

1. デスクトップマシンに32GB以上の容量があるSDカードを挿入する
1. [Etcher](https://www.balena.io/etcher/)を使って、`jetcard_v0p0p0.img`を選択し、SDカードに書き込む
1. デスクトップマシンからSDカードを取り出す

> あらかじめ作成されたSDカードのデフォルトパスワードは`jetson`

## ステップ2  - 電源を入れてUSB経由で接続する
1. 設定したSDカードをJetson Nanoモジュールに挿入する
1.  USBバレルプラグアダプターをUSBバッテリーパックに差し込んで電源を入れる
1.  Windows、Linux、またはMacマシンをマイクロUSB経由でJetson Nanoに接続する
1.  Windows、Linux、またはMacマシンでブラウザを開き、 `192.168.55.1:8888`移動する
1. デフォルトパスワード`jetson`を使ってサインインする


## ステップ2  -  JetRacerをWiFiに接続する

1.  Jupyter Labで`File` - > `New` - > `Terminal`クリックしてターミナルを開き`File`
1. 端末で、次のコマンドを入力して利用可能なWiFiネットワークを一覧表示し、ネットワークの`ssid_name`を見つける

```
sudo nmcli device wifi list
```

1. 選択したWiFiネットワークに接続する

> ウェブブラウザからプログラミングする時に接続するネットワークと、同一ネットワークに所属させます

```
sudo nmcli device wifi connect <ssid_name> password <password>
```

1. 次のコマンドで返されたWiFiインタフェース`wlan0`のWiFi IPアドレス（ `inet` ）を書き留める。これを`jetson_ip_address`と呼ぶ

```
ifconfig
```

## ステップ4  -  WiFi経由でJetRacerに接続する
1. マイクロUSBケーブルをJetson Nanoから取り外す
1. 前のJupyter Labブラウザタブを閉じる
1. 新しいブラウザタブを開き、 `http://<jetson_ip_address>:8888`移動し`http://<jetson_ip_address>:8888`
1. パスワード`jetson`サインイン

## ステップ5  -  Pythonパッケージをインストールする

>  Jetson Nanoがインターネットに接続されていることを確認してください

1. ターミナルを開き、[JetCam](http://github.com/NVIDIA-AI-IOT/jetcam) Pythonパッケージをインストールする

```
cd $HOME git clone https://github.com/NVIDIA-AI-IOT/jetcam
cd jetcam sudo python3 setup.py install
```

1. [torch2trt](http://github.com/NVIDIA-AI-IOT/torch2trt) Pythonパッケージをインストールする

```
cd $HOME git clone https://github.com/NVIDIA-AI-IOT/torch2trt
cd torch2trt sudo python3 setup.py install
```

1. [JetRacer](http://github.com/NVIDIA-AI-IOT/jetracer)パッケージをインストールする

```
cd $HOME git clone https://github.com/NVIDIA-AI-IOT/jetracer
cd jetracer sudo python3 setup.py install
```

## ステップ6  -  Jetson Nanoを5Wモードに設定する

 Jetson Nanoがバッテリーの最大の供給量よりも多くの電力を引き出すのを防ぐために、5Wモードに設定する
1. 端末を開き、以下を呼び出して5Wモードを設定する

```
sudo nvpmodel -m1
```

## 次のステップ

次は[制作例](examples_ja.md)を実行していきます。

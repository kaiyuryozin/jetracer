
#  JetRacer

 <img src = "https://user-images.githubusercontent.com/25759564/60384726-40f1a300-9a36-11e9-90df-e8fdcf2f69ae.jpg" height = 256>

 JetRacerは、NVIDIA Jetson Nanoを使用した教育用AIレースカーです。
- **手頃な価格** -  Jetson Nanoを含めて400USドル以下
- **教育** - 基本動作から、AIでコースに沿って走る自動運転まで
- **楽しい!** -  Webブラウザから対話的にプログラムできる

はじめに、以下の設定方法に沿って進めましょう。

## セットアップ

次のステップで、JetRacerを使い始められます。

1. 部品表から部品を注文する [日本語](docs/bill_of_materials_ja.md) / [英語](docs/bill_of_materials.md)
1. ハードウェアの組み立て [日本語](docs/hardware_setup_ja.md) / [英語](docs/hardware_setup.md)
1. ソフトウェアの設定 [日本語](docs/software_setup_ja.md) / [英語](docs/software_setup.md)
1. 例に沿って実行する [日本語](docs/examples_ja.md) / [英語](docs/examples.md)

## 作例

### 例1 - 基本動作

この例では、あなたのウェブブラウザからプログラム的にJetRacerをプログラムすることを学びます。 [サンプル](docs/examples_ja.md)ドキュメントでもっと学びましょう。

 <img src="https://user-images.githubusercontent.com/4212806/60383497-68d90a80-9a26-11e9-9a18-778b7d3a3221.gif" height=300 />

### 例2 - コースに沿って走る自動運転

この例では、AIを使ってJetRacerにコースの走り方を教えます。 [インタラクティブな学習ノートブック](notebooks/interactive_regression_ja.ipynb)を使ってニューラルネットワークを学習させます。そして、JetRacerに最適化されたライブデモをデプロイします。[制作例](docs/examples_ja.md)にて、さらに学んでみましょう。

 <img src = "https://user-images.githubusercontent.com/4212806/60383389-bd7b8600-9a24-11e9-9f64-926e5edb52cc.gif" height=300 />

## 参考サイト

-  [JetBot](http://github.com/NVIDIA-AI-IOT/jetbot) -  NVIDIA Jetson Nanoをベースにした教育用AIロボット
-  [JetCam](http://github.com/NVIDIA-AI-IOT/jetcam) -  NVIDIA Jetson用の使いやすいPythonカメラインターフェース
-  [JetCard](http://github.com/NVIDIA-AI-IOT/jetcard) -  NVIDIA Jetson NanoによるAIプロジェクトのWebプログラミング用のSDカードイメージ
-  [torch2trt](http://github.com/NVIDIA-AI-IOT/torch2trt) -  PyTorchからTensorRTへのコンバーター

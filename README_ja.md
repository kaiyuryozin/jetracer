
#  JetRacer

 <img src = "https://user-images.githubusercontent.com/25759564/60384726-40f1a300-9a36-11e9-90df-e8fdcf2f69ae.jpg" height = 256>

 JetRacerは、NVIDIA Jetson Nanoを使用した教育用AIレースカーです。
- 手頃な価格 -  Jetson Nano *を含めて* $ 400以下
- 教育 - 基本動作からAIロードフォローまでの例
- 楽しいね！ -  Webブラウザから対話的にプログラムされた

はじめに、以下の[設定](#setup)に従ってください。

## セットアップ

 JetRacerを使い始めるには、次のステップに従ってください。
1. 部品表から部品を注文[する](docs/bill_of_materials.md)
1.  [ハードウェアの設定に](docs/hardware_setup.md)従う
1.  [ソフトウェアの設定に](docs/software_setup.md)従う
1.  [例を](docs/examples.md)実行する

## 例

### 例1  - 基本モーション

この例では、あなたのウェブブラウザからプログラム的にJetRacerをプログラムすることを学びます。 [サンプル](docs/examples.md)ドキュメントでもっと学びましょう。

 <img src = "https://user-images.githubusercontent.com/4212806/60383497-68d90a80-9a26-11e9-9a18-778b7d3a3221.gif" height = 300 />

### 例2  - 道路の流れ

この例では、AIを使ってJetRacerに道を辿る方法を教えます。 [インタラクティブトレーニングノート](notebooks/interactive_regression.ipynb)を使ってニューラルネットワークをトレーニングした後は、JetRacerで最適化されたライブデモをデプロイします。 [例で](docs/examples.md)もっと学びましょう。

 <img src = "https://user-images.githubusercontent.com/4212806/60383389-bd7b8600-9a24-11e9-9f64-926e5edb52cc.gif" height = 300 />

## 参考サイト

-  [JetBot](http://github.com/NVIDIA-AI-IOT/jetbot) -  NVIDIA Jetson Nanoをベースにした教育用AIロボット
-  [JetCam](http://github.com/NVIDIA-AI-IOT/jetcam) -  NVIDIA Jetson用の使いやすいPythonカメラインターフェース
-  [JetCard](http://github.com/NVIDIA-AI-IOT/jetcard) -  NVIDIA Jetson NanoによるAIプロジェクトのWebプログラミング用のSDカードイメージ
-  [torch2trt](http://github.com/NVIDIA-AI-IOT/torch2trt) -  PyTorchからTensorRTへのコンバーター

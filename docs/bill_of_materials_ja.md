
# 部品表

このページはJetRacerを構築するために必要な部分をリストします。部品を受け取ったら、[ハードウェアの設定](hardware_setup_ja.md)に従います。

 <img src = "https://user-images.githubusercontent.com/4212806/60303370-1810c700-98eb-11e9-9393-dfc3e8799453.jpg" height = 256>

> (2019/6/30 訳者注)現時点ではこちらのBOMは, オリジナルのページをそのまま翻訳しており、日本での調達可能性などは未確認ですのでご注意ください。

## Jetson Nano

|部品|数量|コスト| URL |ノート|
|---|---|---|---|---|
|Jetson Nano| 1 | 99.00USD | [NVIDIA](https://developer.nvidia.com/embedded/buy/jetson-nano-devkit) ||
|マイクロSDカード| 1 | 13.99USD| [Amazon](https://amzn.to/2Us6bOv) | 32GB以上でなければなりません|
| USBバッテリー| 1 | 15.95USD| [Amazon](https://www.amazon.com/5000-mah-Attom-Tech-Portable-Emergency/dp/B07MNWPFG8/) |最低5V @ 2Aを供給要|
| USB A  - >2.1mmバレルケーブル| 1 | 7.00USD | [Amazon](https://www.amazon.com/gp/product/B075112RM6/) ||
| 5V @ 4Aバレルプラグ電源| 1 | 14.95USD| [Adafruit](https://www.adafruit.com/product/1466) |内径2.1mm |
|ジャンパーキャップパック| 1 | 5.09USD| [Amazon](http://amzn.com/B077957RN7/) | 2.54mmピッチ|

## シャーシ

|部品|数量|コスト| URL |ノート|
|---|---|---|---|---|
| RCカー| 1 | 109.95USD | [Hobbytown](https://www.hobbytown.com/traxxas-latrax-rally-1-18-4wd-rtr-rally-racer-green-tra75054-5-grn/p630138) ,  [Amazon](http://amzn.com/B06W57XLRW) | Traxxas LaTrax Rally 1/18 4WD w / 2.4GHzラジオ|
| 3Dプリント基板| 1 || [STLファイル](../assets/jetracer_latrax_base_board.stl) ||
| 3Dプリントカメラマウント| 1 || [STLファイル](../assets/jetracer_latrax_cam_mount.stl) |

## エレクトロニクス

|部品|数量|コスト| URL |ノート|
|---|---|---|---|---|
| PWMサーボモータドライバ| 1 | 6.99USD| [Amazon](http://amzon.com/B01D1D0CX2/) | PCA9685 |
| RCサーボマルチプレクサ| 1 | 9.95USD| [Pololu](https://www.pololu.com/product/2806) ||
|サーボ延長ケーブルパック| 1 | 5.91USD| [Amazon](http://amzn.com/B00P6JJFIS/) |オスからオス, 10cm |
|ジャンパー線パック| 1 | 6.98USD| [Amazon](http://amzn.com/B01EV70C78/) |メスからメス, >10cm ||
|手動オーバーライドスイッチパック| 1 | 10.99USD| [Amazon](https://www.amazon.com/gp/product/B07L74MMG8/) |

##  Wi-Fi

|部品|数量|コスト| URL |ノート|
|---|---|---|---|---|
| Wi-Fiカード| 1 | 18.95USD| [Amazon](https://amzn.to/2WKEkum) ,  [Newegg](https://www.neweggbusiness.com/Product/Product.aspx?Item=9SIV21M85N2699) ||
| Wi-Fiアンテナ| 2 | 5.06USD| [Arrow](https://www.arrow.com/en/products/2042811100/molex) |

## カメラ

 JetRacer用の広角カメラが必要です。オプションを選択して, 表示されている部品を注文してください。

### オプション1  - 広角ヒョウイメージングカメラ

|部品|数量|コスト| URL |ノート|
|---|---|---|---|---|
|カメラ| 1 | 29USD| [leopardimaging](https://leopardimaging.com/product/li-imx219-mipi-ff-nano/) |広角（ **H145** ）オプションを選択|

### オプション2  - ラズベリーパイカメラV2 +広角アタッチメント

|部品|数量|コスト| URL |ノート|
|---|---|---|---|---|
|カメラ| 1 | 23.90USD| [Amazon](https://amzn.to/2MSi6lL) ,  [Adafruit](http://adafru.it/3099) |ラズベリーパイ用カメラV2 |
|広角アタッチメント| 1 | 18.99USD| [Amazon(1)](https://amzn.com/B07HMXJ9Y1) ,  [Amazon(2)](https://amzn.com/B07HF81BVL/) ,  [eBay](https://ebay.us/Fz7HGd) | 160度FoV |

## アセンブリハードウェア

|部品|数量|コスト| URL |ノート|
|---|---|---|---|---|
| M2×6mmスクリューパック| 1 | 13.53USD| [Amazon](https://www.amazon.com/gp/product/B01FXGHO2M/) | 3Dプリントベースプレートにアクセサリを取り付けます。 1台あたり12本のネジが必要|
| M3×20mmスタンドオフパック| 1 | 6.99USD| [Amazon](https://www.amazon.com/dp/B072DVGWHZ/ref=cm_sw_su_dp) | 3DプリントベースプレートをRCシャーシに取り付けます。 1台の車に4スタンドオフが必要|
| M2×38mmスクリューパック| 1 | 11.99USD| [Amazon](http://amzn.com/B07CHJBK6F) | 1台につき2台必要|
| M2×30mmスクリューパック| 1 | 7.96USD| [Amazon](https://www.amazon.com/dp/B015A31EVK/ref=cm_sw_su_dp) | 1台につき2台必要|
|粘着パッドパック| 1 | 6.98USD| [Amazon](https://www.amazon.com/gp/product/B001KYSAN4/) | 1台につき4台必要|

## この次は

 [ハードウェアの設定](hardware_setup_ja.md)に沿って進めます。

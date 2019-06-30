
# ハードウェアの組み立て

 以下のステップでJetRacerを組み立ててみましょう。完了したら、次は[ソフトウェア設定](software_setup_ja.md)に進みます。

## 道具

- プラスドライバセット
- 六角ドライバー
- はんだごて
- 3mmと6mmのドリルビットのドリル
- ペンチ
- ワイヤーストリッパー

## フェーズ1  - 車の分解

### ステップ1  - 車からボディを取り外す

<img src="https://user-images.githubusercontent.com/25759564/60310435-c165b600-9907-11e9-858b-238e801b11ab.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60310436-c165b600-9907-11e9-88d1-fd009d015eda.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60310437-c1fe4c80-9907-11e9-8862-f0249a61c680.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60310439-c1fe4c80-9907-11e9-8495-990fa6ae926e.JPG" height=128/>

1. ボディを固定している4本のピンを取り外す
1. シャーシからエアフローカバーを取り外す

### ステップ2  - 車からESCとRC受信機を取り外す

<img src="https://user-images.githubusercontent.com/25759564/60311224-37b7e780-990b-11e9-92b1-04fd1bc78b41.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60311225-37b7e780-990b-11e9-9738-aab32effaf32.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60311226-37b7e780-990b-11e9-9454-9f54187a61af.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60311228-38507e00-990b-11e9-9bb5-53256784ea85.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60311229-38507e00-990b-11e9-890b-3123dcdf4cea.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60311231-38507e00-990b-11e9-832d-fdb3b696f336.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60311233-38e91480-990b-11e9-86be-5b01f8e4a9d2.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60311234-38e91480-990b-11e9-9277-3f71895a40c7.JPG" height=128/>

1. 電子ハブをシャーシに固定している2本のネジを外す
1. シャーシから電子ハブを引き出す
1. 電子ハブからESCとRC受信機を取り外す
1.  RC受信機から2本のサーボケーブルを外す
1.  RCレシーバーからフォーム接着剤をはがす

## フェーズ2  - 車の配線

### ステップ1 - Jetsonをサーボドライバに接続する

<img src="https://user-images.githubusercontent.com/25759564/60311869-ec530880-990d-11e9-9b9b-efabfcef251e.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60315002-a56b1000-9919-11e9-8a53-2d941cc1b139.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60311872-eceb9f00-990d-11e9-8770-3021aa6b11b3.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60311873-eceb9f00-990d-11e9-9872-cae74856b125.JPG" height=128/>

1. バンドルから4本のメス - メスジャンパケーブルを選択
1. サーボドライバピン`VCC`（白）、`SDA`（灰色）、`SCL`（紫）、`GND`（黒）にジャンパを取り付ける
1. ジャンパのもう一方の端を、Jetson Nanoのピン`3.3V`（白）、`3`（灰色）、`5`（紫）、および`GND`（黒）に取り付ける


### ステップ2  - サーボドライバをマルチプレクサに接続する

<img src="https://user-images.githubusercontent.com/25759564/60312424-23c2b480-9910-11e9-824e-7fb36213dd65.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60312425-23c2b480-9910-11e9-94af-ccc7b5d9f07a.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60312427-245b4b00-9910-11e9-8781-ba4ec20c0012.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60312429-245b4b00-9910-11e9-84d5-f3ccf10fcf86.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60312430-245b4b00-9910-11e9-8244-22c40b3b5851.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60312431-245b4b00-9910-11e9-8a6d-f6f1ae954ab2.JPG" height=128/>

1. サーボドライバのチャンネル`0`をマルチプレクサのチャンネル`S1`に接続
1. サーボドライバのチャンネル`1`をマルチプレクサのチャンネル`S2`に接続

### ステップ3 - RC受信機をマルチプレクサに接続

<img src="https://user-images.githubusercontent.com/25759564/60313003-4d7cdb00-9912-11e9-98cb-5890120a7949.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60313004-4d7cdb00-9912-11e9-90bd-2fbe3bee0a05.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60313006-4d7cdb00-9912-11e9-86a9-bbc0dc62b94f.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60313007-4d7cdb00-9912-11e9-84e3-03944f236987.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60313008-4d7cdb00-9912-11e9-9894-eac89f324822.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60313009-4e157180-9912-11e9-984a-afbf62bbb15d.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60313010-4e157180-9912-11e9-858c-6a463433f53f.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60313012-4e157180-9912-11e9-9743-5647a3c5599b.JPG" height=128/>

1.  RCレシーバのチャネル`3`をマルチプレクサの`SEL`に接続
1.  RCレシーバのチャネル`2`をマルチプレクサの`M2`に接続
1.  RCレシーバのチャネル`1`をマルチプレクサの`M1`に接続

### ステップ4  - マルチプレクサをESCとサーボに接続する

<img src="https://user-images.githubusercontent.com/25759564/60314883-1bbb4280-9919-11e9-9f76-c561c9de9cb2.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60314885-1bbb4280-9919-11e9-8eb2-5c1f97b6b6dc.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60314884-1bbb4280-9919-11e9-8c4f-d43a5441fbe7.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60314887-1c53d900-9919-11e9-9d48-3770831164c8.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60314888-1c53d900-9919-11e9-8c84-4a91f0e727af.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60314889-1c53d900-9919-11e9-97aa-9015e4e94aca.JPG" height=128/>

1. サーボをマルチプレクサの`OUT1`に接続
1.  ESCをマルチプレクサの`OUT2`に接続

## フェーズ3  - 自動車組立

### ステップ1 - ESCをベースプレートに取り付ける

<img src="https://user-images.githubusercontent.com/25759564/60316400-2d074d80-991f-11e9-8f4c-49cbf84b3fb8.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60316401-2d074d80-991f-11e9-8f3b-82714cfef58f.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60316392-2c6eb700-991f-11e9-89cc-3f9babc37a17.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60316393-2c6eb700-991f-11e9-94e5-4ebe4b2582fd.JPG" height=128/>

1. ガイドの通り、ESCをベースプレートに取り付ける。ただし、ESC用のベースプレートの2つのスロットに注意する
1. しっかりと押し下げてESCを固定する

### ステップ2 - RCレシーバーをベースプレートに取り付ける

<img src="https://user-images.githubusercontent.com/25759564/60316395-2d074d80-991f-11e9-80dc-63c819b76963.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60316445-5627de00-991f-11e9-8408-35b9c1fec8da.JPG" height=128/>

1. 指示通りにRCレシーバーをベースプレートに取り付ける
1. しっかりと押し下げてRCレシーバーを固定する

### ステップ3  - ベースプレートを取り付けるために使用されるネジ穴を露出させる

<img src="https://user-images.githubusercontent.com/25759564/60317621-bcfbc600-9924-11e9-9cb5-af886100dd48.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317622-bcfbc600-9924-11e9-8893-3c46e21ec259.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317624-bcfbc600-9924-11e9-9b5c-54b6eb311153.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317625-bcfbc600-9924-11e9-9f2b-830cce4cadb3.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317628-bd945c80-9924-11e9-9848-36492cc190cd.JPG" height=128/>

1. ベースプレートを取り付けるために使用される穴を露出させるため、上に示した4本のネジを外す

### ステップ4  - ベースプレートをRCカーに取り付ける

<img src="https://user-images.githubusercontent.com/25759564/60317630-bd945c80-9924-11e9-8139-5d7f5b8ad6a9.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317631-bd945c80-9924-11e9-9eb0-c755fdb6d83f.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317632-be2cf300-9924-11e9-8bd0-7b05f6f0ef2b.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317633-be2cf300-9924-11e9-853a-59a2e0875410.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317634-be2cf300-9924-11e9-83eb-3313d97d535e.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317610-bc632f80-9924-11e9-9290-9b6ba270a515.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317611-bc632f80-9924-11e9-94e2-1bacf358ebe4.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317613-bc632f80-9924-11e9-89ab-a7d3dfec94d7.JPG" height=128/>

1.  `M3x20mm standoffs`、2本の`M2x38mm`ネジと2本の`M2x30mm`、合計4本を選ぶ
1. ガイドの通り、ベースプレートをRCカーのシャーシに取り付ける
1. 六角ドライバを使用してベースプレートを固定する

### ステップ5  - ベースプレートを通してサーボモータワイヤを配線する

<img src="https://user-images.githubusercontent.com/25759564/60318103-976fbc00-9926-11e9-90fc-d17feb20796e.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60318104-976fbc00-9926-11e9-9dc1-9b2f5c9efb0f.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60317768-56c37300-9925-11e9-9ce2-fb43b7a70c4a.JPG" height=128/>

> サーボケーブルがベースプレートの周囲に届くほど長くない場合は、次のように配線してください。

1. 先ほど取り付けたマルチプレクサの`OUT1`からサーボケーブルを外す
1. 示されたスロットベースプレートを通してサーボワイヤーを配線する
1. サーボケーブルをマルチプレクサの`OUT1`に再接続

### ステップ6  - ベースプレートに部品を取り付ける

<img src="https://user-images.githubusercontent.com/25759564/60318997-d9e6c800-9929-11e9-8606-c1f020710518.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60318999-da7f5e80-9929-11e9-921b-c63e1bfc1f9e.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319310-d0aa2b00-992a-11e9-95a0-4e00e010acf9.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319312-d0aa2b00-992a-11e9-9631-d5c688ea67b7.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319370-0e0eb880-992b-11e9-8854-1220bd1e806b.JPG" height=128/>

1.  `M2x6mm`ネジを10本選択します
1. マルチプレクサをベースプレートに固定する
1. サーボドライバをベースプレートに固定する
1. ベースプレートにJetson Nanoを固定する

### ステップ7 - WiFiカードを接続する

<img src="https://user-images.githubusercontent.com/25759564/60319810-87f37180-992c-11e9-87a5-745b7bb57a13.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319811-888c0800-992c-11e9-9b39-01b0df050d69.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319812-888c0800-992c-11e9-8570-e6991fc1ce4d.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319813-888c0800-992c-11e9-9280-de99940abd95.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319815-888c0800-992c-11e9-9884-1bab46691048.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319816-89249e80-992c-11e9-8c5b-7287c798221c.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319817-89249e80-992c-11e9-98d8-0628f0b53d43.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319818-89249e80-992c-11e9-8411-96abda0a94e7.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319819-89249e80-992c-11e9-8cee-9d53e81df454.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60319821-89249e80-992c-11e9-8374-ee5d0ce24fe5.JPG" height=128/>

1.  WiFiカードに2つのアンテナを取り付けます
1. 示されているように、開発者キットのボードからJetson Nanoモジュールを取り外す。
1. 開発キットベースボードのM2コネクタ固定ネジを外す
1.  WiFiカードをM2コネクタスロットに差し込みます
1. ネジを取り付けてWiFiカードを固定する。
1.  Jetson Nanoモジュールを開発者キットボードに再接続

### ステップ8  - カメラを接続する

<img src="https://user-images.githubusercontent.com/25759564/60320486-b4a88880-992e-11e9-93ad-65ea2f051572.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60320259-07ce0b80-992e-11e9-82ae-bf8b7fa09b85.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60320260-07ce0b80-992e-11e9-92f7-fd6e4c83d264.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60320788-a3ac4700-992f-11e9-99d9-1dba9f1897f1.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60320789-a3ac4700-992f-11e9-8280-c689d609c18b.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60320790-a3ac4700-992f-11e9-9afc-f48c9f4a176e.JPG" height=128/>


1. ガイドの通りカメラをJetson Nano開発者キットに取り付ける <blockquote>カメラのコネクタを緩めるときは、壊さないように注意してください。 </blockquote>
1.  4本の`M2x6mm` 6 `M2x6mm`ネジを使用して、カメラマウントを`M2x6mm`取り付けます
1.  4本の`M2x6mm` 6 `M2x6mm`ネジを使用してカメラをカメラマウントに取り付けます

### ステップ9 - USBバッテリーパックをマウントする

<img src="https://user-images.githubusercontent.com/25759564/60321112-b1ae9780-9930-11e9-8f84-24cc304af5f9.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60321113-b1ae9780-9930-11e9-9462-685e0d9e9464.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60321114-b1ae9780-9930-11e9-80bf-84522d1ce708.JPG" height=128/>

1. ガイドの通り、USBバッテリーパックをベースプレートの下側に取り付ける

### ステップ10 - USBバレルプラグを取り付ける

<img src="https://user-images.githubusercontent.com/25759564/60322349-14556280-9934-11e9-8c25-4394eddda4e2.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60322350-14556280-9934-11e9-8c31-70982af7e08e.JPG" height=128/>

1. バレルプラグ電源を有効にするためにJetson Nano開発者キットの`J48`に2ピンジャンパーを取り付けます
1. バレルプラグをJetson Nano開発者キットに挿入します<blockquote>電源を入れる前に、 [ソフトウェアの設定](software_setup.md)に従ってSDカードを設定する必要があります。 </blockquote>

## フェーズ4 - RC送信機の修正

### ステップ1 - Dissasmbleラジオ

<img src="https://user-images.githubusercontent.com/25759564/60376010-fc77f000-99c0-11e9-9e2a-478a5da88062.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60376011-fc77f000-99c0-11e9-827f-77e4df18516f.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60376014-fda91d00-99c0-11e9-8a45-ca3ef0f4831c.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60376015-fe41b380-99c0-11e9-9915-d31b6d32e692.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60376016-fe41b380-99c0-11e9-9f2f-892026211c67.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60376019-feda4a00-99c0-11e9-9aa9-89d6ea78532b.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60376020-ff72e080-99c0-11e9-907e-1ccd5c805a20.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60376023-ff72e080-99c0-11e9-8bad-3bc2d4577207.JPG" height=128/>

1. プラスドライバでラジオの半分を固定している5本のネジを外す
1.  2つの半分を接合するラジオスティックをはがします
1. ラジオの半分にラジオステッカーを貼ります
1. 電池カバーを外す
1. ラジオを半分に分けます

### ステップ2  - トリム/リセットPCBを取り外す

<img src="https://user-images.githubusercontent.com/25759564/60377677-de64bc80-99cd-11e9-90f3-136345e6f49f.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377678-de64bc80-99cd-11e9-994b-0e6bb898c83d.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377679-de64bc80-99cd-11e9-9c79-3a8dbb2efe30.JPG" height=128/>

1. トリム/リセットPCBを固定しているネジを外す
1. ワイヤを固定クリップから慎重に引き出し、PCBを横に引きます。

### ステップ3  - 手動オーバーライドスイッチ用のドリル穴

<img src="https://user-images.githubusercontent.com/25759564/60377680-de64bc80-99cd-11e9-9af6-4f6de5c0c751.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377681-de64bc80-99cd-11e9-8158-161483ac51f7.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377682-defd5300-99cd-11e9-80eb-6d82ea5315eb.JPG" height=128/>

1. ドライバーの先端に合わせてRCトランスミッターに印を付けます
1. 直径`6mm`ドリルビットを使用して、印を付けた場所に穴を開けます

### ステップ4  - スイッチキー用のドリル穴

<img src="https://user-images.githubusercontent.com/25759564/60377685-defd5300-99cd-11e9-8eaa-9048b6e80a7c.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377686-df95e980-99cd-11e9-9417-c4f263ca1da5.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377687-df95e980-99cd-11e9-8c62-bcb5ac5b7ba9.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377688-df95e980-99cd-11e9-8ea5-0161914ba4dc.JPG" height=128/>

1. スイッチをRCトランスミッターに一時的に挿入する
1. キーワッシャーをトランスミッターの反対側に置きます
1. ドライバー先端の位置にRCトランスミッターをマーク
1. およそ`2.5mm - 3.5mm`ドリルビットを使用して、印を付けた場所に穴を開けます

### ステップ5 - RCトランスミッタへの手動スイッチの固定

<img src="https://user-images.githubusercontent.com/25759564/60377694-e0c71680-99cd-11e9-83f7-d67d579241ff.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377689-e02e8000-99cd-11e9-9e8a-aabdc0c82d05.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377690-e02e8000-99cd-11e9-8ee2-06c8951ba19f.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377691-e0c71680-99cd-11e9-8c93-6c6d01b22102.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377695-e15fad00-99cd-11e9-8219-fdc61df2e137.JPG" height=128/>

1. 手動オーバーライドスイッチを穴に再挿入します
1. キー付きワッシャとナットをスイッチに戻します。
1. プライヤーを使用してスイッチをRCトランスミッターに固定する

### ステップ6 - RCトランスミッタPCBへのはんだ付けスイッチ

<img src="https://user-images.githubusercontent.com/25759564/60377697-e15fad00-99cd-11e9-94ea-2704dee00761.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377698-e15fad00-99cd-11e9-8587-538703080ba4.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377700-e1f84380-99cd-11e9-8580-546ff486e2b0.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377702-e1f84380-99cd-11e9-81e1-9d61d72892be.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377703-e1f84380-99cd-11e9-8e78-79393d8b9378.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377705-e290da00-99cd-11e9-9b00-cbed3a20eef2.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377676-de64bc80-99cd-11e9-9997-01baa79ad4cc.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377736-19ff8680-99ce-11e9-895e-0c5a5dbe6915.JPG" height=128/>

1. 指示された長さでワイヤをおおよそ切断する<blockquote>はんだパッドに達するのに十分な長さでワイヤーを切るようにしてください</blockquote>
1. ガイドの通りワイヤをはがします
1. 示されている2つのパッドにはんだを付けます
1. むき出しのリード線にはんだを付ける
1. ペンチを使用して、指示されたパッドにワイヤーを当て、はんだごてで熱を加えます

### ステップ7 - RCトランスミッターを再組み立てする

<img src="https://user-images.githubusercontent.com/25759564/60377737-19ff8680-99ce-11e9-8cf7-715df1081d53.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377760-33a0ce00-99ce-11e9-9a3f-beb0f7c11078.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377761-33a0ce00-99ce-11e9-9410-3f63f91fb4a7.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377762-33a0ce00-99ce-11e9-9071-d2a878a22212.JPG" height=128/>
<img src="https://user-images.githubusercontent.com/25759564/60377763-33a0ce00-99ce-11e9-9c3e-0b3d9de2bf86.JPG" height=128/>

1.  RCトランスミッターの半分を取り付け直します
1. 元のネジを使用して半分を締めます
1.  `AA`電池4 `AA` 、電池カバーを取り付ける

## ハードウェアセットアップ完了！

 <img src="https://user-images.githubusercontent.com/25759564/60377764-33a0ce00-99ce-11e9-8aa4-688d0a05dc01.JPG" height=256/>

## さて次は

次に、 [ソフトウェアの設定](software_setup_ja.md)に沿って進めます。

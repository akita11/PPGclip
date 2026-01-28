# PPG Clip

<img src="https://github.com/akita11/PPGclip/blob/main/images/PPGclip1.jpg" width="240px">

<img src="https://github.com/akita11/PPGclip/blob/main/images/PPGclip2.jpg" width="240px">

[M5Stack社の心拍センサユニット](https://www.switch-science.com/products/5695)を利用した、測定精度・安定度の高い透過型の光学脈波(PPG)計測器です。
マイコン部はM5Stack社のATOMシリーズを取り付けらて一体化できます。
部品セットからこれらを組み立てることができます。

<img src="https://github.com/akita11/PPGclip/blob/main/images/PPGclip3.jpg" width="240px">

ATOMシリーズを使わずに、直接Groveケーブルを接続して、他のM5Stackシリーズ等のマイコンで使用することもできます。


## 必要なもの
- 部品セット（筐体（4点）、LED基板、コネクタ基板、4p/2mmピンソケット×2、ケーブル（色が写真のものと異なる場合があります）、M2.3×8mmタッピングねじ、M2×4mmねじ、押しバネ0.7×7.5×23）
- [M5Stack社の心拍センサユニット](https://www.switch-science.com/products/5695)
- M5Stack社ATOMシリーズ（ディスプレイのついている[ATOMS3](https://www.switch-science.com/products/8670)が脈波確認などができて便利。ATOMS3用のサンプルファームウエアあり）
- 工具（1.5mm六角レンチ、小プラスドライバ）


<img src="https://github.com/akita11/PPGclip/blob/main/images/PPGclip_parts.jpg" width="240px">


# 組み立て

1. 心拍センサユニットを、1.5mm六角レンチを使って分解し、中のボード(1)を取り出します。
1. LED基板(2)とボード(1)を、ケーブル(3)でFig1のようにはんだ付けして接続します。ケーブルの対応関係を間違えないように注意してください。このとき、ボード(1)側は、ケーブルを横側に引き出し、はんだづけ箇所がなるべく平坦になるようにします。
1. コネクタ基板(4)に、4p/2mmピンソケット(5)を2個、傾かないように注意してはんだ付けし、足をなるべく短くカットします。（Fig2）
1. ボード(1)にコネクタ基板(4)を差し込み、Fig3のように筐体(6）にはめます。ケーブル(3)は、図のように上面基板に重ならないようにします。
1. ATOMシリーズを、コネクタ基板(4)の反対側にさしこみ、M2ねじ(7)でFig3のように固定します。
1. 黒い筐体(8)を筐体(6)（向きに注意）に、4個のタッピングねじ(9)でFig4のように固定します。
1. 筐体(9)に、LED基板(2)をFig5のようにはめ、黒い筐体(10)（向きに注意）を、4個のタッピングねじ(9)でFig6のように固定します。
1. Fig7のように、ばね(10)を筐体(9)にはめ、その後、Fig8のように、ばね(10)を反対側の筐体(6)にはめつつ、2つの筐体を押し込んではめこみます。
1. ATOMシリーズにプログラムを書き込み、ボード(1)が動作すると、Fig9のように上下両側のLEDが点灯します。

Fig1.:<img src="https://github.com/akita11/PPGclip/blob/main/images/1.jpg" width="240px">

Fig2:<img src="https://github.com/akita11/PPGclip/blob/main/images/2.jpg" width="240px">

Fig3:<img src="https://github.com/akita11/PPGclip/blob/main/images/3.jpg" width="240px">

Fig4:<img src="https://github.com/akita11/PPGclip/blob/main/images/4.jpg" width="240px">

Fig5:<img src="https://github.com/akita11/PPGclip/blob/main/images/5.jpg" width="240px">

Fig6:<img src="https://github.com/akita11/PPGclip/blob/main/images/6.jpg" width="240px">

Fig7:<img src="https://github.com/akita11/PPGclip/blob/main/images/7.jpg" width="240px">

Fig8:<img src="https://github.com/akita11/PPGclip/blob/main/images/8.jpg" width="240px">

Fig9:<img src="https://github.com/akita11/PPGclip/blob/main/images/9.jpg" width="240px">


# ソフトウエア

M5Stack社の心拍センサユニット用のプログラムはすべて利用できます。サンプルとして、以下の機能をもつATOMS3用のプログラムがsampleFW/内にあります。
- 波形表示(100Hzサンプリング)
- ベースライン変動除去
- 簡易な正常計測チェック（正常計測時は緑色のグラフ）
- ボタンを押すと10秒分の生データをUSU UARTにCSV形式で出力


## Author

Junichi Akita (@akita11) / akita@ifdl.jp







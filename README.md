# myled
"myled" is a turn on the led with Linux

# デモ
LEDをつけて消しました。<br>
https://youtu.be/FXtFQuS2jcM

# 使用する物
・raspberry pi4 Moduoe B ×1<br>
・ブレッドボード　×１<br>
・LED　×1<br>
・ジャンパー線　×6<br>

# 配線
![S__161824778](https://user-images.githubusercontent.com/93694888/146308071-0d371c99-d591-437e-950b-7d61a613ff22.jpg)



# 使い方
ディレクトリ内で以下のコマンドを実行<br>
```bash
git clone git@github.com:KaitoNemoto/LED.git
cd myled
make
sudo insmod myled.ko
sudo chmod 666 /dev/myled0
```

以下のコマンドで点灯
```bash
echo 1 > /dev/myled0
```

以下のコマンドで消灯
```bash
echo 0 > /dev/myled0
```

ディレクトリの後処理は以下のコマンド
```bash
make clean
```

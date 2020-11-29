# 2020年 ロボットシステム学 課題1
=============

## 目標
=============

- rasberry pi 4とUbuntuを用いてLEDを光らせる。
    
## 内容
=============

0. LEDの消灯
1. LEDの点灯
2. LEDのモールス信号点滅 - corona
3. LEDのモールス信号点滅 - abunai
4. LEDのモールス信号点滅 - desu
5. LEDの点滅 - 段々早くなり、最後は消灯
6. LEDの点滅 - 段々遅くなり、最後は消灯

## インストール手順
=============

1. LEDの接続先のピンを22番と39番に繋げる。
2. makeを実行する。
3. sudo insmod myled.koを実行し、インストールする。
4. tail /var/log/messagesでmajor番号を確認する。
5. sudo mknod　/dev/myled0 c {major番号} cと実行する。
6. sudo chmod 666 /dev/myled0を実行する。
7. echo 0 > /dev/myled0でプログラムを実行する。(echo 0,1,2,3,4,5,6を実行することで内容の所を実行できる。)
8. 終わったらsudo rmmod myledを実行し、アンインストールする

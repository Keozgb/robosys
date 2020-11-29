2020年 ロボットシステム学 課題1
=============

目標
=============

- rasberry pi 4とUbuntuを用いてLEDを光らせる。
    
内容
=============
0.LEDの消灯
1.LEDの点灯
1.LEDのモールス信号点滅 - corona
1.LEDのモールス信号点滅 - abunai
1.LEDのモールス信号点滅 - desu
1.LEDの点滅 - 段々早くなり、最後は消灯
1.LEDの点滅 - 段々遅くなり、最後は消灯

インストール手順
=============

1.LEDの接続先のピンを22番と39番に繋げる。
1.makeを実行する。
1.sudo insmod myled.koを実行し、インストールする。
1.tail /var/log/messagesでmajor番号を確認する。
1.sudo mknod　/dev/myled0 c {major番号} cと実行する。
1.sudo chmod 666 /dev/myled0を実行する。
1.echo 0 > /dev/myled0でプログラムを実行する 0の部分を上の内容の数字にすることで、その部分のプログラムを実行できる
1.終わったらsudo rmmod myledを実行し、アンインストールする

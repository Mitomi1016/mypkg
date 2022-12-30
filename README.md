# ros2_mypkg
![test](https://github.com/Mitomi1016/mypkg/actions/workflows/test.yml/badge.svg)

* 2022ロボットシステム学,練習用リポジトリである。

## インストール

Ubuntu22.04 LSTの端末を開き、ターミナル上に以下を入力。

```

$ git clone https://github.com/Mitomi1016/ros2_setup_scripts
$ cd ros2_setup_scripts
$./setup.bash
$ source ~/.bashrc

```

## 起動する手順

端末1のターミナルに以下を入力。

```

端末1 $ ros2 run mypkg talker

```

別の端末を使ってサブスクライブする。

```

端末2 $ ros2 run mypkg listener

```

## 機能

talker(端末1)で整数を0からカウントする
talker(端末1)でカウントした整数をlistener(端末2)で標準出力する
talkerでカウントした整数をパブリッシュし、listenerはtalkerでカウントした整数をサブスクライブして表示する。talkerとlistenerはcountupというトピックによって連結している。

## 実行例

```
[INFO] [1671991971.177618000] [listener]: Listen: 0

[INFO] [1671991971.669417200] [listener]: Listen: 1

[INFO] [1671991972.169457200] [listener]: Listen: 2

[INFO] [1671991972.669297400] [listener]: Listen: 3

[INFO] [1671991973.169653400] [listener]: Listen: 4

[INFO] [1671991973.669616100] [listener]: Listen: 5

[INFO] [1671991974.169463200] [listener]: Listen: 6

[INFO] [1671991974.668907100] [listener]: Listen: 7
```
このように端末2(listener)に出力される。

## 実行例2

launchを使用することにより、一つの端末で動作を確認することができる。

以下を端末1のターミナル上に入力
```
$ ros2 launch mypkg  talk_listen.launch.py
```

```

[listener-2] [INFO] [1671992183.194454600] [listener]: Listen: 0

[listener-2] [INFO] [1671992183.684191200] [listener]: Listen: 1

[listener-2] [INFO] [1671992184.184423100] [listener]: Listen: 2

[listener-2] [INFO] [1671992184.684597200] [listener]: Listen: 3

[listener-2] [INFO] [1671992185.184680100] [listener]: Listen: 4

[listener-2] [INFO] [1671992185.684633400] [listener]: Listen: 5

[listener-2] [INFO] [1671992186.184626800] [listener]: Listen: 6

[listener-2] [INFO] [1671992186.684521100] [listener]: Listen: 7

```

このように端末1に出力される。

## テスト環境
* Ubuntu22.04 LTS

## 必要なソフトウェア
* ROS2 

## 権利
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます。
* © 2022 Shoya Mitomi


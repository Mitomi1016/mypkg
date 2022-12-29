# ros2_mypkg
![test](git@github.com:Mitomi1016/mypkg.git)
2022ロボットシステム学,練習用リポジトリである。

##　使い方　インストール
Ubuntu22.04の端末を開き、ターミナルに以下を入力。

$ git clone git@github.com:Mitomi1016/mypkg.git

$ cd ros2_setup_scripts

$ ./setup.bash

$ source ~/.bashrc

## 起動する手順
端末1のターミナルに以下を入力。

端末1 $ ros2 run mypkg talker

別の端末を使ってサブスクライブする。

端末2 $ ros2 run mypkg listener

## 実行例

[INFO] [1671991971.177618000] [listener]: Listen: 0
[INFO] [1671991971.669417200] [listener]: Listen: 1
[INFO] [1671991972.169457200] [listener]: Listen: 2
[INFO] [1671991972.669297400] [listener]: Listen: 3
[INFO] [1671991973.169653400] [listener]: Listen: 4
[INFO] [1671991973.669616100] [listener]: Listen: 5
[INFO] [1671991974.169463200] [listener]: Listen: 6
[INFO] [1671991974.668907100] [listener]: Listen: 7
このように端末2(listener)に出力される。

## テスト環境
* Ubuntu22.04

## 必要なソフトウェア
* ROS2

## 権利
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます。
* © 2022 Shoya Mitomi


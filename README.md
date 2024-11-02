## 修正の方針
- メソッドに分割する
- 同じようなコード断片はメソッドにまとめる
- 意味のないコメントを削除する

#オブジェクト指向エキササイズのためのクソコード
- このプロジェクトはプログラミング言語論の演習課題「オブジェクト指向エキササイズ」のためのクソコードである．
- オブジェクト指向エキササイズについては下記参照のこと．下記書籍及びスライドに書かれている9つのエキササイズを実施することが目標．
 - ThoughtWorks Inc. (著), 株式会社オージス総研 オブジェクトの広場編集部 (翻訳), ThoughtWorksアンソロジー ―アジャイルとオブジェクト指向によるソフトウェアイノベーション 単行本（ソフトカバー），オライリー・ジャパン，2008/12/27. https://www.amazon.co.jp/dp/487311389X
 - 大圖衛玄，オブジェクト指向できていますか？, http://www.slideshare.net/MoriharuOhzu/ss-14083300, 2012/8/27.

## クソコード作成指針
何か良いのが思いついたら追加予定
- Collectionとパッケージを使わない
- できる限りクラスを作らない
- 作れるsetter/getterは全部作る
- ネストは深ければ深いほど良い
- 1つのメソッド内でできることを分割しない
- if-else if..は長ければ長い方が良い
- 変数名，メソッド名は適当につける
- 一行に付くドットの数の限界に挑戦したい（クラスを作らないと難しい．．．）
- 同じコードを何回でも書く

## monsterzoo仕様
- Main.javaではMonsterZooクラスをnewしたあと，1秒毎にmove()を呼び出し，balls変数が0になるまで（初期値は10）呼び出しを繰り返す．
- move内では，呼び出しごとにdistanceが1.0km増え，ランダムにズーstationでボールやフルーツ，卵をゲットしたり，モンスターと遭遇してボールやフルーツをぶつけて捕まえたりする．
- 卵はGetしてから3kmあるくと孵り，ランダムにモンスターをGetできる
- モンスターはレア度を持っており，ボールをぶつけた際の乱数とレア度を比較して，レア度のほうが小さければGetできる
 - なお，乱数の値はフルーツをぶつけると倍になる（捕まえやすくなる）
- 最終的にballsの値が0になると終了し，何キロ歩いたか，捕まえたモンスターは何かを表示する．

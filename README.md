# robosystem-test

## 概要
このプログラムは、入力したテキストを受け取り、アルファベットを指定された記号に置き換えて暗号化するフィルタコマンドとして動作します。また、オプションとして、アルファベット以外の文字を空白に置き換える機能もあります。

## 使用方法
###1, パイプを使用して簡易的なテキストを入力する場合
以下のコマンドから実行できます。
```bash
$echo 任意の文字列 | ./crypto_generation
```
"任意の文字列"の部分に入力した半角英字のみが暗号化され、その他文字や記号はすべて空白に置き換えられます。
*注意事項*
	コマンドの性質上、"任意の文字列"の部分に''や""を入力する場合は必ずセットで使用してください。
	また、Enterを押すとコマンドが実行されてしまうため改行はできません。
###2, パイプを使用してテキストファイルから読み込む場合
以下のコマンドから実行できます。
```bash
$cat input.txt | ./crypto_generation
```
input.txtに保存されたテキストが暗号化され、標準出力に出力されます。改行も読み込む事が可能です。
*注意事項*
	テキストファイルは予め作成してください
	テキストファイルはinput.txtでは無く任意のテキストファイルで問題ありませんがその場合"cat"と"|"の間のファイル名を変更してください。

###3, パイプを使用せず入力する場合
以下のコマンドから実行できます。
```bash
$./crypto_generation
```
上のコマンドを入力したあと空白の部分で任意のテキストを入力してください。改行も使用できます。
*注意事項*
	改行が使用できる関係上、改行で終了することができません。テキストを入力し終わったらCtrl + Dで終了してください。

## コンパイル方法
プログラムをコンパイルする手順を記載します。
```bash
$g++ -o crypto_generation crypto_generation.cpp
```


# Macros 

マクロとは一連の動作をまとめたもの、
早速作っていきたいと思います

`qa` -> "a にマクロの登録の開始

`q` -> 登録の終了

`reg a` -> 登録したマクロの内容確認

`@a` -> "a のマクロの実行

`@@` -> 前回のマクロのリピート

`3@a` -> 3行続けて "a のマクロを実行

`:1,10 normal @a<ENTER>` -> 1から10行目に "a のマクロを実行

## exsample

before: print "Hello World"
after:  print("Hello World")

- まず`0`でカーソルを先頭に

- `f<SPACE>`カーソルを空白位置に

- `r(`空白を"("に置き換え

- `A)`末尾にインサートモードで")"を入力

- `<ESC>`でノーマルモードに戻して

- `j`で次の行に移って`q`で終了




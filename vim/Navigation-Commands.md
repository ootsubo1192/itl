# Navigation Commands

コマンド表記

`Ctrl-f`のように`-`でつなげている場合は`Ctrl`を押してから
`f`を押す

`Ctrl+f`のように`+`でつなげている場合は`Ctrl`を押しながら
`f`を押す

`gg`と書いてある場合は、`g`のあとに`g`を押す

大文字と小文字で動作が変わるので区別して覚える


カーソル移動

`h` -> 左カーソル

`j` -> 下カーソル

`k` -> 上カーソル

`l` -> 右カーソル

ページ移動

`Ctrl-f` -> 1ページ下に

`Ctrl-b` -> 1ページ上に

単語ごとのカーソルの移動

`w` -> 1単語右の先頭に、`,`や`.`等を単語の一部に含めない

`W` -> `,`や`.`を含めて1単語右の先頭に移動

`b` -> 1単語左の先頭に、`,`や`.`等を単語に一部に含めない

`B` -> `,`や`.`を含めた1単語左の先頭に移動


カーソルの行を指定して移動

`gg` -> 先頭の行に移動

`G`又は`:$<ENTER>` -> 最後の行に移動

`<x>gg`又は`<x>G` -> <x>行目に移動


セーブせずにvimを閉じる

`:q!<ENTER>`


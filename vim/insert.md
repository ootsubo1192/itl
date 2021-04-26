# insert 

### モードの変更

"i" -> 今のカーソル位置で入力モードに変更

"esc" -> ノーマルモードに変更

"I" -> カーソルがある行の先頭で入力モード

"a" -> カーソルの右側で入力モード

"A" -> カーソルがある行の行末で入力モード

"o" -> カーソルがある"下"の行に一行挿入して入力モード

"O" -> カーソルがある"上"の行に一行挿入して入力モード

### 行の合体

"J" -> 下の行をカーソルがある行にくっつける

### 上書きモード

"R" -> 上書きモードに変更

"r" -> 一文字だけ修正、修正したい文字の位置にカーソルを合わせて、"r"を押したあとで、
変更したい文字を入力

"cw" -> 単語の書き換え、カーソル位置以下の1単語を削除して入力モード

"cW" -> 句読点を含む単語の書き換え

"cc" -> 全文を削除して入力モード

### 大文字、小文字の変換

"~" -> カーソル位置の文字を、小文字または大文字に変換

"g~w" -> カーソル以下の1単語を小文字または大文字に変換

"g~~" -> カーソルがある行すべてを小文字と大文字の入れ替え

"gUW" -> カーソル以下の1単語をすべて大文字に変換

"guW" -> カーソル以下の1単語をすべて小文字に変換

###　文字の複製

"<count>i" -> "<strings><esc>" -> "count"の数だけ"esc"が押される間の文字列を入力

"<count>o" -> "<strings><esc>" -> "count"の数だけ複数行に複製


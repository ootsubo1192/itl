# permission

- すべてのファイルには**オーナー**と**グループ**が設定されている

- オーナーはファイルの所有者

- グループにオーナーを所属させ、複数のファイルをグループ権限で管理

```zsh
ls -l
```

```
-rwx-r-xr-x. 1 <OWNER> <GROUP> <> <CREATION_DATE> <FILE_NAME>
```

### permission

```
- rwx r-x r-x
```

- はじめの一つがファイルタイプ("-" 通常のファイル、"d"ディレクトリ、"l"シンボリックリンク)

- 次3つがオーナーのパーミッション

- その次の3つがグループのパーミション

- 最後の3つがその他のユーザーのパーミッション

`r` -> read(読み取り)

`w` -> write(かきこみ)

`x` -> execute(実行)

## chmod

権限の変更を行う

```
chmod 744 <FILENAME>
```

3つの数字は左から、オーナー、グループ、その他のユーザーを表す

`r` -> **4**

`w` -> **2**

`x` -> **1**

この数字を足したものが与える権限になる

## super user

管理者権限を持つ特別なユーザー

switch user and do の略

```
sudo <COMMAND>
```

コマンドの前に`sudo`をつけるとスーパーユーザー権限で実行



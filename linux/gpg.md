# gpg

GnuPGという暗号化プログラムを使用して、ファイルの暗号化や復号を行う

### オプション

| オプション | 説明 |
|:---|:---|
| --gen-key | 公開鍵暗号方式の鍵ペアを生成 |
| --export | 公開鍵をエクスポートする |
| --import | 公開鍵をインポートする |
| --list-keys | 公開鍵を一覧表示する |
| --sign | ファイルに著名する |
| --verify | ファイルの著名を検証する |
| -e ファイル名 | 暗号化データを受け取る側の公開鍵を使用してファイルを暗号化 |
| -o ファイル名 | 出力ファイル名を指定する |
| -r メールアドレス | 暗号化に使用する公開鍵の持ち主のメールアドレスを指定 |

----

gpg-agent -> GunPGにおいて秘密鍵を管理し、パスフレーズによる認証除隊を言って期間キュッシュするデーモンプログラム。SSHにおけるssh-agentと同様



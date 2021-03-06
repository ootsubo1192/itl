# xinetd

inetd より新しいスーパーサーバで、サービス毎に詳細な設定が可能

全体的な設定は[/etc/xinet**d**.conf]ファイルで行い、各サービスの個別設定は[/etc/xinetd.**d/**]ディレクトリ内の設定ファイルで行う

格差ーブスの個別設定ファイルを配置するディレクトリは、[/etc/xinetd.conf]の[includedir]で指定

## スーバーサーバ

以前のLinuxシステムは各プログラムを起動してメモリ上に常駐させていたがリソースの無駄遣いとなるので、サーバプログラムを管理するスーバーサーバが開発された

スーバーサーバは他のサーバプログラムに変わってサービス要求を監視、必要なときだけサーバプログラムを起動してリソースの節約、また、TCPラッパーと組み合わせ、アクセス制御を集中管理

デメリットとしては、応答が遅くなるので、接続頻度の少ないサーバ用

### 主な設定項目

| 項目 | 説明 |
|:---|:---|
| bind or interface | サービスを提供するインタフェースのIPアドレス |
| disable | サービスを無効化するかの設定(yes:**無効化**,no:**有効化** |
| instances | サーバプログラムの最大起動プロセス数 |
| log_type | ログの記録先を指定。syslogや記録するログファイルの絶対パスを指定する |
| no_access | サービスへのアクセスを拒否する接続元 |
| only_from | サービスへのアクセス許可をする接続元 |
| server | サーバプログラムの絶対パス |
| sever_args | サーバプログラム起動時に指定する**引数** |
| socket_type | ストリーム型、データグラム型といった、サービスの接続タイプ |
| user | サーバプログラムを起動するユーザー |
| wait | サーバプログラムへの接続処理を待ち合わせるかの設定。サーバプログラムがマルチスレッドであり1プロセスで同時に複数処理できる場合は**no**、シングルスレッドで処理が完了し、サーバプログラムが終了するまで接続処理を待ち合わせる必要がある場合**yes**とする |


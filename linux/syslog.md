# syslog



## rsyslog (reliable-syslog)

syslog(ログメッセージを送受信する規格)の問題点を克服した次世代のsyslog

主要なディストリビューションで採用されている

### ファシリティ(ログの送信元)

| ファシリティ | 説明 |
|:---|:---|
| auth,authpriv | 認証サービス |
| daemon | デーモン各種 |
| kern | カーネル |
| lpr | 印刷サービス |
| mail | メールサービス |
| syslog | syslogデーモン |
| user | ユーザーアプリケーション |
| local0~7 | 独自に使用可能 |

### プライオリティ(監視レベル)

| プライオリティ | 説明 |
|:---|:---|
| emerg | 非常に危険 |
| alert | 緊急対応が必要な状態 |
| crit | 危険な状態 |
| err | 一般的なエラーメッセージ |
| warning | 警告メッセージ |
| notice | 通知メッセージ |
| info | 情報メッセージ |
| debug | デバッグ時の有益な情報 |
| none | メッセージを送らない |

---

ファシリティとプライオリティを組み合わせてログを特定し、指定した宛先に出力

- ファシリティとプライオリティは[.]で繋ぐ

- ファシリティとプライオリティをあわせて[セレクタ]と呼び、セレクタによって扱うログメッセージを特定

- すべてのファシリティやすべてのプライオリティを指定するには[\*]を使う

- プライオリティは、指定したレベル以上のログを出力(errをしてするとerr,crit,alert,emergを出力)。特定のレベルのログだけを指定するには(=プライオリティ)とする

- アクションは出力先を指定。出力先は、ファイルであれば絶対パス、外部のsyslogサーバであれば(＠サーバアドレス)。(/dev/console)を指定するとログメッセージをコンソールに表示。全ユーザーのコンソールに送信したい場合は(\*)を指定

- (;)で繋ぐことで、1つのアクションに対して複数のセレクタが指定できる 

---

例) kern.=emerg /dev/console -> カーネルに関するプライオリティがemergログをコンソールに出力

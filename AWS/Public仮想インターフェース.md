# パブリック仮想インターフェース

AWS Direct Connect接続を開始するために必要になる仮想インターフェースの一つ

- プライベート仮想インターフェース -> プライベートIPアドレスを使ってVPCにアクセスする場合

- パブリック仮想インターフェース　-> パブリックIPアドレスを使用して、すべてのパブリックなAWSサービスに接続

- トランジット仮想インターフェース -> Direct Connect ゲートウェイに関連付けられた1つまたは複数のVPC*トランジットゲートウェイ*にアクセスする必要がある場合

`トランジットゲートウェイ`とは -> オンプレミスとVPCネットワークを相互に繋ぐための中継ハブ

`インターフェース` -> [Elastic-Network-Interface](Elastic-Network-interface.md)

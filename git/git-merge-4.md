# merge

## 指定したブランチを今いるブランチにマージする

### fast forward

マージ先にコミットポイントがない場合

`$ git merge <branchname>`

必ずマージたいブランチに移動してから行う

マージする前にはdiff(差分)を確認するのがおすすめ

マージするときにfast-forwardしないように設定してる(merge.ff only)

fast-forwardでのマージではコミットが発行されないので作業を取り消しや参照が面倒になるため

オプションで**--ff**をつけることで意図的にfast-forwardをすることができる

ただマージだけをfast-forwardしないようにすると、pullを行うたびにマージコミットが発行されるので(pull.ff only)を追加

### Automatic merge

マージ先にコミットポイントが有り、かつマージ元の変更点が同じではない場合

新たにマージコミットが作られる

### Conflict

マージ先にコミットポイントが有り、かつマージ元の変更点に同じ箇所がある場合

Gitはどちらをコミットすればいいの変わらないので衝突(conflict)が起きる

conflictが起きているファイルをエディタで開いて優先したいヶ所だけを残してファイルを保存



# リソース

## pod
* リソースの最小単位
* 一つ以上のコンテナから構成される
* pod単位でIPアドレスが割り振られる
* 同じpod同士のコンテナはlocalhostでアクセスできる。

## ReplicaSet
* 指定したpodのレプリカ数を維持するために、podを削除したり追加する

## Deployment
* 複数のReplicaSetを管理することでローリングアップデートしたり、ロールバックできる
* 1つのPodを起動するだけにしても、Deploymentを使ったほうがいい
  * pod単体の場合は自動で再作成されない
  * ReplicaSet単体の場合はローリングアップデートできない

## DaemonSet
* 各Nodeに一つpodを配置するReplicaSetみたいなもの
  * fluentdやDataDogを配置するのがいい

## StatefulSet
* DBなどのステートフルなもの用
* 永続化の仕組みがある

## Job
* バッチ的な処理用
* 処理が終了するものに使う

## CronJob
* Jobを管理しているもの
* スケジュールどおりに実行してくれる
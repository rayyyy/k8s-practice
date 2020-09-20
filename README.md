# k8s-practice
k8sの使い方をメモする

前提
Docker for MacでKubernetesインストール済み

## 補完のきかせ方
```
source <(kubectl completion bash)
```

## その他
* kindというツールを使うとローカルでも複数クラスターを作れる
* kubeconfig はデフォルト→にある ~/.kube/config
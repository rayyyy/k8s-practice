# 操作

```
# context操作
kubectl config use-context docker-desktop
kubectl config get-contexts
kubectl config current-context
kubectl --context prd-admin get pod

# ノードの確認
kubectl get nodes

# リソース操作
kubectl create -f sample-pod.yaml
kubectl get pods
kubectl delete -f sample-pod.yaml
kubectl delete pod sample-pod
kubectl delete pod --all
kubectl delete pod --all --wait
kubectl delete -f sample-pod.yaml --grace-period 0 --force
kubectl apply -f sample-pod.yaml --server-side
kubectl apply -f sample-pod.yaml --server-side --force-conflicts
kubectl apply -f sample-pod.yaml --server-side --all --prune

# 特殊操作
kubectl port-forward sample-pod 8888:80
kubectl logs sample-pod -f
stern sample-pod # pod名を部分一致で検索
kubectl cp sample-pod:etc/hostname ./hostname
kubectl exec -it sample-pod -- bash
```

## topコマンド
https://qiita.com/chataro0/items/28f8744e2781f730a0e6
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
kubectl create -f sample-pod.yml
kubectl get pods
kubectl delete -f sample-pod.yml
kubectl delete pod sample-pod
kubectl delete pod --all
kubectl delete pod --all --wait
kubectl delete -f sample-pod.yml --grace-period 0 --force
kubectl apply -f sample-pod.yml --server-side
kubectl apply -f sample-pod.yml --server-side --force-conflicts
```
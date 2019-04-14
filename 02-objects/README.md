# Working with Kubernetes Objects

1. `kubectl run busybox --image=busybox --restart=Never -- ping 1.1.1.1`
2. `kubectl get pods`
3. `kubectl logs busybox`
4. `kubectl get pod busybox -o yaml`
5. `kubectl delete pod busybox`

## Namespaces

1. `kubectl create ns development`
2. `kubectl run nginx --image=nginx --restart=Never -n development`
3. `kubectl get pods`
4. `kubectl get pods -n development`
5. `kubectl run nginx --image=nginx --restart=Never`
6. `kubectl run nginx --image=nginx --restart=Never`
7. `kubectl get pods --all-namespaces`
8. `kubectl delete ns development`
9. `kubectl get pods --all-namespaces`
10. `kubectl delete pod nginx`

## Labels

1. `kubectl run nginx-1 --image=nginx --restart=Never`
2. `kubectl run nginx-2 --image=nginx --restart=Never`
3. `kubectl run redis --image=redis --restart=Never`
4. `kubectl label pod nginx-1 env=dev project=foo`
5. `kubectl label pod nginx-2 env=prod project=foo`
6. `kubectl label pod redis env=prod`
7. `kubectl get pods`
8. `kubectl get pods -l project=foo`
9. `kubectl get pods -l env=prod`
10. `kubectl get pods --show-labels`

## Annotations

1. `kubectl annotate pod nginx-1 desc='my frontend running nginx'`
2. `kubectl describe pod nginx-1`
3. `kubectl delete pods --all`

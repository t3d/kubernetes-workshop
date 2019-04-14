# Pods

1. `kubectl apply -f nginx.yaml`
2. `kubectl get pods -o wide`
3. `kubectl describe pod nginx`
4. `kubectl delete -f nginx.yaml`

## Pod Lifecycle

1. `cat redis.yaml`
2. `kubectl apply -f redis.yaml`
3. `kubectl get pods`
4. `kubectl delete -f redis.yaml`

## Init Containers

1. `cat busybox.yaml`
2. `kubectl apply -f busybox.yaml`
3. `kubectl get pods`
4. `kubectl describe pod busybox`
5. `kubectl logs -f busybox -c container-2`
6. `kubectl delete -f busybox.yaml`

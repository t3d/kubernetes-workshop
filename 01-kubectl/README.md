# Object Management Using `kubectl`

1. `source <(kubectl completion bash)`
2. `kubectl`
3. `kubectl version`
4. `kubectl api-versions`
5. `kubectl api-resources`
6. `kubectl explain pod`

## Kubernetes Object Management

### Imperative commands

1. `kubectl run -i -t busybox --image=busybox --restart=Never --rm`
2. `kubectl create deployment nginx --image=nginx`
3. `kubectl get deployment nginx`
4. `kubectl edit deploy nginx`
5. `kubectl delete deployment/nginx`

### Imperative object configuration

1. `kubectl create -f nginx.yaml`
2. `kubectl replace -f nginx.yaml`
3. `kubectl get -f nginx.yaml`
4. `kubectl delete -f nginx.yaml`

### Declarative object configuration

1. `kubectl apply -f configs/`
2. `kubectl get -f configs/`
3. `kubectl delete -f configs/`

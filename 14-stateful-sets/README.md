# Stateful Sets

1. `cat nginx.yaml`
2. `kubectl apply -f nginx.yaml`
3. `kubectl get po -w`
4. `kubectl get pvc,pv`
5. `kubectl scale --replicas=5 statefulset nginx`
6. `kubectl get po -w`
7. `kubectl scale --replicas=3 statefulset nginx`
8. `kubectl get po -w`
9. `kubectl set image statefulset nginx nginx=nginx:1.15`
10. `kubectl get po -w`
11. `kubectl delete -f nginx.yaml`

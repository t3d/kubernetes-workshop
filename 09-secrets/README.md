# Secrets

1. `cat mysql.yaml`
2. `kubectl apply -f mysql.yaml`
3. `kubectl get secrets`
4. `kubectl describe secret mysql`
5. `kubectl get secret mysql -o yaml`
6. `kubectl get pods`
7. `kubectl describe pod mysql-5d6d5f8f7f-wlbzd`
8. `kubectl exec mysql-5d6d5f8f7f-wlbzd -- env | sort`

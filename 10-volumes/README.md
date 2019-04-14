# Volumes

1. `kubectl describe deploy mysql`
2. `kubectl exec -i -t mysql-5d6d5f8f7f-wlbzd -- mysql -ulobsters -p lobsters`
   1. `SHOW TABLES;`
   2. `CREATE TABLE lobsters (name VARCHAR(255));`
   3. `SHOW TABLES;`
3. `kubectl exec -i -t mysql-5d6d5f8f7f-wlbzd -- sh -c 'kill 1'`
4. `kubectl exec -i -t mysql-5d6d5f8f7f-wlbzd -- mysql -ulobsters -p lobsters`
   1. `SHOW TABLES;`
5. `kubectl apply -f mysql.yaml`
6. `kubectl describe deploy mysql`

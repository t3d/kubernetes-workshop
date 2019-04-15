# [Lobsters](https://lobste.rs/)

1. `cat lobsters-rails-server.yaml`
2. `kubectl apply -f lobsters-rails-server.yaml`
3. `kubectl get svc lobsters-rails-server`
4. [35.205.185.74:31716](http://35.205.185.74:31716/)

## Jobs

1. `cat lobsters-rake-db-schema-load.yaml`
2. `kubectl apply -f lobsters-rake-db-schema-load.yaml`
3. `kubectl get jobs,po`
4. `kubectl logs lobsters-rake-db-schema-load-fhhsj`
5. `cat lobsters-rake-db-seed.yaml`
6. `kubectl apply -f lobsters-rake-db-seed.yaml`
7. `kubectl get jobs,po`
8. `kubectl logs lobsters-rake-db-seed-dgf9b`
9. [35.205.185.74:31716](http://35.205.185.74:31716/)

## Cron Jobs

1. `cat lobsters-script-mail-new-activity.yaml`
2. `cat lobsters-script-post-to-twitter.yaml`
3. `kubectl get cronjobs,jobs,po`
4. `sleep 300`
5. `kubectl get cronjobs,jobs,po`

## Ingress

1. `cat lobsters.yaml`
2. `kubectl apply -f lobsters.yaml`
3. `kubectl get ingress`

## Horizontal Pod Autoscaler

1. `kubectl exec lobsters-rails-server-744c5757d4-pcxlj -- apt update`
2. `kubectl exec lobsters-rails-server-744c5757d4-pcxlj -- apt install stress`
3. `kubectl autoscale deploy lobsters-rails-server --min=1 --max=3 --cpu-percent=80`
4. `kubectl get hpa`
5. `kubectl label hpa lobsters-rails-server app=lobsters`
6. `kubectl describe hpa lobsters-rails-server`
7. `kubectl exec lobsters-rails-server-744c5757d4-pcxlj -- stress --cpu 1 --timeout 1m -v`
8. `kubectl describe hpa lobsters-rails-server`
9. `kubectl get po`

1. `kubectl get all -l app=lobsters`
2. `kubectl delete all -l app=lobsters`
3. `kubectl delete ingress lobsters`
4. `kubectl get all -l app=mysql`
5. `kubectl delete all -l app=mysql`

# Deployments

## Creating a Deployment

1. `kubectl apply -f nginx.yaml`
2. `kubectl get po,rs,deploy`

## Updating a Deployment

1. `kubectl set image deploy nginx nginx=nginx:1.15 --record=true`
2. `kubectl get po,rs`
3. `kubectl rollout status deploy nginx -w`

## Rolling Back a Deployment

1. `kubectl rollout history deploy nginx`
2. `kubectl get deploy nginx -o yaml`
3. `kubectl annotate deploy nginx kubernetes.io/change-cause='update to newest version'`
4. `kubectl rollout history deploy nginx`
5. `kubectl rollout undo deploy nginx --to-revision=1`
6. `kubectl rollout history deploy nginx`
7. `kubectl get rs`

## Pausing and Resuming a Deployment

1. `kubectl rollout pause deploy nginx`
2. `kubectl set image deploy nginx nginx=nginx:1.15 --record=true`
3. `kubectl rollout status deploy nginx -w`
4. `kubectl get rs`
5. `kubectl set image deploy nginx nginx=nginx:1.15-alpine --record=true`
6. `kubectl rollout resume deploy nginx`
7. `kubectl rollout status deploy nginx -w`
8. `kubectl rollout history deploy nginx`

9. `kubectl delete -f nginx.yaml`

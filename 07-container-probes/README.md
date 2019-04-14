# Container Probes

1. `cat nginx.yaml`
2. `kubectl apply -f nginx.yaml`
3. `kubectl get pods`
4. `kubectl edit deploy nginx`
5. `kubectl get pods -w`
6. `kubectl rollout undo deploy nginx`
7. `kubectl exec nginx-64975f8478-lj2hb -- rm -f /usr/share/nginx/html/index.html`
8. `kubectl run -i -t busybox --image=busybox --restart=Never --rm`
   1. `wget -O - nginx`
9. `kubectl exec nginx-64975f8478-llctp -- rm -f /usr/share/nginx/html/index.html`
10. `kubectl delete -f nginx.yaml`

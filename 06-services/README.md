# Services

1. `cat nginx.yaml`
2. `kubectl apply -f nginx.yaml`
3. `kubectl get svc`
4. `kubectl get svc -o wide`
5. `kubectl run -i -t busybox --image=busybox --restart=Never --rm`
   1. `wget -O - nginx-1`
   2. `wget -O - nginx-2.default.svc.cluster.local`
   3. `env | sort`
   4. `wget -O - $NGINX_3_SERVICE_HOST`
   5. `wget -O - --header 'Host: www.google.pl' google`
6. `kubectl get svc`
7. `kubectl get nodes -o wide`
8. [34.76.41.55:30838](http://34.76.41.55:30838)
9. [35.205.224.185:30838](http://34.76.41.55:30838)
10. [34.76.157.172](http://34.76.157.172/)
11. `kubectl delete -f nginx.yaml`

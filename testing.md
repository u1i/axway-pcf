
kubectl get pods --all-namespaces

kubectl run my-app --image=u1ih/hello --port=8080

kubectl expose deployment my-app --type=LoadBalancer --port=8080 --target-port=8080

kubectl get svc

# Shell Access

kubectl exec -it my-app-XXXXXXXXX  -- /bin/sh

# Update
kubectl set image deployment/my-app  my-app=u1ih/hello:10

delete deployment my-app
delete svc my-app

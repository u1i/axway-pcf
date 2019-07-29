kubectl get pods --all-namespaces

kubectl run my-app --image=u1ih/hello --port=8080

kubectl expose deployment my-app --type=LoadBalancer --port=8080 --target-port=8080

kubectl get svc

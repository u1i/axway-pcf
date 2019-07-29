# List all pods
kubectl get pods --all-namespaces

# Deploy test container
kubectl run my-app --image=u1ih/hello --port=8080

# Expose the container
kubectl expose deployment my-app --type=LoadBalancer --port=8080 --target-port=8080

# Get services and public IP
kubectl get svc

# Shell Access
kubectl exec -it my-app-XXXXXXXXX  -- /bin/sh

# Update
kubectl set image deployment/my-app  my-app=u1ih/hello:10

# Delete
delete deployment my-app
delete svc my-app

# GUI
kubectl proxy

http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/

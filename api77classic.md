harbor.rollinghills.cf-app.com/library/api77:1

kubectl create namespace big

kubectl apply -f big.yaml --namespace=big


kubectl run api77 --image=harbor.rollinghills.cf-app.com/library/apim77:1 --port=8080 --namespace=big

kubectl expose deployment  api77 --type=LoadBalancer --port=8080 --target-port=8080 --namespace=big

kubectl expose deployment  api77 --name=apimgr --type=LoadBalancer --port=8075 --target-port=8075 --namespace=big

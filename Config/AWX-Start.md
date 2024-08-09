minikube start --cpus=4 --memory=6g --addons=ingress

alias kubectl="minikube kubectl --"

kubectl config set-context --current --namespace=awx

kubectl get pods

kubectl port-forward svc/awx-service --address 0.0.0.0 8080:80 &> /dev/null &

kubectl get secret awx-admin-password -o jsonpath="{.data.password}" | base64 --decode; echo

kubectl logs -f deployments/awx-operator-controller-manager -c awx-manager

# k8s-command

kubectl apply -f grafana-deployment.yml

kubectl config view

kubectl get pods

kubectl logs <pod-name>

### Get pods names
kubectl get pods -o name

### Delete all pods
kubectl delete $(kubectl get pods -o name)

### Exec
kubectl exec -it <pod-name> sh
ls -lh
df
du

### Get
kubectl get ingress

kubectl get configmap

kubectl get secret

kubectl get deployments

kubectl get services

kubectl get statefulset

kubectl get pvc

kubectl get jobs

### Delete all
kubectl delete ingress --all

kubectl delete configmap --all

kubectl delete secret --all

kubectl delete deployments --all

kubectl delete services --all

kubectl delete statefulset --all

kubectl delete pvc --all

kubectl delete jobs --all

### Get Secret Value
kubectl get secret --namespace <pod-name> -o jsonpath="{.data.mysql-root-password}" | base64 --decode; echo
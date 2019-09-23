# dockerimg


sudo kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml
sudo kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/k8s-manifests/kube-flannel-rbac.yml
sudo kubectl get pods --all-namespaces

kubectl logs --namespace kube-system 
kubectl -n kube-system  delete po,svc --all


• Run the Docker app at port 80. 
docker build -t gcr.io/${PROJECT_ID}/hello-app:v1 .
docker images




• Host the Docker image built on a Kubernetes cluster. 
kubectl create deployment hello-web --image=gcr.io/${PROJECT_ID}/hello-app:v1
kubectl get pods
kubectl expose deployment hello-web --type=LoadBalancer --port 80 --target-port 8080

kubectl get service


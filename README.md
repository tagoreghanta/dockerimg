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

------------
2019-09-23 18:18:38.208312 W | etcdserver: read-only range request "key:\"/registry/clusterroles\" range_end:\"/registry/clusterrolet\" count_only:true " with result "range_response_count:0 size:7" took too long (399.793294ms) to execute
2019-09-23 18:18:38.208697 W | etcdserver: read-only range request "key:\"/registry/mutatingwebhookconfigurations\" range_end:\"/registry/mutatingwebhookconfigurationt\" count_only:true " with result "range_response_count:0 size:5" took too long (563.453292ms) to execute
2019-09-23 18:19:32.514510 W | etcdserver: read-only range request "key:\"/registry/serviceaccounts\" range_end:\"/registry/serviceaccountt\" count_only:true " with result "range_response_count:0 size:7" took too long (506.038583ms) to execute
2019-09-23 18:19:32.514898 W | etcdserver: read-only range request "key:\"/registry/services/endpoints/kube-system/kube-controller-manager\" " with result "range_response_count:1 size:457" took too long (101.596517ms) to execute

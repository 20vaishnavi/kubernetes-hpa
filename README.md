# kubernetes-hpa
create kubernetes horizontal autoscalar

kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/download/v0.3.6/components.yaml

wget -c https://gist.githubusercontent.com/initcron/1a2bd25353e1faa22a0ad41ad1c01b62/raw/008e23f9fbf4d7e2cf79df1dd008de2f1db62a10/k8s-metrics-server.patch.yaml

kubectl patch deploy metrics-server -p "$(cat k8s-metrics-server.patch.yaml)" -n kube-system
kubectl get pods -n kube-system
kubectl create -f hpaexample.yml  kubectl get pods 
 kubectl create -f hpa.yml 
 kubectl get hpa
kubectl get pods -n kube-system
while true; do wget -q -O- http://php-apache.default.svc.cluster.local; done


To verify hpa is working
On another terminal 
kubectl get pods -w




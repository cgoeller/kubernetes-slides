# Kubernetes Demo

```bash
vagrant ssh
cd /vagrant/demo

kubectl run nginx --image=nginx:latest
kubectl expose deployment nginx --port 80 --type NodePort

kubectl create -f nginx.yml
kubectl expose deployment nginx-deployment --type=NodePort

kubectl get services nginx-deployment
minikube service list
curl
```
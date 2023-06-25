# Kubectl Commands


## Installing k8s on macOs m1 silicon

  brew update
  brew install qemu( for m1)/ for others hyper kit
  brew install minikube
  kubectl
  minikube

  minikube start —vm-drive=qemu

  kubectl get nodes
  minikube status

  kubectl get services
  kubectl get pods
  kubectl create -h // help


  ---
  Deployment - abstraction over pods
  Pod - is the smallest unit, But we are creating deployment
  ---

  kubectl create deployment Name —image=image [—dry-run] [options]

  kubectl create deployment ngnix-depl --image=nginx
  kubectl get deployment
  kubectl get pods

  kubectl logs pod-name

  kubectl describe pod pod-name

  kubectl delete deployment deploy-name

  kubectl get replicaset

  kubectl apply -f config_file.yaml


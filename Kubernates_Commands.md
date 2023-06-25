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



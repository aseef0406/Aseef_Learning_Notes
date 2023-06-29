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

  ### Docker
  ---------------
  FROM openjdk:8-jdk-alpine
  COPY target/Docker_Spring_Boot-0.0.1-SNAPSHOT.jar docker_spring_boot_message.jar
  ENTRYPOINT ["java","-jar","/docker_spring_boot_message.jar"]
  -----------------

  docker build --tag=docker_spring_boot_message:latest .

  docker run -p8887:8888 docker_spring_boot_message:latest


  for kube

  start minikube

  eval $(minikube docker-env)       

  docker build -t spring-boot-test .

  kubectl create deployment springboot-kubernetes --image=springboot-kubernetes:1.0 --port=8080







  some references from https://www.kindsonthegenius.com/setup-kubernetes-locally-deploy-springboot-application-step-by-step-tutorial/

# Jenkins-Project

create namespce named jenkins and make it to create
Deployment for each tier in the project (proxy,backend,database) with 2 replica for each
Put all project in namespace called webapp
mount db-credentials in pods on your host machine
Choose which suitable service for grouping each tier
Make sure that the proxy pods commincate with the service that you have select for backend pods 


![Alt text](images/image.png)

![Alt text](images/2024-10-01 at 16.32.47_d6b4e99a.jpg)



## TO Start

kubectl apply -f jenkins-service.yaml

kubectl apply -f jenkins-deployment.yaml

kubectl create serviceaccount jenkins-service-account -n jenkins

kubectl apply -f jenkins-cluster-role.yaml

kubectl apply -f jenkins-cluster-role-binding.yaml

kubectl apply -f jenkins-pv.yaml


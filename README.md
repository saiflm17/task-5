# TASK-5 EXPLANATION

#STEP-1 : am taking a new server with server configurations like server_name, AMI : UBUNTU 24.04 LTS, Instance_Type : t2.medium, key_pair, security_group : All Traffic, EBS : 20 GIB . After launching the server with ssh connection .

#STEP-2 : To change the Root User . by using command .

- COMMAND : sudo -i .

#STEP-3 : So now am installing docker , minikube , kubectl .

- DOCKER :

- COMMAND : yum install docker -y - To install the docker .

- COMMAND : systemctl start docker - To start the docker .

- COMMAND : systemctl status docker - To check the status of the docker .

- MINIKUBE :

- SO Minikube is a single node cluster . So am collecting the link from official document to install the minikube cluster . After am to start the minikube cluster by using command .

- COMMAND : minikube start --driver=docker --force .

- KUBECTL :

-  It is the command-line tool used to interact with a Kubernetes cluster. so am collecting the link from official document to install the kubectl.

-  After am writing a deployment file for an application and the file_name is deployment.yaml .

-  That file its execute by using command .

-  COMMAND : kubectl create -f deployment.yaml - these command works on to execute the file .

-  After deployment file is executed  then PODS are created .

-  In kubernetes THE POD WILL HAVE A CONTAINER INSIDE IT . THE CONTAINER WILL HAVE A APPLICATION ARE RUNNING SUCCESSFULLY INSIDE IT .

-  Now am writing a service file and the file_name is service.yaml .

-  These service file means to expose the deployment file .

-  In Docker we can access the application directly . But in kubernetes we cant access the application directly . so we have to expose the application deployment file .

-  In there are 3 types of services .
      1 . ClusterIP
      2 . NodePort
      3. LoadBalancer

   1. clusterip : it is one of the service so it will give a stable ip address and these service  shows the html format .
 
   2. NodePort : it is a service it will give port numbers from the range 30k To 32767 .
 
   3. LoadBalancer : it is a service it will give DNS name DNS is a Domain Name System . Loadbalancer it distributes the traffic equally .
 
 - COMMAND : kubectl create -f file_name - to execute the file .

 - COMMAND : kubectl get po - to check the list of pods .

 - COMMAND : kubectl get deploy - to check the list of deployments .

 - COMMAND : kubectl get svc - to check the list of services .

 - COMMAND : kubectl describe pod pod_name - to check the pod details .

 - COMMAND : kubectl logs pod_name - pod related logs .

 - In scaling there are two types :

   1. Manual scaling
  
   2. Auto scaling

  - so am using manual scaling by using command .

  - COMMAND : kubectl scale deployment deployment_name --replicas 4 - to increse the pods .

  - COMMAND : kubectl scale deployment deployment_name --replicas 2 - to decrease the pods .
   




Kuberetes :  Open source Container Management tool / Container Orchastration tool.

It is mainely use for autoscaling of containers as per need.(increasing and decresaing the number of containers).

a)It Schedules , run , manage and isolate the containers in all mode (virtual , physical and cloud)

Online platfroms for K8s,
Kubernetes playground
Play with k8s

Cloud based :
GKE - Google kubernetes service
AKS - Azure Kubernetes Service
Amazon EKS 

Tool:
Minicube
kubeadm

K8s Works on Master-node , cluster node , 
1Master - 1 Node
1Master - Number of Nodes
No of Master - No of Nodes

Pod : Using Pod conatiner get monitored.

Container has to create in the POD , and monitored by POD only.

N number of pods can be created in single Node.

N number of Nodes can be created in single cluster.




Flow of K8s

Cluster - Node - POD - Container - Application/microservices

K8s Master slave arch.

1-Master : It works on 4 Parts

a)- Control Manager(CM)-  (actual start=desired state) :  It will control and monitor the work it will try so satisfiy the AS =DS 
b)- kube scheduler     -  (Creating pod in nodes)      :  It will complete the task which is assigned by CM , creating pods in nodes.
c)- etcd cluster       -  (Data Storage )              :  It will store all the record and data of Master Node in it .
d)- API server         -  (Frontend )                  :  It helps all services to communicate with each other.


POD :
Container are created inside the POD and Controlled ,
POD contain IP address , Container are IP less.

Container are tightly coupled in 'pod.

POD get down then new POD will create , old POD will not be created.

Kubelt - POD are controlled by Kubelets.
Kube-proxy - it will monitor all networking task (assiging IP to POD etc.)




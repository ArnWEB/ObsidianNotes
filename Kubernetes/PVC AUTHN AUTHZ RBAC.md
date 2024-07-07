
AuthN->Authenctication : YOU are showin who you are  or not

AuthZ->Authorization: You are authorized for certain action or not

Kube API server is responsible for AuthN + AuthZ

When you run Kubectl :

kubeconfig  stores the user data and cluster information / user

two type of user K8s managed and k8s unmanaged

Authenctiaction way: webhook ,static token , X509 certs , customY

ByDefault Authorization Mode: 1 AlwaysAllow 2 AlwaysDeny 3 RBAC/ABAC

RBAC--Role based access control
ABAC--Attirbute based access control 

to find what mode in authoriztion go to  `cd /etc/kubernetes/manifests` then got to `kube-apiserver.yaml` and check for rbac mode in 3rd row 

Cluster Role binding ---> Cluster level
Role binding --->  Namespace level 
Role ---> Namespace Level (Recommentded)
Cluster Role ---> Both on Namespace lvl and Cluster lvl


1st you have to create roles then you have to bind them ,


Kubectl auth can-i  get pod -n ns --as=system:serviceAccount


***Volumes***

Ephimeral: POD is Ephimeral as when it is deleted all the storage and other resources will be deleted :: not persistent

Disk is added to cluster with pod , so that it can be  persistant , but there arises one problem that shared disk can be deadlock situation.

CSI : Constainer storage Initiative

Volume type:
Cloud: depreciated CSI
emptyDirectory:  storage of node directory bouund to pod life cycle means destroyed when pod destroyed but if crashed it will not removed
hostpath: not reccommend 


PersistentVoulume

Static privisioning: 

Dynamic provisioning does need to calim PV separately 

waitforfirstcustomer 






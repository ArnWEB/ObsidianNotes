- Every Protocol is running in kubernetes  is rather running in GRPC or Rest.
- API server is talking to  etcd in grpc and we means end user mostly call api erver in REST.
- Protbuf is a serialize deserialize language , which is faster tha XML and JSON
- GRPC is able to bidirectional streaming.
- Master Plane Components:
- `1.Kube API server 2.etcd 3.Scheduler 4. Controller Mangaer 5.(optional) Cloud Contoller Manager`
- If your app is aleready deployed , and Kube API server is down, then app will run as it it is , as Master Plane is for only management, means if you want to run update your application then it can caise probem. (**interview**)
- Kube api server has 4 works **Authentication** , **Authorization** , **Admission Controller** , **Monitoing update**
- Admission controller has two type 1. Mutatuion Controller 2.Validation Controller.
- Mutation means chage , its mainly use for controlling addmission controller behaviour means, it can change certain attribute of your deployments,so that it is abidy by organization rules , like you can change cpu usage limit to stck to 500mb any pods that are higher will change to 1000mb
- This is recommended not to change in mutatino controller ,as it can cause productivity use.
- for checking api serer components , you have to go to the master node and cd to /etc/kubernets/
- etcd in database , key value pair , no sql.
- Kubecontroller :  Kubernests controller , mainly supervise that is the component are in desired state , if not goes to api server then goes to kubelet , the make it no schedule, then register to etcd .

- 



- Kubelet is one in Kubelet
- Pod Creation: Kubelete -> CRI -> CRI talk to runC -> runc Create C group -> C group -> CNI to apply Ip -> 
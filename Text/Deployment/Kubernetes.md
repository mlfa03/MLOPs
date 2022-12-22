## Kubernetes

**[back to index](https://github.com/mlfa03/MLOPs/blob/main/README.md)**

Kubernetes is a container platform. Docker can be used to develop and build applications and Kubernetes can be used to run the 
applications on the infrastructure. 

### Kubernetes Features 

* **Multihost container scheduling**: done by Kube scheduler. Assigns pods to nodes at runtime. Checks resources, quality of service, 
policies and user specifications before scheduling. 
* **Scalability and availability**: Kubernetes master can be deployed in a highly available configuration. Multiregion deployments are available. 
* **Flexibility and Modularization**: has a plug and play architecture that allows you to extend architecture when needed. There are several add-ons: 
network drivers, service discovery, container runtime, visualization, command. 
* **Registration**: seamless nodes register themselves with master. 
* **Service discovery**: automatic detection of services and endpoints via DNS or environment variables. 
* **Persistent storage**: pods can use persistent volumes to store data. The data is retained across pod restarts and crashes. 
* **Application upgrades and downgrades**: rolling updates and rollbacks are suported. 
* **Logging and monitoring**: application monitoring is built in. Failures are monitores by the node controller. 

### Kubernetes cluster architecture 

**Master node**: responsible for the overall management of the kubernetes cluster. 


![image](https://user-images.githubusercontent.com/39881974/208985129-c7f417a0-1de4-462e-9827-b4f39142e9c7.png)


* **API server**: is the front end of the kubernetes 
* **Scheduler**: watches created pods, who do not have a node design yet, and designs the pod to run on a specific node. 
* **Controller manager**: runs controllers. These are background threads that run tasks in a cluster. 
* **etcd**: kubernetes database. It stores all cluster data. 
* **kubectl**: to interact with the master node. This is the command line interface with kubernetes. 
* **kubeconfig**: kubectl has a config file called kubeconfig. This file has server information, authentication information to access the API server.
* **worker nodes**: nodes where the application operates. They communicate back with the master node. Worker nodes can be exposed to the internet through load balancers and traffic coming into the node is also handled by kube proxy which is how an end user ends up talking to Kubernetes application. 
* **kubelet process**: communication with a worker node is handled by the kubelet process. It is an agent that communicates with the API server to see 
if pods have been designed to the nodes. It executes the pod containers via the container engine. It mounts and runs pod volume and secrets.It is 
aware of pods and nodes states and responds back to the master. 
* **docker**: runs containers on the node. 
* **pod**: is the smallest unit that can be scheduled as a deployment in kubernetes. These groups of containers share storage, linux namespace, IP addresses...Once pods have been deployed and are running the kubelet process communicates with the pods to check on state and health, and the kube proxy routes any packets to the pods from other resources that might be wanting to communicate with them. 

### Nodes and Pods



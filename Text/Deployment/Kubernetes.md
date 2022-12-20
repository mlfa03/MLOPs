## Kubernetes

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

![image](https://user-images.githubusercontent.com/39881974/208668330-71b1203b-fd72-4a69-bc57-f81e82b1139e.png)

**Master node**: responsible for the overall management of the kubernetes cluster. 

![image](https://user-images.githubusercontent.com/39881974/208671972-f6d0e831-da56-4d4f-a7d5-cb313e29cc70.png)


* **API server**: is the front end of the kubernetes 
* **Scheduler**: watches created pods, who do not have a node design yet, and designs the pod to run on a specific node. 
* **Controller manager**: runs controllers. These are background threads that run tasks in a cluster. 
* **etcd**: kubernetes database. It stores all cluster data. 
* **kubectl**: to interact with the master node. This is the command line interface with kubernetes. 
* **kubeconfig**: kubectl has a config file called kubeconfig. This file has server information, authentication information to access the API server.
* **worker nodes**: nodes where the application operates. They communicate back with the master node. 
* **kubelet process**: communication with a worker node is handled by the kubelet process. It is an agent that communicates with the API server to see 
if pods have been designed to the nodes. It executes the pod containers via the container engine. It mounts and runs pod volume and secrets.It is 
aware of pods and nodes states and responds back to the master. 
* **docker**: runs containers on the node. 


## Kubeflow Pipeline on GCP

**[back to index](https://github.com/mlfa03/MLOPs/blob/main/README.md)**

### System and concept overview

file:///home/mariana.almeida/%C3%81rea%20de%20Trabalho/kubeflow/devops.png![image](https://user-images.githubusercontent.com/39881974/217916407-7d590767-af52-46b5-9798-bde1f15f12c2.png)

Most of the ML systems a large and most of the effort is spent on DevOps. 
Kubeflow was developed to use Kubernetes to standardize and streamline the DevOps work around machine learning. 

Main features of Kubeflow: 
* Leverage containers and Kubernetes so that ML pipelines can be run on the cloud or on premises with Anthos on GKE. 
* Provides a platform for composable, portable, and scalable ML pipelines. 
* Cloud-native, multicloud solution for ML 

**What constitutes a Kubeflow pipeline?**

Containerized implementation of ML tasks:
* Ex: Data import, training, serving, model evaluation 
* Containers provide portability, repeatability and encapsulation 
* A containerized task can invoke other services, such as AI Platform, DataFlow or DataProc. 





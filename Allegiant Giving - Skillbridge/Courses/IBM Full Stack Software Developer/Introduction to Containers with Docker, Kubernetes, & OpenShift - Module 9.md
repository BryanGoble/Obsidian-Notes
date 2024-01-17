# Courses
1. [IBM Full Stack Software Developer Professional](https://www.coursera.org/programs/allegiant-giving-corporation-on-demand-learning-program-mjqmr/professional-certificates/ibm-full-stack-cloud-developer)
	1. [Introduction to Containers with Docker, Kubernetes, & OpenShift](https://www.coursera.org/learn/ibm-containers-docker-kubernetes-openshift/)
# Summary - Week 1

- A container is a unit of software that encapsulates everything needed to build, ship, and run applications.  
- Containers lower deployment time and costs, improve utilization, automate processes, and support next-gen applications (microservices). Major container vendors include Docker, Podman, LXC, and Vagrant. 
- Docker is an open platform used for developing, shipping, and running applications as containers. 
- Docker containers are not a good fit for applications based on monolithic architecture or applications that require high performance or security. 
- Docker architecture consists of the Docker client, the Docker host, and the container registry. 
- The Docker host contains objects such as the Dockerfiles, images, containers, networks, storage volumes, and other objects, such as plugins and add-ons. 
- Docker uses networks to isolate container communications. 
- Docker uses volumes and binds mounts to persist data even after a container stops running. 
- Plugins, such as storage plugins, provide the ability to connect to external storage platforms.

# **Cheat Sheet: Docker CLI**

|Command|Description|
|---|---|
|**curl localhost**|Pings the application.|
|**docker build**|Builds an image from a Dockerfile.|
|**docker build . -t**|Builds the image and tags the image id.|
|**docker CLI**|Start the Docker command line interface.|
|**docker container rm**|Removes a container.|
|**docker images**|Lists the images.|
|**docker ps**|Lists the containers.|
|**docker ps -a**|Lists the containers that ran and exited successfully.|
|**docker pull**|Pulls the latest image or repository from a registry.|
|**docker push**|Pushes an image or a repository to a registry.|
|**docker run**|Runs a command in a new container.|
|**docker run -p**|Runs the container by publishing the ports.|
|**docker stop**|Stops one or more running containers.|
|**docker stop $(docker ps -q)**|Stops all running containers.|
|**docker tag**|Creates a tag for a target image that refers to a source image.|
|**docker –version**|Displays the version of the Docker CLI.|
|**exit**|Closes the terminal session.|
|**export MY_NAMESPACE**|Exports a namespace as an environment variable.|
|**git clone**|Clones the git repository that contains the artifacts needed.|
|**ibmcloud cr images**|Lists images in the IBM Cloud Container Registry.|
|**ibmcloud cr login**|Logs your local Docker daemon into IBM Cloud Container Registry.|
|**ibmcloud cr namespaces**|Views the namespaces you have access to.|
|**ibmcloud cr region-set**|Ensures that you are targeting the region appropriate to your cloud account.|
|**ibmcloud target**|Provides information about the account you’re targeting.|
|**ibmcloud version**|Displays the version of the IBM Cloud CLI.|
|**ls**|Lists the contents of this directory to see the artifacts.|
# **Glossary: Container Basics**

|Term|Definition|
|---|---|
|**Agile**|is an iterative approach to project management and software development that helps teams deliver value to their customers faster and with fewer issues.|
|**Client-server architecture**|is a distributed application structure that partitions tasks or workloads between the providers of a resource or service, called servers, and service requesters, called clients.|
|**A container**|powered by the containerization engine, is a standard unit of software that encapsulates the application code, runtime, system tools, system libraries, and settings necessary for programmers to efficiently build, ship and run applications.|
|**Container Registry**|Used for the storage and distribution of named container images. While many features can be built on top of a registry, its most basic functions are to store images and retrieve them.|
|**CI/CD pipelines**|A continuous integration and continuous deployment (CI/CD) pipeline is a series of steps that must be performed in order to deliver a new version of software. CI/CD pipelines are a practice focused on improving software delivery throughout the software development life cycle via automation.|
|**Cloud native**|A cloud-native application is a program that is designed for a cloud computing architecture. These applications are run and hosted in the cloud and are designed to capitalize on the inherent characteristics of a cloud computing software delivery model.|
|**Daemon-less**|A container runtime that does not run any specific program (daemon) to create objects, such as images, containers, networks, and volumes.|
|**DevOps**|is a set of practices, tools, and a cultural philosophy that automate and integrate the processes between software development and IT teams.|
|**Docker**|An open container platform for developing, shipping and running applications in containers.|
|**A Dockerfile**|is a text document that contains all the commands you would normally execute manually in order to build a Docker image. Docker can build images automatically by reading the instructions from a Dockerfile.|
|**Docker client**|is the primary way that many Docker users interact with Docker. When you use commands such as docker run, the client sends these commands to dockerd, which carries them out. The docker command uses the Docker API. The Docker client can communicate with more than one daemon.|
|**Docker Command Line Interface (CLI)**|The Docker client provides a command line interface (CLI) that allows you to issue build, run, and stop application commands to a Docker daemon.|
|**Docker daemon (dockerd)**|creates and manages Docker objects, such as images, containers, networks, and volumes.|
|**Docker Hub**|is the world's easiest way to create, manage, and deliver your team's container applications.|
|**Docker localhost**|Docker provides a host network which lets containers share your host’s networking stack. This approach means that a localhost in a container resolves to the physical host, instead of the container itself.|
|**Docker remote host**|A remote Docker host is a machine, inside or outside our local network which is running a Docker Engine and has ports exposed for querying the Engine API.|
|**Docker networks**|help isolate container communications.|
|**Docker plugins**|such as a storage plugin, provides the ability to connect external storage platforms.|
|**Docker storage**|uses volumes and bind mounts to persist data even after a running container is stopped.|
|**LXC**|LinuX Containers is a OS-level virtualization technology that allows creation and running of multiple isolated Linux virtual environments (VE) on a single control host.|
|**IBM Cloud Container Registry**|stores and distributes container images in a fully managed private registry.|
|**Image**|An immutable file that contains the source code, libraries, and dependencies that are necessary for an application to run. Images are templates or blueprints for a container.|
|**Immutability**|Images are read-only; if you change an image, you create a new image.|
|**Microservices**|are a cloud-native architectural approach in which a single application contains many loosely coupled and independently deployable smaller components or services.|
|**Namespace**|A Linux namespace is a Linux kernel feature that isolates and virtualizes system resources. Processes which are restricted to a namespace can only interact with resources or processes that are part of the same namespace. Namespaces are an important part of Docker’s isolation model. Namespaces exist for each type of resource, including networking, storage, processes, hostname control and others.|
|**Operating System Virtualization**|OS-level virtualization is an operating system paradigm in which the kernel allows the existence of multiple isolated user space instances, called containers, zones, virtual private servers, partitions, virtual environments, virtual kernels, or jails.|
|**Private Registry**|Restricts access to images so that only authorized users can view and use them.|
|**REST API**|A REST API (also known as RESTful API) is an application programming interface (API or web API) that conforms to the constraints of REST architectural style and allows for interaction with RESTful web services.|
|**Registry**|is a hosted service containing repositories of images which responds to the Registry API.|
|**Repository**|is a set of Docker images. A repository can be shared by pushing it to a registry server. The different images in the repository can be labelled using tags.|
|**Server Virtualization**|Server virtualization is the process of dividing a physical server into multiple unique and isolated virtual servers by means of a software application. Each virtual server can run its own operating systems independently.|
|**Serverless**|is a cloud-native development model that allows developers to build and run applications without having to manage servers.|
|**Tag**|A tag is a label applied to a Docker image in a repository. Tags are how various images in a repository are distinguished from each other.|
# Ingress Objects vs. Ingress Controller

In Kubernetes, external access to cluster services is overseen by Ingress, consisting of two core components: the Ingress API object and the Ingress controller. Let's understand these elements and their collaborative functionality.

## Ingress objects

The [Ingress](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.28/#ingress-v1-networking-k8s-io) acts as a supervisor for external access, exposing routes from outside the cluster to internal [services](https://kubernetes.io/docs/concepts/services-networking/service/), mainly focusing on HTTP and HTTPS traffic. It adheres to rules defined on the Ingress resource to regulate traffic routing.

It doesn't manage arbitrary ports or protocols. Instead, it can provide services with externally accessible URLs, balance traffic, handle SSL/TLS termination, and enable name-based virtual hosting. For non-HTTP and non-HTTPS services, specific service types such as [Service.Type=NodePort](https://kubernetes.io/docs/concepts/services-networking/service/#type-nodeport) or [Service.Type=LoadBalancer](https://kubernetes.io/docs/concepts/services-networking/service/#loadbalancer) are typically used.

## Ingress controllers

On the operational side, the Ingress controller is the deployed cluster resource responsible for implementing rules specified by the Ingress API object. Unlike certain controllers that automatically run as part of the kube-controller-manager binary, the [Ingress controller](https://kubernetes.io/docs/concepts/services-networking/ingress-controllers/) requires explicit activation for the Ingress resource to function. Its primary role is to execute the directives outlined in the Ingress, commonly utilizing a load balancer or setting up additional frontends to handle incoming traffic.

## Ingress objects vs Ingress controllers

|Feature|Ingress Objects|Ingress Controllers|
|---|---|---|
|Definition|API object managing external access to services|Cluster resource implementing rules specified by Ingress|
|Primary Function|Regulates external access routing|Implements rules, fulfilling the Ingress|
|Configuration Source|Rules defined on the Ingress resource|Reads and processes information from the Ingress object|
|Traffic Handling|Manages HTTP and HTTPS routes|Utilizes load balancer, configures frontends for traffic|
|Activation|Active upon configuration with Ingress resource|Must be explicitly running for Ingress to function|
|Handling Protocols|Focused on HTTP and HTTPS|Implements rules for various protocols and ports|
|Automatic Startup|Activated with configuration|Requires explicit activation in the cluster|
|Analogy|Traffic rule set for the cluster|Executor, similar to Nginx instance handling rules|
# Kubernetes Antipatterns

In Kubernetes, identifying and avoiding anti-patterns is crucial for maintaining a robust container orchestration environment. These misleading practices may initially appear effective but can lead to complications. This reading explores ten prevalent Kubernetes anti-patterns and recommends alternative practices for a smoother and more sustainable deployment.

### 1. Avoid baking configuration in container images

Containers offer the advantage of using a consistent image throughout the production process. To achieve adaptability across different environments, building images without embedding configuration directly into containers is essential.

**Issue:** Problems arise when images contain environment-specific artifacts that deviate from the tested version, necessitating image rebuilds and risking inadequately tested versions in production. Identification of environment-dependent container images involves spotting features like hardcoded IP addresses, passwords, and environment-specific prefixes.

**Best practice:** Create generic images independent of specific runtime settings. Containers enable the consistent use of a single image throughout the software lifecycle, promoting simplicity and efficiency.

### 2. Separate application and infrastructure deployment

Infrastructure as Code (IaC) allows defining and deploying infrastructure like writing code. While deploying infrastructure through a pipeline is advantageous, separating infrastructure and application deployment is crucial.

**Issue:** Using a single pipeline for both infrastructure and application deployment leads to resource and time wastage, especially when changes in application code outpace infrastructure changes.

**Best practice:** Split infrastructure and application deployment into separate pipelines to optimize efficiency and resource utilization.

### 3. Eliminate specific order in deployment

Maintaining application stability despite delays in dependencies is crucial in container orchestration. Unlike traditional fixed startup orders, Kubernetes and containers initiate components simultaneously.

**Issue:** Challenges arise when poor network latency disrupts communication, potentially causing pod crashes or temporary service unavailability.

**Best practice:** Proactively anticipate failures, establish frameworks to minimize downtime, and adopt strategies for simultaneous component initiation to enhance application resilience.

### 4. Set memory and CPU limits for pods problem

The default Kubernetes setting without specified resource limits allows an application to potentially monopolize the entire cluster, causing disruptions.

**Best practice:** Establish resource limits for all applications, conduct a thorough examination of each application's behavior under various conditions, and strike the right balance to optimize cluster performance.

### 5. Avoid pulling the latest tag in production problem

Using the "latest" tag in production leads to unintended pod crashes as images are pulled down sporadically, lacking specificity.

**Best practice:** Use specific and meaningful image tags, maintain the immutability of container images, store data outside containers in persistent storage, and avoid modifying containers post-deployment for safer and more repeatable deployments.

### 6. Segregate production and non-production workloads problem

Relying on a single cluster for all operational needs poses challenges. Security concerns arise from default permissions and complications with non-namespaced Kubernetes resources.

**Best practice:** Establish a second cluster exclusively for production purposes, avoiding complexities associated with multi-tenancy. Maintain at least two clusters—one for production and one for non-production.

### 7. Refrain from ad-hoc deployments with kubectl edit/patch problem

Configuration drift occurs when multiple environments deviate due to unplanned deployments or changes, leading to failed deployments.

**Best practice:** Conduct all deployments through Git commits for comprehensive history, precise knowledge of cluster contents, and easy recreation or rollback of environments.

### 8. Implement health checks with liveness and readiness probes problem

Neglecting health checks can lead to various issues. Overly complex health checks with unpredictable timings can cause internal denial-of-service attacks within the cluster.

**Best practice:** Configure health probes for each container, use liveness and readiness probes, and prioritize robust health checks for reliable application responsiveness.

### 9. Prioritize secret handling and use vault problem

Embedding secrets directly into containers is poor practice. Using multiple secret handling methods or complex injection mechanisms can complicate local development and testing.

**Best practice:** Use a consistent secret handling strategy, consider HashiCorp Vault, handle secrets uniformly across environments, and pass them to containers during runtime for enhanced resilience and security.

### 10. Use controllers and avoid running multiple processes per container problem

Directly using pods in production poses limitations. Pods lack durability, automatic rescheduling, and data retention guarantees. Running multiple processes in a single container without controllers can lead to issues.

**Best practice:** Utilize Deployment with a replication factor, define one process per container, use multiple containers per pod if necessary, and leverage workload resources like Deployment, Job, or StatefulSet for reliability and scalability.

# Summary - Week 2

- Container orchestration automates the container lifecycle resulting in faster deployments, reduced errors, higher availability, and more robust security. 
- Kubernetes Is a highly portable, horizontally scalable, open-source container orchestration system with automated deployment and simplified management capabilities.  
- Kubernetes architecture consists of a control plane and one or more worker planes. 
- A control plane includes controllers, an API server, a scheduler, and an etcd. 
- A worker plane includes nodes, a kubelet, container runtime, and kube-proxy. 
- Kubernetes objects include Namespaces, Pods, ReplicaSets, Deployments, and Services. 
- Namespaces help in isolating groups of resources within a single cluster. 
- Pods represent a process or an instance of an app running in the cluster. 
- ReplicaSets create and manage horizontally scaled running Pods. 
- Deployments provide updates for Pods and ReplicaSets. 
- A service in Kubernetes is a REST object that provides policies for accessing the pods and cluster. 
- Kubernetes capabilities include automated rollouts and rollbacks, storage orchestration, horizontal scaling, automated bin packing, secret and configuration management, Ipv4/Ipv6 dual-stack support, batch execution, self-healing, service discovery, load balancing, and extensible design. 
- Services in Kubernetes are REST objects that provide policies for accessing the pods and cluster. ClusterIP provides Inter-service communication within the cluster; a NodePort Service creates and routes the incoming requests automatically to the ClusterIP Service; the External Load Balancer, or ELB, creates NodePort and ClusterIP Services automatically and External Name service represents external storage as well as enables Pods from different namespaces to talk to each other.
- Ingress is an API object that provides routing rules to manage external users' access to multiple services in a Kubernetes cluster; whereas using a DaemonSet ensures that there is at least one copy of the pod on all nodes; a StatefulSet manages stateful applications, manages Pod deployment and scaling, maintains a sticky identity for each Pod request and provides persistent storage volumes for your workloads and lastly a Job creates pods and tracks the Pod completion process; Jobs are retried until completed.
# **Cheat Sheet: Understanding Kubernetes Architecture**

|Command|Description|
|---|---|
|**for …do**|Runs a for command multiple times as specified.|
|**kubectl apply**|Applies a configuration to a resource.|
|**kubectl config get-clusters**|Displays clusters defined in the kubeconfig.|
|**kubectl config get-contexts**|Displays the current context.|
|**kubectl create**|Creates a resource.|
|**kubectl delete**|Deletes resources.|
|**kubectl describe**|Shows details of a resource or group of resources.|
|**kubectl expose**|Exposes a resource to the internet as a Kubernetes service.|
|**kubectl get**|Displays resources.|
|**kubectl get pods**|Lists all the Pods.|
|**kubectl get pods -o wide**|Lists all the Pods with details.|
|**kubectl get deployments**|Lists the deployments created.|
|**kubectl get services**|Lists the services created.|
|**kubectl proxy**|Creates a proxy server between a localhost and the Kubernetes API server.|
|**kubectl run**|Creates and runs a particular image in a pod.|
|**kubectl version**|Prints the client and server version information.|
# **Glossary: Kubernetes Basics**

|Term|Definition|
|---|---|
|**Automated bin packing**|Increases resource utilization and cost savings using a mix of critical and best-effort workloads.|
|**Batch execution**|Manages batch and continuous integration workloads and automatically replaces failed containers, if configured.|
|**Cloud Controller Manager**|A Kubernetes control plane component that embeds cloud-specific control logic. The cloud controller manager lets you link your cluster into your cloud provider's API, and separates out the components that interact with that cloud platform from components that only interact with your cluster.|
|**Cluster**|A set of worker machines, called nodes, that run containerized applications. Every cluster has at least one worker node.|
|**Container Orchestration**|Container orchestration is a process that automates the container lifecycle of containerized applications.|
|**Container Runtime**|The container runtime is the software that is responsible for running containers.|
|**Control Loop**|A non-terminating loop that regulates the state of a system. A thermostat is an example of a control loop.|
|**Control plane**|The container orchestration layer that exposes the API and interfaces to define, deploy, and manage the lifecycle of containers.|
|**Controller**|In Kubernetes, controllers are control loops that watch the state of your cluster, then make or request changes where needed. Each controller tries to move the current cluster state closer to the desired state.|
|**Data (Worker) Plane**|The layer that provides capacity such as CPU, memory, network, and storage so that the containers can run and connect to a network.|
|**DaemonSet**|Ensures a copy of a Pod is running across a set of nodes in a cluster.|
|**Declarative Management**|A desired state that can be expressed (for example, the number of replicas of a specific application),and Kubernetes will actively work to ensure that the observed state matches the desired state.|
|**Deployment**|An object that provides updates for both Pods and ReplicaSets. Deployments run multiple replicas of an application by creating ReplicaSets and offering additional management capabilities on top of those ReplicaSets. In addition, deployments are suitable for stateless applications.|
|**Designed for extensibility**|Adds features to your cluster without adding or modifying source code.|
|**Docker Swarm**|automates the deployment of containerized applications but was designed specifically to work with Docker Engine and other Docker tools making it a popular choice for teams already working in Docker environments.|
|**Ecosystem**|A composition of services, support and tools that are widely available. The Kubernetes ecosystem is a large, rapidly growing ecosystem where its services, support, and tools are widely available.|
|**etcd**|A highly available key value store that contains all the cluster data. For any deployment, the deployment configuration is stored in etcd. It is the source of truth for the state in a Kubernetes cluster, and the system works to bring the cluster state into line with what is stored in etcd.|
|**Eviction**|Process of terminating one or more Pods on Nodes.|
|**Imperative commands**|Create, update, and delete live objects directly.|
|**Imperative Management**|Defining steps and actions to get to a desired state.|
|**Ingress**|An API object that manages external access to the services in a cluster, typically HTTP.|
|**IPv4/IPv6 dual stack**|Assigns both IPv4 and IPv6 addresses to Pods and Services.|
|**Job**|A finite or batch task that runs to completion.|
|**Kubectl**|Also known as kubectl Command line tool for communicating with a Kubernetes cluster's control plane, using the Kubernetes API.|
|**Kubelet**|The kubelet is the primary "node agent" that runs on each node. The kubelet takes a set of PodSpecs (a YAML or JSON object that describes a pod) provided primarily through the apiserver and ensures that the containers described in those PodSpecs are running and healthy. The kubelet doesn't manage containers which were not created by Kubernetes.|
|**Kubernetes**|is the de facto open-source platform standard for container orchestration. It was developed by Google and is maintained by the Cloud Native Computing Foundation (CNCF). Kubernetes automates container management tasks, like deployment, storage provisioning, load balancing and scaling, service discovery, and fixing failed containers. Its open-source toolset and wide array of functionalities are very attractive to leading cloud providers, who both support it, and in some cases, also offer fully managed Kubernetes services.|
|**Kubernetes API**|The application that serves Kubernetes functionality through a RESTful interface and stores the state of the cluster.|
|**Kubernetes API Server**|The Kubernetes API server validates and configures data for the api objects which include pods, services, replication controllers, and others. The API Server services REST operations and provides the frontend to the cluster's shared state through which all other components interact.|
|**Kubernetes Controller Manager**|Runs all the controller processes that monitor the cluster state and ensures that the actual state of a cluster matches the desired state. Examples of controllers that ship with Kubernetes are the replication controller, endpoints controller, namespace controller, and service accounts controller.|
|**Kubernetes Cloud Controller Manager**|A Kubernetes control plane component that embeds cloud-specific control logic. The cloud controller manager lets you link your cluster into your cloud provider's API, and separates out the components that interact with that cloud platform from components that only interact with your cluster.|
|**Kubernetes Proxy**|A network proxy that runs on each node in a cluster. This proxy maintains network rules that allow communication to Pods running on nodes—in other words, communication to workloads running on the cluster. The user must create a service with the apiserver API to configure the proxy.|
|**kube-scheduler**|Control plane component that watches for newly created Pods with no assigned node, and selects a node for them to run on.|
|**Label Selector**|Allows users to filter a list of resources based on labels.|
|**Labels**|Tags objects with identifying attributes that are meaningful and relevant to users.|
|**Load balancing**|Balances traffic across Pods for better performance and high availability.|
|**Marathon**|is an Apache Mesos framework. Apache Mesos is an open-source cluster manager developed by UC Berkeley. It lets users scale container infrastructure through the automaton of most management and monitoring tasks.|
|**Namespace**|An abstraction used by Kubernetes to support isolation of groups of resources within a single cluster.|
|**Node**|The worker machine in a Kubernetes cluster. User applications are run on nodes. Nodes can be virtual or physical machines. Each node is managed by the control plane and is able to run Pods.|
|**Nomad**|(Hashicorp) is a free and open-source cluster management and scheduling tool that supports Docker and other applications on all major operating systems across all infrastructure, whether on-premises or in the cloud. This flexibility lets teams work with any type and level of workload.|
|**Object**|An entity in the Kubernetes system. The Kubernetes API uses these entities to represent the state of your cluster.|
|**Persistence**|Ensures that an object exists in the system, until the object is modified or removed.|
|**Preemption**|Logic in Kubernetes helps a pending Pod to find a suitable Node by evicting low priority Pods existing on that Node.|
|**Self-healing**|Restarts, replaces, reschedules, and kills failing or unresponsive containers.|
|**Service**|An abstract way to expose an application running on a set of Pods as a network service.|
|**Service Discovery**|Discovers Pods using their IP addresses or a single DNS name.|
|**StatefulSet**|Manages the deployment and scaling of a set of Pods, and provides guarantees about the ordering and uniqueness of these Pods.|
|**Storage**|A data store that supports persistent and temporary storage for Pods.|
|**Storage Orchestration**|Automatically mounts your chosen storage system whether from local storage, network storage, or public cloud.|
|**Pod**|The smallest and simplest Kubernetes object. Represents a process running in a cluster; it also represents a single instance of an application running in a cluster. Usually, a Pod wraps a single container but, in some cases encapsulates multiple tightly coupled containers that share resources.|
|**Proxy**|In computing, a proxy is a server that acts as an intermediary for a remote service.|
|**ReplicaSet**|A ReplicaSet (aims to) maintain a set of replica Pods running at any given time.|
|**Workload**|A workload is an application running on Kubernetes.|
# Deployment Strategies

## Overview

A Kubernetes deployment strategy defines an application’s lifecycle that achieves and maintains the configured state for objects and applications in an automated manner. Effective deployment strategies minimize risk.

Kubernetes deployment strategies are used to: 

- Deploy, update, or rollback ReplicaSets, Pods, Services, and Applications 
- Pause/Resume Deployments 
- Scale Deployments manually or automatically 
## Types of deployment strategies

The following are six types of deployment strategies:

1. Recreate
2. Rolling
3. Blue/green
4. Canary
5. A/B testing
6. Shadow   

You can use either a single deployment strategy or a combination of multiple deployment strategies.
## Recreate strategy 

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/S0OHGQciTMiDhxkHIuzIZw_59fd9b955e3749cd8653f50a997075f1_Recreate-Strategy.png?expiry=1705536000000&hmac=VZUImw_VRVl95Ow_HxQA755mYBSmcNBDWgP6weduBpo)

In the recreate strategy, Pods running the live version of the application are all shut down simultaneously, and a new version of the application is deployed on newly created Pods. 

Recreate is the simplest deployment strategy. There is a short downtime between the shutdown of the existing deployment and the new deployment. 

Recreate strategy steps include:

1. A new version of the application (v2) is ready for deployment.
2. All Pods running the current version (v1) are shut down or deleted.
3. New (v2) Pods are created.  

The rollback process is completed in the reverse order, replacing version 2 (v2) with version 1 (v1).

|**Pros**|**Cons**|
|---|---|
|Simple setup|Short downtime occurs between shutdown and new deployment|
|Application version completely replaced||
## Rolling (ramped) strategy 

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/X2UzR6YmTGSlM0emJmxkkw_d9be2366ede249569c7c574db5d75cf1_Rolling-Ramped-Strategy.png?expiry=1705536000000&hmac=qJpX1hVfDhhv7xTcNTnIk8roLG_9RdQpd2OCjdiXcGk)

In a rolling strategy, each Pod is updated one at a time. A single v1 Pod is replaced with a new v2 Pod. Each v1 Pod is updated in this way until all Pods are v2. During a rolling strategy update, there is hardly any downtime since users are directed to either version.

Rolling strategy steps include:

1. A new version of the application (v2) is ready for deployment.
2. One of the Pods running the current version (v1) is shut down or deleted.
3. A new (v2) Pod is created to replace the (v1) Pod that was removed.
4. Steps 2 and 3 are repeated until all (v1) Pods are removed and replaced with (v2) Pods.

The rollback process is reversed, where v2 Pods are replaced by v1 Pods. 

|**Pros**|**Cons**|
|---|---|
|Simple setup|Rollout/rollback takes time|
|Suitable for stateful applications that need to handle rebalancing of the data|You cannot control traffic distribution|
## Blue/green strategy

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/NFTOHT_BSvmUzh0_wfr5jw_81599343d2f2432493a079dd15427cf1_Blue-green-strategy.png?expiry=1705536000000&hmac=ATnyovTdityaX2Mju8NDcoIpOn9PP4Rp09QTpPhbS_Y)

In a blue/green strategy, the blue environment is the live version of the application. The green environment is an exact copy that contains the deployment of the new version of the application. The green environment is thoroughly tested. Once all changes, bugs, and issues are addressed, user traffic is switched from the blue environment to the green environment.

Blue/green strategy steps include:

1. Create a new environment identical to the current production environment.
2. Design the new version and test it thoroughly until it is ready for production.
3. Route all user traffic to the new version. 

To perform a rollback, switch the environments back.

|**Pros**|**Cons**|
|---|---|
|Instant rollout/rollback (no downtime)|Expensive (requires double resources)|
|New version is available immediately to all users|Rigorous testing required before releasing to production|
||Handling stateful applications is difficult|

## Canary strategy

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/0WrU-4r7Qbqq1PuK-3G6Kg_6ca8301e22aa4901867272f13d0f43f1_Canary-Strategy.png?expiry=1705536000000&hmac=IQp5HTqQxoS7tET1nQmbsBMv0M_O6j3HsaG3DwV5_dw)

In a canary strategy, the new version of the application is tested using a small set of random users alongside the current live version of the application. Once the new version of the application is successfully tested, it is then rolled out to all users. 

Canary strategy steps include:

1. Design a new version of the application.
2. Route a small sample of user requests to the new version.
3. Test for efficiency, performance, bugs, and issues, and rollback as needed.
4. Repeat steps 1 to 3. Once all issues are resolved, route all traffic to the new version. 

Rollback has no downtime since few users are exposed to the new version.

|**Pros**|**Cons**|
|---|---|
|Convenient for reliability, error, and performance monitoring|Slow rollout, gradual user access|
|Fast rollback||
## A/B testing strategy

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2qr5RL7vRHmq-US-7_R5jQ_00cb25ca0f5748569d238f17d071c9f1_AB-Testing.png?expiry=1705536000000&hmac=edLQsuQH9_QECy_1RLeyjkMnQhLzdegEKLJbUpBUb8Q)

The A/B testing strategy, also known as split testing, evaluates two versions of an application (version A and version B). With A/B testing, each version has features that cater to different sets of users. You can select which version is best for global deployment based on user interaction and feedback. 

A/B testing strategy steps include:

1. Design a new version of the application by adding mostly UI features.
2. Identify a small set of users based on conditions like weight, cookie value, query parameters, geolocalization, browser version, screen size, operating system, and language.
3. Route requests from the user set to the new version.
4. Check for bugs, efficiency, performance, and issues.
5. Once all issues are resolved, route all traffic to the new version.

Rollbacks can be implemented, but downtime can impact the user.

| **Pros** | **Cons** |
| ---- | ---- |
| Multiple versions can run in parallel | Requires intelligent load balancer |
| Full control over traffic distribution | Difficult to troubleshoot errors for a given session, distributed tracing becomes mandatory |
## Shadow strategy

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/xJnAA_d8T8GZwAP3fP_BRw_e7f8f2808ba44abe850a8d234b0567f1_Shadow-Strategy.png?expiry=1705536000000&hmac=toWj8p8fnNvbbCGDandDmsDpHTippZumj30fP7wUI5o)

In a shadow strategy, a “shadow version” of the application is deployed alongside the live version. User requests are sent to both versions, and both handle all requests, but the shadow version does not forward responses back to the users. This lets developers see how the shadow version performs using real-world data without interrupting user experience.

To perform a rollback, switch the environments back.

| **Pros** | **Cons** |
| ---- | ---- |
| Performance testing with production traffic | Expensive (double resources) |
| No user impact | Not a true user test, can lead to misinterpreted results |
| No downtime | Complex setup |
|  | Requires monitoring for two environments |
## Deployment strategies summary

|**Strategy**|**Zero Downtime**|**Real Traffic Testing**|**Targeted Users**|**Cloud Cost**|**Rollback Duration**|**NegativeUser Impact**|**Complexity of Setup**|
|---|---|---|---|---|---|---|---|
|**Recreate**<br><br>Version 1 is removed then version 2 is rolled out|**X**|**X**|**X**|**•--**|**•••**|**•••**|**- - -**|
|**Ramped**<br><br>Version 1 is replaced by a slow rollout of version 2|**✓**|**X**|**X**|**•--**|**•••**|**•--**|**•--**|
|**Blue/Green**<br><br>Version 2 is released together with version 1, then the traffic is switched to version 2|**✓**|**X**|**X**|**•••**|**- - -**|**••-**|**••-**|
|**Canary**<br><br>Version 2 is first released to a subset of users, then fully rolled out when production ready|**✓**|**✓**|**X**|**•--**|**•--**|**•--**|**••-**|
|**A/B Testing**<br><br>Version 2 is only released to a subset of users with specific traits|**✓**|**✓**|**✓**|**•--**|**•--**|**•--**|**•••**|
|**Shadow**<br><br>Version 2 receives real-world traffic together with version A but doesn’t respond to users|**✓**|**✓**|**X**|**•••**|**- - -**|**- - -**|**•••**|

To create a good strategy:

- Consider the product type and the target audience 
- Shadow and canary strategies use live user requests, as opposed to using a sample of users.  
- The A/B testing strategy is useful if the version of the application requires minor tweaks or UI feature changes. 
- The blue/green strategy is useful if your version of the application is complex or critical and needs proper monitoring with no downtime during deployment. 
- The canary strategy is a good choice if you want zero downtime and are comfortable exposing your version of the application to the public.  
- A rolling strategy gradually deploys the new version of the application. There is no downtime, and it is easy to roll back. 
- The recreate strategy is a good choice if the application is not critical and users aren’t impacted by a short downtime.
# Summary - Week 3

- A ReplicaSet enables scaling by creating or deleting pods.
- A ReplicaSet always tries to match the actual state to the desired state.
- Autoscaling enables scaling as needed at the cluster or node level, and the pod level.
- Autoscaler types include horizontal pod (HPA), vertical pod (VPA), and cluster (CA). 
- Rolling updates roll out app changes in a controlled and automated way.
- Rolling updates and rollback can be performed using all-at-once and one-at-a-time strategies.
- ConfigMaps are used to provide variables for your application.
- Secrets are used to provide sensitive information to your application.
- Binding an external Service to your deployment automatically provides the credentials to use the Service inside the code.
- Binding manages configuration and credentials for back-end Services while protecting sensitive data.
# **Cheat Sheet: Managing Applications with Kubernetes**

|Command|Description|
|---|---|
|**kubectl autoscale deployment**|Autoscales a Kubernetes Deployment.|
|**kubectl create configmap**|Creates a ConfigMap resource.|
|**kubectl get deployments -o wide**|Lists deployments with details.|
|**kubectl get hpa**|Lists Horizontal Pod Autoscalers (hpa)|
|**kubectl scale deployment**|Scales a deployment.|
|**kubectl set image deployment**|Updates the current deployment.|
|**kubectl rollout**|Manages the rollout of a resource.|
|**kubectl rollout restart**|Restarts the resource so that the containers restart.|
|**kubectl rollout undo**|Rollbacks the resource.|
# **Glossary: Managing Applications with Kubernetes**

|Term|Definition|
|---|---|
|**Cluster Autoscaler**|Also known as CA. An API resource that autoscales the cluster itself, increasing and decreasing the number of available nodes that pods can run on.|
|**Config Map**|An API object used to store non-confidential data in key-value pairs. Pods can consume ConfigMaps as environment variables, command-line arguments, or as configuration files in a volume.|
|**Horizontal Pod Autoscaler**|Also known as:HPA An API resource that automatically scales the number of Pod replicas based on targeted CPU utilization or custom metric targets.|
|**Linguistic Analysis**|Detects the tone in a given text.|
|**IBM Cloud catalog**|provides various Services that range from visual recognition to natural language processing and creating chatbots.|
|**Persistent Volume**|An API object that represents a piece of storage in the cluster. Available as a general, pluggable resource that persists beyond the lifecycle of any individual Pod.|
|**Persistent Volume Claim**|Claims storage resources defined in a PersistentVolume so that it can be mounted as a volume in a container.|
|**Rolling Updates**|Provide a way to roll out application changes in an automated and controlled fashion throughout your pods. Rolling updates work with pod templates such as deployments. Rolling updates allow for rollback if something goes wrong.|
|**Secrets**|Stores sensitive information, such as passwords, OAuth tokens, and ssh keys.|
|**Service binding**|is the process needed to consume external Services or backing Services, including REST APIs, databases, and event buses in your applications.|
|**Tone Analyzer Service**|is used for explaining service binding. This IBM Cloud Service uses linguistic analysis to detect tone in a given text.|
|**Vertical Pod Autoscaler also known as VPA**|An API resource that adds resources to an existing machine. A VPA lets you scale a service vertically within a cluster.|
|**Volume**|A directory containing data, accessible to multiple containers in a Pod.|
|**Volume Mount**|entails mounting of the declared volume into a container in the same Pod.|
|**Volume Plugin**|A Volume Plugin enables integration of storage within a Pod.|
# Summary - Week 4

- OpenShift® is an enterprise-ready Kubernetes container platform built for open hybrid cloud. 
- OpenShift is easier to use, integrates with Jenkins, and has more services and features. 
- Custom resource definitions (CRDs) extend the Kubernetes API.
- CRDs paired with custom controllers create new, declarative APIs in Kubernetes.
- Operators use CRDs and custom controllers to automate cluster tasks.
- A build is a process that transforms inputs into an object.
- An ImageStream is an abstraction for referencing container images in OpenShift.
- A service mesh provides traffic management to control the flow of traffic between services, security to encrypt traffic between services, and observability of service behavior to troubleshoot and optimize applications.
- Istio is a service mesh that supports four concepts of connection, security, enforcement, and observability. It is commonly used with Microservices applications.
- Istio provides service communication metrics for basic service monitoring needs: latency, traffic, errors, and saturation.
# **Cheat Sheet: OpenShift CLI**

|Command|Description|
|---|---|
|**oc get**|Displays a resource.|
|**oc project**|Switches to a different project.|
|**oc version**|Displays version information|
# **Glossary: OpenShift Basics**

|Term|Definition|
|---|---|
|**A/B testing**|Strategy is mostly used for testing new features in front-end applications. It is used to evaluate two versions of the application namely A and B, to assess which one performs better in a controlled environment. The two versions of the applications differ in terms of features and cater to different sets of users. Based on the interaction and responses received from the users such as feedback, you can choose one of the versions of the application that can be deployed globally into production.|
|**Build**|The process of transforming inputs into a resultant object.|
|**BuildConfig**|An OpenShift-specific object that defines the process for a build to follow. The build process makes use of the input sources and the build strategy. The BuildConfig is the blueprint, and the build is an instance of that blueprint.|
|**Canary Deployments**|Aims to deploy the new version of the application by gradually increasing the number of users. The canary deployment strategy uses the real users to test the new version of the application. As a result, bugs and issues can be detected and fixed before the new version of the application is deployed globally for all the users.|
|**Circuit breaking**|A method to prevent errors in one microservice from cascading to other microservices.|
|**Configuration Change**|A trigger that causes a new build to run when a new BuildConfig resource is created.|
|**Control Plane**|The control plane takes the desired configuration and its view of the services and dynamically programs and updates the proxy servers as the environment changes.|
|**Custom build strategy**|Requires you to define and create your own builder image.|
|**Custom builder images**|Are regular Docker images that contain the logic needed to transform the inputs into the expected output.|
|**CRDs**|Custom code that defines a resource to add to your Kubernetes API server without building a complete custom server.|
|**Custom controllers**|Reconcile the custom resources (CRDs) actual state with its desired state.|
|**Data plane**|Communication between services is handled by the data plane. If a service mesh is absent, the network cannot identify the type of traffic that flows, the source, and the destination and make any necessary decisions.|
|**Enforceability (Control)**|Istio provides control by enforcing policies across an entire fleet and ensures resources are fairly distributed among consumers.|
|**Envoy proxy**|All network traffic is subject to or intercepted by a proxy, called Envoy, used by the service mesh and allows many features depending on the configuration.|
|**Human operators**|Understand the systems they control. They know how to deploy services and how to recognize and fix problems.|
|**Image Change**|A trigger to rebuild a containerized application when a new or updated version of an image is available. For example, if an application is built using a Node.js base image, that image will be updated as security fixes are released and other updates occur.|
|**ImageStream**|An abstraction for referencing container images within OpenShift. Each image contains an ID, or digest, that identifies it. ImageStreams do not contain image data but rather are pointers to image digests.|
|**ImageStream Tag**|An identity to the pointer in an ImageStream that points to a certain image in a registry.|
|**Istio**|A platform-independent and popular service mesh platform, often used with Kubernetes. It intelligently controls the flow of traffic and API calls between services, conducts a range of tests and reduces the complexity of managing network services. Istio secures services through authentication, authorization, and encryption. Istio provides control by defining policies that can be enforced across an entire fleet. With Istio, you can observe traffic flow in your mesh so you can trace call flows, dependencies, and you can view service communication metrics such as latency, traffic, errors and saturation.|
|**Man-in-the-middle attacks**|A man-in-the-middle (MiTM) attack is a type of cyber-attack where the attacker secretly intercepts and relays messages between two parties who believe they are communicating directly with each other. The attack is a type of eavesdropping in which the attacker intercepts and then controls the entire conversation.|
|**Observability**|Helps to observe the traffic flow in your mesh, trace call flows and dependencies, and view metrics such as latency and errors.|
|**OpenShift**|A hybrid cloud, enterprise Kubernetes application.|
|**OpenShift CI/CD process**|Automatically merges new code changes to the repository, builds, tests, approves, and deploys a new version to different environments.|
|**Operators**|Automate cluster tasks and act as a custom controller to extend the Kubernetes API.|
|**Operator Framework**|Is a family of tools and capabilities to deliver an efficient customer experience. It is not just about writing code; what is also critical is testing, delivery, and updating Operators.|
|**OperatorHub**|Web console lets cluster administrators find Operators to install on their cluster. It provides many different types of Operators available, including Red Hat Operators, Certified Operators from independent service vendors partnered with Red Hat, Community Operators from the open-source community but not officially supported by Red Hat, and custom Operators defined by users.|
|**Operator Lifecycle Manager**|(or OLM) Controls the install, upgrade, and role-based access control (or RBAC) of Operators in a cluster.|
|**Operator maturity model**|Defines the phases of maturity for general day two Operations activities and ranges from Basic Install to Auto Pilot.|
|**Operator Pattern**|A system design that links a Controller to one or more custom resources.|
|**Operator Registry**|Stores CRDs, cluster service versions (CSVs), and Operator metadata for packages and channels. It runs in Kubernetes or OpenShift clusters to provide the Operator catalog data to OLM.|
|**Operator SDK**|(which includes Helm, Go, and Ansible) Helps authors build, test, and package their Operators without requiring knowledge of Kubernetes API complexities.|
|**postCommit**|Section defines an optional build hook.|
|**Retries**|A method to prevent errors in one microservice from cascading to other microservices.|
|**runPolicy**|Field controls how builds created from a build configuration need to run. Values include the default Serial (sequentially) and simultaneously.|
|**Service Broker**|Provides a short-running process that cannot perform the consecutive day’s operations such as upgrades, failover, or scaling.|
|**Service Mesh**|A dedicated layer for making service-to-service communication secure and reliable. It provides traffic management to control the flow of traffic between services, security to encrypt traffic between services, and observability of service behavior; so, you can troubleshoot and optimize applications.|
|**Software operators**|Try to capture the knowledge of human operators and automate the same processes.|
|**Source-to-Image**|A tool for building reproducible container images. Also abbreviated S2i, it injects application source code into a container image to produce a ready-to-run image.|
|**Source strategy**|Section shows the strategy used to execute the build, such as a Source, Docker, or Custom strategy.|
|**Source type**|Determines the primary input like a Git repository, an inline Dockerfile, or binary payloads.|
|**Webhook**|A trigger that sends a request to an OpenShift Container Platform API endpoint. Often this will be a GitHub webhook, though it can also be a generic webhook. If a GitHub webhook is utilized, GitHub can send the request to OpenShift when there is a new commit on a certain branch, or a pull request is merged, or under many more circumstances. Webhooks are a great way to automate development flows so that builds can occur automatically as new code is developed.|
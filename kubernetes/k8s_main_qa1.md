<p align="right" width="100%">

1) what is taint and toleration?

Taint and Toleration: In Kubernetes, taints are used to mark nodes as unsuitable for certain pods, while tolerations are used to indicate which pods can tolerate a taint.

2) node affinity an pod affinity?
Node Affinity and Pod Affinity: Node affinity is used to specify which nodes a pod can be scheduled on, while pod affinity is used to specify which other pods a new pod should be co-located with on the same node.

3) how to check the logs of a pod or deployment?
To check the logs of a pod or deployment, you can use the kubectl logs command followed by the name of the pod or deployment.

4) how to check how many pods are running?
To check how many pods are running, you can use the kubectl get pods command and count the number of pods in the "Running" state.

5) what are deployment strategy used in your project?
Deployment strategies used in a project can vary, but some common ones include rolling updates, blue-green deployments, and canary deployments.

6) what is init container?
Init containers are containers that run before the main container in a pod and are used to perform initialization tasks such as setting up configuration files or databases.

7) what is statefullset?
StatefulSet is a controller in Kubernetes that is used to manage stateful applications by providing stable network identities, persistent storage, and ordered deployment and scaling.

8) what is ingress?
Ingress is an API object in Kubernetes that provides a way to manage external access to the services in a cluster.

9) difference between headfull and headless service?
A headful service is a service that provides access to a set of pods with stable network identities, while a headless service is a service that provides access to individual pods without stable network identities.

10) difference between secret and configmap?
Secrets and ConfigMaps are both Kubernetes objects used to manage application configuration data, but Secrets are used for sensitive data such as passwords and keys, while ConfigMaps are used for non-sensitive data such as configuration files.

11) what is livenessprobe and readynessprobe?
LivenessProbe and ReadinessProbe are both mechanisms used by Kubernetes to monitor the health of a container. LivenessProbe checks if the container is still alive, while ReadinessProbe checks if the container is ready to receive traffic.

12) how to access other pods in a cluster?
To access other pods in a cluster, you can use the Kubernetes DNS service or specify the IP address of the target pod.

13) what is a pod?
A pod is the smallest deployable unit in Kubernetes, consisting of one or more containers that share the same network namespace and are scheduled to run on the same node.

14) how you will make sure that the database should start first and then application?
To ensure that the database starts before the application, you can use a startup probe in the deployment configuration to delay the startup of the application until the database is ready.

15) Types of storage class used in your project?
Storage classes used in a project can vary, but some common ones include AWS EBS, GCE Persistent Disk, and Azure Disk.

16) difference between statefullset and stateless?
Stateless applications do not require persistent storage or stateful data, while stateful applications require persistent storage and have stateful data.

17) describe kubernetes architecture?
Kubernetes architecture consists of three main components: the master node, worker nodes, and etcd cluster. The master node manages the overall state of the cluster, while worker nodes run the containers and execute the workloads. The etcd cluster stores the configuration data and state of the entire cluster.

18) difference between PV and pvc?
PV (Persistent Volume) is a storage resource in Kubernetes, while PVC (Persistent Volume Claim) is a request for a specific type of PV.

19) 2 containers are running inside a pod if one container goes down then will it affect other running container?
If one container in a pod goes down, it will not affect the other running container in the same pod.

20)  Update the password in secret without restarting the pod or deployment ,is it possible ?
Yes, it is possible to update the password in a secret without restarting the pod or deployment using the kubectl apply command.

21) how to rollback the deployment?
To rollback a deployment in Kubernetes, you can use the kubectl rollout undo command followed by the name of the deployment. This command will revert the deployment to the previous revision. You can also specify the revision number to which you want to rollback using the --to-revision option.


22) what is the reason for pod eviction?
A pod may be evicted due to various reasons, such as:
Node failure
Resource constraints (e.g., memory or CPU limits)
Image pull failures
Node maintenance
Pod startup failures
Incorrect configuration

22) pod is in pending state ,what are the possible reasons?
There could be several reasons why a pod is in the pending state, such as:
Insufficient resources on the node to schedule the pod
Unsatisfied pod scheduling constraints (e.g., node affinity, pod anti-affinity, taints and tolerations)
Volume creation or attachment issues
Network-related issues (e.g., misconfigured networking, lack of available IP addresses)


23) how you will make sure that in rolling update strategy 2 pods are always available?
Use the maxUnavailable field in the deployment's spec to limit the number of unavailable pods during the update process.

24) crashloopbackoff, what are the possible reasons?
CrashLoopBackOff is a container state that occurs when a container repeatedly fails to start. There could be several reasons why this happens, such as:
Incorrect container configuration (e.g., missing or invalid command or entrypoint)
Incompatible image with the cluster or the node
Resource constraints (e.g., memory or CPU limits)
Volume creation or attachment issues
Network-related issues (e.g., port conflicts)

25) why you are using 3 master node in production?
Using 3 master nodes in production provides high availability and fault tolerance. With 3 master nodes, the Kubernetes control plane can continue functioning even if one node fails, ensuring that the cluster is always available.

26) how you will make sure that pod should be running on a specific node?
You can ensure that a pod is running on a specific node by using node affinity rules. Node affinity allows you to specify constraints on which nodes a pod can be scheduled. You can use node labels to specify the affinity rules.

27) how to check what are the activities performed by the container while creating the pod?
You can check the activities performed by a container while creating the pod by examining the container logs. You can use the kubectl logs command to view the logs of a container. You can specify the name of the pod and the container using the --container option.

28) how to get the ip of a pod ?
You can get the IP address of a pod using the kubectl get pod <pod-name> -o wide command. The output of this command will show the IP address of the pod under the IP column.

29) which network plugin you are using?
There are several network plugins that can be used with Kubernetes, such as Calico, Flannel, and Weave Net. The choice of network plugin depends on the specific requirements of the cluster, such as network performance, security, and scalability.

30) how you are monitoring the kubernetes cluster and the containers?
There are several tools available for monitoring Kubernetes clusters and containers, such as Prometheus, Grafana, and Kubernetes Dashboard. These tools allow you to monitor resource utilization, application performance, and cluster health, among other metrics.

31) Job should be terminated after 40 seconds ? ActiveDeadLineSeconds: 40
You can set the activeDeadlineSeconds field in a Job specification to specify the maximum amount of time that a Job should be allowed to run before being terminated. Once this limit is reached, the Job will be terminated, and any running pods will be deleted.

32) Ingress VS Loadbalancer ?
Both Ingress and LoadBalancer are used to expose services outside of the Kubernetes cluster.
LoadBalancer creates a cloud provider's load balancer to expose a service externally. It provides a simple layer 4 (TCP/UDP) load balancing.
Ingress is an API object that manages external access to the services inside the cluster. It acts as a reverse proxy and provides a more advanced layer 7 (HTTP/HTTPS) load balancing. It can be configured with rules and annotations to support advanced routing and load balancing features.
So, if you need a simple way to expose a service externally, use LoadBalancer. But if you need advanced routing and load balancing features, use Ingress.

</p>

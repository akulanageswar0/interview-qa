<p align="right" width="100%">

Kubernetes (k8s) supports several types of deployments, each with its own unique characteristics and use cases. Some of the most common types of k8s deployments are:

<em>
ReplicaSet: ReplicaSet is the basic building block of Kubernetes. It is responsible for maintaining a set of identical pods running at the same time.

Deployment: A Deployment is a higher-level abstraction that builds on top of the ReplicaSet. It provides additional functionality such as rolling updates, scaling, and rollback capabilities.

StatefulSet: A StatefulSet is used for stateful applications that require stable network identities, persistent storage, and ordered scaling.

DaemonSet: A DaemonSet ensures that a specific pod is running on each node in the cluster. This is useful for tasks such as log collection, monitoring, and other system-level tasks.

Job: A Job is used for batch processing tasks, where a certain number of pods run to completion and then exit.

CronJob: A CronJob is similar to a Job, but it runs on a predefined schedule. This is useful for running periodic tasks, such as backups or cleanup jobs.

</em>
Kubernetes (K8s) offers several deployment strategies for managing and rolling out updates to containerized applications. Here are some of the most common types of deployment strategies in K8s:
<em>
Rolling deployment—replaces pods running the old version of the application with the new version, one by one, without downtime to the cluster.

Recreate-terminates all the pods and replaces them with the new version.

Blue/Green- Deployment: In this strategy, two identical environments or "color-coded" clusters are set up, one running the current version of the application (blue) and the other running the new version (green). Once the green environment is fully tested and validated, the traffic is switched over to the new environment, and the blue environment is decommissioned.

Canary Deployment: In a canary deployment, a small subset of users or traffic is redirected to the new version of the application to test it in a live production environment. If the new version performs well, more traffic is gradually redirected to it, until the entire application is running on the new version. If issues arise, the canary deployment can be quickly rolled back to the previous version

A/B Testing: This strategy is similar to a canary deployment, but instead of testing the entire application, only specific features or functionalities are tested with a subset of users. This approach enables developers to compare the performance of different features and validate new ones before releasing them to a wider audience.

</em>
</p>
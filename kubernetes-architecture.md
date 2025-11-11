# Kubernetes Architecture

## Control Plane
The control plane manages the cluster and consists of:

- **API Server:** Central communication hub.
- **etcd:** Stores cluster state.
- **Controller Manager:** Ensures desired state matches actual state.
- **Scheduler:** Assigns Pods to Nodes.

## Data Plane
The data plane runs workloads on nodes:

- **Kubelet:** Runs and monitors Pods.
- **Kube-proxy:** Handles networking for Services.
- **Container Runtime:** Runs containers (Docker, containerd, CRI-O).

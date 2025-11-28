\# Today I Learned: Kubernetes Self-Healing



\## Commands I Used



\- `kubectl apply -f pod.yml` → Create Pod from YAML

\- `kubectl get pods` → List all Pods

\- `kubectl get pods -o wide` → List Pods with IP and node info

\- `kubectl apply -f deployment.yml` → Create Deployment

\- `kubectl delete pod <pod-name>` → Delete a Pod manually

\- `minikube ssh` → Access Minikube cluster

\- `notepad pod.yml` → Edit YAML from CLI



---



\## YAML Used for Deployment



```yaml

apiVersion: apps/v1

kind: Deployment

metadata:

&nbsp; name: nginx-deployment

&nbsp; labels:

&nbsp;   app: nginx

spec:

&nbsp; replicas: 3

&nbsp; selector:

&nbsp;   matchLabels:

&nbsp;     app: nginx

&nbsp; template:

&nbsp;   metadata:

&nbsp;     labels:

&nbsp;       app: nginx

&nbsp;   spec:

&nbsp;     containers:

&nbsp;     - name: nginx

&nbsp;       image: nginx:1.14.2

&nbsp;       ports:

&nbsp;       - containerPort: 80






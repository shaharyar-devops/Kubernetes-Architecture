\# Today I Learned: Kubernetes Self-Healing



This property pf Kubernetes is very good as it heals itself when ever a pod is deleted by mistake or  by any error .


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






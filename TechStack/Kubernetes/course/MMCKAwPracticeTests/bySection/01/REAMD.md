### ETCD

ETCD is a distributed reliable key-value store that is simple, secure and fast.

### Kube-API Server

### Kube Controller Manager

#### Controller

- Watch Status
- Remediate Situation

### Kube Scheduler

- to decide which POD goes to which node
- steps:
  - filter nodes
  - rank nodes

### Kubelet

- Register Node
- Create PODs
- Monitor Node & PODs

Kubeadmin does not deploy Kubelets

### Kube Proxy

- POD Network

### PODs with YAML

```
> kubectl run nginx --image=nginx
> kubectl run nginx --image=nginx --dry-run=client -o yaml
```

### ReplicaSets

```
> kubectl create -f nginx-deployment.yaml
> kubectl get replicaset
> kubectl delete replicaset myapp-replicaset
> kubectl replace -f replicaset-definition.yml
> kubectl scale -replicas=6 -f replicaset-definition.yml
```

### Deployments

```
> kubectl create -f replicaset-definition.yml
> kubectl create deployment --image=nginx nginx --dry-run=client -o yaml
> kubectl create deployment --image=nginx nginx --dry-run=client -o yaml > nginx-deployment.yaml
> kubectl create deployment --image=nginx nginx
> kubectl create -f deployment-definition.yml
> kubectl get deployments
> kubectl get replicaset
> kubectl get pods
> kubectl get all
```

### Namespace

```
// only list the pods in the default namespace
> kubectl get pods

// to create the namespace
> kubectl create namespace dev-ns
> kubectl create ns dev-ns

// list the pods in the namespace "kube-system"
> kubectl get pods --namespace=kube-system
> kubectl create -f pod-definition.yml --namespace-dev

> kubectl create -f namespace-dev.yml
> kubectl create namespace dev

// to switch the namespace
> kubectl config set-context $(kubectl config current-context) --namespace=dev

// to view pods in all namespaces
> kubectl get pods --all-namespaces

// used in the quiz
> kubectl get ns --no-headers | wc -l
> kubectl -n research get pods --no-headers
> kubectl run redis --image=redis --dry-run=client -o yaml > pod.yaml
> kubectl get pods --all-namespaces | grep blue
> kubectl -n dev get svc
```

### Services

```
> kubectl get svc
> kubectl create -f service-definition.yml
> kubectl get services
> kubectl expose deployment simple-webapp-deployment --name=webapp-service --target-port=8080 --type=NodePort --port=8080 --dry-run=client -o yaml > svc.yaml

> kubectl run httpd --image=httpd:alpine --port=80 --expose
```

### Service Cluster IP

### Services - Loadbalancer

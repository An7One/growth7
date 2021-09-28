## Section 05 Application Lifecycle Management

### Application Lifecycle Management - Section Introduction

### Rolling Updates and Rollbacks

```
> kubectl rollout status deployment/myapp-deployment

> kubectl rollout history deployment/myapp-deployment

> kubectl apply -f definition-deployment.yaml

// be careful because it does not modify the YAML file, and thus easily leads to inconsistency between the state of the pod and the definition YAML file
> kubectl set image deployment/myapp-deployment nginx=nginx:1.9.1

> kubectl get replicasets

> kubectl get deployments

> kubectl rollout undo deployment/myapp-deployment

> kubectl rollout status deployment/myapp-deployment

> kubectl rollout undo deployment/myapp-deployment

> kubectl rollout history deployment/myapp-deployment
```

### Commands

### Commands and Arguments

### Configure Environment Variables in Applications

```
> docker run -e APP_COLOR=pink simple-webapp-color

> kubectl create configmap webapp-config-map --from-literal=APP_COLOR=darkblue
```

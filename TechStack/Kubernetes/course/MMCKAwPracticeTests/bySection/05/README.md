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

> kubectl create cm webapp-config-map --from-literal=APP_COLOR=darkblue

> kubectl explain pods --recursive | grep envFrom
```

### Configure Secrets in Applications

```
// kubectl create secret generic <secret-name> --from-literal=<key>=<value>
> kubectl create secret generic app-secret --from-literal=DB_Host=mysql \
                                           --from-literal=DB_USER=root \
                                           --from-literal=DB_Password=passwrd

> kubectl create secret generic <secret-name> --from-file=<path-to-file>

> kubectl create secret generic app-secret --from-file=app_secret.properties

> kubectl get secrets

> kubectl describe secrets

> kubectl get secret app-secret -o yaml

> kubectl -n elastic-stack exec -it app -- cat /log/app.log

> kubectl run yellow --image=busybox --restart=Never --dry-run -o yaml > pod.yaml

> kubectl -n elastic-stack get pod,svc

// Linux commands to encode the input
> echo -n 'mysql' | base64
> echo -n 'root' | base64
> echo -n 'paswrd' | base64

// Linux commands to decode the input
> echo -n 'bXlzcWw=' | base64 --decode
> echo -n 'cm9vdA==' | base64 --decode
> echo -n 'cGFzd4JK' | base64 --decode
```

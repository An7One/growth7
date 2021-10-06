## Section 07 Security

### Security - Security Introduction

### Kubernetes Security Primitives

### Authentication

### Article on Setting up Basic Authentication

### TLS Introduction

### TLS Basics

### TLS in Kubernetes - Certificate Creation

```
// OpenSSL Commands
// to generate keys
> openssl genrsa -out ca.key 2048
// certificate signing request
> openssl req -new -key ca.key -subj "/CN=KUBERNETES-CA" -out ca.csr
// sign certificates
> openssl x509 -req -in ca.csr -signkey ca.key -out ca.crt
```

Kube API Server

- kubernetes 10.96.0.1
- kubernetes.default 172.17.0.87
- kubernetes.default.svc
- kubernetes.default.svc.cluster.local

### View Certificate Details

```
> journalctl -u etcd.service -l

> kubectl logs etcd-master
```

Reference:

- kubernetes-the-hard-way - [github](https://github.com/mmumshad/kubernetes-the-hard-way/tree/master/tools)

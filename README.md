# Kubernetes ConfigMap & Secret Lab

This repository contains a hands-on Kubernetes lab focused on working with **ConfigMaps and Secrets** for managing application configuration and sensitive data.

The lab demonstrates different techniques for injecting configuration into containers using environment variables and Deployments.

---

## Lab Overview

This lab includes **7 tasks** covering:

- Creating ConfigMaps using imperative commands
- Injecting ConfigMap values as environment variables
- Selective key injection from ConfigMaps
- Creating Kubernetes Secrets
- Injecting Secrets into containers
- Combining ConfigMap and Secret in a single Pod
- Using ConfigMap and Secret with a scalable Deployment

---

## Repository Structure

```
.
├── K8s-ConfigMap-Secret-Lab-Solution.pdf
├── cm-env.yaml
├── cm-sel.yaml
├── secret-env.yaml
├── cmsec.yaml
├── deploy-config.yaml
└── README.md
```

## Kubernetes Concepts Practiced

### ConfigMap

Used to store **non-sensitive configuration data** such as:

- Application environment
- Ports
- Feature flags
- System limits

Example keys used in this lab:


APP_ENV=production
APP_PORT=8080
APP_COLOR=blue
MAX_CONNECTIONS=100


---

### Secret

Used to store **sensitive information** such as:

- Database credentials
- API tokens
- Passwords

Example keys used:


DB_USER=admin
DB_PASSWORD=p@ssw0rd123
DB_NAME=myapp


Secrets are stored in Kubernetes as **Base64 encoded values**.

---

## Key Learning Points

✔ Separation of configuration from application code  
✔ Secure handling of credentials using Kubernetes Secrets  
✔ Injecting configuration using environment variables  
✔ Selective environment variable injection  
✔ Combining multiple configuration sources  
✔ Managing configuration in scalable Deployments

---

## Verification Commands

Check ConfigMaps


kubectl get configmap
kubectl describe configmap app-config


Check Secrets


kubectl get secret
kubectl describe secret db-secret


Verify Pods


kubectl get pods
kubectl logs env-pod
kubectl logs db-pod


Check Deployment


kubectl get deployment
kubectl get pods -l app=webapp-configured


---

## Author

Ahmed Amr  
DevOps Engineer | Containerization & Cloud Infrastructure


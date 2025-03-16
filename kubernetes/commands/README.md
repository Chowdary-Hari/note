
# ReplicaSet
### 1. **Create a ReplicaSet**
```sh
kubectl apply -f replicaset.yaml
```
OR
```sh
kubectl create -f replicaset.yaml
```

### 2. **List all ReplicaSets**
```sh
kubectl get rs
```

### 3. **Describe a specific ReplicaSet**
```sh
kubectl describe rs <replica-set-name>
```

### 4. **Scale a ReplicaSet**
```sh
kubectl scale rs <replica-set-name> --replicas=<number>
```

Example:
```sh
kubectl scale rs my-replicaset --replicas=5
```

### 5. **Delete a ReplicaSet**
```sh
kubectl delete rs <replica-set-name>
```
OR
```sh
kubectl delete -f replicaset.yaml
```

### 6. **Get the Pods managed by a ReplicaSet**
```sh
kubectl get pods --selector=app=<label-name>
```

### 7. **Check the ReplicaSet rollout status**
```sh
kubectl rollout status rs <replica-set-name>
```
---
# **Deployment**

#### **1. Create a Deployment**
```sh
kubectl apply -f deployment.yaml
```
OR
```sh
kubectl create -f deployment.yaml
```

#### **2. List Deployments**
```sh
kubectl get deployments
```

#### **3. Describe a Deployment**
```sh
kubectl describe deployment <deployment-name>
```

#### **4. Check the Status of a Deployment**
```sh
kubectl rollout status deployment <deployment-name>
```

#### **5. Scale a Deployment**
```sh
kubectl scale deployment <deployment-name> --replicas=<number>
```
Example:
```sh
kubectl scale deployment my-app --replicas=5
```

#### **6. Update a Deployment**
- Modify the `deployment.yaml` file and then run:
```sh
kubectl apply -f deployment.yaml
```
OR update the image directly:
```sh
kubectl set image deployment/<deployment-name> <container-name>=<new-image>
```
Example:
```sh
kubectl set image deployment/my-app my-container=my-app:v2
```

#### **7. Restart a Deployment**
```sh
kubectl rollout restart deployment <deployment-name>
```

#### **8. Rollback to a Previous Version**
```sh
kubectl rollout undo deployment <deployment-name>
```

#### **9. View the Deployment History**
```sh
kubectl rollout history deployment <deployment-name>
```

#### **10. Delete a Deployment**
```sh
kubectl delete deployment <deployment-name>
```
OR
```sh
kubectl delete -f deployment.yaml
```
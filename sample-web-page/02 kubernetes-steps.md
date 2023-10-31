### 1. Create kubernetes deployment from image available at docker hub

```bash
kubectl create deployment sample-web-node --image=sanppatil/sample-web-page
```

### 2. View the deployments

```bash
kubectl get deployments
```

### 3. View the pods

``` =bash
kubectl get pods
```

### 4. View logs

```bash
kubectl logs sample-web-node-7c89cc8686-fgmr8
```

### 5. Expose the Pod to the public internet

```bash
kubectl expose deployment sample-web-node --type=LoadBalancer --port=8080
```

- --type=LoadBalancer flag indicates that you want to expose your Service outside of the cluster.
- Application code inside the test image only listens on TCP port 8080.
        
### 6. View service and get external IP

```bash
kubectl get services
```
- On cloud providers that support load balancers, an external IP address would be provisioned to access the Service. 
- On minikube, the LoadBalancer type makes the Service accessible through the minikube service command.

```bash
minikube service sample-web-node
```

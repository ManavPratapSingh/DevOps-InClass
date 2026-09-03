# K8S Pod

### Pod config
```yml
apiVersion: v1
kind: Pod
metadata:
  name: my-pod
spec:
  containers:
    - image: nginx:latest
      name: nginx
      ports:
        - containerPort: 80
```

### Stages of a pod init:
![_](./assets/3%20stages%20of%20pods.png)


### Running Website
![_](./assets/nginx%20from%20k8s%20pod.png)
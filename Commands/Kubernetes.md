# Kubernetes

## Create

```kubectl create deployment <deployment_name> --image=<image_name>```

Create deployment

## Apply

```kubectl apply -f <file_name>.yml --dry-run```

Shows output for the deployment without actually running

```kubectl apply -f <file_name>.yml --server-dry-run```

Shows output for deployment by checking API (If deployment exists it will list changes)

## Diff

```kubectl diff -f <file_name>.yml```

Compare differences between current deployment and yml deployment

## Scale

```kubectl scale deployment/<deployment_name> --replicas 5```

Scaling to 5 replicas

## Expose

```kubectl expose deployment/<deployment_name> --port 8080```

Expose port inside Kubenetes cluster

```kubectl expose deployment/<deployment_name> --port 8080 --name <name> --type NodePort```

Expose port outside cluster (Used for Docker Desktop)

## Get

```kubectl get all```

List all Kubernetes services and resources

```kubectl get services```

List deployed services

```kubectl get namespaces```

List namespaces in your curent context

```kubectl get all --all-namespaces```

List all namespaces

## Explain

```kubectl explain services.spec```

List information about services.spec (yaml spec)

## Delete

```kubectl delete deployment <deployment_name>```

Delete deployment

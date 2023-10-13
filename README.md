# Go Microservices

# Utils

[Course Certificate](https://udemy.com/certificate/UC-eaff279c-513a-47dd-8b7a-d26ba06d79a8/)

[Go](https://go.dev/dl/)

[VisualStudioCode](https://code.visualstudio.com/download)

[Docker](https://www.docker.com/products/docker-desktop/)

[Make](https://www.gnu.org/software/make/)

[Chocolately](https://chocolatey.org/install)

[Protocol Buffer Compiler Installation](https://grpc.io/docs/protoc-installation/)

[Minikube](https://minikube.sigs.k8s.io/docs/start/)

[Kubectl](kubernetes.io/docs/tasks/tools/)

[How to find and edit a Windows Hosts File](https://www.freecodecamp.org/news/how-to-find-and-edit-a-windows-hosts-file/)

[How To Configure Ingress TLS/SSL Certificates in Kubernetes](https://devopscube.com/configure-ingress-tls-kubernetes/)

# Commands

## Make

Build executable of a microservice `make {microservice}`

Build and run docker images `make build_up`

Drops docker images `make down`

## Docker

```
docker build -f {ms}.dockerfile -t {user}/{ms}:1.0.0 .

docker push {user}/{ms}:1.0.0

docker swarm init

docker swarm service ls

docker stack deploy -c swarm.yml {name}

docker swarm leave -f
```

### Docker Compose

```
docker-compose -f {container} up -d
```

### Access Mongo in Docker CLI

```
docker exec -it {mongo container ID} bash

mongo admin -u admin -p password
```

### Protocol Buffer

```
protoc -go_out=[folder] --go_opt=paths=source_relative --go-grpc_out=[folder] --go-grpc_opt=source_relative [proto file]

protoc -go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=source_relative logs.proto
```

## Kubernetes

```
minikube start [--nodes=2]

minikube status

minikube stop

minikube dashboard

minikube tunnel
```

```
kubectl get pods [-A]

kubectl apply -f {path or file}

# Get services

kubectl get svc

kubectl get deployments

kubectl logs {pod name}

kubectl delete deployments {pod/s}

kubectl delete svc {pod/s}

kubectl expose deployment {name} --type=LoadBalancer --port={port} --target-port={target port}
```

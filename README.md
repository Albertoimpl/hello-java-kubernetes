# hello-java-kubernetes

Build the image:

```bash

./gradlew bootBuildImage --imageName=albertoimpl/hello-java
```

or:

```bash
pack set-default-builder paketobuildpacks/builder:base
pack build albertoimpl/hello-java
```

Push it to a registry:

```bash
docker push albertoimpl/hello-java
```

Create a Kubernetes cluster:

```bash
kind create cluster
```

Deploy it into Kubernetes:

```bash
kubectl apply -f k8s/
```


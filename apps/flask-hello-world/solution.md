# Docker
## build with:
```docker build -t freddo256/pxl .```

## push
```docker push freddo256/pxl:latest```

## run locally
```docker run -dp 5000:5000 hello-flask```

# K3d
## create cluster
```k3d cluster create mycluster -p "5000:5000@loadbalancer" --servers 2 --agents 3```

# Kubernetes
## apply deployment.yaml
```kubectl apply -f deployment.yaml```


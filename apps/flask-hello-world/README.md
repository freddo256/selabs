# Kubernetes Deployment Exercise

From source code to Kubernetes Deployment.

Given a python flask web app that runs a web server on port 5000, deploy this app on a local k3d Kubernetes cluster, with at least 3 replicas.

Steps:

- Containerize using a Dockerfile
- Push the image to docker hub
- Create a kubernetes deployment

## flask-hello-world

### Description

This is a lightweight web application serving a hello world message on TCP port 5000.

### Components

The Flask app consists of the following components:

- `app.py` - the python flask app
- `requirements.txt` - a list of python packages with a specified version to be used by pip
- `templates\index.html` - html page to display

### Building and running the app

Required pyton version >= Python 3.8.

The following command will install the packages according to the configuration file requirements.txt.

```
pip install -r requirements.txt
```

Run the application with

```
python ./app
```

### Containerizing

The flask app can be easily containerzied by using the official `python:3.8` image on docker hub.

## Useful tips

- Writing Dockerfiles<br>
  https://docs.docker.com/develop/develop-images/dockerfile_best-practices/
- Docker Hub Quickstart<br>
  https://docs.docker.com/docker-hub/
- Exposing services on k3d<br>
  https://k3d.io/usage/guides/exposing_services/

## Troubleshooting

- Always run `kubectl get events -A -w` to screen for issues
- `kubectl logs` to check pod logs
- Kube DNS check `kubectl run -it --rm --restart=Never busybox --image=busybox:1.28 -- nslookup $YOUR_DNS_NAME_WITH_NAMESPACE`
- `kubectl describe svc` and `kubectl describe endpoint`
- logon to the k3s instance (docker) with docker excec
- if you're lazy, use [Lens](https://k8slens.dev) for all of the above :^)

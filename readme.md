# Rancher Kubernetes K3S Cluster

Table of Contents
- Setup cluster

## Setup cluster
[K3S Quick Start Guide](https://docs.k3s.io/quick-start)


## Connect to cluster
ssh [USER]@[SYSTEM LOCAL IP]
ssh lasse@192.168.50.180

## Pre-installed charts
/var/lib/rancher/k3s/server/static/charts

## Download Helm
Follow Helm [Instalation Guide for Binarty Releases](https://helm.sh/docs/intro/install/)
Download tar - curl -L 
tar -zxvf https://get.helm.sh/helm-v4.0.0-linux-amd64.tar.gz


## Install Longhorn
Follow K3s [Longhorn instalation guide](https://docs.k3s.io/add-ons/storage)
kubectl apply -f https://raw.githubusercontent.com/longhorn/longhorn/v1.10.1/deploy/longhorn.yaml


## Installing Flux
Installing Flux cli for local computer


flux bootstrap github --components-extra=image-reflector-controller,image-automation-controller --owner=TheLoGgI --repository=rancher-k3s-cluster --branch=master --path=projects/flux --read-write-key --personal


## Trafik

### Get TLS - Self signed Certificate
https://doc.traefik.io/traefik/setup/kubernetes/


## TODO LIST
- [ ] - GitOps
- [x] - Install Storage Manager Longhorn


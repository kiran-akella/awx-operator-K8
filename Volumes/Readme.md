**This directory is created to help beginners to understand the importance of volume in awx-operator application deployment in kubernetes.**

# Introduction

Managing storage is a distinct problem from managing compute instances. The PersistentVolume subsystem provides an API for users and administrators that abstracts details of how storage is provided from how it is consumed.
To do this,kubernetes introduced two new API resources: PersistentVolume and PersistentVolumeClaim.

A **Kubernetes StorageClass** is a Kubernetes storage mechanism that lets you dynamically provision persistent volumes (PV) in a Kubernetes cluster

A **PersistentVolume** (PV) is a piece of storage in the cluster that has been provisioned by an administrator or dynamically provisioned using Storage Classes. 

While **PersistentVolumeClaims** allow a user to consume abstract storage resources, it is common that users need PersistentVolumes with varying properties.

PVs must be requested through persistent volume claims (PVCs), which are requests for storage. A PVC is essentially a request to mount a PV meeting certain requirements on a pod. PVCs do not specify a specific PV—instead.

# Setup

Create a **postgres-15** directory in **data** folder with below commands on your Kubernetes master node and copy the above attached pv, pvc and storage class files into your machine. once directories are created, execute the kubectl create -f filename commands provided below to create the volume.

```
sudo mkdir -p /data/postgres-15/data
```
```
sudo chmod 700 /data/postgres-15/data
```
```
kubectl create -f storage_class.yml
```
```
kubectl create -f pv.yaml
```
```
kubectl create -f pvc.yaml
```

# Installation

Now you can continue your installation as per the documentation. 

https://github.com/kiran-akella/awx-operator-K8/blob/12edc2e2b7c61a34b88ca807c15a3350ddc1fdf3/docs/installation/basic-install.md

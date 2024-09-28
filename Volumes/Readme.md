Volumes directory is created to broadcast the importance of volumes in awx-operator application in kubernetes.

# Introduction

Managing storage is a distinct problem from managing compute instances. The PersistentVolume subsystem provides an API for users and administrators that abstracts details of how storage is provided from how it is consumed.
To do this,kubernetes introduce two new API resources: PersistentVolume and PersistentVolumeClaim.

A **Kubernetes StorageClass** is a Kubernetes storage mechanism that lets you dynamically provision persistent volumes (PV) in a Kubernetes cluster

A **PersistentVolume** (PV) is a piece of storage in the cluster that has been provisioned by an administrator or dynamically provisioned using Storage Classes. 

While **PersistentVolumeClaims** allow a user to consume abstract storage resources, it is common that users need PersistentVolumes with varying properties.

PVs must be requested through persistent volume claims (PVCs), which are requests for storage. A PVC is essentially a request to mount a PV meeting certain requirements on a pod. PVCs do not specify a specific PV—instead.

# Setup

Create a **postgres-15** directory in **data** folder with below commands on your Kubernetes master node

sudo mkdir -p /data/postgres-15/data

sudo chmod 700 /data/postgres-15/data

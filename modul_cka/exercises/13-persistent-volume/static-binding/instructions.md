# Exercise 13

In this exercise, you will create a PersistentVolume using static binding and mount it to a Pod.

> **_NOTE:_** If you do not already have a cluster, you can create one by using minikube or you can use the Katacoda lab ["Creating a PersistentVolume via static binding"](https://learning.oreilly.com/scenarios/cka-prep-creating/9781492099154/).

1. Create a PersistentVolume named `pv`, access mode `ReadWriteMany`, 512Mi of storage capacity and the host path `/data/config`.
2. Create a PersistentVolumeClaim named `pvc`. The claim should request 256Mi and use an empty string value for the storage class. Ensure that the PersistentVolumeClaim is properly bound after its creation.
3. Mount the PersistentVolumeClaim from a new Pod named `app` with the path `/var/app/config`. The Pod uses the image `nginx`.
4. Open an interactive shell to the Pod and create a file in the directory `/var/app/config`.
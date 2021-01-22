# drozdnikita_platform
drozdnikita Platform repository

## PODs self-restoration:

1. the desired number of coredns pods is described via ReplicaSet coredns-f9fd979d6, thus once the pod gets killed it gets restored immediately
2. etcd-minikube, kube-apiserver-minikube, kube-controller-manager-minikube, kube-scheduler-minikube are part on the node and described as Non-terminated pods there
3. the desired number of kube-proxy pods is described via DaemonSet kube-proxy, and the same as with coredns gets restored right away

## Dockerfile

busybox as a base image running httpd via CMD. The resulting docker image is drozdnikita/drozd_web_app:1.0.0.

## web pod yaml

works as expected, nothing to add really

## healthy frontend

it required variables to added in the 'env' of pod manifest
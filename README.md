# docker-registry-pull-through-cache
A sample configuration how to proxy different public container registries with Docker distribution.

It uses Docker Compose to launch registry mirrors for hub.docker.com, quay.io, gcr.io and k8s.gcr.io. Each registry mirror caches images only in memory.

This repository also contains a usage example for K3S/K3D. Just launch k3d with the ``--registry-config`` parameter:

``
k3d cluster create sample-cluster --registry-config "rancher-registries.yaml"
``
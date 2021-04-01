# JupyterHub Learning Experiment Repo

Research lab to install JupyterHub on Kubernetes 1.18 and simulate NAS
mounted on `/s/<user>` matching an annotation in the `<user>` namespace
(assuming Oauth2 authentication, which is not included) to load
notebooks.

## Caveats

* `GOPATH=~/.local/go`
* `GOBIN=~/.local/bin/go`
* Kubernetes 1.18.0 from source

## Script Order

```
install-kubectl
install-k8s-src     # or not (see kind create ...)
install-kind    
kind create cluster # or add --image kindest/node:v1.18
install-jhub
```

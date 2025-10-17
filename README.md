Introduction

This repository contains all the files used during the Youtube video about Tetragon

> **Note:** All commands are for demonstration purposes. Adjust them according to your OS and environment.

# Setup

## Configure Kind

Copy kind/config.yaml in /etc/kind, create it.

```bash
sudo mkdir -p /etc/kind/
sudo cp kind/*.yaml /etc/kind/
sudo mkdir -p /var/log/kubernetes
sudo chmod 755 /var/log/kubernetes
sudo kind create cluster --config kind/config.yaml
helm repo add cilium https://helm.cilium.io
helm repo update
helm upgrade --install tetragon cilium/tetragon -n kube-system --values install/first-installation.yaml --version 1.5.0

k0s 
```

## Useful commands

```bash
```


# Links

* https://mtardy.com/posts/try-tetragon-on-linux/
* https://ebpf.hamza-megahed.com/docs/chapter5/5-tetragon/
* https://srekubecraft.io/posts/tetragon/
* <https://medium.com/@techpaul/my-favourite-kubernetes-audit-log-policy-385ab8a4200a>

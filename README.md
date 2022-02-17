# ansible-devbox

This repo contains different playbooks to install and configure software
to run a Linux development box for a DevOps/SRE engineer.

Every playbook is for a specific Linux distro.

## Configurations

We're using some Github repos for adding configurations, this is opinionated.
For instance, for NeoVim we're using [this repo](https://github.com/bsnux/nvim).

## How to run a playbook

First of all, configure the `hosts` file with the hosts where you want to
run the playbooks.

Running playbook for CentOS 7:

```
$ ansible-playbook -K  -i hosts centos.yaml
```

Running specific tasks, for instance Python ones:

```
$ ansible-playbook -K  -i hosts --tags "python" centos.yaml
```

## Included software

* DevOps
  * Terraform
  * Vault
  * Git
  * Github CLI
  * kubectl
  * kubens
  * kubectx
  * docker
* Helpers
  * curl
  * jq
  * tmux
* Shells
  * zsh
* Editors
  * NeoVim
* Programming
  * Python
    * boto3
    * requests
    * ipython

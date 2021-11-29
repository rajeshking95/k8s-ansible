# Welcome to k8s-ansible!
Ansible Playbook to install Kubernetes

## Files
|File|Description|
|-|-|
|`hosts`|List of the hosts|
|`install-k8s.yaml`|Playbook code to install Kubernetes|

## Installing Ansible on Ubuntu
`sudo apt update`
`sudo apt install software-properties-common`
`sudo add-apt-repository --yes --update ppa:ansible/ansible`
`sudo apt install ansible`
`sudo apt install python3-pip`
`sudo pip install netaddr`

## Running the Playbook
```bash
ansible-playbook -i hosts -l k8s_cluster install-k8s.yaml
ansible-playbook -i hosts -l k8s_cluster install-k8s.yaml --start-at-task='<name of the task>'
ansible-playbook -i hosts -l k8s_cluster install-k8s.yaml --step --start-at-task='<name of the task>'
ansible-playbook -i hosts -l k8s_cluster install-k8s.yaml --list-hosts
```

## Checking Kubernetes Installation
```bash
kubectl get nodes
```

## Source
- https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-ubuntu
- https://www.cyberciti.biz/faq/ansible-apt-update-all-packages-on-ubuntu-debian-linux/
- https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/
- https://stackedit.io/app#
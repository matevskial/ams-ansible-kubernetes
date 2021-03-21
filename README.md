# Ansible and Kubernetes 

Project configuration files for the subject Administration of network services in my uni.

# General

The configuration files for ansible and kubernetes currently assume the following hosts:

* VM 1:
	* Ubuntu server 18.04 and later
	* hostname ```kubemaster```
	* static ip ```192.168.0.13```
	* storage 20GB fixed allocation
	* RAM 2048MB
	* 2 CPUs
	* username: kubenode
	* password: 12345678
	* no password for sudo

* VM 1:
	* Ubuntu server 18.04 and later
	* hostname ```kubenode```
	* static ip ```192.168.0.14```
	* storage 20GB fixed allocation
	* RAM 2048MB
	* 2 CPUs
	* username: kubenode
	* password: 12345678
	* no password for sudo

# Ansible

There are 3 playbooks, to install kubernetes, to set up the kubernetes cluster on maste, and to join the kubernetes workers to the cluster

To set up the kubernetes cluster, execute the following commands:

```
cd ansible
ansible-playbook install_kubernetes.yaml
ansible-playbook setup_kubernetes_cluster.yaml
ansible-playbook setup_kubernetes_workers.yaml
```

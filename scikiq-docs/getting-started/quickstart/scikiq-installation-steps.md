---
hidden: true
icon: instalod
---

# ScikIQ Installation Steps

## Installing Elasticsearch Rabbit MQ NEO4J and MYSQL with Docker Compose <a href="#toc131657357" id="toc131657357"></a>

Create docker compose file \scikiq\es-data\ ,\scikiq\mysql, \scikiq\mq, \scikiq\neo4j directory in this 172.31.22.163 server

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FUy4luix5QqirmXKrsMpd%252F0.png%3Falt%3Dmedia\&width=300\&dpr=4\&quality=100\&sign=7c0631d2\&sv=1)

#### Kubernetes Installation <a href="#toc131657358" id="toc131657358"></a>

## Kubernetes Pre-Installation <a href="#toc131657359" id="toc131657359"></a>

Lab Setup

Master Node: 172.31.31.172– ip-172-31-31-172

Worker Node: 172.31.22.163 – ip-172-31-22-163

Set hostname and add entries in the hosts file

_hostnamectl set-hostname " ip-172-31-31-1"_

_hostnamectl set-hostname " ip-172.31.22.2"_

_hostnamectl set-hostname " ip-172.31.22.3"_

Add the machine node IP and hostname in /etc/hosts

_echo "172.31.31.1 ip-172-31-31-1" >> /etc/hosts_

_echo "172.31.22.2 ip-172-31-22-2" >> /etc/hosts_

_echo "172.31.22.3 ip-172-31-22-2" >> /etc/hosts_

Above command used to fetch or ping one machine to another machine

Run the command to Disable swap & add kernel setting

_swapoff -a_

_sed -i '/ swap / s/^\\(.\*\\)$/#\1/g' /etc/fstab_

Above command to use disable the swap memory

Load the following kernel modules on all the node

_tee /etc/modules-load.d/containerd.conf <\<EOF_

_overlay_

_br\_netfilter_

_EOF_

Run the following command

modprobe overlay

modprobe br\_netfilter

we configure iptables to allow traffic across the network bridge. This change is vital because iptables (the servers default firewall) should always examine what traffic passes over the connections. Now we will load the br\_netfilter add-on module.

Set the following Kernel parameters for Kubernetes, run beneath tee command

_tee /etc/sysctl.d/kubernetes.conf <\<EOF_

_net.bridge.bridge-nf-call-ip6tables = 1_

_net.bridge.bridge-nf-call-iptables = 1_

_net.ipv4.ip\_forward = 1_

_EOF_

In the sysctl configuration from K8s, we assign the value 1, which means to check traffic.

Reload the above changes, run

_sysctl –system_

The sysctl command is used to list, read, and set kernel tunables. It can filter tunables when listing or reading and set tunables temporarily or permanently.

Install containerd run time

_apt install -y curl gnupg2 software-properties-common apt-transport-https ca-certificates_

Enable docker repository

_curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -_

_add-apt-repository "deb \[arch=amd64] https://download.docker.com/linux/ubuntu $(lsb\_release -cs) stable"_

Now, run following apt command to install containerd

\# apt update

_apt install -y containerd.io_

Configure containerd so that it starts using systemd as cgroup

_containerd config default | sudo tee /etc/containerd/config.toml >/dev/null 2>&1_

_sed -i 's/SystemdCgroup \\= false/SystemdCgroup \\= true/g' /etc/containerd/config.toml_

Restart and enable containerd service

_systemctl restart containerd_

_systemctl enable containerd_

Add apt repository for Kubernetes

_curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -_

_apt-add-repository "deb http://apt.kubernetes.io/ kubernetes-xenial main"_

## **Kubernetes application packages installation** <a href="#toc131657360" id="toc131657360"></a>

Install Kubernetes components Kubectl, kubeadm & kubelet

We can now update the server and then install the packages.

_apt update_

_apt install -y kubelet kubeadm kubectl_

_apt-mark hold kubelet kubeadm kubectl_

We set the kubelet kubeadm kubectl to standby mode because it restarts every few seconds as it is in a standby loop and waiting for further actions.

## **Kubernetes post installation** <a href="#toc131657361" id="toc131657361"></a>

Kubeadm init

#### Initialize Kubernetes cluster with Kubeadm command <a href="#toc131657362" id="toc131657362"></a>

Now, we are all set to initialize Kubernetes cluster. Run the following Kubeadm command from the master node only.

_kubeadm init --control-plane-endpoint= ip-172-31-31-1 --cri-socket unix:///var/run/containerd/containerd.sock --pod-network-cidr=192.166.0.0/16_

To begin using our cluster, we need to allow and configure our user to run kubectl.

_mkdir -p $HOME/.kube_

_sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config_

_sudo chown $(id -u):$(id -g) $HOME/.kube/config_

**untained nodes**

kubectl taint nodes --all node-role.kubernetes.io/control-plane- node-role.kubernetes.io/master- command didn't work in pcbb prod but below one update

_kubectl taint node fit-prod2-app1 node-role.kubernetes.io/control-plane:NoSchedule-_

Taints allow a node to repel a set of pods

_mkdir -p $HOME/.kube_

_sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config_

_sudo chown $(id -u):$(id -g) $HOME/.kube/config_

Cluster Status

_kubectl cluster-info_

The above command shows Kubernetes master is running or not

_kubectl get nodes_

_kubeadm join ip-172-31-31-1:6443 --token 0tq5cj.jvfqcxlmryh4q6i4 \\_

_--discovery-token-ca-cert-hash sha256:f828c4600f0e0243f08e07b1e7a0adff38e089993574dbc10c293cbe14ab9969kkubectl get nodes_

Install Calico Pod Network Add-on

A Pod Network is a way to allow communication between different nodes in the cluster. This tutorial uses the calico virtual network.

_curl https://projectcalico.docs.tigera.io/manifests/calico.yaml -O_

_kubectl apply -f calico.yaml_

_kubectl get pods -n kube-system_

_kubectl get nodes_

_kubectl create deployment nginx-app --image=nginx --replicas=2_

_kubectl get deployment nginx-app_

## **MetalLB Config Process** <a href="#toc131657363" id="toc131657363"></a>

MetalLB is a load-balancer implementation for bare metal Kubernetes clusters, using standard routing protocols. MetalLB is a young project. MetalLB is a Kubernetes-aware solution that will **monitor for services with the type LoadBalancer and assign them an IP address from a virtual pool**. It uses BGP(Border Gateway Protocol) or Layer 2 (with ARP Address Resolution Protocol) to expose services.

_kubectl edit configmap -n kube-system kube-proxy_

When we run kubectl edit configmap command. After run this command generate a file. We edit below written text in the generated file.

\###needed to set strict arp to true####

apiVersion: kubeproxy.config.k8s.io/v1alpha1

kind: KubeProxyConfiguration

mode: "ipvs"

ipvs:

strictARP: true

kubectl apply -f [https://raw.githubusercontent.com/metallb/metallb/v0.13.7/config/manifests/metallb-native.yaml](https://raw.githubusercontent.com/metallb/metallb/v0.13.7/config/manifests/metallb-native.yaml)

\##ips set---

cat <\<EOF | kubectl create -f -

apiVersion: v1

kind: ConfigMap

metadata:

namespace: metallb-system

name: config

data:

config: |

address-pools:

\- name: default

protocol: layer2

addresses:

\- _172-31-31-1_/32 machine IP

\- _172-31-31-2_/32 machine IP

EOF

## **Helm-install and Deployment Process** <a href="#toc131657364" id="toc131657364"></a>

Helm-install Process

_curl -fsSL -o get\_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3_

_chmod 700 get\_helm.sh_

_./get\_helm.sh_

Deployment

_kubectl create namespace ancr_

The above command used to create a prod namespa&#x63;_&#x65;_

_kubectl config set-context --current --namespace=ancr_

The above command used to set a current prod namespa&#x63;_&#x65;_

Below command is use to create secret docker-registry

_kubectl create secret docker-registry scikiq1-cred --docker-username= --docker-password= --docker-email=example.com -n ancr_

_first helm installation_

_helm install scikiq ./scikiq -n ancr_

helm upgrade use after delete kube-config

_helm upgrade scikiq ./scikiq -n ancr_

nodes-selection

_kubectl get nodes --show-labels_

List the nodes in your cluster, along with their labels

A customized lebel has been provided to nodes to avoid conflicts for web and backened deployments.

_kubectl label nodes ip-172-31-31-172 kname=ancr_

Choose one of your nodes, and add a label to it

## **After kubernetes installation Process** <a href="#toc131657365" id="toc131657365"></a>

We edit the values.yaml file content in our services.

\------------------------------------------------------------values.yml file contents-----------------------------------------

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FfSjmt3dwTSHwdj3O5nLd%252F1.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=2d6f345e\&sv=1)

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FZJ4O84nc9MHr7f6KVMHL%252F2.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=ed867e2d\&sv=1)Text Description automatically generated

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FuSSuyHhifne6zNd0IdKO%252F3.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=84edbb35\&sv=1)

![](https://scikiq.gitbook.io/~gitbook/image?url=https%3A%2F%2F3752922935-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FTBtqzPHa5xWCyJ0FI87l%252Fuploads%252FVlXKmDtqfVXr4jZbqof7%252F4.png%3Falt%3Dmedia\&width=768\&dpr=4\&quality=100\&sign=d74a8cc6\&sv=1)Text Description automatically generated

## **Kubernetes Exceptional Use Case Command** <a href="#toc131657367" id="toc131657367"></a>

We can use the below command if you want to create a new machine setup of kubernetes. You get an error to run after kubeadm init command.

_kubeadm reset_

kubeadm reset is responsible for cleaning up a node local file system from files that were created using the kubeadm init or kubeadm join commands. For control-plane nodes reset also removes the local stacked etcd member of this node from the etcd cluster

First, we use the reset command to run again kubeadm init or kubeadm join commands.

_rm -f /etc/cni/net.d/\*_

When running kubeadm reset removed the entire /etc/cni/net.d directory. This caused podman and any other tools using CNI networking to stop.

_iptables -F_

_iptables -X_

_iptables -t nat -F_

_iptables -t nat -X_

_iptables -t mangle -F_

_iptables -t mangle -X_

_iptables -P INPUT ACCEPT_

_iptables -P FORWARD ACCEPT_

_iptables -P OUTPUT ACCEPT_

Use the command below to generate the join command for worker node.

_kubeadm token create --print-join-command_

After run above command will show below token

_kubeadm join ip-172-31-31-172:6443 --token 0tq5cj.jvfqcxlmryh4q6i4 \ --discovery-token-ca-cert-hash sha256:f828c4600f0e0243f08e07b1e7a0adff38e089993574dbc10c293cbe14ab9969kkubectl_

This above token runs on the worker node only

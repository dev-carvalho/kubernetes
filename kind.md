
## InstalaΓ§Γ£o do KIND no Linux Ubuntu 22.04

```bash
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.17.0/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/kind
```


### Criando um Cluster com apenas um node

```bash
# kind create cluster --name zeta
```
```
Creating cluster "zeta" ...
 β Ensuring node image (kindest/node:v1.25.3) πΌ
 β Preparing nodes π¦
 β Writing configuration π
 β Starting control-plane πΉοΈ
 β Installing CNI π
 β Installing StorageClass πΎ
Set kubectl context to "kind-zeta"
You can now use your cluster with:

kubectl cluster-info --context kind-zeta

Thanks for using kind! π
```


### Criando um Cluster multi-node com arquivo YAML

```bash
# kind create cluster --name zeta --config=kind.yml
```
```
Creating cluster "zeta" ...
 β Ensuring node image (kindest/node:v1.25.3) πΌ
 β Preparing nodes π¦ π¦ π¦ π¦ π¦
 β Writing configuration π
 β Starting control-plane πΉοΈ
 β Installing CNI π
 β Installing StorageClass πΎ
 β Joining worker nodes π
Set kubectl context to "kind-zeta"
You can now use your cluster with:

kubectl cluster-info --context kind-zeta

Thanks for using kind! π
```

### Apagando um Cluster

```bash
# kind delete cluster --name zeta
```



<br><br>
ReferΓͺncias:
- https://kind.sigs.k8s.io/
- https://www.zup.com.br/blog/kind-cluster-kubernetes
- https://www.youtube.com/watch?v=00wlGss2stY (Rodando Kubernetes local usando Kind) 

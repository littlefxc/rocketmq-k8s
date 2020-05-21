# rocketmq-k8s

## Docker 镜像编译，推送

```sh
cd docker
docker build -t 192.168.195.2/dev/rocketmq:v4.4.0 . 
docker login 192.168.195.2 -u admin -p Harbor12345
docker push 192.168.195.2/dev/rocketmq:v4.4.0
```

## kubernetes 部署

```sh
cd Kurbernetes
kubectl apply -f rocketmq-namespace.yaml
kubectl apply -f rocketmq-pvc.yaml
kubectl apply -f rocketmq-configmap.yaml
kubectl apply -f rocketmq-deployment.yaml
kubectl apply -f rocketmq-admin-deployment.yaml
```

或者

```sh
kubectl apply -f Kurbernetes/
```


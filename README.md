# Домашнее задание к занятию "12.2 Команды для работы с Kubernetes"

## Задание 1
<img width="866" alt="1" src="https://user-images.githubusercontent.com/72221502/162696894-afcc9ecd-286e-4e5e-8b56-d8c21ba447af.png">

## Задание 2

### Вывод команд
```
❯ kubectl describe pod hello-node-6b89d599b9-s9p6z
Name:         hello-node-6b89d599b9-s9p6z
Namespace:    app-namespace
Priority:     0
Node:         minikube1/10.128.0.18
Start Time:   Mon, 11 Apr 2022 01:47:34 +0300
Labels:       app=hello-node
              pod-template-hash=6b89d599b9
Annotations:  <none>
Status:       Running
IP:           172.17.0.11
IPs:
  IP:           172.17.0.11
Controlled By:  ReplicaSet/hello-node-6b89d599b9
Containers:
  echoserver:
    Container ID:   docker://74e810ce2a358054a31e49b5cbfe1420ca2157860a5f0b73b7510ec686942ae1
    Image:          k8s.gcr.io/echoserver:1.4
    Image ID:       docker-pullable://k8s.gcr.io/echoserver@sha256:5d99aa1120524c801bc8c1a7077e8f5ec122ba16b6dda1a5d3826057f67b9bcb
    Port:           <none>
    Host Port:      <none>
    State:          Running
      Started:      Mon, 11 Apr 2022 01:47:36 +0300
    Ready:          True
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from kube-api-access-qvdns (ro)
Conditions:
  Type              Status
  Initialized       True
  Ready             True
  ContainersReady   True
  PodScheduled      True
Volumes:
  kube-api-access-qvdns:
    Type:                    Projected (a volume that contains injected data from multiple sources)
    TokenExpirationSeconds:  3607
    ConfigMapName:           kube-root-ca.crt
    ConfigMapOptional:       <nil>
    DownwardAPI:             true
QoS Class:                   BestEffort
Node-Selectors:              <none>
Tolerations:                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                             node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:                      <none>
❯ kubectl logs hello-node-6b89d599b9-s9p6z
❯ kubectl logs pod hello-node-6b89d599b9-s9p6z
Error from server (NotFound): pods "pod" not found
❯ kubectl logs  hello-node-6b89d599b9-s9p6z
❯ kubectl get nodes
Error from server (Forbidden): nodes is forbidden: User "system:serviceaccount:app-namespace:developer" cannot list resource "nodes" in API group "" at the cluster scope
```
### Конфиг локального куба
<img width="328" alt="2" src="https://user-images.githubusercontent.com/72221502/162696852-e8ecc15f-d797-4516-8f0c-233c9030c70c.png">


## Задание 3
<img width="542" alt="3" src="https://user-images.githubusercontent.com/72221502/162696927-19678550-a1ca-4067-b826-80937b4d384c.png">

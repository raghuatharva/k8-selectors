# k8-selectors
affinity , tolerations
# Selectors

Taint the node

```
kubectl taint nodes ip-192-168-44-187.ec2.internal hardware=gpu:NoSchedule
```
NoSchedule -- it means strictly no new pods can be entered
PreferNoSchedule  -- can be entered 
NoExecute -- it means iro pods na kooda aaache haakutte node inda ;
-->        special case:  
  if a pod with toleration , then that pod will stay in node with NoExecute. no new pod with or without toleration can enter


Untaint
```
kubectl taint nodes ip-192-168-44-187.ec2.internal hardware=gpu:NoSchedule-
```

Label node

```
kubectl label nodes ip-192-168-44-187.ec2.internal hardware=gpu
```
Ref: https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes

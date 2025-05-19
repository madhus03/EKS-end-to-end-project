# Install EKS
---------------------------------------------------------------------------------------------------------------------------------------------------------------------


Please follow the prerequisites doc before this.

## 1. Install using Fargate

 ```bash  
`eksctl create cluster --name demo-cluster --region us-east-1 --fargate
```

## 2. Delete the cluster

```bash   
`eksctl delete cluster --name demo-cluster --region us-east-1
```


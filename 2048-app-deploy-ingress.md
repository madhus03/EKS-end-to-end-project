# 1. How to create a Fargate profile 

```bash
     eksctl create fargateprofile \
    --cluster demo-cluster \
    --region us-east-1 \
    --name alb-sample-app \
    --namespace game-2048`
```


# 2. Deploy the deployment, service and ingress as a single YAML file and host that YAML file online. 
to do that :

- Login to your github account 
- create a public repo
- upload the filenamefull.yaml file 
- After uploading, click on the file and then click “Raw”
- Copy the raw file URL — it will look like: https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/examples/2048/2048_full.yaml


now, 

```bash kubectl apply -f https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/examples/2048/2048_full.yaml```


![alt text](image.png)

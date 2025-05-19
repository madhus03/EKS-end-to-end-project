how to create a Fargate profile 

```eksctl create fargateprofile \
    --cluster demo-cluster \
    --region us-east-1 \
    --name alb-sample-app \
    --namespace game-2048```


Deploy the deployment, service and ingress as a single YAML file and host that YAML file online. 
to do that :

1. Login to your github account 
2. create a public repo
3. upload the filenamefull.yaml file 
4. After uploading, click on the file and then click “Raw”
5. Copy the raw file URL — it will look like: https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/examples/2048/2048_full.yaml


now, 

`kubectl apply -f https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.5.4/docs/examples/2048/2048_full.yaml`


![alt text](image.png)
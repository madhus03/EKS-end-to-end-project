STEP BY STEP INSTRCUTIONS ON SETTING UP alb add on & DEPLOYING ALB CONTROLLER

1. Download IAM POLICY 

<<<<<<< HEAD
'curl -O https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.11.0/docs/install/iam_policy.json'

2. Create IAM Policy

'''aws iam create-policy \
    --policy-name AWSLoadBalancerControllerIAMPolicy \
    --policy-document file://iam_policy.json'''

3. Create IAM Role    

'''eksctl create iamserviceaccount \
=======
`curl -O https://raw.githubusercontent.com/kubernetes-sigs/aws-load-balancer-controller/v2.11.0/docs/install/iam_policy.json`

2. Create IAM Policy

```aws iam create-policy \
    --policy-name AWSLoadBalancerControllerIAMPolicy \
    --policy-document file://iam_policy.json```

3. Create IAM Role    

```eksctl create iamserviceaccount \
>>>>>>> c47092f ( code changes are fixed)
  --cluster=<your-cluster-name> \
  --namespace=kube-system \
  --name=aws-load-balancer-controller \
  --role-name AmazonEKSLoadBalancerControllerRole \
  --attach-policy-arn=arn:aws:iam::<your-aws-account-id>:policy/AWSLoadBalancerControllerIAMPolicy \
<<<<<<< HEAD
  --approve'''
=======
  --approve```
>>>>>>> c47092f ( code changes are fixed)

Deploy ALB controller

1. Add helm repo 

<<<<<<< HEAD
'helm repo add eks https://aws.github.io/eks-charts'

2. Update the repo 

'helm repo update eks'

3. Install 

'''helm install aws-load-balancer-controller eks/aws-load-balancer-controller \            
=======
`helm repo add eks https://aws.github.io/eks-charts`

2. Update the repo 

`helm repo update eks`

3. Install 

```helm install aws-load-balancer-controller eks/aws-load-balancer-controller \            
>>>>>>> c47092f ( code changes are fixed)
  -n kube-system \
  --set clusterName=<your-cluster-name> \
  --set serviceAccount.create=false \
  --set serviceAccount.name=aws-load-balancer-controller \
  --set region=<region> \
<<<<<<< HEAD
  --set vpcId=<your-vpc-id>'''

4. verify that the deployments are running 

'kubectl get deployment -n kube-system aws-load-balancer-controller'
=======
  --set vpcId=<your-vpc-id>```

4. verify that the deployments are running 

`kubectl get deployment -n kube-system aws-load-balancer-controller`
>>>>>>> c47092f ( code changes are fixed)

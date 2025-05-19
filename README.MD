**FOLLOW THE ENTIRE DOCUMENTATION ON MEDIUM - https://medium.com/@mathangi2197/deploying-a-serverless-2048-game-using-aws-eks-and-fargate-2587338c2440**

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Setting up your AWS Environment for EKS

1. Configuring the AWS CLI and kubectl

1.1 Installing the AWS CLI:

- Download and install the AWS CLI on your local machine. You can find installation instructions for various operating systems here.

1.2 Configuring AWS CLI Credentials:

- Open a terminal or command prompt and run the following command:

```bash 
aws configure
```

- Enter the access key ID and secret access key of the IAM user you created earlier.
- Choose a default region and output format for AWS CLI commands.

1.3 Installing kubectl:

- Install kubectl on your local machine. 

1.4 Configuring kubectl for EKS:

- Once kubectl is installed, you need to configure it to work with your EKS cluster.
- In the AWS Management Console, go to the EKS service and select your cluster.
- Click on the "Config" button and follow the instructions to update your kubeconfig file. - Alternatively, you can use the AWS CLI to update the kubeconfig file:

```bash
aws eks update-kubeconfig --name your-cluster-name
```

- Verify the configuration by running a kubectl command against your EKS cluster:

```bash
kubectl get nodes
```



Setting up your AWS Environment for EKS

1.1 Configuring the AWS CLI and kubectl

Installing the AWS CLI:

- Download and install the AWS CLI on your local machine. You can find installation instructions for various operating systems here.

Configuring AWS CLI Credentials:

- Open a terminal or command prompt and run the following command:

aws configure

- Enter the access key ID and secret access key of the IAM user you created earlier.
- Choose a default region and output format for AWS CLI commands.

Installing kubectl:

- Install kubectl on your local machine. 

Configuring kubectl for EKS:

- Once kubectl is installed, you need to configure it to work with your EKS cluster.
- In the AWS Management Console, go to the EKS service and select your cluster.
- Click on the "Config" button and follow the instructions to update your kubeconfig file. - Alternatively, you can use the AWS CLI to update the kubeconfig file:

aws eks update-kubeconfig --name your-cluster-name

- Verify the configuration by running a kubectl command against your EKS cluster:

kubectl get nodes



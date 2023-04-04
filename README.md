# Kube-Deployment-AWS-EKS-

# 🍎Deployment Options

## 1\Custom Data Center

## 2\Cloud Prodiver

# 🍉 AWS EKS vs AWS ECS

## 1\ AWS EKS => Elstic Kubernetes Service

## 2\ AWS ECS => Elastic Container service

## The differnce between the EKS & ECS , EKS is managed service for kubernetes, and ECS managed service for container deployments

7W1SGOwTdVpxTjFa

## To get the service name the url adres: minikube service users-service

# 🌈 Create EKS cluster

## 1\ From AWS console search for EKS

## 2\ Cleck on Create Cluster

## 3\ Provide a Cluster name

## 4\ Add IAM role

### a\ chose EKS, then EKS Cluster, this will give EKS all permissons it needs, cleck next, give the cluster name, then create role

## 5\ Back to configuration cluster, choose the role created, then cleck next

## 6\ Set up the network for the cluster

## 7\ Search for cloud formation then open it, cloud formation is a service that allow to create things with services

### a\ Cleck create, then copy: https://s3.us-west-2.amazonaws.com/amazon-eks/cloudformation/2020-10-29/amazon-eks-vpc-private-subnets.yaml, then cleck next

### b\ give a name , for example: eksvpc, then next, then next, then submit, this will creat a vpc network for you

## 8\ Go to Cluster page then choose the VPC created

## 9\ For cluster endpoint choose public and privite, then next, then next

## 10\ Finally we have EKS CLUSTER CREATED

## 11\ Modify kubectl config file , that exist root user ".kube", before kubectl oint to minikube, but now we want it to point to EKS, so copy the file the change the name then modify the file to connect to EKS

## 12\ The easiest way to overwrite the config file is by using AWS CLI

## 13\ Configure your AWS CLI on your machine

## 14\ run: aws eks --region use-east-1 update-kubeconfig --name kube-dep-demo => this we configure the file in order to allow to kubectl to talk aws cluster

## 15/kubectl get pods

## 16\ delete minikube cluster

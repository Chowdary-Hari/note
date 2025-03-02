## Ebs volumes
- create EBS volume in AWS
- install EBS drivers in the EKS cluster
- attach EBS-CSI policy in the IAM role `To allow your EC2 instances (nodes) to connect with EBS (Elastic Block Store) volumes, you need to attach the AmazonEC2EBSCSI policy to the IAM role assigned to your EC2 instances`
---
  - **AmazonEBSCSIDriverPolicy**  
    *Allows EKS nodes to interact with Amazon Elastic Block Store (EBS) using the EBS CSI (Container Storage Interface) driver.*

    - **AmazonEC2ContainerRegistryReadOnly**  
      *Grants read-only access to Amazon Elastic Container Registry (ECR).*

    - **AmazonEKS_CNI_Policy**  
      *Grants permissions required by the Amazon VPC CNI plugin, which manages networking for EKS pods.*

    - **AmazonEKSWorkerNodePolicy**  
      *Provides necessary permissions for EKS worker nodes to function properly, including communication with the EKS control plane.*

    - **AmazonSSMManagedInstanceCore**  
      *Grants permissions for AWS Systems Manager (SSM) to manage EC2 instances.*
---
- create pv 
- create pvc
- create pod
  

# Palo Alto VM-Series & CN-Series AWS Security Lab
<img src="https://i.imgur.com/2Qjg8L3.png" height="80%" alt="AWS" />
## Overview
This lab explores **Palo Alto Networks VM-Series & CN-Series firewalls in AWS** using the **Ultimate Test Drive (UTD) AWS 3.0 Workshop**. It provides hands-on experience with **AWS-based network security**, focusing on **firewall deployment, Zero Trust policies, Log4j attack defense, machine learning-powered threat prevention, and Kubernetes security**.

## Lab Setup
The lab consists of:
- **Palo Alto VM-Series Firewall on AWS**
- **AWS VPC, EC2 Instances, and AWS Gateway Load Balancer (GWLB)**
- **CN-Series Firewall on Amazon Elastic Kubernetes Service (EKS)**
- **AWS IAM, Terraform, and CloudWatch Integration**

## Objectives
- **Deploy and configure the Palo Alto VM-Series firewall** in AWS
- **Secure inbound, outbound, and east-west traffic** in a cloud environment
- **Implement Zero Trust security policies** for AWS workloads
- **Enable ML-powered threat intelligence** for malware and URL filtering
- **Simulate and block Log4j attacks** using Palo Alto's advanced security controls
- **Deploy CN-Series containerized firewall** in Amazon EKS
- **Secure Kubernetes workloads** using dynamic address groups and security policies
- **Integrate with AWS CloudWatch** for real-time firewall monitoring

## Configuration Steps

### **1. Deploy VM-Series Firewall on AWS**
- Log into AWS Console and provision **EC2 instances**
- Deploy VM-Series firewall with **AWS Gateway Load Balancer (GWLB)**
- Configure firewall **interfaces, zones, and routing**

### **2. Review & Secure VM-Series Firewall Configuration**
- Install the **latest Application & Threat Content**
- Enable **Vulnerability Protection, Anti-Spyware, and WildFire Analysis**
- Configure **Zero Trust security policies** for inbound and outbound traffic

### **3. Simulate and Block Log4j Attacks**
- Execute a simulated **Log4j exploit** on a vulnerable web server
- Review attack logs in **Palo Alto Threat Monitor**
- Configure security policies to **block Log4j attacks**

### **4. Enable ML-Powered Security & Threat Intelligence**
- Enable **Inline ML-powered analysis** in AV and URL filtering profiles
- Apply updated **security profiles** to the firewall rules
- Enable **real-time WildFire signature updates**

### **5. Optimize Security Policies with Policy Optimizer**
- Identify and convert **port-based rules** into **application-based policies**
- Enable **dynamic security rule adjustments** based on real-time analytics

### **6. Enable AWS CloudWatch Integration**
- Configure the firewall to **publish security metrics** to AWS CloudWatch
- Monitor **firewall performance and threat activity** in CloudWatch

### **7. Deploy CN-Series Firewall in Amazon EKS**
- Set up **IAM permissions** and deploy **Kubernetes clusters**
- Deploy **CN-Series Management & Data Plane** components
- Integrate **Panorama Kubernetes Plugin** for centralized security management

### **8. Secure Kubernetes Workloads with CN-Series Firewall**
- Deploy **application pods** in Amazon EKS
- Configure **Dynamic Address Groups (DAGs) and security policies**
- Enforce security rules for **pod-to-pod and external communication**

## **Verification & Testing**
### **1. Verify Firewall Security Policies & Logs**
```shell
show security policies
show session all
show traffic log
```
### **2. Check Log4j Attack Prevention Logs**
```shell
show threat log | match log4j
```
### **3. Verify Kubernetes Security Rules**
```shell
kubectl get pods -A | grep pan
kubectl get services -n sample-app
```

## **Repository Structure**
```
├── configs/
│   ├── VM-Series_AWS_Config.txt  # Configuration for VM-Series on AWS
│   ├── CN-Series_EKS_Config.txt  # Configuration for CN-Series on Kubernetes
├── README.md                     # Documentation
├── screenshots/                  # Screenshots of verification outputs
└── topology.png                   # Network diagram
```

## **Conclusion**
This lab provides **real-world experience in deploying and securing workloads in AWS** using **Palo Alto VM-Series and CN-Series firewalls**. It covers **Zero Trust policies, cloud-native security, machine learning-driven threat protection, and Kubernetes security automation**, making it an essential resource for **cloud security professionals**.

---
**Author:** Travis Johnson  
**Company:** 10Digit Solutions LLC  
**GitHub Repository:** [Add link when available]

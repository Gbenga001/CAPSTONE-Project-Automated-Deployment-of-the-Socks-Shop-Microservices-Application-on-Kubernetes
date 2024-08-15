# **Socks Shop Microservices-based Application Deployment on Kubernetes using IaC.**
![image](https://github.com/user-attachments/assets/9a386d37-9ac3-49c1-971f-646a10e96c73)

![image](https://github.com/user-attachments/assets/37cdb6b5-767b-475f-9800-9bae79c7db6e)

**PROJECT LIVE LINK:** [CAPSTONE PROJECT LINK](https://docs.google.com/document/d/1Jp7MKwC2iJD4UObQOvz5wtdPY5gmRkLlIclGIpOmLFU/edit)

##

## **Project Overview:**

The Socks Shop application is a popular microservices-based e-commerce platform that is used as a reference application for demonstrating modern cloud-native technologies. The application is composed of multiple microservices, each of which is responsible for a specific function, such as product catalog, shopping cart, and user authentication. The application is designed to be highly scalable, resilient, and fault-tolerant, making it an ideal candidate for deployment on Kubernetes.

The project will involve deploying the Socks Shop application on a Kubernetes cluster using an Infrastructure as Code (IaC) approach. This will include provisioning the necessary infrastructure resources on AWS, setting up a deployment pipeline, monitoring the performance and health of the application, and securing the infrastructure.

The project will be implemented using Terraform for infrastructure provisioning, GitHub Actions for the deployment pipeline, Kubernetes for container orchestration, Helm for package management, Prometheus for monitoring, ELK Stack for logging, and Ansible for security.

## **This project will include the following components:**

- [Infrastructure Provisioning](#infrastructure-provisioning)
- [Deployment Pipeline](#deployment-pipeline)
- [Monitoring](#monitoring)
- [Logging](#logging)
- [Security](#security)
- [conclusion](#conclusion)
- [References](#references)

## **Project Requirements:**

- Terraform
- AWS Account
- Kubernetes
- Helm
- Prometheus
- ELK Stack
- Let's Encrypt
- Socks Shop Application

## **Project Deliverables:**

- Terraform configuration files for provisioning the infrastructure on AWS
- Deployment pipeline configuration using GitHub Actions
- Kubernetes manifests for deploying the Socks Shop application
- Prometheus configuration for monitoring the Socks Shop application
- ELK Stack configuration for centralized logging
- Ansible playbooks for securing the infrastructure
- Documentation on how to run the project

## **Project Structure:**

```
socks-shop-deploy/
├── .github/
│   └── workflows/
│       └── ci-cd.yaml    # GitHub Actions workflow for CI/CD
├── k8s/
│   ├── deployment.yaml   # Kubernetes deployment manifests
│   └── ingress.yaml      # Kubernetes ingress manifest
├── monitoring/
│   ├── prometheus/
│   │   └── values.yaml   # Custom values for Prometheus Helm chart
│   └── grafana/
│       └── values.yaml   # Custom values for Grafana Helm chart
├── logging/
│       ├── elasticsearch.yaml  # Elasticsearch deployment
│       ├── filebeat.yaml       # Fluentd configuration
│       └── kibana-deployment.yaml         # Kibana dashboard configuration
|       └── cronjob.yaml        # Fluentd configuration
|       └── metricbeat.yaml     #  Fluentd configuration
|       └── logstash-deployment.yaml        # Fluentd configuration
├── terraform/
│   ├── main.tf         # Main Terraform configuration for AWS EKS
│   ├── terraform.tf    # Terraform configuration
│   ├── outputs.tf      # Terraform outputs
│   ├── provider.tf     # Provider configuration
│   └── vpc.tf          # VPC configuration
└──README.md
```

The project will be organized into the following directories:

- `Infrastructure`: This directory will contain the Terraform configuration files for provisioning the necessary infrastructure resources on AWS, including VPCs, subnets, security groups, and EKS cluster.
- `kubernetes`: This directory will contain the Kubernetes manifests for deploying the Socks Shop application, including deployment and ingress resources.
- `CI/CD`: This directory will contain the GitHub Actions workflow files for setting up a deployment pipeline to build and deploy the Socks Shop application to the Kubernetes cluster.
- `Monitoring`: This directory will contain the configuration files for setting up Prometheus to monitor the performance and health of the Socks Shop application.
- `Logging`: This directory will contain the configuration files for setting up a centralized logging solution, such as ELK stack, to collect and analyze logs from the Socks Shop application.

The project will also include a `README.md` file in each directory to provide detailed instructions on how to set up and configure the components.

## **Prerequisites:**

The following tools and technologies will be used in the project:

- Terraform: Terraform is an open-source infrastructure as code software tool that provides a consistent CLI workflow to manage hundreds of cloud services. It codifies APIs into declarative configuration files, creating infrastructure as code using a high-level configuration language called HCL (HashiCorp Configuration Language).

- AWS Account: An AWS account will be required to provision the necessary infrastructure resources, such as VPCs, subnets, security groups, and EKS cluster.

- GitHub Actions: GitHub Actions will be used to set up a deployment pipeline to build and deploy the Socks Shop application to the Kubernetes cluster.

- Kubernetes: Kubernetes is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications.

- Helm: Helm is a package manager for Kubernetes that provides an easy way to find, share, and use software built for Kubernetes.

- Prometheus: Prometheus is an open-source monitoring and alerting toolkit designed for reliability and scalability. It collects metrics from configured targets at given intervals, evaluates rule expressions, displays the results, and can trigger alerts if some condition is observed to be true.

- ELK Stack: The ELK Stack is a collection of three open-source products — Elasticsearch, Logstash, and Kibana — all developed, managed, and maintained by Elastic. The ELK Stack is used to collect, search, analyze, and visualize log data in real time.

- Let's Encrypt: Let's Encrypt is a free, automated, and open certificate authority brought to you by the nonprofit Internet Security Research Group (ISRG).

- Docker: Docker is a set of platform as a service (PaaS) products that use OS-level virtualization to deliver software in packages called containers.

- Socks Shop Application: The Socks Shop application is a popular microservices-based e-commerce platform that is used as a reference application for demonstrating modern cloud-native technologies.

## **Project Objectives:**

The main objectives of the project are as follows:

- Deploy the Socks Shop application on a Kubernetes cluster using an Infrastructure as Code (IaC) approach
- Provision the necessary infrastructure resources on AWS, including VPCs, subnets, security groups, and EKS cluster
- Set up a deployment pipeline using GitHub Actions to build and deploy the Socks Shop application to the Kubernetes cluster
- Monitor the performance and health of the Socks Shop application using Prometheus
- Collect and analyze logs from the Socks Shop application using a centralized logging solution, such as ELK stack.

#

## **GETTING STARTED**

Socks Shop Resources: https://github.com/microservices-demo/microservices-demo.github.io

Demo: https://github.com/microservices-demo/microservices-demo/tree/master

## **Infrastructure Provisioning:**

Using Terraform, we will provision the necessary infrastructure resources on AWS, including VPCs, subnets, security groups, and EKS cluster. This will allow for a clear and reproducible infrastructure setup.

1.  Make sure you have installed Terraform alongside AWS CLI on your local machine. If not, you can download it from the official website.

    [AWS CLI Installation guide](https://aws.amazon.com/cli/)

    [Terraform Download](https://www.terraform.io/downloads.html)

2.  Create a new directory for the Terraform configuration files and navigate to it.

        mkdir Socks-Shop_Terraform
        cd Socks-Shop_Terraform

3.  Git clone this repository and navigate to the terraform folder to have the Terraform configuration files and initiate the Terraform project.

        git clone https://github.com/Gbenga001/Socks-Shop/Terraform

4.  Run the following command to initialize the Terraform project:

        terraform init
![terraforminit](https://github.com/user-attachments/assets/66e74391-7907-4b90-a71f-3afb0b91a0d8)


5.  Run the following command to create an execution plan:

        terraform plan

6.  Run the following command to apply the changes:

7. ![terraformapply](https://github.com/user-attachments/assets/842dccbd-4425-4de2-ad1c-08701f95b07e)


        terraform apply --auto-approve

        #the flag --auto-approve can be added to avoid the prompt for confirmation.

![terraform-init](https://github.com/user-attachments/assets/f609c40c-d0a9-4fc9-93fd-9d02828f581f)


Below is a screenshot of my EKS cluster being provisioned by terraform👇🏽:

![AWS-EKS](https://github.com/user-attachments/assets/96f6cfdf-a111-4179-a99c-25a64f224321)
My VPC
![AWSVPC](https://github.com/user-attachments/assets/85dd8cfe-bb77-4385-80f2-92f08d4f0b3f)


This below command allow us to configure the kubectl to connect to the EKS cluster, the specified region and the cluster name.



    aws eks update-kubeconfig --name=socksShop-eks-U2VM9 --region=us-east-1
![awsnodegroups](https://github.com/user-attachments/assets/801610b3-1e92-4ef8-8d09-5a465d5a41bb)


7.  After the infrastructure has been provisioned, you will see the output of the Terraform apply command, including the EKS cluster endpoint and the kubeconfig file.

- We apply our deployment manifests to our cluster using the following command:

        kubectl apply -f kubernetes/deployment.yaml
![eks](https://github.com/user-attachments/assets/96bfbb8a-3a1a-4e56-abfd-6b042de79e44)


8.  You can use the kubeconfig file to access the Kubernetes cluster and deploy the Socks Shop application.

![frontend](https://github.com/user-attachments/assets/9dfad751-40fb-46e5-ab06-7dff9c73f78f)


9.  You can also use the following command to verify that the Socks Shop application is running on the Kubernetes cluster:

        kubectl get all -A

   ![kubectldescribe](https://github.com/user-attachments/assets/31431316-ce1a-4f5c-b4cc-2017af6d4c45)


10. After we confirm that our pods are running, we can now test the application by port-forwarding the service to our local machine using the following command:

        kubectl port-forward service/front-end -n sock-shop 30001:80

   ![kubectl-get-pods](https://github.com/user-attachments/assets/e6cbd5f2-b4d9-4b4e-ad2a-e33e0aad7f0a)

The following screenshot captures the pods running
   ![kubectl-get-svc](https://github.com/user-attachments/assets/934e151b-00d6-44b0-9c99-c5d41a495052)



## **Deployment Pipeline:**

The deployment pipeline will be configured using a GitHub Actions workflow file, which will define the steps required to build and deploy the Socks Shop application. The workflow file will be triggered by a push to the main branch of the repository, and will include the following steps:

Our workflow file must be in our root directory for our GitHub Actions to detect the file automatically.

- Checkout the source code from the repository
- Build the Docker images for the Socks Shop application
- Deploy the Socks Shop application to the Kubernetes cluster

The deployment pipeline will be configured to run automatically whenever changes are pushed to the main branch of the repository, ensuring that the Socks Shop application is always up to date and running the latest version.

![image](https://github.com/user-attachments/assets/e9dfee90-3736-44f1-8a27-a660b972cea8)

![image](https://github.com/user-attachments/assets/3c9809a1-0d11-4952-9326-6fe3d7b8f632)


## **Monitoring**

Prometheus will be used to monitor the performance and health of the Socks Shop application. This will include metrics such as request latency, error rate, and request volume. The Prometheus server will be configured to scrape metrics from the Socks Shop application and store them in a time-series database. Grafana will be used to visualize the metrics and create dashboards to monitor the performance and health of the application.

First create the monitoring namespace using the `00-monitoring-ns.yaml` file:

    kubectl create -f 00-monitoring-ns.yaml

![image](https://github.com/user-attachments/assets/fab14ca2-bce1-48bf-a2d6-90bfcb27e396)


- **Prometheus**

To deploy simply apply all the prometheus manifests (01-10) in any order:

    kubectl apply $(ls *-prometheus-*.yaml | awk ' { print " -f " $1 } ')

The prometheus server will be exposed on Nodeport `31090` using the following command:

    kubectl port-forward service/prometheus 31090:9090 -n monitoring


![image](https://github.com/user-attachments/assets/fab14ca2-bce1-48bf-a2d6-90bfcb27e396)

- **Grafana**

First apply the grafana manifests from 20 to 22:

    kubectl apply $(ls *-grafana-*.yaml | awk ' { print " -f " $1 }'  | grep -v grafana-import)

Once the grafana pod is in the Running state apply the `23-grafana-import-dash-batch.yaml` manifest to import the Dashboards:

    kubectl apply -f 23-grafana-import-dash-batch.yaml

Grafana will be exposed on the NodePort `31300` using the following command:

    kubectl port-forward service/grafana 31300:3000 -n monitoring

- Below is the screenshot:👇🏽
  ![image](https://github.com/user-attachments/assets/08c1c38a-c6cc-4a72-b460-fb622c3df8a1)

  ![image](https://github.com/user-attachments/assets/ce013b06-988b-4568-9e77-3dc7d47e7782)


## **Logging:**

We will use the ELK stack to collect and analyze logs from the Socks Shop application. The ELK stack is a collection of three open-source products — Elasticsearch, Logstash, and Kibana — all developed, managed, and maintained by Elastic. The ELK Stack is used to collect, search, analyze, and visualize log data in real time.

- Below is the screenshot showing the deployment of logging to our cluster:👇🏽

![image](https://github.com/user-attachments/assets/37d23cf4-709b-4731-97d9-a034e3ddab98)


- We verify that our pods are running the freshly deployed logging services.
 ![image](https://github.com/user-attachments/assets/f70c2267-9679-496c-8716-4e8c9f50675a)

- After the successful deployment of the loggings into our cluster, we use the following command to portfoward the service to we can access it locally;

        kubectl port-forward service/kibana 5601:5601 -n kube-system

![image](https://github.com/user-attachments/assets/cd953cbf-fadc-4c30-bad0-cad2630fc1c6)


## **Security:**

The application will be secured with HTTPS using a Let's Encrypt certificate. Let's Encrypt is a free, automated, and open certificate authority that provides free SSL/TLS certificates for websites. The certificate will be used to secure the communication between the client and the Socks-Shop application, ensuring that the data is encrypted and secure.


![image](https://github.com/user-attachments/assets/a2e9e77a-c304-41d5-8658-b3babffe63e1)

## **Conclusion:**

This project will provide hands-on experience with Infrastructure as Code, Kubernetes, DevOps best practices, and cloud security. It will also demonstrate the value of automation and monitoring in ensuring the reliability and performance of microservices-based applications. By the end of the project, you will have a fully functional deployment pipeline for the Socks Shop application, including infrastructure provisioning, monitoring, logging, and security.

![CATALOGUE](https://github.com/user-attachments/assets/36417fda-4e4a-48ec-a2ff-dda41b190144)


#

## **References:**

- [Terraform Documentation](https://www.terraform.io/docs/index.html)
- [AWS Documentation](https://docs.aws.amazon.com/index.html)
- [Kubernetes Documentation](https://kubernetes.io/docs/home/)
- [Prometheus Documentation](https://prometheus.io/docs/)
- [ELK Stack Documentation](https://www.elastic.co/guide/index.html)
- [Ansible Documentation](https://docs.ansible.com/ansible/latest/index.html)
- [Let's Encrypt Documentation](https://letsencrypt.org/docs/)
- [Docker Documentation](https://docs.docker.com/)
- [Socks Shop Application](https://github.com/microservices-demo/microservices-demo.github.io)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)


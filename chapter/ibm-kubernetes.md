# IBM Kubernetes Service Ashley Thornton sp20-516-230

## Introduction

The IBM Cloud Kubernetes service deploys highly available containers by
 creating a cluster of compute hosts. It allows users to manage the resources
  they need securely, deploying, updating, and scaling applications 
  [@kubernetescluster-sp20-516-230].
 
Here we can see the evolution of containers to visually understand how
 Kubernetes is an ideal solution.
 
![Container Evolution[@container_evolution]](container_evolution.png){#fig:container_evolution}

## Features

* IBM Cloud Kubernetes service is fully managed at scale and enable workload
 diversity. IBM Watson and IBM Blockchain Platform both run on Kubernetes. The 
 service provides continuous availability through clusters across 35 data
 centers.
 
* The clusters used within the Kubernetes service are highly secure at the
 container level and compliant with industry standards.
 
* Kubernetes provides the ability to integrate with other IBM products
 automatically and securely.
  
* Intelligent provisioning places containers onto available hosts.
 
* If a container is damaged, measures are in place for it to self-heal.
 
* High operational visibility is provided so that users can troubleshoot and
 monitor as appropriate.
  
[@containerservice-sp20-516-230]
 
## Pricing
 
IBM offers a free version that includes:
* 2 CPUs
* 4 GB RAM
* 1 worker node
 
IBM also offers a pay-as-you-go plan. Details on the pricing for this option
 can be found [here](https://www.ibm.com/cloud/container-service/pricing
 ) [@pricing-sp20-516-230].
  
## Getting Started

To begin using the free version of Kubernetes, one must first create a Lite
 account. That can be accomplished [here](https://www.ibm.com/cloud/free
 ) [@createaccount-sp20-516-230].

After logging in, one must upgrade their account to pay-as-you-go. Although
 the Kubernetes cluster we will be creating is free, the account must be
  first upgraded to access the Kubernetes service.

Next, a free cluster can be created. In the IBM cloud catalog found 
[here](https://cloud.ibm.com/catalog), click on `Kubernetes Service` under 
`Featured` [@catalog-sp20-516-230]. This can be found towards the top left-hand 
side of the page. From here, click on `Free cluster` and then `Create`. If
 desired, a standard cluster can be created instead starting at $0.11 per hour.
    
The next web page provides instructions on how to set up CLI tools and gain
 access to the new cluster.
 
 * Run the following command in PowerShell in order to download and install
  the necessary CLI tools:
  
        Set-ExecutionPolicy Unrestricted; iex(New-Object Net.WebClient).DownloadString('http://ibm.biz/idt-win-installer')
  
 * Log into your IBM cloud account you created earlier using the following
  command:
  
        ibmcloud login -a cloud.ibm.com -r us-south -g <resourceGroupName>

 * Download necessary files to your new cluster:
 
        ibmcloud ks cluster config --cluster bps0pned0g43mrlq5vp0
        
 * Set the environmental variable for KUBECONFIG. This can be done by
  copying the output from the prior command, and should look similar to this:
  
        export KUBECONFIG=%HOMEPATH%\.bluemix\plugins\container-service\clusters\bps0pned0g43mrlq5vp0\kube-config-hou02-mycluster.yml
  
 * Verify connectivity to the cluster via the following command:
 
        kubectl version --short

 These instructions detail how to get started. If interested, one can create
  a registry and enable continuous delivery. IBM even offers a free hour-long
   virtual consultation to help make the most out of Kubernetes.
 
 ## Kubernetes in Action
 
 As previously mentioned, Kubernetes can easily be integrated with other IBM
  products. One example of this is the IBM Cloud Kubernetes Service, which is
   a managed container solution. This product automates operations and
    deployments plus add IBM capabilities. It can bind to other services
     include IBM blockchain and Watson.
     
 Another example is Red Hat OpenShift on IBM Cloud. It includes the ability
  of using OpenShift clusters, from the Kubernetes platform, on the IBM Cloud
   platform [@kubernetes-sp20-516-230].
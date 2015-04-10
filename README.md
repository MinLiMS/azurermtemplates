# Azure Resource Manager Templates

# Contributing guide

This is a repo that contains all the currently available Azure Resource Manager templates contributed by the community. We'll soon allow a way for these templates to be indexed on [Azure.com](http://azure.microsoft.com) and be discoverable from there.

To make sure your template is added to Azure.com index, please follow these guidelines. Any templates that are out of compliance will be added to the **blacklist.json** file and not be indexed on Azure.com

1.	Every template must be contained in its own **folder**. Name this folder something that describes what your template does
2.	The template file must be named **azuredeploy.json**
3.	The template folder must host the **scripts** that are needed for successful template execution
4.	The template folder must contain a **metadata.json** file to allow the template to be indexed on [Azure.com](http://azure.microsoft.com)
  *	Guidelines on the metadata file below
5.	Every parameter in the template must have the **description** specified using the metadata property. See the starter template is provided [here](https://github.com/azurermtemplates/azurermtemplates/tree/master/100-starter-template-with-validation) on how to do this
6.	OPTIONAL: The folder may contain a **Readme.md** file for any additional information about the template

## metadata.json file

Here are the required parameters for a valid metadata.json file

<del>
    {
      "TemplateName": "",
      "Description": "",
      "ShortDescription": "",
      "GithubUsername": "",
      "DateUpdated": "<e.g. 2015-12-20>"
    }
</del>

####Update 4/9####
To be more consistent with the Visual Studio and Gallery experience we're updating the metadata.json file structure. The new structure looks like below

    {
      "itemDisplayName": "",
      "description": "",
      "summary": "",
      "githubUsername": "",
      "dateUpdated": "<e.g. 2015-12-20>"
    }

The metadata.json file will be validated using these rules

**itemDisplayName**
*	Cannot be more than 60 characters

**description**
*	Cannot be more than 1000 characters
*	Cannot contain HTML

**summary**
*	Cannot be more than 200 characters

**githubUsername**
*	Username must be the same as the username of the author submitting the Pull Request

**dateUpdated**
*	Must be in yyyy-mm-dd format.
*	The date must not be in the future to the date of the pull request

## Starter template

A starter template is provided [here](https://github.com/azurermtemplates/azurermtemplates/tree/master/100-starter-template-with-validation) for you to follow

## 101 templates
These are simple example templates with single actions for common requirements.

| # | Deploy to Azure  | Author                          | Template Name   | Description     |
|:------|:-----------------|:--------------------------------| :---------------| :---------------|
| 101-1 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-create-availability-set" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy an Availability Set](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-create-availability-set) | This template allows you to create an Availability Set in your subscription.|
| 101-2 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-loadbalancer-with-nat-rule" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy a Load Balancer with an Inbound NAT Rule](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-loadbalancer-with-nat-rule) | This template allows you to create a load balancer with NAT rule in your subscription.|
| 101-3 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-virtual-network" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy a Virtual Network](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-virtual-network) | This template allows you to deploy a Virtual Network. |
| 101-4 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-simple-vm-from-image" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy a Simple Virtual Machine from an  Image](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-simple-vm-from-image) | This template allows you to deploy a Simple Virtual Machines from an Image. |
| 101-5 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-networkinterface-with-publicip-vnet" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Create a Network Interface in a Virtual Network and associate it with a Public IP](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-networkinterface-with-publicip-vnet) | This template creates a simple Network Interface in a Virtual Network and attaches a Public IP Address to it. |
| 101-6 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-customdata" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy a Virtual Machine with Custom Data](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-customdata) | This template allows you to deploy a Virtual Machines by passing Custom Data to the VM. |
| 101-7 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101_create_key_vault" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [[101] Create a key Vault](https://github.com/azurermtemplates/azurermtemplates/tree/master/101_create_key_vault) | This template creates a Key Vault |
| 101-8 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-empty-data-disk" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [kenazk](https://github.com/kenazk) | [Windows VM with Empty Data Disk](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-empty-data-disk) | This template creates a Windows VM with a new empty data disk. |
| 101-9 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-from-user-image" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy a Virtual Machine from a User Image](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-from-user-image) | This template allows you to create a Virtual Machines from a User image. Prerequisite - The Storage Account with the User Image VHD should already exist in the same resource group. |
| 101-10 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-rbac-builtinrole-resourcegroup" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [manavis](https://github.com/manavis) | [Assign RBAC BuiltInRoles to an Existing Resource Group](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-rbac-builtinrole-resourcegroup) | This template assigns Owner, Reader or Contributor access to an existing resource group. |
| 101-11 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-sshkey" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Create Linux Virtual Machine and configure SSH Key](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-sshkey) | This template creates a Linux Virtual Machine and configures SSH Keys. Note: This template will be slightly modified in the coming weeks to allow SSH Keys to be passed in the standard PEM format  |
| 101-12 | <a href="https://github.com/azurermtemplates/azurermtemplates/tree/master/101-create-availability-set-3FDs" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [kenazk](https://github.com/kenazk) | [Create an Availability Set with 3 FDs configured](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-create-availability-set-3FDs) | This template snippet creates an Availability Set with 3 FDs |
| 101-13 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-create-security-group" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Create a network Security Group](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-create-security-group) | This template creates a Network Security Group|
| 101-14 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-multiple-data-disk" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> |[kenazk](https://github.com/kenazk) | [Create a VM from a Windows Image with 4 Empty Data Disks](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-multiple-data-disk) | Create a VM from a Windows Image with 4 Empty Data Disks|
| 101-15 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-empty-disk" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [kenazk](https://github.com/kenazk) | [Linux VM with Empty Data Disk](https://github.com/azurermtemplates/azurermtemplates/tree/master/101-vm-empty-disk) | This template creates a Linux VM with a new empty data disk. |

## 201 templates
These are more complex example templates with single actions for more advanced requirements.

| # | Deploy to Azure  | Author                          | Template Name   | Description     |
|:------|:-----------------|:--------------------------------| :---------------| :---------------|
| 201-1 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/201-discover-private-ip-dynamically" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Discover a VMs Private IP Dynamically](https://github.com/azurermtemplates/azurermtemplates/tree/master/201-discover-private-ip-dynamically) | This templates discovers a private ip of another VM dynamically|
| 201-2 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/201-2-vms-loadbalancer-natrules" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy 2 Windows VMs under Availability Set with NAT Rules through Load balancer](https://github.com/azurermtemplates/azurermtemplates/tree/master/201-2-vms-loadbalancer-natrules) | This template allows you to create 2 Windows Virtual Machines in an Availability Set and configure NAT rules through a load balancer. We also use the resource loops capability to create the network interfaces and virtual machines |
| 201-3 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/201-2-vms-loadbalancer-lbrules" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [ypitsch](https://github.com/ypitsch) | [Deploy 2 Windows VMs under a load balancer and configure a LB rule](https://github.com/azurermtemplates/azurermtemplates/tree/master/201-2-vms-loadbalancer-lbrules) | This template allows you to create 2 Windows Virtual Machines in an under a Load Balancer, configure LB rules for load balancing and NAT rules for RDP Access to each VM. We also use the resource loops capability to create the network interfaces and virtual machines. |
| 201-4 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/201-vm-different-rg-vnet" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Create a VM referencing a VNET in a different Resource Group](https://github.com/azurermtemplates/azurermtemplates/tree/master/201-vm-different-rg-vnet) | This template creates a VM in a VNET which is in a different Resource Group. You'll need to have the VNET created before running this template and pass the VNET name and its resource group name as input to this parameter. |
| 201-5 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/vm-push-certificate" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Create a VM and install a certificate referenced from an Azure Key Vault](https://github.com/azurermtemplates/azurermtemplates/tree/master/vm-push-certificate) | This template creates a VM and installs a certificate from the Azure Keyvault on the Virtual Machine. The template expects the Keyvault Name and the certificate URL of the certificate in KeyVault. |
| 201-6 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/201-dependency-between-scripts-using-extensions" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Execute Dependent script extensions to Configure and Install Mongo DB on a Ubuntu Virtual Machine](https://github.com/azurermtemplates/azurermtemplates/tree/master/201-dependency-between-scripts-using-extensions) | This template deploys Configures and Installs Mongo DB on a Ubuntu Virtual Machine in two separate scripts. This template is a sample that showcases how to express dependencies between two scripts running on the same virtual machine.|
| 201-7 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/201-2-vms-2-FDs-no-resource-loops" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Create 2 VMs in a Availability Set with 2 FDs without resource loops](https://github.com/azurermtemplates/azurermtemplates/tree/master/201-2-vms-2-FDs-no-resource-loops) | This template allows you to create 2 VMs in an Availabiltiy Set with 2 Fault Domains without resource loops |
| 201-8 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/201-vm-from-specialized-vhd" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Create a VM from a specialized VHD disk](https://github.com/azurermtemplates/azurermtemplates/tree/master/201-vm-from-specialized-vhd) | This template creates a VM from a specialized VHD |


## General Workloads
You can deploy the template to Azure by clicking the "Deploy to Azure" button below next to each template.

| # | Deploy to Azure  | Author                          | Template Name   | Description     |
|:------|:-----------------|:--------------------------------| :---------------| :---------------|
| 1 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/dsc-extension-iis-server-windows-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [VM DSC Extension IIS Server](https://github.com/azurermtemplates/azurermtemplates/tree/master/dsc-extension-iis-server-windows-vm) | This template allows you to deploy a VM with with a DSC extension that sets up an IIS server |
| 2 | <a href="https://azuredeploy.net/?repository=https://github.com/coreysa/deploy-docker-container" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [coreysa](https://github.com/coreysa) | [Deploy from DockerHub](https://github.com/coreysa/deploy-docker-container) | This template allows you to deploy a Docker container from DockerHub using Compose. |
| 3 | <a href="https://azuredeploy.net/?repository=https://github.com/coreysa/ubuntu-azure-dev-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [coreysa](https://github.com/coreysa) | [Deploy Ubuntu Azure Dev VM](https://github.com/coreysa/ubuntu-azure-dev-vm) | This template deploys an Ubuntu VM with the Azure Dev tools installed, which includes node. This executes a bash script pulled from GitHub. |
| 4 | <a href="https://azuredeploy.net/?repository=https://github.com/coreysa/deploy-docker-container-simple" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [coreysa](https://github.com/coreysa) | [Deploy from DockerHub (Simple Template)](https://github.com/coreysa/deploy-docker-container-simple) | This template allows you to deploy a Docker container from DockerHub using Compose with a very small amount of parameters (simple). |
| 5 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/chocolatey-app-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [drewm3](https://github.com/drewm3) | [Chocolatey VM](https://github.com/azurermtemplates/azurermtemplates/tree/master/chocolatey-app-vm) | This template allows you to create a VM with an application from Chocolatey.org installed. |
| 6 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/chef-extension-windows-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [VM with Chef extension](https://github.com/azurermtemplates/azurermtemplates/tree/master/chef-extension-windows-vm) | This template allows you to deploy a windows VM with Chef extension and run any recipe |
| 7 | <a href="https://azuredeploy.net/?repository=https://github.com/coreysa/ubuntu-azure-add-new-user" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [coreysa](https://github.com/coreysa) | [Deploy an Ubuntu VM with an additional sudo user](https://github.com/coreysa/ubuntu-azure-add-new-user) | The purpose of this script is to show how to execute a custom script with parameters passed throguh the template that will create an additional user with sudo access. The value of the sample is to show how to pass template parameter based input into a bash Linux script.|
| 8 | <a href="https://azuredeploy.net/?repository=https://github.com/liupeirong/Azure/tree/master/ARMPXC/ARMPXC.Deployment/Templates" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [paigeliu](https://github.com/liupeirong) | [Deploy a Percona XtraDB Cluster on CentOS or Ubuntu](https://github.com/liupeirong/Azure/tree/master/ARMPXC/ARMPXC.Deployment/Templates) | This template deploys a 3-node high availability MySQL Percona XtraDB Cluster 5.6 on CentOS 6.5 or Ubuntu 12.04 LTS.|
| 9 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/lamp-app" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> |[gbowerman](https://github.com/gbowerman) | [Deploy LAMP app on Ubuntu](https://github.com/azurermtemplates/azurermtemplates/tree/master/lamp-app) | This template uses the Azure Linux CustomScript extension to deploy a LAMP application by creating an Ubuntu VM, doing a silent install of MySQL, Apache and PHP, then creating a simple PHP script.|
| 10 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/openjdk-tomcat-ubuntu-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [snallami](https://github.com/snallami) | [VM-Ubuntu - Tomcat and Open JDK installation](https://github.com/azurermtemplates/azurermtemplates/tree/master/openjdk-tomcat-ubuntu-vm) | This template allows you to create a Ubuntu VM with OpenJDK and Tomcat.|
| 11 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/resource-loop-vms-vnet" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy 'N' Virtual Machines in a Single Click](https://github.com/azurermtemplates/azurermtemplates/tree/master/resource-loop-vms-vnet) | This template allows you to deploy 'n' virtual machines in a Single Click. |
| 12 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/mongodb-on-centos" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Install Mongo DB on CentOS Virtual Machine](https://github.com/azurermtemplates/azurermtemplates/tree/master/mongodb-on-centos) | This template deploys Mongo DB on CentOS Virtual Machine. |
| 13 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/mongodb-on-ubuntu" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Install Mongo DB on Ubuntu Virtual Machine](https://github.com/azurermtemplates/azurermtemplates/tree/master/mongodb-on-ubuntu) | This template deploys Mongo DB on Ubuntu Virtual Machine. |
| 14 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/zookeper-cluster-ubuntu-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Create a Zookeeper cluster](https://github.com/azurermtemplates/azurermtemplates/tree/master/zookeper-cluster-ubuntu-vm) | This template deploys a 3-node Zookeeper cluster on Ubuntu Virtual Machines. |
| 15 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/apache2-on-ubuntu-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [gbowerman](https://github.com/gbowerman) | [Deploy an Apache webserver on Ubuntu](https://github.com/azurermtemplates/azurermtemplates/tree/master/apache2-on-ubuntu-vm) | This template uses the Azure Linux CustomScript extension to deploy an Apache web server. The deployment template creates an Ubuntu VM, installs Apache2 and creates a demo HTML file. |
| 16 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/chef-ubuntu-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [kundanap](https://github.com/kundanap) | [Bootstrap a Ubuntu VM with Chef Agent](https://github.com/azurermtemplates/azurermtemplates/tree/master/chef-ubuntu-vm) | This templates provisions a Ubuntu VM and bootstraps Chef Client on it.|
| 17 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/resource-loop-vm-template-linking" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy Virtual Machines across 5 regions using Template Linking](https://github.com/azurermtemplates/azurermtemplates/tree/master/resource-loop-vm-template-linking) | This template showcases the 'Template Linking' capability in Azure Resource Manager. This template deploys 'n' Virtual Machines across 5 regions in parallel. |
| 18 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/custom-script-list-storage-keys-windows-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Windows VM with custom script extension](https://github.com/azurermtemplates/azurermtemplates/tree/master/custom-script-list-storage-keys-windows-vm) | This template creates a VM and runs a PowerShell script using the custom script extension. |
| 19 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/diagnostics-extension-windows-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [kenazk](https://github.com/kenazk) | [Windows VM with Azure Diagnostics Extension](https://github.com/azurermtemplates/azurermtemplates/tree/master/diagnostics-extension-windows-vm) | This template creates a VM and deploys the Azure Diagnostics Agent to emit performance metrics from within the VM to a Table in the Storage Account specified. |
| 20 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/blob/master/chef-json-parameters-ubuntu-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [kundanap](https://github.com/kundanap) | [Bootstrap a Ubuntu VM with Chef Agent with Json paramters](https://github.com/azurermtemplates/azurermtemplates/blob/master/chef-json-parameters-ubuntu-vm) | This templates provisions a Ubuntu VM and bootstraps Chef Client on it by taking only json parameters.|
| 21 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/wordpress-single-vm-ubuntu" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [tomconte](https://github.com/tomconte) | [Deploy a single-VM WordPress to Azure](https://github.com/azurermtemplates/azurermtemplates/tree/master/wordpress-single-vm-ubuntu) | This template deploys a complete LAMP stack, then installs and initializes WordPress.Once the deployment is finished, you need to go to http://fqdn.of.your.vm/wordpress/ to finish the configuration, create an account, and get started with WordPress. |
| 22 | <a href="https://azuredeploy.net/?repository=https://github.com/simongdavies/AzureRMActiveDirectory" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [simongdavies](https://github.com/simongdavies) | [This template creates an Azure VM with AD](https://github.com/simongdavies/AzureRMActiveDirectory) | This template creates a new Azure VM, with a public IP address, load balancer and VNet, it configures the VM to be an AD DC for a new Forest. |
| 23 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/docker-containers-vm-resource-loops" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [coreysa](https://github.com/coreysa) | [Deploy Docker Containers on Virtual Machines across 5 regions using Loops & Template Linking](https://github.com/azurermtemplates/azurermtemplates/tree/master/docker-containers-vm-resource-loops) | This template allows you to create 'N' number of Virtual Machines based on the 'numberOfInstances' parameter specified during the template deployment and deploys 2 docker containers [nginx & redis] on each VM. |
| 24 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/resource-loop-vms-userimage" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy 'n' Virtual Machines from a user image using Resource Loops](https://github.com/azurermtemplates/azurermtemplates/tree/master/resource-loop-vms-userimage) | This template allows you to create 'N' number of Virtual Machines from a User image based on the 'numberOfInstances' parameter specified during the template deployment.  |
| 25 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/resource-loop-vms-userimage-mutilplestorageaccounts" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [mahthi](https://github.com/mahthi) | [Deploy 'n' Virtual Machines from a user image across 3 storage accounts in the same region](https://github.com/azurermtemplates/azurermtemplates/tree/master/resource-loop-vms-userimage-mutilplestorageaccounts) | This template allows you to create VMs from User image across 3 Storage accounts in the same region. You can also chose to specify the number of Virtual Machines that you want to spin up per storage accounts where the user image is placed [Recommended number is 40]. There are some critical pre-requisties for this template, please refer to the readme in the template folder for additional details.  |
| 26 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/memcached-multi-vm-ubuntu" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [arsenvlad](https://github.com/arsenvlad) | [Deploy 'n' Ubuntu VMs with memcached service and one Apache test VM](https://github.com/azurermtemplates/azurermtemplates/tree/master/memcached-multi-vm-ubuntu) | This template allows you to create multiple (based on the 'numberOfMemcachedInstances' parameter) Ubuntu 14.04 VMs in a private-only subnet and installs and configures memcached service on each VM. It also creates one publicly accessible Apache VM with a PHP test page to confirm that memcached is installed and accessible. |
| 27 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/redis-on-ubuntu" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [thecaterminator](https://github.com/TheCATerminator) | [Deploy a Redis cluster with configurable number of nodes](https://github.com/azurermtemplates/azurermtemplates/tree/master/redis-on-ubuntu) | This template deploys a Redis cluster on the Ubuntu virtual machines. The deployment topology is comprised of a customizable number of nodes joined into a cluster. The cluster is pre-configured with persistence and other optimizations as per best practices. |
| 28 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/elasticsearch-on-ubuntu" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [trentmswanson](https://github.com/trentmswanson) | [Install Elasticsearch cluster on Ubuntu Virtual Machines using Custom Script Linux Extension](https://github.com/azurermtemplates/azurermtemplates/tree/master/elasticsearch-on-ubuntu) | This template deploys an Elasticsearch cluster on Ubuntu Virtual Machines. The template provisions 3 dedicated master nodes in one availability set, and a configurable number of data nodes in another availability set. A load balancer is configured with a rule to route traffic on port 9200 to the client/data nodes, and also includes SSH nat rules for management. Elasticsearch data nodes are configured to store indexes using multiple data disks attached to each virtual machine. |
| 29 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/drone-ubuntu-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [anweiss](https://github.com/anweiss) | [Deploy an Ubuntu VM with Drone CI.](https://github.com/azurermtemplates/azurermtemplates/tree/master/drone-ubuntu-vm) | This template provisions an Ubuntu Linux VM on Azure and bootstraps it with the latest release of the Drone continuous integration toolset. |
| 30 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/create-hpc-cluster" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [justintian](https://github.com/justintian) | [Create HPC Cluster on Azure](https://github.com/azurermtemplates/azurermtemplates/tree/master/create-hpc-cluster) | This template provisions an HPC Pack Cluster on Azure |
| 31 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/create-hpc-cluster" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [kenazk](https://github.com/kenazk) | [Create 5 VMs in an Availability Set with 3 FDs](https://github.com/azurermtemplates/azurermtemplates/tree/master/resource-loop-vms-availabilityset-3FDs) | This template provisions 5 VMs in an Availability Set with 3 FDs|
| 32 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/anti-malware-extension-windows-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Windows VM with Anti-Malware extension](https://github.com/azurermtemplates/azurermtemplates/tree/master/anti-malware-extension-windows-vm) | This template creates a Windows VM with Anti-Malware extension|
| 33 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/postgresql-multi-vm-ubuntu" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [arsenvlad](https://github.com/arsenvlad) | [Create PostgreSQL on Ubuntu with one master and 'N' replicas](https://github.com/azurermtemplates/azurermtemplates/tree/master/postgresql-multi-vm-ubuntu) | This template allows you to create one master PostgreSQL 9.3 server with streaming-replication to multiple (based on the 'numberOfSlaveInstances' parameter) slave servers in a private-only subnet. Each database server is configured with 2 data disks that are striped into RAID-0 configuration using mdadm. The template also creates one publicly accessible VM to serve as a jumpbox for ssh into the backend database servers. |
| 34 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/create-storage-account" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [singhkay](https://github.com/singhkay) | [Create Storage Account](https://github.com/azurermtemplates/azurermtemplates/tree/master/create-storage-account) | This template creates a Storage Account|
| 35 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/centos-mesosphere-cluster-high-availability" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [hausdorff](https://github.com/hausdorff) | [Spin up a Mesosphere cluster with 3 master nodes](https://github.com/azurermtemplates/azurermtemplates/tree/master/centos-mesosphere-cluster-high-availability) | Template spins up and configures a fully-functional mesosphere cluster.|
| 36 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/centos-mesosphere-cluster-simple" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [hausdorff](https://github.com/hausdorff) | [Spin up a Mesosphere cluster with a single master node](https://github.com/azurermtemplates/azurermtemplates/tree/master/centos-mesosphere-cluster-simple) | Spin up a Mesosphere cluster with a single master node|
| 37 | <a href="https://azuredeploy.net/?repository=https://github.com/azurermtemplates/azurermtemplates/tree/master/diskraid-ubuntu-vm" target="_blank"><img src="http://azuredeploy.net/deploybutton_small.png"/></a> | [trentmswanson](https://github.com/trentmswanson) | [Create Ubuntu vm data disk raid0](https://github.com/azurermtemplates/azurermtemplates/tree/master/diskraid-ubuntu-vm) | Create Ubuntu vm data disk raid0|

 

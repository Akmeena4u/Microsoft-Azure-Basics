

<img width="420" alt="image" src="https://github.com/Akmeena4u/Microsoft-Azure-Basics/assets/93425334/1665cda5-96f7-4778-bb12-9aad892ff678">



<img width="434" alt="image" src="https://github.com/Akmeena4u/Microsoft-Azure-Basics/assets/93425334/d633a6ed-bf61-4f85-afd8-5846816c6c48">


# Day-5 | Azure Virtual Network (VNet) Simplified

Welcome to Day 5 of our Azure journey! Today, we'll dive into Azure Virtual Network (VNet), a crucial component for building your cloud infrastructure. By the end of this, you'll have a solid understanding of VNets in Azure.

## What is Azure Virtual Network (VNet)?

**Azure VNet** is like your private network in the cloud. It allows you to securely connect and isolate your Azure resources, creating a virtualized network environment. Just think of it as your own piece of the Azure cloud where your resources live and communicate.

### Key Concepts:

1. **Isolation:** VNets provide isolation for your resources. You can have multiple VNets, and resources within a VNet can talk to each other while being isolated from resources in other VNets.

2. **Subnets:** Inside a VNet, you can create subnets. These subnets help you organize and segment your resources. For example, you might have a subnet for web servers and another for databases.

3. **Connectivity:** VNets allow you to connect to your on-premises network, creating a hybrid network. You can also connect VNets together to allow communication between them.

4. **Security:** Network Security Groups (NSGs) can be associated with VNets to control inbound and outbound traffic. This adds an extra layer of security to your resources.

## Creating a VNet in Azure:

Let's walk through the steps to create a simple VNet:

1. **Azure Portal:**
   Open the [Azure Portal](https://portal.azure.com/).

2. **Create a Resource:**
   Click on "Create a resource" and search for "Virtual Network."

3. **Basic Settings:**
   - Choose a subscription and a resource group.
   - Give your VNet a name and choose a region.

4. **Address Space:**
   Specify the address space for your VNet. This is the IP range your resources will use.

5. **Subnets:**
   Add one or more subnets within your VNet. Each subnet can have its own address range.

6. **Security:**
   Optionally, configure network security groups to control traffic.

7. **Review and Create:**
   Review your settings and click "Create."

## Connecting Resources to the VNet:

After creating your VNet, you can connect various Azure resources to it:

- **Virtual Machines:** When creating a VM, you can choose to put it in a specific subnet within your VNet.

- **Azure SQL Database:** You can configure your SQL Database to be part of your VNet, adding an extra layer of security.

- **App Services:** By integrating with Azure VNets, your App Services can securely access resources inside your VNet.


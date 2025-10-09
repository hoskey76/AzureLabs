# Create a Virtual Machine and Configure Network Access
## Overview
This lab is split into two parts.

1. Creating a Linux VM and installing Nginx
2. Configuring access to the Linux VM

   
In **Part 1** you'll create a Linux VM and install Nginx. After your VM is created, you'll use the Custom Script Extension to install Nginx.  The VM you created and installed Nginx on won't be accessible on the Internet so, in **Part 2** you'll configure the access to the virtual machine (VM) you created in **Part 1**.

> [!NOTE]
> The Custom Script Extension is an easy way to download and run scripts on your Azure VMs. It's just one of the many ways you can configure the system after your VM is up and running.

## About Azure Virtual Machines
Azure virtual machines (VMs) are one of several types of on-demand, scalable computing resources that Azure offers. Typically, you choose a virtual machine when you need more control over the computing environment than the other choices offer. This article gives you information about what you should consider before you create a virtual machine, how you create it, and how you manage it.

An Azure virtual machine gives you the flexibility of virtualization without having to buy and maintain the physical hardware that runs it. However, you still need to maintain the virtual machine by performing tasks, such as configuring, patching, and installing the software that runs on it.

Azure virtual machines can be used in various ways. Some examples are:

   - Development and test – Azure virtual machines offer a quick and easy way to create a computer with specific configurations required to code and test an application.
   - Applications in the cloud – Because demand for your application can fluctuate, it might make economic sense to run it on a virtual machine in Azure. You pay for extra virtual machines when you need them and shut them down when you don’t.
   - Extended datacenter – virtual machines in an Azure virtual network can easily be connected to your organization’s network.




## ⚠️ Cost & Resource Disclaimer  

These labs and projects are designed with free or low-cost Azure resources whenever possible. If you attempt to replicate them in your own Azure environment, be aware that **some costs may be incurred depending on your configuration and resource choices**.  

- Whenever possible, use a **sandbox environment** (e.g., Microsoft Learn sandbox).  
- Take advantage of **resources provided by your employer, school, or training platform** if available.  
- **Always shut down or delete resources** once you’ve completed a lab to avoid unexpected charges from services left running.  

Use these labs responsibly and with cost-awareness in mind.  

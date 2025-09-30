In this exercise, you’ll use the Azure portal to create a resource. The focus of the exercise is observing how Azure resource groups populate with created resources. 



### Task 1: Create a virtual machine

In this task, you’ll create a virtual machine using the Azure portal.

1. Open the browser from the taskbar and sign in to the [Azure portal](https://portal.azure.com/learn.docs.microsoft.com?azure-portal=true).  
2. Select **Create a resource** > **Compute** > **Virtual Machine** > **Create**.  
3. The **Create a virtual machine** pane opens to the **Basics** tab.  
4. Verify or enter the required values for each setting. If a setting isn’t specified, leave the default value.  
5. Select **Review + create**.  
6. Select **Create**.

Wait while the VM is provisioned. Deployment is in progress will change to Deployment is complete when the VM is ready.

### Task 2: Create a virtual machine

Once the deployment is created, you can verify that Azure created not only a VM, but all of the associated resources the VM needs.

1. Select **Home**.
2. Select **Resource groups**.
3. Select the resource group you created earlier in previous task.

You should see a list of resources in the resource group including your new virtual machine. The rest of the resources were created when you created the virtual machine. By default, Azure gives them all a similar name to help with association and grouped them in the same resource group.

### **DONE**

> [!TIP]
> Do not forget to shutdown or delete any resources you have made. This will help keep you from incurring unwanted costs!

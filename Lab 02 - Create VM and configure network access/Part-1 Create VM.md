# Create a Virtual Machine


Use the following Azure CLI commands to create a Linux VM and install Nginx. After your VM is created, you'll use the Custom Script Extension to install Nginx. 

1. From your browser go to https://portal.azure.com and sign in to your subscribtion, alternatively use a sandbox if you have access to one.

2. From the Azure portal, open the Azure Cloud Shell by clicking on the icon in the top right of the Azure Portal which is next to the notification bell icon.

3. In the Welcome to Azure Cloud Shell dialog, when prompted to select either Bash or PowerShell, select **Bash**.

4. A new window will open appear, select **No storage account required**, select your subscription and click **Apply**.

5. Run the following command to create the resource group. Replace with the unique name for the new resource group.

   ```
   az group create --name <ResourceGroupName> --location eastus
   ```

6. From Cloud Shell, run the following az vm create command to create a Linux VM: 
Replace with your resource group that you created in previous step:

    ```
    az vm create --resource-group <ResourceGroupName> --name my-vm --public-ip-sku Standard --image Ubuntu2204 --admin-username azureuser --generate-ssh-keys
    ```

    Your VM will take a few moments to come up. You named the VM my-vm. You use this name to refer to the VM in later steps.
7. Run the following az vm extension set command to configure Nginx on your VM:

    Replace with your resource group that you created earlier:

    ```
    az vm extension set --resource-group <ResourceGroupName> --vm-name my-vm --name customScript --publisher Microsoft.Azure.Extensions --version 2.1 --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'
    ```

> [!NOTE]
> This command uses the Custom Script Extension to run a Bash script on your VM. The script is stored on GitHub. While the command runs, you can navigate to https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh?azure-portal=true from a separate browser tab. To summarize, the script:
>
>
> ***i***. It runs apt-get update to download the latest package information from the internet. This step helps ensure that the next command can locate the latest version of the Nginx package.
>
> 
> ***ii***. Installs Nginx.
>
> 
> ***iii***. Sets the home page, **/var/www/html/index.html**, to print a welcome message that includes your VM's host name.

8. Once the script is done you should see some JSON output in thte Azure CLI look for the line **"provisioningState": "Succeeded"** to confirm script success.

### Done
You are now ready to move on to [**Part 2**](https://github.com/hoskey76/AzureLabs/blob/main/Lab%2002%20-%20Create%20VM%20and%20configure%20network%20access/Part-2%20Configure%20Network%20Access.md)

# Create Blob Storage

### Part 1 - Create a New Storage Account

1. Open your browser and sign in to the Azure portal at https://portal.azure.com
2. Select **+ Create a resource**.
3. Under **Categories**, select **Storage**.
4. Under **Storage account**, select **Create**.
5. On the **Basics** tab of the **Create a storage account** blade, fill in the information from the table below. Leave the defaults for everything else.

   
  |Setting|Value|
  |:---:|:---:|
  |Subscription|your default Subscription|
  |Resource group|Click **Create new** type **learn** as resource group name then click **OK**|
  |Storage account name|Create a **unique** storage account name|
  |Region|Leave default|
  |Performance|Standard|
  |Redundancy|Locally redundant storage (LRS)|

  
7. Click the **Advanced** tab of the **Create a storage account** blade, check the box next to Allow enabling anonymous access on individual containers. Leave the defaults for everything else.


> [!NOTE]
> Blob containers, by default, do not permit anonymous access to their content. This setting allows authorized users to selectively enable anonymous access on specific containers. You can use Azure policy to audit this setting or prevent this setting from being enabled.


7. Select **Review + create** to review your storage account settings and allow Azure to validate the configuration.
8. Once validated, select **Create**. Wait for the notification that the account was successfully created.
9. Select **Go to resource**.


### Part 2 - Create a Blob Container and Upload a Picture


1. Under **Data storage** if required expand first, select **Containers**.
2. Select **+ Add Container** and fill in the following information:
   
  | Setting | Value |
  |:---:|:---:|
  |Name|Enter a **unique** name for the container|
  |Public access level|Private (no anonymous access)|

  
4. Select **Create**


> [!IMPORTANT]
> Step 4 will need an image. If you want to upload an image you already have on your computer, continue to Step 4. Otherwise, You may use the image located [**here**](https://github.com/hoskey76/AzureLabs/blob/main/Lab%2003%20-%20Create%20blob%20storage/Blob%20Test%20File/blob_ferrari_image.jpg) or search and download any image of your choosing.


4. Back in the **Azure portal**, select the container you created, then select **Upload**.
5. Browse for the image file you want to upload. Select it and then select **Upload**.


> [!TIP]
> You can upload as many blobs as you like in this way. New blobs will be listed within the container.


6. Select the **Blob (file)** you just uploaded. You should be on the properties section.
7. Copy the URL from the **URL** field and paste it into a new tab. 


> [!NOTE]
> You should receive an error message similar to the following.

	<Error>
  		<Code>ResourceNotFound</Code>
 		<Message>The specified resource does not exist. RequestId:4a4bd3d9-101e-005a-1a3e-84bd42000000</Message>
	</Error>	


### Part 3 - Change the Access Level of Your Blob


1. Go back to the **Azure portal > Container** page.
2. On the above menubar select **Change access level**.
3. Set the **Anonymous access level** to **Blob (anonymous read access for blobs only)**.
4. Select **OK**.
5. Refresh the tab where you attempted to access the file earlier.


### **DONE**

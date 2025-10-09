# Create Blob Storage
## Overview
You will create a storage account, adde a container to the storage account, and then uploaded Blobs (files) to your container. Then you will change the access level so you can access your Blobs (files) from the internet.

### About Blob Storage

Azure Blob Storage is Microsoft's object storage solution for the cloud. Blob Storage is optimized for storing massive amounts of unstructured data. Unstructured data is data that doesn't adhere to a particular data model or definition, such as text or binary data.


Blob Storage is designed for:

   - Serving images or documents directly to a browser.
   - Storing files for distributed access.
   - Streaming video and audio.
   - Writing to log files.
   - Storing data for backup and restore, disaster recovery, and archiving.
   - Storing data for analysis by an on-premises or Azure-hosted service.

Users or client applications can access objects in Blob Storage via HTTP/HTTPS, from anywhere in the world. Objects in Blob Storage are accessible via the Azure Storage REST API, Azure PowerShell, Azure CLI, or an Azure Storage client library. Client libraries are available for different languages, including:

   - .NET
   - Java
   - Node.js
   - Python
   - Go

Clients can also securely connect to Blob Storage by using SSH File Transfer Protocol (SFTP) and mount Blob Storage containers by using the Network File System (NFS) 3.0 protocol.

## ⚠️ Cost & Resource Disclaimer  

These labs and projects are designed with free or low-cost Azure resources whenever possible. If you attempt to replicate them in your own Azure environment, be aware that **some costs may be incurred depending on your configuration and resource choices**.  

- Whenever possible, use a **sandbox environment** (e.g., Microsoft Learn sandbox).  
- Take advantage of **resources provided by your employer, school, or training platform** if available.  
- **Always shut down or delete resources** once you’ve completed a lab to avoid unexpected charges from services left running.  

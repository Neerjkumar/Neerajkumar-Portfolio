# Neerajkumar-Portfolio

A [personal portfolio](https://neerajkumarportfolio.z5.web.core.windows.net/) is an evidentiary document designed to provide qualitative and quantitative information.

Clients want to see your thought process and the ideas behind your designs. Our creative recruiters recommend that your portfolio include mood boards, color stories, silhouette and print ideas, hand and/or illustrator sketches as well as the final product shots.

A personal website or portfolio is an opportunity to reach more people with your work. It's also an extension of your personality and gives you the chance to craft a design that reflects who you are as a creative. Just as there are many types of creatives, there are many ways to put together a personal website.

I have created my portfolio using [HTML](https://www.w3schools.com/html/html_intro.asp) and [CSS](https://www.w3schools.com/css/css_intro.asp). <br>
[HTML](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics): HTML is the standard markup language for creating Web pages. HTML is the code that is used to structure a web page and its content. For example, content could be structured within a set of paragraphs, a list of bulleted points, or using images and data tables.

[CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps): CSS is the language we use to style a Web page. CSS is used to style and lay out web pages — for example, to alter the font, color, size, and spacing of your content, split it into multiple columns, or add animations and other decorative features.



## Introduce yourself
* Aim for a friendly, casual tone
* Decide which professional experience to include
* Consider listing awards and accolades
* Add a few personal details
* Include a photo of yourself


## Benifites
Portfolio (we can also say candidate resume) that contain all details about the candidates. I divided all the skills, project, experience ,.... etc to different-different section. It is very helpful for the recruiters to know all about candidates in just oneshot. Using this strategy we can save the recruiters time and stress.

# Pre-requisites



# I used [Microsoft Azure](https://portal.azure.com/#home) Services to deploy the project on server.
* Static Website
* Storage
* Containers


## Steps to deploy the project on [Microsoft Azure](https://portal.azure.com/#home)
* Type "[portal.azure.com](https://portal.azure.com/)" in google search bar
* Now, login your Microsoft Azure account with your credential. 
* Click on "Menu". After clicking on Menu, click on "Storage Account". 
* Create a storage account

![image](https://user-images.githubusercontent.com/44793025/155853576-399b8c81-42f9-4030-a704-116ec67ab62e.png)

* After Creating the Storage account, click "Go to the resources".
* Click on "Static Website" write "Index document name" after writing this save it.

![image](https://user-images.githubusercontent.com/44793025/155854246-be1c6360-db7f-4910-ab59-65336018a2bd.png)

* Click on "Container" after clicking on container click on "$web".

![image](https://user-images.githubusercontent.com/44793025/155854356-18837b31-7ff4-4df7-ac09-6bed04ca5332.png)

* Now click on "Upload" select file and upload it.

![image](https://user-images.githubusercontent.com/44793025/155854445-4db4cc7f-5910-4e3f-935a-90e2196f1d78.png)

* Go back to Static website and copy the URL. After copyed the URL open new tap and paste the copied link and hit enter.

![image](https://user-images.githubusercontent.com/44793025/155854532-46ec2806-d703-4f0c-962b-652fbd5af992.png)

* Final our portfolio is this. Running on Microsoft Azure.

![image](https://user-images.githubusercontent.com/44793025/155854581-503b9937-af9e-43c6-9c0f-762fe9682dca.png)










# Learning objectives

## [Storage account settings](https://docs.microsoft.com/en-us/learn/modules/create-azure-storage-account/2-decide-how-many-storage-accounts-you-need) 

* Subscription: The Azure subscription that will be billed for the services in the account.
* Location: The datacenter that will store the services in the account.
* Performance: Determines the data services you can have in your storage account and the type of hardware disks used to store the data. <br>
   
        
        Standard allows you to have any data service (Blob, File, Queue, Table) and uses magnetic disk drives.
        Premium provides more services for storing data. For example, storing unstructured object data as block blobs or append blobs, and specialized file storage used to store and create premium file shares. These storage accounts use solid-state drives (SSD) for storage.
* Replication: Determines the strategy used to make copies of your data to protect against hardware failure or natural disaster. At a minimum, Azure automatically maintains three copies of your data within the datacenter associated with the storage account. The minimum replication is called locally redundant storage (LRS), and guards against hardware failure but does not protect you from an event that incapacitates the entire datacenter. You can upgrade to one of the other options such as geo-redundant storage (GRS) to get replication at different datacenters across the world.
* Access tier: Controls how quickly you will be able to access the blobs in a storage account. Hot gives quicker access than Cool, but at increased cost. Hot access tier applies only to blobs, and serves as the default value for new blobs.
* Secure transfer required: A security feature that determines the supported protocols for access. Enabled requires HTTPS, while disabled allows HTTP.
* Virtual networks: A security feature that allows inbound access requests only from the virtual network(s) you specify.

## [Account settings](https://docs.microsoft.com/en-us/learn/modules/create-azure-storage-account/3-choose-your-account-settings)
* Name
   * Each storage account has a name. The name must be globally unique within Azure, use only lowercase letters and digits and be between 3 and 24 characters.
   
* Deployment model
   * Resource Manager: the current model that uses the Azure Resource Manager API
   * Classic: a legacy offering that uses the Azure Service Management API
* Account kind
   * StorageV2 (general purpose v2): the current offering that supports all storage types and all of the latest features
   * Storage (general purpose v1): a legacy kind that supports all storage types but may not support all features
   * Blob storage: a legacy kind that allows only block blobs and append blobs

## [Account creation tool](https://docs.microsoft.com/en-us/learn/modules/create-azure-storage-account/4-choose-an-account-creation-tool)
* [Azure Portal](https://portal.azure.com/)
   1. Sign in to the [Azure portal](https://portal.azure.com/) using the same account.
   2. On the resource menu, or from the Home page, select Storage accounts. The Storage accounts pane appears.
   3. On the command bar, select Create. The Create a storage account pane appears.
   4. On the Basics tab, enter the following values for each setting.
   5. Select Next : Advanced. On the Advanced tab, enter the following values for each setting.
   6. Select Next : Networking. On the Networking tab, enter the following values for each setting.
   7. Select Next : Data protection. On the Data protection tab, enter the following values for each setting.
   8. Select Next : Encryption. Accept the defaults.
   9. Select Next : Tags. Here, you can associate key/value pairs with the account for your categorization to determine if a feature is available to selected Azure resources.
   10. Select Review + create to validate your options and to ensure all the required fields are selected. If there are issues, this tab will identify them so you can correct them.
   11. When validation passes successfully, select Create to deploy the storage account.
   12. When deployment is complete, which may take up to two minutes, select Go to resource to view Essential details about your new storage account.

* [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/#:~:text=The%20Azure%20command%2Dline%20interface,with%20an%20emphasis%20on%20automation.) (Command-line interface)
* [Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/?view=azps-7.2.0#:~:text=Azure%20PowerShell%20is%20a%20collection,managing%20Azure%20resources%20from%20PowerShell.)
* [Management client libraries](https://docs.microsoft.com/en-us/java/api/overview/azure/core-management-readme?view=azure-java-stable)


## Data types in Azure storage services
* Blobs: A massively scalable object store for text and binary data. Can include support for Azure Data Lake Storage Gen2.
   * Serving images or documents directly to a browser, including full static websites.
   * Storing files for distributed access.
   * Streaming video and audio.
   * Storing data for backup and restoration, disaster recovery, and archiving.
   * Storing data for analysis by an on-premises or Azure-hosted service.
* Files: Managed file shares for cloud or on-premises deployments.
   * Storing shared configuration files for VMs, tools, or utilities so that everyone is using the same version.
   * Log files such as diagnostics, metrics, and crash dumps.
   * Shared data between on-premises applications and Azure VMs to allow migration of apps to the cloud over a period of time.
* Queues: A messaging store for reliable messaging between application components.
* [Table Storage](https://docs.microsoft.com/en-us/azure/storage/tables/table-storage-overview): A NoSQL store for schema-less storage of structured data. Table Storage is not covered in this module.

# Create an Azure storage account
* Use the following example command to create a storage account. Remember to replace <name> with your unique storage account name.
<pre>
<code> 
az storage account create \
  --resource-group [sandbox resource group name] \
  --location westus \
  --sku Standard_LRS \
  --name <name> </code>
  </pre>

Setting up your environment for the labs
========================================
In this lab you will find the prerequisites and steps to help you set up your computer. After completing the lab you will have a working environment, ready for the other labs.


If not using your own Windows computer: Create an Azure Virtual Machine
-----------------------
### Create a new Visual Studio 2015 Preview Virtual Machine
If you don't have a computer running windows with Visual Studio 2013 or 2015 installed, it is faster and easier to create a new VM on your Azure subscription, and use that VM to complete the labs.

At this stage you should have an Azure subscription - if not please talk to your instructor first before continuing.

Follow these instructions to create the Visual Studio 2015 Preview virtual machine:

1. Log in to the ([Azure management portal with your credentials](http://manage.windowsazure.com/))
1. From the bottom of the portal, go to **New > Compute > Virtual Machine > From Gallery**

![New > Compute > Virtual Machine > From Gallery](images/gallery.png?raw=true)

1. From the image menu on the left, select Visual Studio, and then select the **Visual Studio Ultimate 2015 Preview** image

![Visual Studio Ultimate 2015 Preview](images/visual-studio-image.png?raw=true)

1. On the **'Virtual machine configuration**' page, select a **Standard D2** machine size and choose a user name and password that you will remember then click next

![Virtual Machine Configuration](images/vm-configuration.png?raw=true)

1. On the next '**Virtual machine configuration**' page, choose one of the Australia regions if they are available, otherwise either West US or Southeast Asia will work, then click next

![Virtual Machine Configuration](images/vm-configuration2.png?raw=true)

1. On the next page click the **checkbox button** to start creating the virtual machine.
1. It can take 5 to 10 minutes for the VM to be created. Once it is ready it will show with a status of '**Running**'.
1. Once the status of the VM is '**Running**' for a couple of minutes, select it and click **Connect** at the bottom and you'll be able to remote desktop into your shiny new VM.



Configure your computer (perform these actions from inside the VM you created one above)
-----------------------

### Download content of this GitHub repository (optional but recommended)

The labs provided have a combination of text documentation and sample code. In order to have the necessary sample files locally inside your VM, we strongly recommend you to [**download**](https://github.com/Azure-Readiness/HOL-Intro-to-Azure/archive/master.zip) all content in this repository to your VM. This is a zip archive, so make sure to [unblock](http://blogs.msdn.com/b/delay/p/unblockingdownloadedfile.aspx) the zip file before extracting it.

### Install Microsoft Azure PowerShell Cmdlets

The **Azure PowerShell** modules and all dependencies are available through the [Microsoft Web Platform Installer](http://www.microsoft.com/web/downloads/platform.aspx). To install it, follow these instructions:

1. Open Microsoft Web Platform Installer.
1. Find the row for **Microsoft Azure PowerShell with Microsoft Azure SDK** and click the **Add** button. 
1. Click **Install**.

![Install MS Azure Powershell in MS WebPlatform Installer](images/install-ms-azure-powershell.png?raw=true)

_Install Microsoft Azure PowerShell_

>**Note:** The Microsoft Azure PowerShell Cmdlets are only required for the _Create Virtual Machine using PowerShell_ task of the [Infrastructure As A Service in Microsoft Azure](../create-virtual-machine) lab.

###Install the Azure Cross-Platform Command-Line Interface

There are two ways to install the **Azure Cross-Platform Command-Line Interface** (or xplat-cli): using installer packages for Windows and OS X, or if Node.js is installed on your system, the **npm** command. 

Once the xplat-cli has been installed, you will be able to use the **azure** command from your command-line interface (Bash, Terminal, Command prompt) to access the xplat-cli commands.

In order to install the **Azure Cross-Platform Command-Line Interface** using the installer, just download the package for your platform and follow the instructions. The following installer packages are available:

* [Windows installer](http://go.microsoft.com/?linkid=9828653&clcid=0x409)

* [OS X installer](http://go.microsoft.com/fwlink/?linkid=252249&clcid=0x409)

	> **Note:** If Node.js is already installed on your system, use the following command to install the xplat-cli:

	> ````
	> npm install azure-cli -g
	> ````

	>**Note:** The Azure Cross-Platform Command-Line Interface is only required for the _Create Virtual Machine using Cross-Platform Command Line Interface_ task of the [Infrastructure As A Service in Microsoft Azure](../create-virtual-machine) lab.

To verify that ensure that you have the **Azure Cross-Platform Command-Line Interface** correctly installed, open a **Command Prompt** and execute the following command:

	````
	azure
	````

	You should get a message similar to the following:

	````
	info:             _    _____   _ ___ ___
	info:            /_\  |_  / | | | _ \ __|
	info:      _ ___/ _ \__/ /| |_| |   / _|___ _ _
	info:    (___  /_/ \_\/___|\___/|_|_\___| _____)
	info:       (_______ _ _)         _ ______ _)_ _
	info:              (______________ _ )   (___ _ _)
	info:
	info:    Microsoft Azure: Microsoft's Cloud Platform
	info:
	info:    Tool version 0.8.13
	help:
	help:    Display help for a given command
	help:      help [options] [command]
	help:
	help:    Log in to an Azure subscription using Active Directory. Currently, the user can login only via Microsoft organizational account
	help:      login [options]
	help:
	help:    Log out from Azure subscription using Active Directory. Currently, the user can log out only via Microsoft organizational account
	help:      logout [options] [username]
	help:
	help:    Open the portal in a browser
	help:      portal [options]
	help:
	help:    Commands:
	help:      account        Commands to manage your account information and publish settings
	help:      config         Commands to manage your local settings
	help:      hdinsight      Commands to manage your HDInsight accounts
	help:      mobile         Commands to manage your Mobile Services
	help:      network        Commands to manage your Networks
	help:      sb             Commands to manage your Service Bus configuration
	help:      service        Commands to manage your Cloud Services
	help:      site           Commands to manage your Web Sites
	help:      sql            Commands to manage your SQL Server accounts
	help:      storage        Commands to manage your Storage objects
	help:      vm             Commands to manage your Virtual Machines
	help:
	help:    Options:
	help:      -h, --help     output usage information
	help:      -v, --version  output the application version
	````

Summary
-------

You have Visual Studio 2015 Previewand the _Azure SDK installed on a VM and you are now good to go with the rest of the labs.

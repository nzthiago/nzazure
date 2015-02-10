Working with the Management Portal
========================================

The Azure Management Portal is your one-stop-shop for creating and managing new cloud resources, like websites, virtual machines, and storage accounts. Once you get started, the portal will be your home to configure, monitor, and scale your resources with ease and agility.

This lab includes the following tasks:

1. [Portal Overview](#Task1)
1. [Creating new elements](#Task2)
1. [Managing existing elements](#Task3)

In this lab, you will learn how to:

- Work with the Azure Management Portal
- Create new elements and services
- Manage allocated resources

<a name="Task1" />
##Portal Overview

In this task you will walk through the different pieces of the Azure Management Portal.

1. Open you browser and navigate to [http://manage.windowsazure.com](http://manage.windowsazure.com).
2. Enter your credentials to access your _Azure Subscription_. 

	You will land on the portal's home view. By default this view will show all the items you have ever created under your subcription.

	![Management Portal - Landing Page](images/portal-landing-page.png?raw=true)

	_Management Portal - Landing Page_

3. On the left side, notice the sidebar displaying all the available services and tools. Clicking any of these items will filter the list by that specific type.

	![Left Sidebar](images/portal-left-sidebar.png?raw=true)

	_Left Sidebar_

4. Look at the portal's footer and notice the **NEW** button on the left and the **Help** button on the right. You will see more about these two items as you move on to the other tasks.

	![New Button](images/portal-new-button.png?raw=true)

	_NEW and Help Buttons_

<a name="Task2" />
##Creating new elements and services
In this task you will go through the process of creating a new element for your subscription. In particular, you will create a new website using the **Create Wizard**.

1. Click the **NEW** button located at the bottom left part of the screen.

	![New Button Click](images/new-button-clicked.png?raw=true)

	_NEW Button Clicked_

	This will display the _Create Wizard_. In this section you can select the type of element, service or resource we want to create. In this case you will create a _Website_.

2. Click **COMPUTE**. The compute services will be displayed alongside.

3. Click **WEBSITE**. 

	Three options will be shown.

	- **QUICK CREATE**: This option will allow you to setup your website with the minimum amount of steps.

	- **CUSTOM CREATE**: You will have the chance to create a SQL Database to attach to this website and setup a continuous deployment source.

	- **FROM GALLERY**: The gallery features a list of templates ready to jumpstart your website.

	![Website Creation Options](images/create-flow.png?raw=true)
	_Website Creation Options_

4. Click **QUICK CREATE**. 

	The creation form is presented. Here you will select the URL for your website and the region where you would like to deploy. It is recommended to select the region which is closest to your audience; for this task leave the field as is.

5. Enter the **URL** for your website, and click **CREATE WEBSITE**.

	> **Note:** The website URL has to be unique since it will be of public access.


	![Creating the Website](images/create-flow-quick-create-clicked.png?raw=true)

	_Creating the Website_

6. After a few minutes the website will be created and you will see a notification on the status bar. The **WEBSITES** item is selected on the sidebar, and the asset just created is displayed.

	![Website Create](images/website-listing.png?raw=true)

	_Website Created_
	
7. Click the site name you have just created to navigate to the website's _Quick Start Management_ page. 

	![Entering the site's management](images/website-clicked.png?raw=true)

	_Entering the site's management page_

1. Click **BROWSE**, located at the bottom of the page, to navigate to the site.

	![Clicking Browse to view the site](images/clicking-browse-to-view-the-site.png?raw=true)

	_Clicking Browse_

	![Browsing the Website](images/browsing-the-website.png?raw=true)

	_Browsing the Website_

1. Close the website and return to the **Management Portal**.
	
<a name="Task3" />
##Managing allocated resources
In this task you will go through the available options for managing the recently created website.

1. If not already in the _Quick Start Management_ page, click the website's name to display it. 
	
	This page provides quick access to important actions related to managing the deployment of a site in Windows Azure. This is also the default landing page in the portal for a newly created website.

    ![_Website's Landing Page](images/website-quickstart.png?raw=true)

    _Website's Quickstart Management page_

2. Notice the commands located at the bottom of the page. These are:

    - **BROWSE**: To navigate to the current deployed version of the website
    - **STOP**: To stop the website's deployment
    - **RESTART**: To restart the website's deployment
    - **DELETE**: To delete the website
    - **WEBMATRIX**: Allows to install WebMatrix, Microsoft's new one-stop website authoring tool that lets you create, edit, and publish websites easily.

3. Look at the top bar to see the different sections available. These sections are:

    - Dashboard
	- Monitor
	- Webjobs
    - Configure
    - Scale
    - Linked Resources
    - Backups

	The rest of the task will describe the more important ones.
  
	> **Note**: For more information about all these options, see [Manage websites through the Azure Management Portal](http://azure.microsoft.com/en-us/documentation/articles/web-sites-manage/).
    
4. Click **DASHBOARD**. 

	The website's dashboard will show. This view will provide you with the most important information at a glance. Ranging from a health report to usage statistics, this view provides the core details of your service.

	![Website Clicked](images/website-dashboard-view.png?raw=true)

	_The Dashboard view_
    
5. On the top bar, click **MONITOR**. 

	This view allows the setup of tests to check the availability of HTTP or HTTPS endpoints, from up to three geo-distributed locations. A monitoring test fails if the HTTP response code is an error (4xx or 5xx) or the response takes more than 30 seconds. An endpoint is considered available if the monitoring tests succeed from all the specified locations.

	![Website Clicked](images/website-monitor-view.png?raw=true)

	_The Monitor view_
    
6. On the top bar, click **WEBJOBS**. 

	The WebJobs management page lets you create tasks for your website that can run on-demand, on a schedule or continuously.

	> **Note**: For more information regarding the use of Webjobs, see [How to Use the WebJobs feature in Microsoft Azure Web Sites](http://azure.microsoft.com/en-us/documentation/articles/web-sites-create-web-jobs/).
    
    ![Website Clicked](images/website-webjobs-view.png?raw=true)

	_The Webjobs view_
    
7. Lastly, click **SCALE** on the top bar, to go to the scaling options. 

	For increased performance and throughput for your websites on Microsoft Azure, you can scale your Web Hosting Plan mode from Free to _Shared_, _Basic_, or _Standard_. Scaling up on Azure Websites involves two related actions: changing your _Web Hosting Plan_ mode to a higher level of service, and configuring certain settings after you have switched to the higher level of service. You can scale up or down as required. These changes take only seconds to apply and affect all websites in your Web Hosting Plan. They do not require your code to be changed or your applications to be redeployed.

    ![Website Clicked](images/website-scale-view.png?raw=true)

	_The Scale view_

	>**Note:** It is good practice to cleanup any resources that will not be used. To delete the demo website just created, follow these steps:
	>
	>1. Click **DASHBOARD** at the top of the page.
	>
	>1. Click **DELETE** at the bottom of the page.
	>
	>![Clicking Delete website](images/clicking-delete-website.png?raw=true)
	>
	>_Clicking Delete_
	>
	>1. In the **Delete Confirmation** dialog that pops up, click the **checkmark** button.
	>
	>![Delete Confirmation dialog](images/delete-confirmation-dialog.png?raw=true)
	>
	>_Delete Confirmation_
	>
	>After a few moments you should see a notification indicating the website was deleted. The website will not be listed under **WEBSITES** either.



## Summary
In this lab you have seen the _Azure Management Portal_, starting by the basic layout of the hub page, moving to the creation and management of resources. Finally you have explored some of the features that the portal provides.

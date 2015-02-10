Introduction to the Azure Preview Portal
=============================================

The new Azure Preview portal is an all-in-one, work-anywhere experience. Now you can manage websites, databases and Visual Studio Online team projects in a reimagined UX personalized to your work style. It was built from the ground up to put your _applications_ at the center of the experience. 

This unified hub radically simplifies building, deploying, and managing your cloud resources. Imagine a single, easy-to-use console built just for you, your team, your projects. It brings together all of the cloud resources, team members, and lifecycle stages of your application and provides you with a centralized place to plan, develop, test, provision, deploy, scale, and monitor those applications. This approach can help teams embrace a DevOps culture by bringing both development and operations capabilities and perspectives together in a meaningful way.

The new portal allows each user to transform the portal home page (called the _Startboard_) into their own customized dashboard. Stay on top of the things that matter most by pinning them to your **Startboard**. Resize parts to show more or less data. Drill in for all the details. And see insights (and opportunities) across apps and resources. New components include the following:

* **Simplified Resource Management**. Rather than managing standalone resources such as Microsoft Azure Websites, Visual Studio Projects or databases, customers can now create, manage and analyze their entire application as a single resource group in a unified, customized experience, greatly reducing complexity while enabling scale. Today, the new Azure Manager is also being released through the latest Azure SDK for customers to automate their deployment and management from any client or device. 

* **Integrated billing**. A new integrated billing experience enables developers and IT pros to take control of their costs and optimize their resources for maximum business advantage.

* **Gallery**. A rich gallery of application and services from Microsoft and the open source community, this integrated marketplace of free and paid services enables customers to leverage the ecosystem to be more agile and productive.

* **Visual Studio Online**. Microsoft announced key enhancements through the Microsoft Azure Preview Portal. This includes Team Projects supporting greater agility for application lifecycle management and the lightweight editor code-named "Monaco" for modifying and committing Web project code changes without leaving Azure. Also included is Application Insights, an analytics solution that collects telemetry data such as availability, performance and usage information to track an application's health. Visual Studio integration enables developers to surface this data from new applications with a single click.

## Creating a Web Site + SQL ##

Historically, managing a resource (a user-managed entity such as a database server, database or web site) in Microsoft Azure required you to perform operations against one resource at a time. When developing for the cloud today, we are often managing _individual resources_ (databases, storage, cloud services, virtual machines, and so on). It is left up to us, as cloud developers and IT professionals, to piece these resources together in a meaningful way and manage them over time. The Microsoft Azure Preview portal was designed to bring together all of the individual resources of an application into a consolidated view. Resource group is a new concept in Azure that serves as the lifecycle boundary for all of its resources. 

In this task, you will learn about the preview portal and how to create a new Web Site and a SQL Server using it.

1. Open a browser and browse to http://portal.azure.com and log in using your credentials.

2. The first thing you will see is the **Startboard**. This is your home page, where you can see dynamic data from your resources and all the details you care about. You can customize it as you see fit.

	> **Note:** You can right-click the tiles of the Startboard to customize it. You can pin or unpin tiles and change their size.
	
	![Startboard](Images/startboard.png?raw=true)
	
	_Your Home Page: The Startboard_

3. On the left side, you will see the **Hub Menu**. This is the navigation menu where you can access all of your resources and options. Click the **New** button at the bottom of the **Hub Menu**.

	![Creating a new resource](Images/creating-a-new-resource.png?raw=true)
	
	_Creating a new resource_

4. A panel is displayed with different options. You can choose one of the options to create a new resource. Click the **Everything** button to see all the available options.

	![Displaying every resource type](Images/displaying-resource-types.png?raw=true)
	
	_Displaying every resource type_
	
	
5. Scroll down to the **Web** category, and select **Website +SQL**. Then click **Create**.

	![Selecting Website](Images/selecting-website-sql.png?raw=true)
	
	_Selecting Website + SQL_
	
	A _blade_ is opened. Blades are your entry point to discovering insights, performing actions and building applications. This particular _blade_ collects input from you to create a new **Website**.

	> **Note:** For more information about _blades_, you can click the **Tour** tile on your **Startboard**. On the **Tour** blade, scroll down to the bottom and click **Learn more**. A new blade is opened with further information. You can continue the **Tour** to learn the basics of Blades, Commands, Lenses and more.
	
	> ![Tour](Images/tour.png?raw=true)

6. When you create an application that consists of several resources working together (like in this example, a Website + SQL), it is always created in its own resource group so that you can manage the lifecycle of all related assets. Choose a name for the **Resource Group**, for example _MyResourceGroup_, and click the **Website** option.

	> **Note:** Resource group names can only contain letters, numbers, periods, underscores and dashes.

	![New Website](Images/new-resource-group.png?raw=true)
		
	_New Resource Group_

7. Another blade is opened which displays the options to create a new **Website**. Select a URL for your Website, for example _myMSAzureWebsite_. Take into account that this name must be unique. Click the **Web Hosting Plan** option.

	![Changing the Web Hosting Plan](Images/changing-the-web-hosting-plan.png?raw=true)
	
	_Changing the Web Hosting Plan_

8. Scroll to the bottom of the **Web hosting plan** blade, and click **Browse all pricing tiers**. In the _Choose your pricing tier_ blade, you can choose the hosting plan that fits your needs. 

	Web hosting plans represent a set of features and capacity that you can share across your Websites. Web hosting plans support several pricing tiers (e.g. Free, Shared, Basic and Standard), each with its own capabilities. There are a couple of differences among these tiers. Plans in the Free and Shared tier provide sites with a shared infrastructure, meaning that your sites share resources with other customers' sites. Web hosting plans in the Basic and Standard tiers provider sites with a dedicated infrastructure, meaning that only the site or sites you choose to associate with this plan will be running on those resources. In this tier you can configure your web hosting plan to use one or more virtual machine instances. As we are going to use the default web hosting plan, just close this blade.

	> **Note:** For all tiers (except 'Shared') you pay one price for the web hosting plan based on the tier and your chosen capacity with no additional charge for each site that uses the plan. Shared web hosting plans are different; due to the nature of the shared infrastructure, you are charged separately for each site in the plan. 
	
	![_Selecting a Web Hosting Plan](Images/selecting-a-web-hosting-plan.png?raw=true)
	
	_Selecting a Web Hosting Plan_

9. Click **Ok** to go back to the **Website** blade. You can change or leave the default location for the Website. Click **OK** to go to the previous blade.

10. Click **Database** to change the settings for your new database.

	>**Note:** If there are any existing databases asociated to the user, the **Database** blade will show up. Select **Create a new Database**. 
	
	![Changing your database settings](Images/changing-your-database-settings.png?raw=true)
	
	_Changing your database settings_
	
11. Set a name for the database, e.g. _mywebsite-db_, and click the **Server** option.

	> **Note:** You can also enter in the **Pricing Tier** section and explore the different pricing tiers.


	![Database Settings](Images/database-settings.png?raw=true)
	
	_Database Settings_

12. Enter the **Server Name**, **Server admin login** and a **Password**. Click **OK** to go back to the **New Database** blade, and click **OK** to close it.

	![Configuring the Database Server](Images/configuring-the-database-server.png?raw=true)
	
	_Configuring the Database Server_ 	
	
13. Now you are ready to create your resource group. Click **Create**.

	![Configured Resource Group](Images/configured-resource-group.png?raw=true)
	
	_Configured Resource Group_

14. You can see when the new resource group is created by accessing the **Notifications** tool. On the **Hub Menu**, click **Notifications**.

	![Notifications](Images/notifications.png?raw=true)
	
	_Notifications_
	
15. Once completed, you can click the notification to open the resource group blade.

	![Created Resource Group Notification](Images/created-resource-group-notification.png?raw=true)
	
	_Created Resource Group Notification_

16. You created your new resource group, which includes a Website and SQL Server database.

	![New Resource Group Blade](Images/new-resource-group-blade.png?raw=true)
	
	_New Resource Group Blade_
	
	> **Note:** Notice that the recently created resource group was automatically added to the Startboard for easy access.
	![Resource Group added to Startboard](Images/resource-group-added-to-startboard.png?raw=true)

	>**Note 2:** It is good practice to cleanup any resources that will not be used. To delete the demo resources just created, follow these steps:
	>
	>1. In the Resource Group, click **DELETE** at the top of the page.
	>
	>![Clicking Delete Resource Group](Images/clicking-delete-resource-group.png?raw=true)
	>
	>_Clicking Delete_
	>
	>1. In the Confirmation blade that opens, type the name of the resource group and click the **Delete** button.
	>
	>![Deleting Resource Group Confirmation](Images/deleting-resource-group-confirmation.png?raw=true)
	>
	>_Delete Confirmation_
	>
	>After a few moments you should see a notification in the Notifications Hub indicating the resource group was deleted. 
	>
	>![Notification after Resource Group was deleted](Images/notification-after-resource-group-was-deleted.png?raw=true)
	>
	>1. Click **Home** to navigate to the StartBoard. Once there, find and right-click the tile for the resource group. Click **unpin from Startboard**.
	>
	>![Unpin Resource Group from StartBoard](Images/unpin-resource-group-from-startboard.png?raw=true)
	>
	>_Unpinning Resource Group from StartBoard_
	>The tile is removed.


<a name="Summary" />
## Summary ##

The new Azure Preview portal offers an exciting look into the future of DevOps. This is a first-of-its-kind experience which brings together all of the individual resources, people, and lifecycle stages of your application into a unified portal. In this lab, you learned about the preview portal and how to create a new resource group by building a Website.
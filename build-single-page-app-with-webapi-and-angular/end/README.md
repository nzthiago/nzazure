##Setting up the End Solution for Geek Quiz

In the lab "**Building a Single Page Application (SPA) with ASP.NET Web API and Angular.js using Azure Active Directory to log in users**" you are given instructions to create a new project for the Geek Quiz application. The final code for the app is provided in the folder. In order to be able to run it, you need to configure it.

To do that, perform the following steps:

1. Browse to the [Azure Management Portal](https://manage.windowsazure.com/) and then to **Active Directory**. 
2. Select the desired directory, for example **Default Directory**.
3. Click **Applications** in the top bar.
4. Create a new application by clicking the **Add** button. Click **Add an application my organization is developing**. Enter a name for your app, such as _GeekQuiz_ and click the next button.
5. In the **App properties** tab, enter the **Sign-on URL** of your application, it should look like _https://localhost:44302/_. Additionally, enter the **App ID URL**, it has the form https://\<yourCustomDirectory\>.onmicrosoft.com/GeekQuiz; where _GeekQuiz_ is the name of the App ID you want to use, we will use _GeekQuiz_ for the rest of the example.

	> **Note:** The **App ID Uri** must be unique within your organization's directory.

6. Open Visual Studio and then the _Geek Quiz_ solution.

7. Open the Web.config file.

8. Find the `appSettings` element and update the following values with the appropriate values corresponding to your Azure subscription:

	* **[YOUR-FEDERATION-METADATA-LOCATION]**: It has the form https://login.windows.net/ \<yourCustomDirectory\>.onmicrosoft.com/FederationMetadata/2007-06/FederationMetadata.xml

	* **[YOUR-REALM]**: It is the **App ID URL** selected when creating the App in Azure AD. It has the form https://\<yourCustomDirectory\>.onmicrosoft.com/GeekQuiz

	* **[YOUR-AUDIENCE-URI]**: It is the **App ID URL** selected when creating the App in Azure AD. It has the form https://\<yourCustomDirectory\>.onmicrosoft.com/GeekQuiz

	Now you will obtain the **Client ID** and **Password**:	

9. Go back to the Azure Management Portal, and click your recently created application, and then in **Configure** in the top bar. Scroll down. 

10. Click the button to the right of the value to copy the **Client ID**.

	![Client ID for the app](images/client-id-for-the-app.png?raw=true)

	_Copying the Client ID_

11. Switch back to Visual Studio and in the `appSettings` section of the web.config file replace **[YOUR-CLIENT-ID]** with the value just copied.

12. Switch back to the browser and scroll down to the **Keys** section. You will add a new key by selecting a duration in the dropdown and then clicking **Save** in the bottom bar.

	![Adding a new key](images/adding-a-new-key.png?raw=true)

	_Adding a new key_

	Once it is saved, you can copy the new key to the clipboard by clicking the button next to it, as shown in the image.

	![Adding a new key](images/copying-a-new-key.png?raw=true)
	
	_Copying the key_

13. Change back to Visual Studio and in the `appSettings` section of the web.config file replace [YOUR-PASSWORD] with the value just copied.


14. Find the `audienceUris` element under `system.identityConfiguration` and replace [AUDIENCE-URI] with the same value as in the previous step.

15. Find the `wsFederation` element under `system.identityModel.services` and replace the following:

	* [WS-FEDERATION-ISSUER]: It has the form https://login.windows.net/ \<myCustomDirectory\>.onmicrosoft.com/wsfed

	* [WS-FEDERATION-REALM]: same as in previous step.

16. Save the file.

You should now be ready to run the solution.
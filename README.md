## Register the App on Azure AD

1. Sign in to the [Azure portal](https://portal.azure.com/).

2. If you have access to multiple tenants, use the Directories + subscriptions filter  in the top menu to switch to the tenant in which you want to register the application.

3. Search for App registrations > New registration.

4. Fill the ***Register an application*** form:
   - Enter a display Name for your application.
   - Specify which accounts will be using this application. [It can be modified later if needed](https://learn.microsoft.com/en-us/azure/active-directory/develop/howto-modify-supported-accounts)  
     *This app has been tested using "Accounts in this organizations directory only".*
   - Select *Public client.native (mobile & desktop)* and write "http://localhost/" as URI.

[More information regarding app registration](https://learn.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app)

![Image](URL "https://github.com/Barbarur/NovaPoint/blob/main/res/doc/AppRegister.png")

![ImageScript](assets/ScriptPreview.png)

![Alt text](https://github.com/Barbarur/NovaPoint/blob/main/res/doc/AppRegister.png)

<br> 
 
## Provide permissions to the App

1. Search for **App registrations** > Click on your App. *You should have been redirected already from the previous step though*

2. On the left options click on **API permissions**.

1. Click on **Add Permissions** and add the below permissions:
  - Microsoft Graph
    - *Directory.ReadWrite.All*
    - *Group.ReadWrite.All*
  - SharePoint
    - *AllSites.FullControl*

4.  Click on **Grant Admin consent for *Contoso***.

<br>

## Enable custom scripts App Settings

1. Navigate to SharePoint **Admin Center** > **Settings**.

2. At the bottom of the page you can find **Go to the classic settings page**.

3. At the classic settings page scroll down until you find the section **Custom Script**.

4. We recommend to select **Allow users to run custom script on personal sites** and **Allow users to run custom script on self-service created sites**.

5. Click **OK** at the bottom of the page.

<br>

## Application Setting 

Open **NovaPoint** and click on the Settings button at the left navigation pane.

1. Tenant ID: Navigate to *App Registration; Navigate to Azure AD > App registrations > Click on your App > Overview* > **Directory (tenant) ID**

3. Client ID: Navigate to *App Registration; Navigate to Azure AD > App registrations > Click on your App > Overview* > **Application (client) ID**

4. Save Access Token. This is optional. If you use it, remember to *Delete Cache* if you want to use a different account for using the app.


# Google Sheet API Project
Connecting users with the Google sheet to get access to the data. This API integration let us read and write to the spread sheet which is useful in many areas of technology.

## Prerequisite
### Softwares / Tools required
- JDK 8
- Java IDE (Ex: Eclipse, VsCode)
- A Google Account
### Java dependencies / JARs requried
- [Javax Mail](https://jar-download.com/artifacts/com.sun.mail/javax.mail)
- [Google API Client](https://jar-download.com/artifact-search/google-api-client)
- [Google API Service](https://jar-download.com/artifacts/com.google.apis/google-api-services-drive)
- [Google API Sheets](https://jar-download.com/artifact-search/google-api-services-sheets)
- [Google Oauth Client Java6](https://jar-download.com/artifacts/com.google.oauth-client/google-oauth-client-java6)

## Road Map
1. Creating a Google Account
2. Enabling a Google API Service
3. Downloading Client Secret JSON file
4. Creating a Google Sheet
5. Accessing Google Sheet data using Java

## Installation
### JDK 8 Installation
Download and install Java 8 JDK on your system if not already done.
You can download Java 8 from the official [Oracle Website](https://www.oracle.com/in/java/technologies/javase/javase8-archive-downloads.html) 

Once downloaded, Install and setup your environemntal variables for Java 8 properly. If you don't know how to setup your environmental variables, kindly follow the steps given in this [link](https://www.javatpoint.com/how-to-set-path-in-java).

To check the version of Java installed in your system, kindly execute the following command on your CMD.

```bash
  java -version
```
The output will be displayed like the following.

```bash
  java version "1.8.0_101"
  Java(TM) SE Runtime Environment (build 1.8.0_101-b13)
  Java HotSpot(TM) 64-Bit Server VM (build 25.101-b13, mixed mode)
```

## Creating a Google Account
To create a google Account if you don't have any, open a browser window and click on **Sign In** button on google search page. Click **Create account** on the Sign In page.

Enter the Details as shown in the below image.

![Create_Google_Account](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/1create_google_account.JPG)

CLick **Next** and enter the other personal details on the form and Agree the Terms and Conditions.

Finaly create the Google Account.

## Managing Google Account
Once the Google Account is successfully created, open **Manage your Google Account** page.

Click **Security Tab** on the left and verify whether **2-Step Verification** is disabled. If it is enabled, please disable it.

![Two_Step_Verification](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/2disable_2step_verification.JPG)

Then Navigate below to find **Less Secure app access** option and enable it.

![Less_secure_apps](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/3enable_less_secure_apps.JPG)

## Generating Client Secret JSON

Open [Google Console](https://console.cloud.google.com/) with your account created on this [Step](https://github.com/CHANDRASEKAR98/google-sheet-api-project/edit/main/README.md#creating-a-google-account).

- ### Creating New Project
  1. Navigate to **IAM & Admin -> Create a Project** to create your new project on google developer console.

  ![create_a_project](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/4google_console_create_project.jpg)

  2. Enter the **Project name** and choose the organization. If you aren't beloging to any organization, then let it be **No Organization**.

  ![creating_project](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/5google_cloud_creating_project.JPG)

  3. Once you click **CREATE** button, the project will be created in a minute and you'll be redirected to Google Console's Dashboard screen.

  ![google_cloud_dashboard](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/6google_console_created_project.JPG)

- ### Enable a Google API Service
  1. Navigate to **APIs & Services -> Enabled APIs & Services** to enable the Google APIs that you want for your project.
  
  ![apis_services](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/7api%26services.jpg)
  
  2. Once APIs & Services section is loaded, click on **ENABLE APIS AND SERVICES**.
  
  ![enable_apis_services](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/8enabing_api%26services.JPG)
  
  3. API Library screen will be opened. On the search bar, search for "Google Sheet API".
  
  ![google_sheet_api](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/9search_google_sheet.JPG)
  
  4. Click on "Google Sheet API" and click **ENABLE** to enable this API.

  ![enable_google_sheet_api](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/10enabing_google_sheet_api.jpg)
  
  5. Once the API is enabled, the following screen will be displayed.

  ![enabled_google_sheet](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/11enabled_google_sheet_api.JPG)
  
  **Note:** The OAuth consent screen is required to be configured with the information of your application.
  
- ### Configuring OAuth Consent screen
  1. Click OAuth Consent screen tab using the side menu. By default, no option is selected for the User type. If you aren't Google Workspace user, then click on **External** option.
  
  ![oauth_consent_register](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/12creating_oauth_consent_screen.JPG)
  
  2. Once **CREATE** is clicked, **Edit app registration** screen will be displayed with **oauth consent screen** section loaded.
  App Information will automatically loaded with app name and the user support email will be selected with the current google account.
  
  ![step1_oauth_consent](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/13oauth_screen_step1.JPG)
  
  If you want to receive any further updates or notifications regarding your application, Enter an email address in the last field and click **SAVE AND CONTINUE**.
  
  3. If no authorization regarding the users is required, then scroll down the **Scopes** section and simply click **SAVE AND CONTINUE**.
  
  ![step2_oauth_consent](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/14oauth_step2_just_save_continue.JPG)
  
  4. Entering information on **Optional Info** is optional. If you don't like to enter it, simply click **SAVE AND CONTINUE**.

  ![step3_oauth_consent](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/15oauth_step3_save_continue.JPG)
  
  5. Finally **Summary** section will be loaded to verify the overall app registration.

  ![step4_oauth_consent](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/16oauth_step4.JPG)
  
  Once the summary is verified, click on **"GO TO DASHBOARD"**.
  
  6. Now the OAuth Consent screen is configured with the information abou your application.

  ![final_oauth_consent](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/17oauth_consent_created.JPG)

- ### Creating Credentials

  Once OAuth consent screen is configured, follow the below steps to create a client secret credentials and download it to your local system.
  
  1. Click the Credentials tab from the side menu. Thereby Credentials screen will be diplayed.
  
  2. Click **+ CREATE CREDENTIALS** button as shown in the image below.

  ![click_create_credential](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/18create_credentials.JPG)
  
  3. On clicking the create credentials button, the following options will be displayed.

          - API Key
          - OAuth Client ID
          - Service Account
          - Help me choose
  Among theose options, we have to select "OAuth Client ID" because **Google Sheet API** we enabled in this [Step](https://github.com/CHANDRASEKAR98/google-sheet-api-project/edit/main/README.md#enable-a-google-api-service) needs client authorization in order to acceess the spreadsheet data.
  Refer the below image.
  
  ![client_id_options](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/19oauth_client_id.jpg)
  
  4. Once "OAuth Client ID" option is selected, **Create OAuth Client ID** screen opens.
  
  5. Choose Application Type based on the your need. For this project I have selected Application Type as "Desktop app".
  
  6. Name your OAuth Client which is used to identify the client in the console only.

  ![creating_credentials](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/20creating_oauth_client_id.JPG)
  
  7. on clicking **CREATE** button, OAuth Client will be created and a pop up will be displayed like the below image. Download the OAuth Client Credentials by clicking the **DOWNLOAD JSON** button.
  
  ![download_json](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/21download_client_secret_JSON.JPG)
  
  8. Once the JSON file is downloaded to your system, optionally rename it to "client_secret.json" if you want to.
  
  ![rename_credentials](https://github.com/CHANDRASEKAR98/google-sheet-api-project/blob/main/images/22rename_json_optionally.JPG)
  

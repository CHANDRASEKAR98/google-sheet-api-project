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
// 

CLick **Next** and enter the other personal details on the form and Agree the Terms and Conditions.
Finaly create the Google Account.

Once the Google Account is successfully created, open Manage your Google Account page.

Click on Security Tab on the left and verify whether the **2 Step Verification** is disabled.
//

Then Navigate below to find **Less Secure apps** option and enable it.
//




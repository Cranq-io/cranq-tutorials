# 📊 Using Google API (drive & spreadsheet)

_In order to be able to use Google Sheets or Drive API, you must first authenticate yourself with the service. All Google APIs use the OAuth 2.0 protocol for authentication and authorization, which simplifies the process. Moreover, you can also create a service account that can be used to access all of Google’s resources._

## Setting up <a href="#setting-up" id="setting-up"></a>

### **Enable the Google Sheets API**

*   Go to the [Google APIs Console](https://console.developers.google.com/)

    Click “**Select a project**” in the top-right corner\


    <figure><img src="../.gitbook/assets/image (19).png" alt="" width="563"><figcaption></figcaption></figure>


*   Click the “**New Project”** option\
    \


    <figure><img src="../.gitbook/assets/image (42).png" alt="" width="563"><figcaption></figcaption></figure>


*   Give a unique name to your project and click **“Create”**\


    <figure><img src="../.gitbook/assets/image (25).png" alt="" width="477"><figcaption></figcaption></figure>


*   Go to the [APIs dashboard](https://console.cloud.google.com/apis/dashboard)&#x20;

    Search for “**Google Sheets API**” and click on it\


    <figure><img src="../.gitbook/assets/image (31).png" alt="" width="563"><figcaption></figcaption></figure>


*   Click **“Enable”** and wait for the API to be enabled\
    \


    <figure><img src="../.gitbook/assets/image (29).png" alt="" width="375"><figcaption></figcaption></figure>



**Create a Service Account**

*   When the API is enabled, move to the [Credentials](https://console.cloud.google.com/apis/credentials) page

    Click the “**Create credentials**” option and select “**Service Account**”\
    \


    <figure><img src="../.gitbook/assets/image (36).png" alt="" width="563"><figcaption></figcaption></figure>


*   Give a name to the service account and click **“Create”**\
    \


    <figure><img src="../.gitbook/assets/image (35).png" alt="" width="516"><figcaption></figcaption></figure>


*   Click **“Select a role”** => **“Project”** => **“Editor”**\
    \


    <figure><img src="../.gitbook/assets/image (34).png" alt="" width="560"><figcaption></figcaption></figure>


*   Click **“Done”**\


    Now that your service account has been created, you will have to create a key, which will allow you to connect to the API automatically via this service account.

**Create a Service Key**

*   In the [Credentials](https://console.cloud.google.com/apis/credentials) page, click on your service account name\
    \


    <figure><img src="../.gitbook/assets/image (6).png" alt="" width="563"><figcaption></figcaption></figure>


*   Go to “**Keys**”\
    \


    <figure><img src="../.gitbook/assets/image (41).png" alt="" width="511"><figcaption></figcaption></figure>


*   Select **“Add Key”** => **“Create new key”**\
    \


    <figure><img src="../.gitbook/assets/image (32).png" alt="" width="428"><figcaption></figcaption></figure>


*   Leave the option as **JSON** and click “**Create”**\
    \


    <figure><img src="../.gitbook/assets/image (39).png" alt="" width="412"><figcaption></figcaption></figure>


*   Rename the downloaded file to  `client_secret.json`The file contains all the sensitive information that will allow your app to authenticate with Google and have access to the API. **It’s critical for this file to be kept private so that only your application has access to it.**\
    \
    The file will look like this:\
    \


    <figure><img src="../.gitbook/assets/image (2).png" alt="" width="563"><figcaption></figcaption></figure>

    Find the **“**`client_email`**”** value and copy the email address. Each spreadsheet that you want to be manipulated by your app must provide access to this email.

**Share your spreadsheet with `client email`**

*   Click **“Share”** in the top-right corner of your spreadsheet.\
    \


    <figure><img src="../.gitbook/assets/image (40).png" alt="" width="563"><figcaption></figcaption></figure>


*   Use  `client_email` from the  `client_secret.json`**.** Give **Editor** right. \
    Click "**Send**".\
    \
    \
    \


    <figure><img src="../.gitbook/assets/image (4).png" alt="" width="473"><figcaption></figcaption></figure>



Now your service account has **Edit** access to the sheet and your application can use Google Sheets API to access the spreadsheet.&#x20;

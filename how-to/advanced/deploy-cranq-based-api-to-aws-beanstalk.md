# Deploy CRANQ based API to AWS Beanstalk

### Before you begin

**Get familiar with AWS Beanstalk:** [https://docs.aws.amazon.com/elastic-beanstalk/index.html](https://docs.aws.amazon.com/elastic-beanstalk/index.html)

**Have a Beanstalk web server environment created:**

* Managed platform Node.js platform
* Name it e.g cranq-api

**More:** [https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/GettingStarted.CreateApp.html](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/GettingStarted.CreateApp.html)

### **Deployment steps**

* [Compile ](compiling-programs.md)the CRANQ program o NodeJS
* Extract the generated .tgz file. When you unzip it, it will create a package folder.
* Navigate under the package folder. You’ll find two files:
  * \<program\_name>.js
  * package.json
* Execute npm i (It generates a node\_modules directory and a package-lock.json file)
* Compress the folder to e.g cranq-api.zip
* [Upload and deploy](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.deploy-existing-version.html) the ZIP file to Beanstalk as a new application version


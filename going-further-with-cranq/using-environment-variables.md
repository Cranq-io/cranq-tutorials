---
description: >-
  This how-to explains using environment variables in CRANQ through a simple
  example.
---

# ❓ Using Environment Variables

Environment variables provide a safe way to store secrets that we don't want to bundle into our CRANQ project.

It's also a great way to share variables between projects.

You find a couple of nodes in the CRANQ repo that deal with environment variables based on whether you're looking to read one variable at a time or more, or whether you want to provide default values, or just want to get the ones that have assigned values in the environment.

<figure><img src="../.gitbook/assets/Screenshot 2022-09-18 at 11.50.53 (1).png" alt=""><figcaption><p>List of environment-related nodes</p></figcaption></figure>

The _Environment variables getter with fallback_ node is a good choice in most situations.

## **Setting up the CRANQ graph**

In the following example, we'll focus on two environment variables: "API\_KEY" and "PRIVATE\_KEY".

### **1. Drag an environment variable getter node onto the canvas**

Find `system/Environment variables getter with fallback` in the repo, drag it onto the canvas, then click on the `default values` port and set an empty dictionary.

<img src="../.gitbook/assets/image (6).png" alt="" data-size="original">![](<../.gitbook/assets/image (1).png>)

### **2. Drag a store node onto the canvas**

Find `data/Store` in the repo and drag it onto the canvas. This will hold the list of variable names. Then, click on the `data` input port and set the value to the list of environment variable names: `["API_KEY", "PRIVATE_KEY"]`.

![](<../.gitbook/assets/image (7).png>)![](<../.gitbook/assets/image (12).png>)

### **3. Connect nodes**

First connect the <mark style="color:orange;">`start`</mark> output of <mark style="color:blue;">`start`</mark> to the <mark style="color:green;">`read`</mark> input of <mark style="color:blue;">`store`</mark>. This will cause the <mark style="color:blue;">`store`</mark> node to send out the list of variable names we stored in it via its <mark style="color:orange;">`data`</mark> output.

Then, connect the <mark style="color:orange;">`data`</mark> output of <mark style="color:blue;">`store`</mark> to the <mark style="color:green;">`variable names`</mark> input of <mark style="color:blue;">`environment variable getter...`</mark> node.

Finally, connect the <mark style="color:orange;">`resolved variables`</mark> output of the <mark style="color:blue;">`environment variable getter...`</mark> node to the <mark style="color:green;">`data`</mark> input of the <mark style="color:blue;">`logger`</mark> node. This will allow us to see the environment variables' values in the output window.

![](<../.gitbook/assets/image (4).png>)![](<../.gitbook/assets/image (13).png>)![](<../.gitbook/assets/image (5).png>)

## **The .env file**

Upon first run, you'll likely see something like this on the output:

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

The values are empty, because there are no such environment variables set up yet. And even if there were, the CRANQ app doesn't actually read from the real environment. It reads environment variables from a _.env_ file stored in the CRANQ folder. This way you have more control over these variables during the development process. (Once the program is compiled to NodeJS it will read the actual environment, but more on that later.)

To create a .env file, first open the CRANQ folder via the Help menu.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>Open the CRANQ folder</p></figcaption></figure>

Make note of the absolute path, and using a text or code editor, save the .env file there with the following content:

```
API_KEY=My API key
PRIVATE_KEY=My private key
```

Once saved, head back to CRANQ, and re-run the program. This time we'll see the values we just added to the .env file.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>Values read from .env file</p></figcaption></figure>

## **Sharing environment variables with other projects**

CRANQ's .env file is a regular dotenv ([https://www.npmjs.com/package/dotenv](https://www.npmjs.com/package/dotenv)) file, so other projects that use the dotenv library can read from it.

CRANQ uses the same .env file across projects, so you don't have to do anything extra to share environment variables between CRANQ projects. Just switch to another project and the variables will be accessible form there too.

## **Running the compiled code**

The .env file works great in the CRANQ app, but CRANQ programs are ultimately meant to be run independently from the CRANQ app, where you want to access the actual environment variables, not the contents of a .env file.The good news is that you can do it without any extra effort. CRANQ programs compiled to NodeJS get the real environment variables through the same nodes. All you have to do is compile your CRANQ program, and then, run it or use it as an NPM dependency in your JavaScript project.To compile, simply select "Compile" / "NodeJS" from the menu, and save the zipped NPM package.

![](https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FOAyvGDT2zXMtcUTDVXAy%2Fuploads%2FfxSeBu3rSZtgpPhw3FQ4%2FScreenshot%202022-09-18%20at%2013.58.58.png?alt=media\&token=74e80aa1-c178-4db5-8bc4-a5a6e841bb18)![](<../.gitbook/assets/image (10).png>)

After compiling this program, unzipping, installing dependencies, and running it through node, you'll likely see the same output as when we ran it from CRANQ for the first time.\
\


<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FOAyvGDT2zXMtcUTDVXAy%2Fuploads%2FYeXXMy7u0W7X4Llc5WmF%2FScreenshot%202022-09-18%20at%2014.04.10.png?alt=media&#x26;token=5fd73c2f-b486-4823-80ad-9a5e97d647f1" alt=""><figcaption><p><strong>Running compiled program</strong></p></figcaption></figure>

It's because, again, these variables are not set in the environment. Once we set them, they'll be read out correctly. (Screenshot below shows setting environment variables in macOS. Other OSes have similar commands to set environment variables.)\


<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FOAyvGDT2zXMtcUTDVXAy%2Fuploads%2Fh8qnXwFoK0EJUkykcg7f%2FScreenshot%202022-09-18%20at%2014.07.07.png?alt=media&#x26;token=128aba03-3c31-4d01-b3af-72ee0a0d43dd" alt=""><figcaption><p>Setting environment variables and re-running program</p></figcaption></figure>

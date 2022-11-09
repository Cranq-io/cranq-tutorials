---
description: Having trouble getting test ETH?  Might be time to try Ganache.
---

# 🍫 Setting up Ganache with Metamask

Ganache is a development tool in the Truffle Suite and is used for setting up a personal Ethereum Blockchain to deploy contracts, develop your applications, and run tests. MetaMask is a software cryptocurrency wallet used to interact with the Ethereum blockchain.  Getting test ETH is a nightmare these days so we recommend using local network for development. In a local network, there is no ETH limitation, and you don't have to wait for transactions to complete. \
\
In this tutorial we will install and setup Ganache and import your Ganache account to Metamask. When you are done you can:

* Sign Ganache transactions from Metamask
* Check your (Ganache) assets in Metamask
* Check every (Ganache) transaction which affected your wallet in Metamask

## Steps

1. Download Ganache from: [https://trufflesuite.com/ganache/](https://trufflesuite.com/ganache/)\
   \
   ![](<../.gitbook/assets/image (16).png>)
2. Install Ganache
3. Run Ganache
4. Select QUICKSTART ETHEREUM as workspace\
   \
   ![](<../.gitbook/assets/image (22).png>)
5. Goto setting\
   \
   ![](<../.gitbook/assets/image (14).png>)
6. Select SERVER tab\
   \
   ![](<../.gitbook/assets/image (20).png>)
7. Select 127.0.0.1 as HOSTNAME\
   \
   ![](<../.gitbook/assets/image (25).png>)
8. Switch off AUTOMINE toggle\
   \
   ![](<../.gitbook/assets/image (35).png>)
9. Set MINING BLOCK TIME to 10\
   \
   ![](<../.gitbook/assets/image (4).png>)
10. Click on SAVE AND RESTART\
    \
    ![](<../.gitbook/assets/image (5).png>)
11. Setting up ganache network in Metamask
    1. Open Metamask\
       \
       ![](<../.gitbook/assets/image (6).png>)
    2. Select Settings\
       \
       ![](<../.gitbook/assets/image (31).png>)
    3. Select Networks\
       \
       ![](<../.gitbook/assets/image (2).png>)
    4. Click on Add Network\
       \
       ![](<../.gitbook/assets/image (32).png>)
       1. Set the Network Name e.g ganache\
          \

       2.  The RPC URL value comes from ganache\
           \
           ![](<../.gitbook/assets/image (33).png>)\
           \
           &#x20;                                                              i.      &#x20;

           ![](<../.gitbook/assets/image (34).png>)\
           \

       3. Set the Chain ID
          1. Type e.g 1 and a hint appears about the exact Chain ID so use that.\
             \
             ![](<../.gitbook/assets/image (28).png>)
          2. **Type the suggested chain id which is 1337.**\
             ****\
             ****![](../.gitbook/assets/image.png)****
       4. Set the Currency symbol\
          \

       5. Click on Save\
          \
          ![](<../.gitbook/assets/image (23).png>)
    5. Open My accounts\
       \
       ![](<../.gitbook/assets/image (26).png>)
    6. Import your Ganache account&#x20;
       1. Click on Show keys of the account to import in Ganache\
          \
          ![](<../.gitbook/assets/image (21).png>)
       2. Copy the PRIVATE KEY\
          \
          ![](<../.gitbook/assets/image (19).png>)
       3. Open Metamask\
          \
          ![](<../.gitbook/assets/image (13).png>)
       4. Open My Accounts\
          \
          ![](<../.gitbook/assets/image (15).png>)
       5. Select Import Account\
          \
          ![](<../.gitbook/assets/image (18).png>)
       6. Enter your private key and import\
          \
          ![](<../.gitbook/assets/image (7).png>)\

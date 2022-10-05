---
description: >-
  We follow Toby as he gathers crypto exchange rate data from Yahoo Finance,
  manipulates it into a new data format, and inserts it into an AirTable via the
  AirTable API using a loop
---

# ⬆ Updating an AirTable With Exchange Rates

## Intro

Here's one I made earlier.  Let's see how it works.

{% embed url="https://youtu.be/kINDoJgXRnU" %}

## Getting an Exchange Rate and Inserting it into Airtable

We will use Yahoo Finance to get prices, then we will convert them into records.  Then, we will authenticate the Airtable API, and insert our records into an AirTable.

{% embed url="https://youtu.be/bYmi5NBcMfM" %}
Getting Rates and Inserting Them
{% endembed %}

## Updating the Exchange Rates and Creating a Loop

Now we have the records inserted, we can retrieve them, separate out their IDs, and update them with a loop.  At the end, we'll clean everything up and make sure that we have a single point where we input pair names and authentication details.  Hope you enjoyed this course!

{% embed url="https://youtu.be/09agh3mJvms" %}

---
description: >-
  We follow Toby as he gathers crypto exchange rate data from Yahoo Finance,
  manipulates it into a new data format, and inserts, and updates it in AirTable
  using a loop
---

# ⬆ Build an Exchange Rate Tracker in AirTable

## Intro

This project is going to help you master some fundamental skills in CRANQ!  We're going to pull data from the Yahoo Finance API, and insert it into AirTable, all with low-code.  Then we're going to map that data, and continuously update it, so we could make a trading alert, for example.  Along the way, we'll also work on using variables and buffers.  In this first video in the series, we'll look at a completed version of the programme we will build.

{% embed url="https://youtu.be/kINDoJgXRnU" %}

## Getting an Exchange Rate and Inserting it into Airtable

We will use the Yahoo Finance API to get prices, then we will convert them into records, and subsequently, AirTable records.  After we've authenticated the Airtable API, we can insert our records into an AirTable.  As preparation for this course, you should open an AirTable account.

{% embed url="https://youtu.be/bYmi5NBcMfM" %}
Getting Rates and Inserting Them
{% endembed %}

## Updating the Exchange Rates and Creating a Loop

Now we have the records inserted into AirTable, we can retrieve them, separate out their IDs, and update them with a loop.  At the end, we'll clean everything up and make sure that we have a single point where we input pair names and authentication details.  \
\
I hope you enjoyed this course, what will you do with your new low-code skills?

{% embed url="https://youtu.be/09agh3mJvms" %}

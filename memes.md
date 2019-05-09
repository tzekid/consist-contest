# search

## What is search ?

Search is the meat of Splunk, but what do you search for anyhow ?

There's a bunch of data floating around but no one has any idea how to put it all together. Splunk offers you the possibility to look for correlations (todo: synonym) in the data, or have use cases to look out for.

Say you have a shop, a bunch of social media accounts and maybe a mailing list. As a business owner you would like to see what's trending, who's talking about you or even if someone has a complain about your shop - who knows, maybe something's not working proper.

Splunk allows you to take all this data in and look for connections.

## Installing Splunk

Before starting everything you have to install Splunk. To do that, you have to go on their page and [create a new account](https://www.splunk.com/page/sign_up?redirecturl=https://ilieploscaru.xyz). After you've done that, log in and [download their client](https://www.splunk.com/en_us/download/splunk-enterprise.html) on the platform of your choice. For more instructions on that, have a look at [the official docs](https://docs.splunk.com/Documentation/Splunk/7.2.6/Installation/Chooseyourplatform). 

After you've successfully installed it, open your browser and enter  `http://localhost:8000/` in the search(?) bar.

There you can enter your Splunk login credentials (username | password). Once logged in click on the "Search & Reporting" app on the bar on the left.

 ((( Image with Splunk Home -> highlight Search App ))) You should get something like this.

## Importing sample data

Now, the search view is empty because there's no data. So let's import some.

In the upper left corner, click on the Splunk logo. That will take you to the home screen. From here, click on "Add Data".

In this screen you have multiple options of how to get data into Splunk. All we want for now is to upload a set of data. Click on the Upload button. 

Once there, you can upload [this dataset](#). Splunk can handle a buttload of different data types, which you can manage in this screen however you like. But, in our case, it is already in the format we want so you'll just have to click "next" a bunch of times. Once done, click on "Start searching", which will take you back to the search app. 

## The Search interface

( TODO: always click on `all time` )

( TODO: pivot from status to action )

((( Image with Search App interface: highlighted searchbar, fields and events)))

This is where you will be spending most of your time in Splunk. The interface can be broadly broken down in three areas: Events, Fields-bar and Searchbar.

### Searchbar

((( TODO ? or skip entirely )))

### Events

((( Image with expanded event )))

In the middle of the screen you see a table with three columns: **i**, **Time** and **Event**. The **Event**s might look scary mess at first, but don't worry. Look at the first event and click on the right arrow on the left, in the **i** column. The big, scary string is now broken down and categorized into a bunch of smaller fields. If you're somewhat familiar with websites, then this data be familiar to you.

Once you input something in Splunk, it looks for patterns and tries to make something out of the data you give it. In the worst case scenario, it will at least try to categorize the data by some kind of time-stamp.

### Fields-bar

Now, if you shrink the event (by clicking on the down-arrow) you can have a look on the left side at the Fields-bar. There you see many, if not all, of the fields that you saw in the event. The number next to the field shows how many different kind of values a field can have.

Let's say you want to see if the shop works correctly. When you browse the web and go on a page, the server that send you the page also gives you a status response. This status can be **200**: success, **404**: not found or **503**: server error.

((( Image with expanded status )))

If you click on the **status** field on the Field-bar you will see which status has been sent how many times and it's percentage compared to the whole. This is already very powerful information, because we can see at a glance how well our site performs.

Above the table there are some 'Reports' ready for us. These are quick, general searches which are generally useful. By clicking on **Top values by time** you will be taken to a visualization of the statuses over time.

((( Image with Top values by time ))) 

If you look at the search bar you will see a pre-built search which will look something like:

((( Image breaking down the syntax like 97 in dingding )))

Which more or less means: ((( paraphrase the explanation in one sentence. )))

## The Splunk Processing Language (SPL)

((( * -> status=503 )))

- searching for stuff
  - simple searching
    - wildcards
    - operators (and, or, not)
  - searching fields
- pipe(s)
- stats and timechart
  - nice stuff you can do with it
- 

### How to search for stuff

### Filtering your results



### Tables and Visualizations

--> link to Dashboards







[^0]: in Splunk it is called "machine data", because it refers to data that is created by machines. 



- what kind of search you do in splunk
  - fwd to big data

- splunk setup (for extra-dummies)
  - it's annoying, we know, and let's make fun of it

- a brief introduction to the SPL with examples (ongoing theme ?)
  - time is important. in splunk everything is timestamped

  - UI: it's actually useful
    - what can you see / do with the search UI at first glance

  - search queries. the core of spl
    - fields

  - functions. do fun stuff with your data
  - put your data in tables and create visualisations
    - fwd. to dashboards

# dashboards

- data is not always easy to understand, that's why we visualize it
- how to dashboards in splunk
  - after you have a search (take some examples out of search) you can save them
- use cases and how dashboards play a role
- use cases. different types of dashboards and some helpful plugins

# big data

- buzz word that nobody really understands
- big data from a splunk perspective in one (or a few) simple, concise sentences
- how splunk deals with big data

How Splunk works:
Forwardeer on a server and sends data to an Indexer
The indexer prepares the data for processing and sends the to the Search Head
The Search Head does the searching - the main component of the hackathon.

- usecases and where / how it would be implemented
  - reports


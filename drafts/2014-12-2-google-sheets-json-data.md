---
title: Using Google Sheets as a JSON Data Source
layout: default
comments: true
---

## {{ page.title }}

### Things I have learned that might help you

Earlier this year, I developed a Bootstrap based site to list my home for sale by owner. Once that exercise was complete and we have now settled into our new place, I had this idea of converting the site into a template for others. There are lots of folks trying to sell their homes, but the resources available to them might not necessarily be the best.

In planning on what I was going to do, the goal was to make it as easy to modify for someone who had limited web development skills. My first idea was to use a spreadsheet to hold the detailed specification information and then import that into the site. The easiest way I found was to use Google Sheets.  Google Sheets provides for a JSON data source, which should make the task of displaying detailed home specifications simple.

>Google Sheets provides for a JSON data source

I had other ideas around how to import the photos using Flickr or other photo sharing services. These I will incorporate into a later version of the template.

Of course every project begins with some Googling to see what others have done. This proved both useful and frustrating. The useful part showed that it could be done, the frustraing part was that Google had made some changes and the URL's weren't exactly the same.

After some good ole fashioned testing and changing one parameter at a time, I got it to go.  The following should prove to be helpful until the spec changes again.

The Google Sheet was setup to mirror the presentation in the website.
![Alt "Google Sheets"](/assets/images/2014-12-2/googleSheets.png "Google Sheets")

Note the headings; desc1, data1, etc. These heading names are become JSON field names and are then used to parse the data into the web page table.

With the spreadsheet complete, we need to make it public. (I am not sure what the process is, should you not wish to make your sheet public.) This step can be a little confusing, as there are a number of ways to make a sheet public, but only one way that works for this purpose.

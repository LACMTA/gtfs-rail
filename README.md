# Los Angeles County Metropolitan Transportation Authority's GTFS for Rail.
## updated 2022-10-07 01:30:12 PDT America/Los_Angeles

As of May 6th, 2016 The LACMTA is now publishing our Bus and Rail Services in separate Google Transit Exports ONLY. As a customer service, and to allow us to update these files more frequently, we have split these files up. The new rail-only export will be updated Daily (generally Tuesday-Saturday mornings), to allow us to send out more timely information and to allow our users to capture all temporary rail service changes that may occur on a daily basis. The bus-only exports will continue to be provided as large-scale changes to the system occur -- generally once every one or two months. We will NOT continue to maintain the combined service feeds.

### Join our developer community at [http://developer.metro.net](http://developer.metro.net) to learn more about using this data.

### Link to LACMTA's Bus Data repository: [https://gitlab.com/LACMTA/gtfs_bus/](https://gitlab.com/LACMTA/gtfs_bus/)

---

### Evergreen link to the gtfs_rail.zip archive: [https://gitlab.com/LACMTA/gtfs_rail/raw/master/gtfs_rail.zip](https://gitlab.com/LACMTA/gtfs_rail/raw/master/gtfs_rail.zip?1665131412.4460428)

### Today's link to the gtfs_rail.zip archive: [https://gitlab.com/LACMTA/gtfs_rail/raw/master/gtfs_rail.zip?1665131412.4460428](https://gitlab.com/LACMTA/gtfs_rail/raw/master/gtfs_rail.zip?1665131412.4460428)


### zip archive contents
```
 Length   Creation datetime         Name        
-----------------------------------------------
     174  2022-10-07 00:08   agency.txt         
    1458  2022-10-07 00:08   calendar.txt       
      32  2022-10-07 00:08   calendar_dates.txt 
     712  2022-10-07 00:08   routes.txt         
  330545  2022-09-23 14:07   shapes.txt         
   35567  2022-09-23 14:05   stops.txt          
11762111  2022-10-07 00:09   stop_times.txt     
  386461  2022-10-07 00:08   trips.txt          
     285  2022-10-07 00:32   feed_info.txt      
```

## Summary of changes
```
commit f7356486c440cc421f9e1f928c2bb316cd21faa6
Author: activebatch <activebatch@MTAABEXEC01>
Date:   Thu Oct 6 01:30:13 2022 -0700

    2022-10-06 01:30:08 PDT America/Los_Angeles

 README.md      |   38 +-
 calendar.txt   |   24 +-
 gtfs_rail.zip  |  Bin 800674 -> 848400 bytes
 stop_times.txt | 6761 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 trips.txt      |  507 +++++
 5 files changed, 7300 insertions(+), 30 deletions(-)
```

## Subscribing to changes

### Get the latest commit ID with Curl

```
#!/bin/sh

url="https://gitlab.com/LACMTA/gtfs_rail/commits/master.atom"

curl --silent "$url" | grep -E '(title>|updated>)' | \
  sed -n '4,$p' | \
  sed -e 's/<title>//' -e 's/<\/title>//' -e 's/<updated>/   /' \
      -e 's/<\/updated>//' | \
  head -2 | fmt

# returns:
# 2015-12-31T13:09:36Z
#    new info from SPA and instructions on preparing the archive
```

### Get the latest commit ID with Python

```
#!/bin/env python

import feedparser

url = 'https://gitlab.com/LACMTA/gtfs_rail/commits/master.atom'
d = feedparser.parse(url)
lastupdate = d['feed']['updated']

print(lastupdate)

```

See the [http://developer.metro.net/the-basics/policies/terms-and-conditions/](http://developer.metro.net/the-basics/policies/terms-and-conditions/) page for terms and conditions.

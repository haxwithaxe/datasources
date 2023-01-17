This is a set of RSS feeds from NOAA's National Hurricane Center with notices about tropical storms in the Atlantic and Pacific. These include map data and storm forecasts ("outlooks").

https://www.nhc.noaa.gov/aboutrss.shtml and archived data that can be used for testing https://www.nhc.noaa.gov/aboutrssupdates.shtml

# Docs

The "wallets" are a fixed number of slots that are assigned to active storms.

# Examples
## Get GIS data
Get a feed of the Atlantic Storm GIS data.

### Request
GET `https://www.nhc.noaa.gov/rss_examples/gis-at.xml`

### Response
```xml
<rss version="2.0">
  <channel>
    <pubDate>Thu, 06 Jun 2013 03:07:32 GMT</pubDate>
    <title>National Hurricane Center GIS Data (Atlantic)</title>
    <description>
      Atlantic Basin GIS Data for Active Tropical Cyclones
    </description>
    <link>http://www.nhc.noaa.gov/gis/</link>
    <copyright>none</copyright>
    <managingEditor>nhcwebmaster@noaa.gov (NHC Webmaster)</managingEditor>
    <language>en-us</language>
    <webMaster>nhcwebmaster@noaa.gov (NHC Webmaster)</webMaster>
    <image>
      <url>http://www.nhc.noaa.gov/gifs/xml_logo_nhc.gif</url>
      <link>http://www.nhc.noaa.gov/</link>
      <title>National Hurricane Center GIS Data (Atlantic)</title>
      <description>NOAA logo</description>
      <width>95</width>
      <height>45</height>
    </image>
    <item>
      <title>
        Graphical Tropical Weather Outlook [shp] - Multiple Basins
      </title>
      <description>
        Shapefile last updated Thu, 06 Jun 2013 02:34:27 GMT
      </description>
      <pubDate>Thu, 06 Jun 2013 02:34:27 GMT</pubDate>
      <link>http://www.nhc.noaa.gov/gtwo/two.zip</link>
      <guid isPermaLink="false">gis-gtwo-shp-201306052336</guid>
      <author>nhcwebmaster@noaa.gov (NHC Webmaster)</author>
    </item>
...
```

## Get outlook text
Get a feed of the tropical storm outlook text for the Eastern Pacific.

### Request
GET `https://www.nhc.noaa.gov/rss_examples/index-ep.xml`

### Response
```xml
<rss version="2.0">
  <channel>
    <pubDate>Thu, 30 May 2013 19:07:15 GMT</pubDate>
    <title>National Hurricane Center (Eastern Pacific)</title>
    <description>Active tropical cyclones in the Eastern Pacific</description>
    <link>http://www.nhc.noaa.gov/</link>
    <copyright>none</copyright>
    <managingEditor>nhcwebmaster@noaa.gov (nhcwebmaster)</managingEditor>
    <language>en-us</language>
    <webMaster>nhcwebmaster@noaa.gov (nhcwebmaster)</webMaster>
    <image>
      <url>http://www.nhc.noaa.gov/gifs/xml_logo_nhc.gif</url>
      <link>http://www.nhc.noaa.gov/</link>
      <title>National Hurricane Center (Eastern Pacific)</title>
      <description>NOAA logo</description>
      <width>95</width>
      <height>45</height>
    </image>
    <item>
      <title>Eastern Pacific Tropical Weather Outlook</title>
      <description>
        <br/> 000<br/> ABPZ20 KNHC 301733<br/> TWOEP <br/> <br/> TROPICAL WEATHER OUTLOOK<br/> NWS NATIONAL HURRICANE CENTER MIAMI FL<br/> 1100 AM PDT THU MAY 30 2013<br/> <br/> FOR THE EASTERN NORTH PACIFIC...EAST OF 140 DEGREES WEST LONGITUDE..<br/> <br/> THE NATIONAL HURRICANE CENTER IS ISSUING ADVISORIES ON TROPICAL<br/> DEPRESSION BARBARA...LOCATED NEAR THE GULF COAST OF MEXICO.<br/> <br/> SHOWERS AND THUNDERSTORMS HAVE MOSTLY DISSIPATED IN ASSOCIATION WITH<br/> THE AREA OF LOW PRESSURE LOCATED ABOUT 500 MILES SOUTH OF THE<br/> SOUTHERN TIP OF THE BAJA CALIFORNIA PENINSULA. ENVIRONMENTAL<br/> CONDITIONS DO NOT FAVOR REDEVELOPMENT OF THE LOW AS IT MOVES<br/> NORTHEASTWARD AT ABOUT 10 MPH DURING THE NEXT COUPLE OF DAYS. THIS<br/> SYSTEM HAS A LOW CHANCE...NEAR 0 PERCENT...OF BECOMING A TROPICAL<br/> CYCLONE DURING THE NEXT 48 HOURS.<br/> <br/> ELSEWHERE...TROPICAL CYCLONE FORMATION IS NOT EXPECTED DURING THE<br/> NEXT 48 HOURS.<br/> <br/> $$<br/> FORECASTER LANDSEA<br/> <br/>
      </description>
      <pubDate>Thu, 30 May 2013 17:33:25 GMT</pubDate>
      <link>http://www.nhc.noaa.gov/gtwo_epac.shtml</link>
      <guid>
        http://www.nhc.noaa.gov/gtwo_epac.shtml?201305301733
      </guid>
      <author>nhcwebmaster@noaa.gov (nhcwebmaster)</author>
    </item>
...
```

Keywords: weather, hurricane, typhoon, tropical storm, US government

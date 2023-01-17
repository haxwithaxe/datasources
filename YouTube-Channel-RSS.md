Get an RSS feed of a YouTube channel's video releases.

http://youtube.com

# Docs
Original source of this process https://danielmiessler.com/blog/rss-feed-youtube-channel/

## Steps
1. Find the RSS URL. To find the URL search the channel page source for an `rssUrl` json key in one of the script tag texts (at least right now Jan 2023).
    ```sh
    $ wget -q "https://www.youtube.com/c/Level1Techs" -O - | grep rssUrl | sed 's/.*rssUrl":"\([^"]\+\)".*/\1/'
    https://www.youtube.com/feeds/videos.xml?channel_id=UC4w1YQAJMWOz4qtxinq55LQ
    ```
1. Request the feed with the URL.

# Examples
## Get Level1Techs RSS
Get https://www.youtube.com/@Level1Techs as an RSS feed.

1. Get the channel RSS URL
    ```sh
    $ wget -q "https://www.youtube.com/c/Level1Techs" -O - | grep rssUrl | sed 's/.*rssUrl":"\([^"]\+\)".*/\1/'
    https://www.youtube.com/feeds/videos.xml?channel_id=UC4w1YQAJMWOz4qtxinq55LQ
    ```
1. Request the feed (see below)

### Request
GET `https://www.youtube.com/feeds/videos.xml?channel_id=UC4w1YQAJMWOz4qtxinq55LQ`

### Response
```xml
<feed>
  <link rel="self" href="http://www.youtube.com/feeds/videos.xml?channel_id=UC4w1YQAJMWOz4qtxinq55LQ"/>
  <id>yt:channel:</id>
  <yt:channelId/>
  <title>Level1Techs</title>
  <link rel="alternate" href="https://www.youtube.com/channel/UC4w1YQAJMWOz4qtxinq55LQ"/>
  <author>
  <name>Level1Techs</name>
  <uri>
    https://www.youtube.com/channel/UC4w1YQAJMWOz4qtxinq55LQ
  </uri>
  </author>
  <published>2011-08-22T23:02:54+00:00</published>
  <entry>
    <id>yt:video:AGJFWbqGCoQ</id>
    <yt:videoId>AGJFWbqGCoQ</yt:videoId>
    <yt:channelId>UC4w1YQAJMWOz4qtxinq55LQ</yt:channelId>
    <title>
      The Level1 Show January 17 2023: Selling England By The (Digital) Pound
    </title>
    <link rel="alternate" href="https://www.youtube.com/watch?v=AGJFWbqGCoQ"/>
    <author>
    <name>Level1Techs</name>
    <uri>
      https://www.youtube.com/channel/UC4w1YQAJMWOz4qtxinq55LQ
    </uri>
    </author>
    <published>2023-01-17T05:30:04+00:00</published>
    <updated>2023-01-17T07:51:47+00:00</updated>
    <media:group>
    <media:title>
      The Level1 Show January 17 2023: Selling England By The (Digital) Pound
    </media:title>
    <media:content url="https://www.youtube.com/v/AGJFWbqGCoQ?version=3" type="application/x-shockwave-flash" width="640" height="390"/>
    <media:thumbnail url="https://i2.ytimg.com/vi/AGJFWbqGCoQ/hqdefault.jpg" width="480" height="360"/>
    <media:description>
      https://linode.com/level1techs https://www.one-tab.com/page/pWtRl3BATuSZ9rudBQOjEw 0:00 - Intro 1:32 - FCC's Robocaller Crackdown Brings Stark Warning for Voice Providers 2:47 - The FCC wants carriers to notify you sooner when there's a data breach 3:59 - A corrupt file led to the FAA ground stoppage. It was also found in the backup system 5:39 - A government watchdog spent $15,000 to crack a federal agency’s passwords in minutes 6:41 - DHS, CISA plan AI-based cybersecurity analytics sandbox 7:53 - House GOP to investigate Big Tech's communications with Biden admin 8:20 - U.S. Supreme Court lets Meta's WhatsApp pursue 'Pegasus' spyware suit 10:19 - Ex-Coinbase manager's brother sentenced to 10 months in insider trading case 11:11 - SEC Charges Genesis and Gemini for the Unregistered Offer and Sale of Crypto Asset Securities through the Gemini Earn Lending Program 13:15 - Crypto.com Will Delist Tether in Canada to Comply With Ontario Regulator 14:14 - Gigabit internet is now a legal requirement for new homes in England 15:48 - UK Treasury considers plan for digital pound 16:46 - Apple Faces Rare $8.5M Fine For Illegal Data Harvesting 18:43 - Belarus Legalizes Piracy of Movies, Music & Software of 'Unfriendly' Nations 19:40 - US tech giants say Indian panel’s recommended competition act ‘absolutist and regressive’ 22:28 - Japan Wants Semiconductor Manufacturing Back Home to Frustrate China 23:32 - Iran Says Face Recognition Will ID Women Breaking Hijab Laws 24:49 - Researchers Could Track the GPS Location of All of California’s New Digital License Plates 26:10 - Identity Thieves Bypassed Experian Security to View Credit Reports 28:06 - Guardian confirms it was hit by ransomware attack 28:46 - Hackers hit websites of Danish central bank, other banks 29:05 - New SHC-compiled Linux malware installs cryptominers, DDoS bots 29:44 - San Jose police recover three stolen cars using license-plate recognition and helicopter 30:20 - TPD: Man arrested after being recognized wearing underwear as mask in porch pirate cases 31:26 - Woman sentenced to three years in state prison for collecting $400,000 in viral GoFundMe scam 32:58 - Two men charged with attacks on four power substations in Washington state #level1show ********************************** Check us out online at the following places! https://bio.link/level1techs *IMPORTANT* Any email lacking “level1techs.com” should be ignored and immediately reported to Queries@level1techs.com. ------------------------------------------------------------------------------------------------------------- Intro and Outro Music By: Kevin MacLeod (incompetech.com) Licensed under Creative Commons: By Attribution 3.0 License http://creativecommons.org/licenses/by/3.0/
    </media:description>
    <media:community>
    <media:starRating count="641" average="5.00" min="1" max="5"/>
    <media:statistics views="6421"/>
    </media:community>
    </media:group>
  </entry>
...
```

Keywords: youtube, rss, video

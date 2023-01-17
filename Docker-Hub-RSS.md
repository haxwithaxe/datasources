From the project's README.md:

> RSS feed for Docker Hub images
> Docker Hub doesn't provide notifications for new image releases, so Docker Hub RSS turns image tags into an RSS feed for easy consumption. Subscribe using Slack RSS, Feedly, or any other RSS feed reader to get notified when a new image is published.

It is possible to self host this service.

https://rss.p.theconnman.com and https://github.com/TheConnMan/docker-hub-rss

# Docs
There is a web form at https://rss.p.theconnman.com that can be poked at to get the desired query.

The regex fields are not matching against the whole tag version. Adding `^` to the beginning and `$` to the end to force a match of the whole tag version. For example `^[0-9]` will match `12.1-bullseye`.

# Examples
## Get all tags
Get all the tags for the official Postgres image (`_/postgres`).

### Request
GET `https://rss.p.theconnman.com/_/postgres.atom`

### Response
An atom feed with all tags including latest, latest-dev, alpine, bullseye, major version, and major and minor version entries.

`pubDate` is the publication date of the tag.

```xml
<rss version="2.0">
<channel>
  <title>library/postgres | Docker Hub Images</title>
  <description>
    The PostgreSQL object-relational database system provides reliability and data integrity.
  </description>
  <link>https://hub.docker.com/r/library/postgres</link>
  <generator>RSS for Node</generator>
  <lastBuildDate>Tue, 17 Jan 2023 14:20:46 GMT</lastBuildDate>
  <item>
    <title>library/postgres:latest</title>
    <link>https://hub.docker.com/r/library/postgres/tags?name=latest</link>
    <guid isPermaLink="false">20561-1673528179964</guid>
    <pubDate>Thu, 12 Jan 2023 12:56:19 GMT</pubDate>
  </item>
...
```

## Get major version tags
Get all the major version tags for the official Postgres image (`_/postgres`). For example `postgres:12`, `postgres:13`, `postgres:14`, `postgres:15`. The "Include Regex" field (in the web form) used for this example is `^[0-9]+$`.

### Request
GET `https://rss.p.theconnman.com/_/postgres.atom?includeRegex=%5E%5B0-9%5D%2B%24`

### Response
An atom feed with all tags excluding latest, latest-dev, alpine, bullseye, and major and minor version entries. While including major version only tags such as `12`, `13`, `14`, `15`. 

The feed is the same format as the previous example.

Keywords: RSS, docker, DockerHub

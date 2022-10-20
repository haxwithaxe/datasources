Github has ATOM feeds for various things in repos.

https://github.com

# Docs
No authentication needed.

# Examples
## Commits
Commits are organized by branch.
The URL format is `https://github.com/<username>/<repo>/commits/<branch>.atom`
The example below uses pylint for the project and main as the branch.

### Request
Get https://github.com/PyCQA/pylint/commits/main.atom

### Response
```
<?xml version="1.0" encoding="UTF-8"?>
<feed xmlns="http://www.w3.org/2005/Atom" xmlns:media="http://search.yahoo.com/mrss/" xml:lang="en-US">
  <id>tag:github.com,2008:/PyCQA/pylint/commits/main</id>
  <link type="text/html" rel="alternate" href="https://github.com/PyCQA/pylint/commits/main"/>
  <link type="application/atom+xml" rel="self" href="https://github.com/PyCQA/pylint/commits/main.atom"/>
  <title>Recent Commits to pylint:main</title>
  <updated>2022-10-20T14:35:53Z</updated>
  <entry>
    <id>tag:github.com,2008:Grit::Commit/15dd079792ce8e6b37856450f9e4a928f11b3549</id>
    <link type="text/html" rel="alternate" href="https://github.com/PyCQA/pylint/commit/15dd079792ce8e6b37856450f9e4a928f11b3549"/>
    <title>
        Remove __index__ from unnecessary-dunder-call check (#7650)
    </title>
    <updated>2022-10-20T14:35:53Z</updated>
    <media:thumbnail height="30" width="30" url="https://avatars.githubusercontent.com/u/112832187?s=30&amp;v=4"/>
    <author>
      <name>clavedeluna</name>
      <uri>https://github.com/clavedeluna</uri>
    </author>
    <content type="html">
      &lt;pre style=&#39;white-space:pre-wrap;width:81ex&#39;&gt;Remove __index__ from unnecessary-dunder-call check (#7650)&lt;/pre&gt;
    </content>
  </entry>
...
```

## Tags
This example gets the tags feed for Ansible.

### Request
Get https://github.com/ansible/ansible/tags.atom

### Response
```
<?xml version="1.0" encoding="UTF-8"?>
<feed xmlns="http://www.w3.org/2005/Atom" xmlns:media="http://search.yahoo.com/mrss/" xml:lang="en-US">
  <id>tag:github.com,2008:https://github.com/ansible/ansible/releases</id>
  <link type="text/html" rel="alternate" href="https://github.com/ansible/ansible/releases"/>
  <link type="application/atom+xml" rel="self" href="https://github.com/ansible/ansible/releases.atom"/>
  <title>Tags from ansible</title>
  <updated>2022-10-17T14:11:12-04:00</updated>
  <entry>
    <id>tag:github.com,2008:Repository/3638964/v2.14.0rc1</id>
    <updated>2022-10-17T14:11:12-04:00</updated>
    <link rel="alternate" type="text/html" href="https://github.com/ansible/ansible/releases/tag/v2.14.0rc1"/>
    <title>v2.14.0rc1</title>
    <content></content>
    <author>
      <name>rcarrillocruz</name>
    </author>
    <media:thumbnail height="30" width="30" url="https://avatars.githubusercontent.com/u/1419467?s=60&amp;v=4"/>
  </entry>
...
```

## Releases
This example gets the releases feed for ntfy.sh.

### Request
Get https://github.com/binwiederhier/ntfy/releases.atom

### Response
```
<?xml version="1.0" encoding="UTF-8"?>
<feed xmlns="http://www.w3.org/2005/Atom" xmlns:media="http://search.yahoo.com/mrss/" xml:lang="en-US">
  <id>tag:github.com,2008:https://github.com/binwiederhier/ntfy/releases</id>
  <link type="text/html" rel="alternate" href="https://github.com/binwiederhier/ntfy/releases"/>
  <link type="application/atom+xml" rel="self" href="https://github.com/binwiederhier/ntfy/releases.atom"/>
  <title>Release notes from ntfy</title>
  <updated>2022-09-27T16:50:07Z</updated>
  <entry>
    <id>tag:github.com,2008:Repository/420503947/v1.28.0</id>
    <updated>2022-09-27T17:03:19Z</updated>
    <link rel="alternate" type="text/html" href="https://github.com/binwiederhier/ntfy/releases/tag/v1.28.0"/>
    <title>v1.28.0</title>
    <content type="html">&lt;p&gt;This release primarily adds icon support for the Android app, and adds a display name to subscriptions in the web app. Aside from that, we fixed a few random bugs, most importantly the &lt;code&gt;Priority&lt;/code&gt; header bug that allows the use behind Cloudflare. We also added a ton of documentation. Most prominently, an &lt;a href=&quot;https://ntfy.sh/docs/integrations/&quot; rel=&quot;nofollow&quot;&gt;integrations + projects page&lt;/a&gt;.&lt;/p&gt;
...
```

Keywords: Github, ATOM, RSS

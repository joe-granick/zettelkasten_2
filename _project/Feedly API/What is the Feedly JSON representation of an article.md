---
aliases: []
---
Name: 
Tags: #blog
Topics: 
Author: 
Year: 
Date:
URL: 
Cite: 
[[What_is_the_Feedly_JSON_representation_of_an_article.pdf]]

>[!info]
>When an article is open in the Feedly Web Application, you can press SHIFT+D to see the JSON presentation appear
>


## The core

```JSON
{
// The article id is unique and immutable
// (it won’t change over time) for a given article.
"id": "PSNTZO8gXFUe+cpCZyApw0vEKWPT4b14D6teBEocIAE=_174faa24b8c:18d07f2:2694a93d",
"originId": "https://www.theverge.com/2020/10/5/21503082/slack-down-issues-slow-loading-threads-messages",
// When was the last time the article was recrawled?
"recrawled": 1601945947549,
// What is the language associated with this article
"language": "en",
// content.content or summary.content capture the html content (full or snippet)
// shared by the publisher in the RSS/ATOM feed
"content": { "content": "html representation of the article", "direction": "ltr" },
// What is the title of this article
"title": "Slack experienced performance issues for more than six hours",
// When was this article crawled/fetched by feedly for the first time?
"crawled": 1601932774284,
// Who is the author of the article?
"author": "Bijan Stephen",
// information about the source/origin publishing the RSS feed
"origin": {
"streamId": "feed/http://www.theverge.com/rss/full.xml",
"title": "The Verge",
"htmlUrl": "https://www.theverge.com/"
},
// alternate.href is the URL of the article shared by the publisher
"alternate": [{
"href": "https://www.theverge.com/2020/10/5/21503082/slack-down-issues-slow-loading-threads-messages",
"type": "text/html"
}],
// Updated date provided by the publisher
"updated": 1601932198000,
// Published date provided by the publisher
"published": 1601932198000,
// If available, the canonicalUrl of the article. The alternate might be a non canonical URL
"canonicalUrl": "https://www.theverge.com/2020/10/5/21503082/slack-down-issues-slow-loading-threads-messages"
}

```

## HTML Content

## Article URL

## Featured Visual

## Folders, Boards, Leo Web Alerts, and Leo Priorities

## Read/Unread Status

## Notes and Highlights

## Leo Named Entities

## Leo Topics

## Leo Business Events

## Leo Threat Actors

## Leo Malware Families

## Leo Cyber Attacks

## Leo CVE Information

## Leo IoC Information

## Leo MITRE ATT&CK TTPs

## Leo Custom Topics

## Leo Summary Sentences

## Leo Deduplication

## Leo Clustering

## Leo Company Lists

## Engagement/Social Sharing

## Linked Entries

## Twitter/Reddit Author Details

## Search Terms




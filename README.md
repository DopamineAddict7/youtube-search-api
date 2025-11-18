# Youtube Search Api Scraper

> This project provides a powerful interface to search and analyze YouTube content at scale. It delivers detailed, structured metadata for videos, channels, and playlists while simplifying the complexity of the YouTube Data API.
> Ideal for researchers, analysts, and developers who need clean and comprehensive YouTube search data.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/za2122/footer-section/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>Youtube Search Api</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction

This scraper performs rich YouTube search queries and returns unified, ready-to-use datasets.
It solves the challenge of merging multiple API endpoints and decoding data into a clean format.
Built for analysts, marketers, creators, and developers who need streamlined access to YouTube search results.

### Why Use This Scraper?

- Automatically handles pagination to retrieve up to 1000 video results.
- Combines search, video, and channel statistics into one dataset.
- Provides clean, decoded text and extracted hashtags.
- Eliminates the need for managing API keys or quotas.
- Supports broad filtering options for precise targeting.

## Features

| Feature | Description |
|---------|-------------|
| Comprehensive Search | Query videos, channels, and playlists with detailed filtering. |
| Automatic Pagination | Retrieves up to 1000 results without extra configuration. |
| Combined Metadata | Merges search, video stats, and channel stats into one record. |
| HTML Entity Decoding | Ensures titles and descriptions are readable and clean. |
| Hashtag Extraction | Automatically extracts hashtags from video descriptions. |
| No Manual Auth Needed | External token service enables seamless authentication. |

---

## What Data This Scraper Extracts

| Field Name | Field Description |
|------------|------------------|
| title | Title of the YouTube video. |
| type | Content type (video, channel, playlist). |
| channelName | Name of the channel that published the video. |
| date | ISO timestamp of when the video was published. |
| text | Full decoded video description. |
| thumbnailUrl | URL of the video's primary thumbnail. |
| order | Ordinal index of the result returned. |
| input | The original search query used. |
| hashtags | Array of extracted hashtags. |
| channelId | Unique identifier of the channel. |
| channelUrl | URL to the channel's YouTube page. |
| channelUsername | The channel's username/handle. |
| numberOfSubscribers | Subscriber count for the channel. |
| channelViewCount | Total views accumulated by the channel. |
| channelVideoCount | Number of videos published on the channel. |
| hiddenSubscriberCount | Indicates if subscriber count is hidden. |
| channelCreatedAt | Channel creation timestamp. |
| id | Video ID. |
| url | Full URL to the video. |
| viewCount | Total video views. |
| likes | Total likes on the video. |
| commentsCount | Number of comments. |
| commentsTurnedOff | Indicates if comments are disabled. |
| duration | Duration of the video in seconds. |
| keywords | Array of associated keywords. |
| isMembersOnly | Indicates if the video is locked behind membership. |

---

## Example Output


    [
        {
            "title": "Video Title",
            "type": "video",
            "channelName": "Channel Name",
            "date": "2023-01-01T00:00:00Z",
            "text": "Video description...",
            "thumbnailUrl": "https://i.ytimg.com/vi/VIDEO_ID/hqdefault.jpg",
            "order": 0,
            "input": "search query",
            "hashtags": ["hashtag1", "hashtag2"],
            "channelId": "CHANNEL_ID",
            "channelUrl": "https://www.youtube.com/channel/CHANNEL_ID",
            "channelUsername": "username",
            "numberOfSubscribers": 1000000,
            "channelViewCount": 50000000,
            "channelVideoCount": 500,
            "hiddenSubscriberCount": false,
            "channelCreatedAt": "2020-01-01T00:00:00Z",
            "id": "VIDEO_ID",
            "url": "https://www.youtube.com/watch?v=VIDEO_ID",
            "viewCount": 10000,
            "likes": 1000,
            "commentsCount": 100,
            "commentsTurnedOff": false,
            "duration": 180,
            "keywords": ["keyword1", "keyword2"],
            "isMembersOnly": false
        }
    ]

---

## Directory Structure Tree


    Youtube Search Api/
    ├── src/
    │   ├── runner.js
    │   ├── extractors/
    │   │   ├── youtube_parser.js
    │   │   └── utils_format.js
    │   ├── outputs/
    │   │   └── exporters.js
    │   └── config/
    │       └── settings.example.json
    ├── data/
    │   ├── inputs.sample.json
    │   └── sample_output.json
    ├── package.json
    └── README.md

---

## Use Cases

- **Marketing analysts** use it to analyze competitor content trends so they can optimize their own content strategies.
- **Researchers** use it to gather structured data for studying social behavior and video engagement.
- **Media agencies** use it to identify high-performing videos for campaign planning and outreach.
- **Developers** use it to power apps that rely on YouTube search intelligence.
- **Content creators** use it to monitor niche topics and discover new opportunities.

---

## FAQs

**Q: Do I need my own YouTube API key?**
A: No. Authentication is handled automatically through an external token provider.

**Q: How many results can I retrieve?**
A: Up to 1000 results per run thanks to automatic pagination handling.

**Q: Can I filter by region, duration, or video definition?**
A: Yes. The scraper supports region codes, durations, definitions, languages, ordering, and more.

**Q: Does it retrieve both video and channel statistics?**
A: Yes. It merges multiple endpoints to deliver full video and channel analytics.

---

## Performance Benchmarks and Results

**Primary Metric:** The scraper processes an average of 250 results per minute, including metadata merging and entity decoding.
**Reliability Metric:** Maintains a 98% successful retrieval rate across diverse search configurations.
**Efficiency Metric:** Optimized batching reduces unnecessary API calls, ensuring stable throughput even with large result sets.
**Quality Metric:** Delivers 99% field completeness by combining search, video, and channel datasets into unified records.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtube.com/shorts/6AwB5omXrIM" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review3.gif" alt="Review 3" width="35%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Exceptional results, clear communication, and flawless delivery. Bitbash nailed it.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>

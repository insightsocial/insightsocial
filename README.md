# InsightSocial — Multi-platform social media scraper

> One-click data export from Instagram, TikTok, Facebook, LinkedIn, X (Twitter), Threads,
> YouTube, Reddit and Pinterest. Runs as a Chrome extension. No code required.

[**Install from Chrome Web Store →**](https://chromewebstore.google.com/detail/insight-social-ai-web-dat/cddgiejchlkeedmhjeodlcjdiddlcdld)
&nbsp;·&nbsp; [Website](https://www.insightsocial.app)
&nbsp;·&nbsp; [Use cases](https://www.insightsocial.app/use-cases)
&nbsp;·&nbsp; [What's new](https://www.insightsocial.app/whats-new)

![Instagram hashtag results in the InsightSocial web portal — 500 creators with contact info, follower counts, engagement rate, and bio fields](screenshots/instagram-result-page.png)

*Example: scraping `#fitness` on Instagram. 500 creator profiles with contact info, engagement rates, and bios — exportable to CSV in one click.*

---

## What it does

InsightSocial scrapes the social platforms you're already logged into — directly from your browser — and exports the results to CSV or JSON. There is no third-party server between you and the platform, your password and cookies are never shared with us, and there's nothing to configure beyond installing the extension. Rows sync to your own account as a run progresses so results are waiting in the web portal.

### Supported platforms & sources

| Platform | Sources |
|---|---|
| **Instagram** | Hashtag · Profile · Single Post · Home Feed · Explore · Followers list · Following list |
| **TikTok** | Single Video · Profile · Hashtag · Search · For You |
| **Facebook** | Group · Page · Profile · Home Feed · Search Results · Single Post · Followers · Following |
| **LinkedIn** | Home Feed · Company · Profile · Single Post · People search |
| **X (Twitter)** | Home Feed · Profile · Search · Hashtag · Explore · Single Post · Followers list · Following list · List · Community |
| **Threads** | Home Feed · Profile · Single Post · Search |
| **YouTube** | Video · Shorts |
| **Reddit** | Single Post · Search Results |
| **Pinterest** | Search Results |

## How it works

1. **Install** the extension from the Chrome Web Store.
2. **Open** a supported page (e.g. an Instagram hashtag, a Facebook group, a TikTok profile).
3. **Click the InsightSocial side panel** and pick what to scrape. The extension scrolls + collects in the background.
4. **Export** to CSV or JSON, or view results in the [web portal](https://www.insightsocial.app/portal/history).

### See it in action

<table>
  <tr>
    <td align="center" width="33%">
      <img src="screenshots/instagram-hashtag.png" alt="InsightSocial side panel detecting an Instagram hashtag and showing scrape configuration" /><br/>
      <sub><b>1. Detect & configure</b><br/>Side panel auto-detects the page type and shows what's scrapeable.</sub>
    </td>
    <td align="center" width="33%">
      <img src="screenshots/instagram-scraping.png" alt="Live progress: scraping profile 7 of 100 from #fitness hashtag" /><br/>
      <sub><b>2. Scrape live</b><br/>Real-time progress, ETA, and a queue of what's being collected.</sub>
    </td>
    <td align="center" width="33%">
      <img src="screenshots/instagram-result-screen.png" alt="Scrape complete: 500 posts, 500 authors, 30.5K likes from #fitness" /><br/>
      <sub><b>3. Done</b><br/>Summary stats, then jump to the full results table.</sub>
    </td>
  </tr>
</table>

## Use cases

- **[Audience research](https://www.insightsocial.app/use-cases/audience-research)** — pull followers from Instagram profiles, engaged audiences from LinkedIn company pages, creators behind a hashtag.
- **[Competitor analysis](https://www.insightsocial.app/use-cases/competitor-analysis)** — track what competitor accounts post, who engages, what hashtags they ride.
- **[Content research](https://www.insightsocial.app/use-cases/content-research)** — pull top-performing TikToks for a hashtag, viral X threads, Instagram hashtag feeds.

## FAQ

**Is this safe for my account?**
The extension runs inside your normal browser session and mimics human scrolling. There are no third-party servers between you and the platform. That said, all scraping carries some risk — use a secondary account if you're doing high volume.

**How do I export data?**
After a scrape session completes, click **Export** in the side panel. CSV and JSON are both supported, with per-platform column sets.

**Do scheduled scrapes work when my browser is closed?**
No — schedules run via Chrome alarms, which require the browser to be open. We're upfront about this; nobody else's "scheduled scraper" works closed either, they just don't tell you.

**Where is my data stored?**
Rows are buffered in your browser (IndexedDB) and synced to your own account as a run progresses, so you can pick them up in the web portal or export straight from the side panel. Synced data is readable only by your account.

**Is there an API?**
Not yet a public/programmatic API — talk to us if you need that.

## Roadmap

- More platforms — ongoing (YouTube, Reddit and Pinterest have shipped)
- Public API + Zapier integration — exploring
- Bulk export from saved sessions — in progress

[See the public changelog →](https://www.insightsocial.app/whats-new)

## Support

- Email: **insightsocial.xyz@gmail.com**
- Web portal: **https://www.insightsocial.app/portal/history**

## About

InsightSocial is built by independent makers shipping in public. Follow along:
- Twitter/X: [@dovy_dev](https://x.com/dovy_dev)
- Blog: [insightsocial.app/blog](https://www.insightsocial.app/blog)

---

*InsightSocial is not affiliated with Meta, ByteDance, X Corp, Microsoft, Google, Reddit or Pinterest. All platform names are trademarks of their respective owners.*

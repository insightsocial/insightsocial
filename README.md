# InsightSocial — Multi-platform social media scraper

> One-click data export from Instagram, TikTok, Facebook, LinkedIn, X (Twitter), Threads,
> YouTube, Reddit and Pinterest. Runs as a Chrome extension. No code required.

[**Install from Chrome Web Store →**](https://chromewebstore.google.com/detail/insight-social-ai-web-dat/cddgiejchlkeedmhjeodlcjdiddlcdld)
&nbsp;·&nbsp; [Website](https://www.insightsocial.app)
&nbsp;·&nbsp; [Use cases](https://www.insightsocial.app/use-cases)
&nbsp;·&nbsp; [What's new](https://www.insightsocial.app/whats-new)

<sub>**Last verified: 2026-08-31 · extension v4.0.3.** Full capability matrix, plan
limits and known-stale claims: **[FACTS.md](FACTS.md)**.</sub>

![Instagram hashtag results in the InsightSocial web portal — 500 creators with contact info, follower counts, engagement rate, and bio fields](screenshots/instagram-result-page.png)

*Example: scraping `#fitness` on Instagram. 500 creator profiles with contact info, engagement rates, and bios — exportable to CSV in one click.*

---

## What it does

InsightSocial scrapes the social platforms you're already logged into — directly from your browser — then hands you the results as a spreadsheet. The scraping never routes through a third-party server, your password and cookies are never shared with us, and there's nothing to configure beyond installing the extension. Rows sync to your own account as a run progresses, so results are already waiting in the web portal when it finishes.

### Supported platforms & sources

9 platforms, 48 sources. A "source" is a page type the extension recognizes.

| Platform | Sources |
|---|---|
| **Instagram** | Hashtag · Profile · Single Post · Home Feed · Explore · Audio · Reels feed · Profile Reels · Followers list · Following list |
| **Facebook** | Home Feed · Search Results · Single Post · Group · Group Search · Profile · Page · Followers · Following · Reels |
| **X (Twitter)** | Home Feed · Explore · Single Post · Profile · Followers list · Following list · Search · Hashtag · List · Community |
| **LinkedIn** | Home Feed · Profile · Company · Single Post |
| **Threads** | Home Feed · Profile · Single Post · Search |
| **TikTok** | Single Video · Profile · Hashtag · Search |
| **Reddit** | Single Post · Search Results · Subreddit |
| **YouTube** | Video · Shorts |
| **Pinterest** | Search Results |

What each one actually captures — and what it deliberately doesn't — is in
[FACTS.md](FACTS.md).

## How it works

1. **Install** the extension from the Chrome Web Store and sign in with Google.
2. **Open** a supported page (e.g. an Instagram hashtag, a Facebook group, a TikTok profile).
3. **Click the InsightSocial side panel** and pick what to scrape. The extension scrolls + collects in the background, syncing rows to your account as it goes.
4. **Open the [web portal](https://www.insightsocial.app/portal/history)** to filter the results and export them — Google Sheets, CSV, Excel or JSON.

Export happens in the portal, not the side panel. The extension collects; the portal
stores and exports.

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

## Pricing

Scraping and browsing your results are unlimited on every plan. The only thing
metered is **rows you export** — 1 credit per row, reset monthly.

| | Free | Pro |
|---|---|---|
| **Price** | $0 forever | **$9.99/mo**, or **$7.99/mo** billed yearly ($95.88/yr) |
| Exported rows / month | 500 | 10,000 |
| Scraping + dashboard | Unlimited | Unlimited |
| Platforms | All 9 | All 9 |
| Formats | Sheets · CSV · Excel · JSON | Sheets · CSV · Excel · JSON |
| Scheduled scrapes | Yes | Yes |
| Data history | 30 days | 3 years |
| Ask AI · DM openers · contact enrichment | — | Yes |

Need rows once rather than monthly? A one-time pack of **2,000 credits is $9**, and
it never expires. No credit card for the free plan.

[Full pricing →](https://www.insightsocial.app/pricing)

## FAQ

**Is this safe for my account?**
The extension runs inside your normal browser session and mimics human scrolling. Nothing sits between you and the platform — no cloud worker signs in as you, and we never receive your password or cookies. Collected rows do sync to your own account so you can use the portal, and contact enrichment (Pro) visits bio-link pages server-side; neither one touches the platform on your behalf. That said, all scraping carries some risk — use a secondary account if you're doing high volume.

**How do I export data?**
Open the [web portal](https://www.insightsocial.app/portal/history), pick a session, and export — Google Sheets, CSV, Excel (.xlsx) or JSON, with per-platform column sets. All four formats work on the free plan. The side panel doesn't produce files; it shows your remaining credits and links through.

**What counts against my limit?**
Only exported rows. You can scrape as much as you want and read all of it in the dashboard for free — the meter moves when you take rows out.

**Do scheduled scrapes work when my browser is closed?**
No — schedules run via Chrome alarms, which need Chrome running with a visible window. We're upfront about this; nobody else's "scheduled scraper" works closed either, they just don't tell you.

**Where is my data stored?**
Rows are buffered in your browser (IndexedDB) and synced to your own account as a run progresses, so they're waiting for you in the web portal. Synced data is readable only by your account, and is kept 30 days on Free, 3 years on Pro.

**What can't it do?**
Private accounts you don't follow, anything behind a login you don't have, Instagram Stories and DMs, LinkedIn search, TikTok's For You feed, YouTube channels (comments only), Pinterest boards and pins. The full list is in [FACTS.md](FACTS.md).

**Is there an API?**
No public or programmatic API — talk to us if you need that.

**Which browsers?**
Chrome and Chromium-based browsers, version 114+. No Firefox or Safari build.

## Roadmap

- More platforms and more sources per platform — ongoing
- Public API + Zapier integration — exploring, nothing shipped
- Deeper contact enrichment — in progress

[See the public changelog →](https://www.insightsocial.app/whats-new)

## Support

- Email: **support@insightsocial.app**
- Web portal: **https://www.insightsocial.app/portal/history**

## About

InsightSocial is built by independent makers shipping in public. Follow along:
- Twitter/X: [@dovy_dev](https://x.com/dovy_dev)
- Blog: [insightsocial.app/blog](https://www.insightsocial.app/blog)

---

*InsightSocial is not affiliated with Meta, ByteDance, X Corp, Microsoft, Google, Reddit or Pinterest. All platform names are trademarks of their respective owners.*

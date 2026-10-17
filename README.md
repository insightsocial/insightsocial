# InsightSocial — social media data API, MCP server and Chrome extension

> Public social media data two ways, on one credit balance. A
> [REST API](https://www.insightsocial.app/social-media-api) and
> [hosted MCP server](https://www.insightsocial.app/mcp) return profiles, posts, comments,
> followers and search from 25 platforms (Instagram, TikTok, LinkedIn, Facebook, X, YouTube,
> Reddit, Threads, Pinterest, Bluesky, Telegram, Twitch and more) for scripts and AI agents.
> A free Chrome extension exports the same kinds of data from 9 of them to Excel, no code
> required.

[**Install from Chrome Web Store →**](https://chromewebstore.google.com/detail/insightsocial-free-social/cddgiejchlkeedmhjeodlcjdiddlcdld)
&nbsp;·&nbsp; [Website](https://www.insightsocial.app)
&nbsp;·&nbsp; [Use cases](https://www.insightsocial.app/use-cases)
&nbsp;·&nbsp; [API docs](https://www.insightsocial.app/docs)
&nbsp;·&nbsp; [What's new](https://www.insightsocial.app/whats-new)

<sub>**Last verified: extension 2026-10-17 (v4.6.1 on the Chrome Web Store; v4.7.0 additions marked "from v4.7.0") · API 2026-10-14.** Full capability matrix, plan
limits and known-stale claims: **[FACTS.md](FACTS.md)**.</sub>

![Instagram hashtag results in the InsightSocial web portal — 500 creators with contact info, follower counts, engagement rate, and bio fields](screenshots/instagram-result-page.png)

*Example: scraping `#fitness` on Instagram. 500 creator profiles with contact info, engagement rates, and bios — exportable to CSV in one click.*

---

## What it does

InsightSocial scrapes the social platforms you're already logged into — directly from your browser — then hands you the results as a spreadsheet. The scraping never routes through a third-party server, your password and cookies are never shared with us, and there's nothing to configure beyond installing the extension. Rows sync to your own account as a run progresses, so results are already waiting in the web portal when it finishes.

### Supported platforms & sources

9 social platforms. A "source" is a page type the extension recognizes.

| Platform | Sources |
|---|---|
| **Instagram** | Hashtag · Profile · Single Post · Home Feed · Explore · Audio · Reels feed · Profile Reels · Followers list · Following list |
| **Facebook** | Home Feed · Search Results · Single Post · Group · Group Search · Profile · Page · Followers · Following · Reels |
| **X (Twitter)** | Home Feed · Explore · Single Post · Profile · Followers list · Following list · Your Likes · Search · Hashtag · List · Community |
| **LinkedIn** | Home Feed · Profile · Company · Single Post |
| **Threads** | Home Feed · Profile · Single Post · Search |
| **TikTok** | Single Video · Profile · Hashtag · Search |
| **Reddit** | Single Post · Search Results · Subreddit · User Profile comments (from v4.7.0) |
| **YouTube** | Video · Shorts · Channel (Videos or Shorts tab) · Search Results · Home Feed |
| **Pinterest** | Search Results |

Runs keep going when you switch to another tab or app (since v4.5.0). A few pages
still need their tab in front, such as X search and hashtags, and the side panel says
so before you start.

### Review and discussion sites (from v4.7.0)

Extension v4.7.0 adds ten review and discussion sites. Version 4.6.1, the build on the
Chrome Web Store until 4.7.0 clears review, cannot read them; installed extensions
update themselves once it is published.

| Site | What a run collects |
|---|---|
| **Trustpilot** | A company's reviews, with stars, dates, verified flags and the company's replies |
| **Google Maps** | A place's reviews and the owner's replies (sign in to Google first; keep the tab in front) |
| **Amazon** | A product's reviews on Amazon's storefronts (sign in to Amazon to see more than the few shown signed out) |
| **Etsy** | Reviews of a listing or a whole shop, with the seller's replies |
| **Steam** | A game's reviews, newest first, recommended or not |
| **Product Hunt** | A product's reviews and a launch's comments |
| **Hacker News** | A whole comment thread, however deep |
| **Quora** | The answers to a question, with their comments |
| **Blind** | The comments on a post |
| **Notion** | Public Notion pages and databases |

One page per run. Each site asks Chrome for access the first time you use it; nothing
extra is requested at install. Rows export from the same portal, in the same four
formats. Overview: [insightsocial.app/scraper/reviews](https://www.insightsocial.app/scraper/reviews).

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

Scraping and browsing your results are unlimited on every plan. In the extension the
only thing metered is **rows you export** — 1 credit per row, reset monthly. API calls
draw on the same balance, priced per endpoint.

| | Free | Pro | Studio |
|---|---|---|---|
| **Price** | $0 forever | **$9.99/mo**, or **$7.99/mo** billed yearly ($95.88/yr) | **$49/mo** |
| Credits / month (exports + API) | 500 | 10,000 | 150,000 for exports; API calls use the first 10,000, as on Pro |
| Scraping + dashboard | Unlimited | Unlimited | Unlimited |
| Platforms | All 9 | All 9 | All 9 |
| Formats | Sheets · CSV · Excel · JSON | Sheets · CSV · Excel · JSON | Sheets · CSV · Excel · JSON |
| Scheduled scrapes | Yes | Yes | Yes |
| Data history | 30 days | 3 years | Same as Pro |
| Ask AI · DM openers · contact enrichment | — | Yes | Yes |

Need rows once rather than monthly? One-time credit packs run from **250 for $2** to
**25,000 for $39**, and they never expire. No credit card for the free plan.

[Full pricing →](https://www.insightsocial.app/pricing)

## FAQ

**Is this safe for my account?**
The extension runs inside your normal browser session and mimics human scrolling. Nothing sits between you and the platform — no cloud worker signs in as you, and we never receive your password or cookies. Collected rows do sync to your own account so you can use the portal, and contact enrichment (Pro) visits bio-link pages server-side; neither one touches the platform on your behalf. That said, all scraping carries some risk — use a secondary account if you're doing high volume.

**How do I export data?**
Open the [web portal](https://www.insightsocial.app/portal/history), pick a session, and export — Google Sheets, CSV, Excel (.xlsx) or JSON, with per-platform column sets. All four formats work on the free plan. The side panel doesn't produce files; it shows your remaining credits and links through.

**What counts against my limit?**
Only exported rows. You can scrape as much as you want and read all of it in the dashboard for free — the meter moves when you take rows out.

**Do scheduled scrapes work when my browser is closed?**
No. Schedules fire from Chrome itself (Chrome alarms), so Chrome has to be running; a turn missed by more than an hour while the browser was closed is skipped rather than run late. A run that starts in a background window keeps going on every social platform (since v4.5.0).

**Where is my data stored?**
Rows are buffered in your browser (IndexedDB) and synced to your own account as a run progresses, so they're waiting for you in the web portal. Synced data is readable only by your account, and is kept 30 days on Free, 3 years on Pro.

**What can't it do?**
Private accounts you don't follow, anything behind a login you don't have, Instagram Stories and DMs, LinkedIn search, TikTok's For You feed, Pinterest profiles, boards and single pins (Pinterest works from search results), and bulk lists of URLs in one run. YouTube channels, searches and the home feed have been supported since v4.6.0. The full list is in [FACTS.md](FACTS.md).

**Is there an API?**
Yes, since 2026-09-22. `https://api.insightsocial.app/v1` returns public data from 25
platforms as JSON (300+ endpoints), authenticated with an `x-api-key` header and paid from the same
credit balance. Failed calls and empty results are free. Start with the
[Quickstart](https://www.insightsocial.app/docs/quickstart), or set up a coding agent
with `npx -y insightsocial init` ([CLI + MCP server](https://github.com/insightsocial/cli)).
Claude, ChatGPT and other AI apps can connect to the hosted MCP server at
`https://api.insightsocial.app/mcp` with one URL and a sign-in ([setup](https://www.insightsocial.app/mcp)).
API facts are in [FACTS.md](FACTS.md#api).

**Which browsers?**
Chrome and Chromium-based browsers, version 114+. No Firefox or Safari build.

## Roadmap

- More platforms and more sources per platform — ongoing
- Zapier integration — exploring, nothing shipped
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

*InsightSocial is not affiliated with Meta, ByteDance, X Corp, Microsoft, Google, Reddit or Pinterest, or with any review or discussion site it reads. All platform and site names are trademarks of their respective owners.*

# cl-6.sherpa: first cold read, 26 November 2026 (2026-11-26T06:19Z)

Live site https://promptugal.news at v0.1.2294 and v0.1.2295. Chromium, phone 390 x 844 (iPhone user agent) and desktop 1366 x 800. 12 pages on each, measured by script (status, first heading, phone screens, sideways overflow, broken images, console errors); three phone screenshots looked at by me (in shots/). Compared with my last read, 16 Nov (history/board/team/sherpa/review-2026-11-16-1930-restart-cold-read.md, R1 to R8). This is my reading, not research with real readers. The owner of each fix is named by role; I have no inbox yet, so the conductor routes.

**Not checked:** the iOS app itself (I have no build), the 33 other place pages, the desktop screenshots by eye, the vaults. No sideways overflow, no broken images and no console errors anywhere except the expected 404.

| # | Finding (rank 1 first) | Owner |
|---|---|---|
| S1 | **/contribute/ is still the Summit page, ten days on (was R1, R2).** It says "starting with Web Summit Lisbon, 10 to 12 November 2026", its seven tasks are summit tasks ("Write up a session you saw"), and rule 7 says "No payment, for now". A local journalist or editor finds nothing for their town, and the page tells a partner the opposite of "paid from day one". | journalist (words), accountant (the money line), dev.places (place picker) |
| S2 | **/values/ is still a 404 (was R3).** Nothing on the site says "not replacing journalism". | journalist (draft); I test it on a first phone screen |
| S3 | **The web app (/app/) is the summit app and opens on an empty last day.** On phone it opens on Fri 13 with only a notice and a "Get the app first" button; on desktop the header still says "Web Summit Lisbon, 9 to 12 November". The newly approved iOS app is the local news app: the reader who follows "App" from the home meets the old product. Needs a decision on what /app/ is now. | conductor (decision), dev, designer |
| S4 | **Place pages are longer than in the last read (R6 worse):** /algarve/faro/ 40.5 phone screens (27.6 on 16 Nov), /algarve/ 34.1 (29.2), /portugal/ 28.3. The first phone screen is the mandate sentence and share buttons, no local news or live data. | designer, dev.places |
| S5 | **A Faro page dated today shows "Live · updated 2026-11-21"**, five days old, beside "site identity site.faro-promptugal" (R7, still there). A reader reads the date as the page being stale, and the identity string means nothing to them. | place agent (Faro), designer |
| S6 | **Home: the visible headline and the page's first heading differ (new).** The reader sees "PrompTugal.news goes local: an AI agent for every Algarve town"; the h1 in the page is "Portugal's tech investment is set to enter Europe's top ten" and is 0 px tall. Screen readers, search engines and anything that reads the h1 get a different story. | dev, correspondent |
| S7 | **Home: the first story is still the agents' own announcement (was R5).** Written by "the conductor, an AI agent": the reader meets the machinery before any local news. The "Now in the Algarve" line below it is a flights-and-weather item. 12.7 phone screens. | correspondent |
| S8 | **The data and feed describe the old product.** /api/v1/ says "The Web Summit 2026 newsroom's data as JSON" and lists 0 people while 115 companies and 34 events are listed; the iOS app reads this. Also feed.xml items carry a pubDate of Thu 26 Nov 09:00 GMT, three hours after this read (06:1x UTC): check whether that is a scheduled time or a wrong one. The articles API is current (102 items, newest 26 Nov). | dev, ontologist |
| S9 | **Three taglines on one visit (R4, partly open):** "Portugal town by town" in the title, "People and AI agents, reporting together" in the page header (seen on /contribute/). Dinis chose "Portugal's news, town by town" on 16 Nov. | designer, dev |

## Keep
- The home phone first screen: brand, one headline, one story, one button (12.7 phone screens, against 61 in the first weeks).
- Articles (7.5 phone screens), People (4.1) and Companies (10.0) are short enough on a phone; the 404 page is clear and on brand.

## Next
Re-measure after each fix. I will test /values/ and the new /contribute/ on a first phone screen as soon as they exist, and read the iOS app's feed once I know where it is published.

## Addendum (2026-11-26T06:21Z): what the iOS app reads
From the conductor's brief (https://github.com/PrompTugal/PrompTugal__Agent__Conductor/blob/dev/board/briefs/2026-11-26-ios-app.md, section 1) I fetched the app's feeds at v0.1.2295. Reachable: api/v1/index.json, places.json, live/agenda.json, live/videos.json (all 200); the startups feed reports v0.1.87 built 2026-11-26T02:42Z. **S10:** api/v1/by-place/faro.json, which the app's "my places" view would read, says "updated": "2026-11-21", the same stale date as the Faro page (S5), so the app inherits it until dev's sync from the homes ships. api/v1/search.json is a 404 (the brief lists search as 1,198 files under another path; not checked). Next wake: re-read by-place/ for three towns and the date each carries.

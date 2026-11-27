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

## Re-measure at the 09:27 wake, read at 2026-11-26T11:16Z (site v0.1.2306; was v0.1.2294)
| # | Now |
|---|---|
| S1 | **Open, unchanged.** /contribute/ still says "starting with Web Summit Lisbon, 10 to 12 November" and "No payment, for now." The money line is settled for now (Dinis's decision); the Summit wording and the missing place picker are not. |
| S2 | **Open.** /values/ is still a 404 (phone and desktop). |
| S3 | **Open.** /app/ unchanged (opens on the last summit day with only the notice); waits on the conductor's decision. |
| S4 | **Open, unchanged.** Phone screens: Faro 40.8 (40.5), Algarve 34.4 (34.1), Portugal 28.6 (28.3). |
| S5 | **Done.** Faro now says "Live · updated 2026-11-26"; api/v1/by-place/faro.json says 2026-11-26. The "site identity site.faro-promptugal" string is still on the page (the renderer's, with the designer). |
| S6, S7 | **Done.** The home's visible headline and its h1 are now the same story ("Portugal's tech investment is set to enter Europe's top ten"), the kicker reads "PORTUGAL, TOWN BY TOWN", and the home is 11.5 phone screens (12.7). I did not weigh whether this lead is a better first story than the old one; that is the correspondent's call. |
| S8 | **Partly done.** The API's about line now reads "The data behind PrompTugal.news as JSON: Portugal's news, town by town ..." Still 0 people (by rule, withheld; I have not seen the withheld flag the ontologist proposed). feed.xml items still say pubDate 09:00 GMT, which has now passed, so it looks like a scheduled time, not an error. |
| S9 | Not re-checked this wake. |
| S10 | **Done** (see S5). |

No console errors, no sideways overflow on the pages measured. Not checked: the iOS app, the other place pages, the section sites.

## Re-measure at the 20:27 wake (site v0.1.2343; read 2026-11-26T20:29Z)
| # | Now |
|---|---|
| S1 | **Open, unchanged.** /contribute/ still says "starting with Web Summit Lisbon, 10 to 12 November" and "No payment, for now." (8.6 phone screens). |
| S2 | **Open.** /values/ is still a 404. |
| S3 | **Done in part.** /app/ is now "The PrompTugal.news app": says the iOS app is approved, has no public link yet, lists what it reads (index, articles, places, live agenda and videos, translations, newsletter), says a count of nought is "held back", not "none exist", and keeps the summit programme app as an archive. 4.6 phone screens. Not checked: its links, and whether "the Web Summit app" archive link works. |
| S4 | **Open, unchanged.** Faro 41.0, Algarve 34.3, Portugal 28.7 phone screens. |
| S5, S6, S7, S10 | **Still done.** Faro "updated 2026-11-26" on the page and in by-place/faro.json and loule.json; the home leads with the Portugal investment story, 11.6 phone screens. |
| S8 | As at 11:14: 0 people (by rule, now explained on /app/ and, per the page, in the index). |
| N1 (new) | **The phone masthead is two button rows and a "£4.98" chip.** The headline now starts about 100 px lower than at 06:20 (about y 310, was 215); the chip is a bare amount with no word, which a cold reader reads as a bill (it read "£4.97" an hour earlier; I do not know what it counts). cl-6.dev has a commit on the chip's label already; I have not re-read it after that. "Follow" is also new and untested. Owner: dev. |
| N2 (new) | **The home's byline reads "the 6.journalist desk, an AI agent".** "6.journalist" is an internal account prefix, not a name a reader knows. Owner: journalist. |

No console errors and no sideways overflow on the pages measured (home, place pages, contribute, values, app, articles, people). Not checked: S9, the iOS app itself, other place pages, the section sites.

## Re-measure at the 27 Nov 09:27 wake (site v0.1.2382; read 2026-11-27T09:28Z)
| # | Now |
|---|---|
| S4 | **Much better, done in part.** Phone screens: Faro 14.8 (41.0), Algarve 18.5 (34.3), Portugal 21.0 (28.7). Not checked: whether the first phone screen now carries local news. |
| N1 | **Done at 390 px.** One tools row (Search and the "Credit £4.99" chip); the headline starts near y 253 (312 at 20:27, 215 at 06:20). At 320 px see N3. |
| N2 | **Done.** The byline reads "the journalist, an AI agent, for Dinis Cruz". |
| N3 (new) | **At 320 px the home scrolls sideways by 32 px** (document 352 px wide in a 320 px window; the section strip's Startups, Travel and Events items run past the edge). No overflow at 390 px, and /algarve/faro/ is clean at 320. Owner: designer (who said they would check 320 and 375). |
| S1 | **Open.** /contribute/ still says "starting with Web Summit Lisbon, 10 to 12 November" and "No payment, for now."; no place picker yet (waits on dev and on Dinis for the content write). |
| S2 | **Open.** /values/ is still a 404. |
| S3, S5, S6, S7, S10 | Still done. Home is 10.6 phone screens. |

No console errors and no broken images on the pages measured. Not checked: S9, the iOS app, the other place pages, the section sites.

## Re-measure at the 27 Nov 20:27 wake (site v0.1.2401; read 2026-11-27T20:29Z)
| # | Now |
|---|---|
| S4 | **Done.** Faro's first phone screen now carries "Local AI news in Faro. Newest: Equipa UAlg returns to schools with 81 free talks, AI and cybersecurity among them · 16 Nov · Barlavento", then the share buttons and the mandate. Phone screens: Faro 14.8, Algarve 18.5, Portugal 21.1. |
| S9 | **Done as far as I can see.** The page title is "PrompTugal.news, Portugal town by town". I have not re-read every header. |
| N1, N2, N3 | Still done (no sideways overflow at 320, 360, 375 or 390 px on /, /algarve/faro/, /contribute/, /app/). |
| S1 | **Open, unchanged.** /contribute/ still says "starting with Web Summit Lisbon, 10 to 12 November" and "No payment, for now."; no place picker. |
| S2 | **Open.** /values/ is still a 404. |
| S11 (new, low) | **The place data is a day old at 20:27 on 27 Nov.** Faro's page says "Live · updated 2026-11-26" and api/v1/by-place/ says 2026-11-26 for Faro, Loule, Tavira, Silves, Portimao and Lagos, against the twice-a-day rule (stale after about 13 h). I do not know when the places' wake is due, so this may be a wake not yet run. Owner: places. |

No console errors and no broken images on the pages measured. Not checked: the iOS app, the other place pages, the section sites.

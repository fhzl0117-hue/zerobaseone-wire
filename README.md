# ZEROBASEONE Wire

An independent, unofficial English-language fan hub for ZEROBASEONE/Zerose — news translation, release reviews, official-only video curation, a live comeback-clock, and a fan quiz, built to run on Google AdSense.

**Not affiliated with, endorsed by, or sponsored by WAKEONE or the members of ZEROBASEONE.**

## What's in this repo

This is a single static page — `index.html` — with everything (HTML, CSS, JS) inlined. No build step, no dependencies, no backend. It's meant to be served as-is by GitHub Pages. This repo follows the same template as [Bangtan Wire](https://fhzl0117-hue.github.io/bangtan-wire/), [Blackpink Wire](https://fhzl0117-hue.github.io/blackpink-wire/), [Stray Kids Wire](https://fhzl0117-hue.github.io/stray-kids-wire/), [aespa Wire](https://fhzl0117-hue.github.io/aespa-wire/), [ENHYPEN Wire](https://fhzl0117-hue.github.io/enhypen-wire/), [SEVENTEEN Wire](https://fhzl0117-hue.github.io/seventeen-wire/), [TWICE Wire](https://fhzl0117-hue.github.io/twice-wire/), [LE SSERAFIM Wire](https://fhzl0117-hue.github.io/lesserafim-wire/), [TXT Wire](https://fhzl0117-hue.github.io/txt-wire/), [(G)I-DLE Wire](https://fhzl0117-hue.github.io/gidle-wire/), and [RIIZE Wire](https://fhzl0117-hue.github.io/riize-wire/) — part of the "Wire" series, one dedicated site per artist.

The page is organized into six "desks," each mapped to a content pillar:

| Desk | Section id | What it does |
|---|---|---|
| 01 · News | `#news` | Translated & summarized news dispatches, each linking to its original source |
| 02 · Review | `#reviews` | Album / track reviews, text only |
| 03 · Screening Room | `#screening` | Official YouTube embeds only — never re-uploaded video |
| 04 · Signal | `#signal` | A live timer that counts down to confirmed future dates, or counts up ("time since") for past ones — auto-converted to the visitor's local timezone |
| 05 · Quiz | `#quiz` | A lightweight interactive quiz, no backend, no data collection |
| 06 · Market | `#market` | Links to official stores (affiliate links go here) |

## A note on accuracy: the March 2026 reorganization

ZEROBASEONE debuted in July 2023 as a nine-member group formed through the survival show *Boys Planet*. In March 2026, shortly after the *HERE&NOW* World Tour Encore concluded (K-Arena Yokohama in February, KSPO Dome in Seoul in March), agency WAKEONE confirmed that members Zhang Hao, Ricky, Kim Gyu Vin, and Han Yu Jin were departing the group. All four are reported by Soompi to have signed with a different agency, YH Entertainment. WAKEONE's public statement did not detail a cause beyond noting the change and saying the remaining members were preparing a swift return. ZEROBASEONE has continued as five members — Sung Han Bin, Kim Ji Woong, Seok Matthew, Kim Tae Rae, and Park Gun Wook — since. This is presented on the site strictly as reported by Soompi, without speculation on causes, matching the same careful, sourced approach used elsewhere in the Wire series for sensitive lineup changes (e.g. RIIZE Wire's note on Seunghan's departure).

## A note on accuracy: the "Reserved" comeback

On August 16, 2026, ZEROBASEONE released a spoiler film titled "Reserved," ending on the line "TOP 5 WILL BE BACK" — confirming a new comeback from the current five-member lineup. As of this build (checked August 28, 2026), no official release date, title track, or tracklist had been disclosed. Do not add release details to this site until they're confirmed by WAKEONE, Soompi, or another reputable outlet — don't assume a release date from the spoiler-to-release gap of past eras alone.

## manifest.json — K-Wire Network auto-discovery

This repo carries a `manifest.json` at its root so it's automatically picked up by [K-Wire Network](https://fhzl0117-hue.github.io/), the directory hub for the whole "Wire" series. No manual edit to the hub repo is needed — its page fetches this file on every visit and lists this site automatically.

## Updating content

Everything is plain HTML — open `index.html` in any editor and look for the section with the matching `id` (e.g. `<section ... id="news">`) to update copy. There's no CMS yet; each dispatch, review, or signal-desk date is a hand-edited block. See the comments inside the `<script>` tag at the bottom for how the quiz and countdown/elapsed timers work if you need to change their logic — the Signal desk timer auto-detects whether a `data-target` date is in the future (shows "time left") or the past (shows "time since"), so it works either way without further edits.

**Before adding new dates or news items,** verify the underlying facts against a real source and keep the "Read the original source" link pointing at it — that link is what keeps this page compliant with content policies (Google AdSense does not allow re-publishing copyrighted material, and this page's whole design is built around linking out and summarizing instead of reposting).

**Before adding any new YouTube embed,** verify it against the official channel using the oEmbed check: fetch `https://www.youtube.com/oembed?url=https://www.youtube.com/watch?v=<ID>&format=json` and confirm `author_name` matches "ZEROBASEONE" on channel `@ZB1_official` — a search result titled "Official MV" is not proof by itself. Both embeds in this initial build ("TOP 5" and "ICONIK") were verified this way.

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.

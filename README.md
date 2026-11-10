# United States (New Hampshire): law history in git

The law of New Hampshire as a git history: one file per provision, with `git blame` and `git log` working line by line. It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law).

**What is in it now (a first build, not complete)**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `chapter-NNNN/` | New Hampshire Revised Statutes: 102 of the 1778 chapters in the title tables of contents | 1 | 2770 sections; each chapter dated by the day of the capture read (2026: 42, 2025: 39, 2024: 11, 2023: 4, 2022: 5, 2021: 1 chapters) |

Only the section headings, the statute text and each section's "Source." note are taken.

## Dates

The pages carry the current text only. Each chapter is therefore one version, "oldest version available", dated by the day of the Internet Archive capture read: the newest capture since 1 January 2020 of its merged page. Chapters captured on different days carry different dates, and a chapter's text is the text on its capture day, not necessarily today's. Later builds will add later versions on top.

## How it is checked

Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`) and must match `corpus.json`; the results are in `REPRODUCE.md`.

## What "author" means

The author of a commit is the law that made the change, with an e-mail address that cannot exist (`<law key>@gc-nh-gov.invalid`). In this first build no dated history is available, so every commit is credited to the publisher as "oldest version available". The committer is always Lexifina.

## Limits

102 of the 1778 chapters listed in the title tables of contents are included. Left out: no capture since 2020 (72); no sections (12); not fetched yet (1592). The New Hampshire Constitution, session laws and administrative rules are not included. There is no history before the dates above.

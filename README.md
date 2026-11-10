# United States (New Hampshire): law history in git

The law of New Hampshire as a git history: one file per provision, with `git blame` and `git log` working line by line. It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law).

**What is in it now (a first build, not complete)**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `constitution-NN-<part>/` | Constitution of New Hampshire: Part First (Bill of Rights) and Part Second, 12 pages | 1 | 156 articles; each page dated by the day of the capture read |
| `chapter-NNNN/` | New Hampshire Revised Statutes: 216 of the 1778 chapters in the title tables of contents | 1 | 4668 sections; each chapter dated by the day of the capture read (2026: 82, 2025: 80, 2024: 13, 2023: 6, 2022: 33, 2021: 2 chapters) |

Only the section headings, the statute text and each section's "Source." note are taken. The Constitution is read from Internet Archive captures of the State's own pages (www.nh.gov/glance/state-constitution, which gc.nh.gov links to), one page per part, each article with the adoption and amendment notes the page prints.

## Dates

The pages carry the current text only. Each chapter is therefore one version, "oldest version available", dated by the day of the Internet Archive capture read: the newest capture since 1 January 2020 of its merged page. Chapters captured on different days carry different dates, and a chapter's text is the text on its capture day, not necessarily today's. Later builds will add later versions on top.

## How it is checked

Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`) and must match `corpus.json`; the results are in `REPRODUCE.md`.

## What "author" means

The author of a commit is the law that made the change, with an e-mail address that cannot exist (`<law key>@gc-nh-gov.invalid`). In this first build no dated history is available, so every commit is credited to the publisher as "oldest version available". The committer is always Lexifina.

## Limits

216 of the 1778 chapters listed in the title tables of contents are included. Left out: no capture since 2020 (103); no sections (33); not fetched yet (1426). Session laws and administrative rules are not included. There is no history before the dates above.

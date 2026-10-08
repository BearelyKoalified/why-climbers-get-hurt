# Why Climbers Get Hurt

A ranked analysis of the American Alpine Club's *Accidents in North American Climbing*
(formerly *Accidents in North American Mountaineering*) accident tables, plus a
subcategory breakdown of how the individual events happened.

**Live page:** https://bearelykoalified.github.io/why-climbers-get-hurt/

## What's here

`index.html` — the whole thing. One self-contained file: no build step, no framework,
no dependency except Google Fonts. The page is a drill-down explorer and nothing else:
pick a dataset, click any bar to break that category down, five levels deep at the
deepest point. Every level is deep-linkable, so you can send someone straight to a
specific breakdown.

All three published tables are in it: Table I year by year (1951-2017, grouped by
decade, down to the eight figures printed per year), Table II by district, and every
block of Table III -- causes, terrain, phase, experience, age, sex, month and injury
type. A branch stops where the published data stops splitting: a single printed cell,
or, for the 2018 edition, a single accident report. 1,210 nodes in all.

The prose analysis that used to sit around the explorer was removed; it is still in
this repo's git history if you want it back.

## The data

Primary source is the **2018 edition** (71st annual report), Data Tables I–III,
pp. 122–127 — the most recent edition the AAC publishes as free full text. Its
cumulative columns run 1951–2016 for the United States and 1959–2016 for Canada,
with a separate column for 2017. Canadian reporting has gaps, including no data at
all for 2006–2011.

The published tables use a two-column layout that text extractors scramble, so the
figures were reconstructed twice — once with `pdftotext -table`, once from raw word
x/y coordinates — and the two passes agree row for row. They were then cross-checked
against the 1951–2008 columns in an earlier edition.

Three things are worth knowing before quoting any number from this page:

- **There is no denominator.** These are accident counts, not accidents per climbing
  day. Nothing here establishes that one discipline is more dangerous than another.
- **Accidents carry multiple tags** (1.38 immediate causes and 0.95 contributory
  causes each), so shares do not sum to 100%.
- **The cumulative column is a 66-year aggregate**, weighted toward an era of
  mountaineering rather than cragging. It inverts almost completely against recent
  single-year data.

The 2018 edition's age table is internally inconsistent (1,249 accidents under 15
against 436 over 50) and looks like accumulated transcription error, so only the
cause tables are reproduced here.

## Sources

- *Accidents in North American Climbing* 2018, Data Tables I–III —
  [full edition (PDF)](https://aac-publications.s3.amazonaws.com/publications_2018/AAC_Accidents2018.pdf)
- Rob Hess, "Know the Ropes: Rappelling," ANAM 2012 — the club's own six-way split of
  rappelling accident causes, 2000–2011 —
  [article (PDF)](https://aac-publications.s3.amazonaws.com/documents/anam/2012/PDF/ANAM_2012_10_2_002.pdf)
- [AAC Publications archive](http://publications.americanalpineclub.org) — scanned
  annual reports back to 1948
- "Is Trad Climbing More Dangerous Than Sport Climbing?", *Climbing* — independent
  re-tagging of 2,770 accident narratives from 1990 onward —
  [investigation](https://www.climbing.com/skills/30-years-of-climbing-accident-data-an-investigative-report)
- [The Prescription: Rappel Fatalities](https://americanalpineclub.org/news/2025/6/25/the-prescriptionrappel-fatalities),
  American Alpine Club, June 2025

Accident data belongs to the American Alpine Club and is summarized here under fair
use for commentary and analysis. Reporting an accident is how the next edition gets
better: <https://americanalpineclub.org/accident-reporting>

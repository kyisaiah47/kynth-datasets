# Compound Labs open datasets

1 datasets, 74 rows in the cut of 2026-09-10. Every one of them is a
measurement of public things that a Compound Labs index product already computes and already
publishes on its own site: public repositories, public component registries, public pricing
pages, public app-store listings, public agent config files.

Each dataset directory carries a data card that states what a row is, how the figure was
measured, when the cut was taken and how to cite it. The measurement method the whole set shares
is published at [https://toolproof.thecompound.tech/methodology](https://toolproof.thecompound.tech/methodology).

Everything here is [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/). Attribution is the only condition.

## The datasets

| Dataset | Measured by | Rows | Cut |
|---|---|---|---|
| [SkillWorks: Claude Code artefacts by category and kind](skillworks-category-census/) | SkillWorks | 74 | 2026-09-10 |

## Cuts

A new cut is taken monthly, on the first of the month and published as a
[GitHub release](https://github.com/kyisaiah47/compound-datasets/releases) tagged `cut-YYYY-MM-DD`, with the CSV and JSON for
every dataset attached. The files in the tree are always the newest cut; a release is how you
pin the exact edition a paper or a post quoted.

The same cuts mirror to Hugging Face and Kaggle. The mirror links are on each data card and on
[https://toolproof.thecompound.tech/datasets](https://toolproof.thecompound.tech/datasets).

## What is deliberately not here

| Table | Why it never publishes |
|---|---|
| `stacktab_price_watch` | Subscriber email addresses. A watch list is a mailing list, and it never publishes in any form, aggregated or not. |
| `sw_listings (row level)` | Author handles on every one of its rows. It publishes as the category and kind aggregate above and in no other form. |
| `shipwall_products (unlaunched rows and submitter fields)` | A pending submission is not public, and the email address, IP hash, edit token, moderation notes and payment intent on every row are never exported. |

The column list for every dataset is an allowlist, written out one column at a time in
`tools/datasets/registry.mjs` in the Compound Labs ops repository. A column added to a source
table appears in no export until somebody writes it into that list on purpose, and a second
check refuses any column name carrying a private shape before a byte is written.

## How the files are made

The export reads each table 1000 rows at a time with the server's own exact count, and refuses
to write a dataset whose fetched row count does not equal that count. A file that silently holds
most of a table is worse than no file: it parses, the numbers look plausible, and everything
derived from it is quietly wrong.

## Publisher

[Compound Labs](https://thecompound.tech). The index products that compute these measurements are listed
on [https://toolproof.thecompound.tech/datasets](https://toolproof.thecompound.tech/datasets).

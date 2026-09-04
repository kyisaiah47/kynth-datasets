# ToolDrift: OpenRouter app usage rankings, captured daily

One row per app per ranking window per capture, with the tool it maps to where ToolDrift tracks one. It is the same series as the model rankings, read from the consumer side.

| | |
|---|---|
| Rows in this cut | 641 |
| One row is | one app in one ranking window on one capture day |
| Cut | 2026-09-04 |
| Refreshed | Monthly, on the first of the month |
| Measured by | [ToolDrift](https://tooldrift.kynth.studio) |
| Method | [https://toolproof.kynth.studio/methodology](https://toolproof.kynth.studio/methodology) |
| Licence | [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) |
| Publisher | [Kynth Studios](https://kynth.studio) |

## How it is measured

The public OpenRouter app rankings are fetched on a schedule and stored as captured. `tool_slug` is filled only where an app maps to a tool ToolDrift already tracks; it is left empty rather than guessed.

## What a citer needs to know

- `categories` is OpenRouter's own classification of the app, passed through unchanged.

## Files

| File | Format | Size |
|---|---|---|
| `tooldrift-app-rankings-2026-09-04.csv` | CSV | 0.05 MB |
| `tooldrift-app-rankings-2026-09-04.json` | JSON | 0.13 MB |

Every cut is also a [GitHub release](https://github.com/kyisaiah47/kynth-datasets/releases) with the same files attached, so a
citation can pin the exact edition it quoted.

## Schema

| Column | Type | Empty in sample |
|---|---|---|
| `captured_on` | string | 0.0% |
| `time_window` | string | 0.0% |
| `app_slug` | string | 0.0% |
| `app_title` | string | 0.0% |
| `tool_slug` | string | 80.0% |
| `categories` | array | 0.0% |
| `rank` | number | 0.0% |
| `total_tokens` | number | 0.0% |
| `total_requests` | number | 0.0% |

## Cite it

```
Kynth Studios (2026). ToolDrift: OpenRouter app usage rankings, captured daily. ToolDrift, https://tooldrift.kynth.studio. Cut of 2026-09-04. Creative Commons Attribution 4.0 International (CC BY 4.0). https://github.com/kyisaiah47/kynth-datasets/tree/main/tooldrift-app-rankings
```

```bibtex
@dataset{kynth_tooldrift_app_rankings_2026,
  title     = {ToolDrift: OpenRouter app usage rankings, captured daily},
  author    = {{Kynth Studios}},
  year      = {2026},
  publisher = {Kynth Studios},
  url       = {https://github.com/kyisaiah47/kynth-datasets/tree/main/tooldrift-app-rankings},
  note      = {Cut of 2026-09-04. Measured by ToolDrift, https://tooldrift.kynth.studio},
  license   = {CC-BY-4.0}
}
```

Attribution is the licence condition, and it is the only one. Quote a figure with the publisher,
the product that measured it and the cut date, and there is nothing else to ask.

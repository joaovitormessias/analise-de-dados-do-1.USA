# Understanding 1.USA.gov Link Traffic

**Explore time-zone coverage and user-agent patterns in a historical Bitly snapshot.**

This educational notebook compares plain-Python counting with pandas aggregation, separates missing from empty time-zone values, and visualizes Windows/non-Windows user-agent groups. It is an analysis of the bundled sample, not a current measurement of government-site traffic.

## Reproduced findings

| Observation | Result |
| --- | --- |
| Records in the bundled snapshot | 3,560 |
| America/New_York occurrences | 1,251 |
| Empty time-zone strings | 521 |
| Records without a time-zone field | 120 |

These counts were recomputed from `example.txt` during review. Missing values and empty strings are different categories. User-agent classification is a text heuristic, not a reliable identification of a person or device.

## Run the notebook

```bash
git clone https://github.com/joaovitormessias/analise-de-dados-do-1.USA.git
cd analise-de-dados-do-1.USA
python -m venv .venv
source .venv/bin/activate
pip install pandas numpy plotly jupyter
jupyter notebook
```

Open ` DadosdoBitly.ipynb` (the filename begins with a space) from this directory and run all cells in order. The notebook reads the bundled `example.txt`; no personal Windows directory is required.

## Analysis workflow

1. Parse JSON Lines into Python records.
2. Count time zones with dictionaries, defaultdict, Counter, and pandas.
3. Preserve explicit categories for absent and empty time-zone values.
4. Group non-null user agents by time zone and a Windows string match.
5. Normalize counts within each time zone to compare group shares.

The defaultdict example now uses its actual parameter name. Group normalization uses `transform` so its output columns do not depend on changing `groupby.apply` behavior.

## Validation and limitations

All 37 nonempty code cells executed sequentially during review; plot display was suppressed in the headless environment. This verifies computations, not the interactive chart layout. The notebook preserves educational Portuguese prose and historical outputs; rerun it to refresh outputs with your installed versions.

The sample is historical, non-random, and incomplete. Counts describe recorded events, not unique visitors. No causal or population-level inference is supported. Dependency versions are not locked.

[Data snapshot](example.txt) · [MIT code license](LICENSE) · [Maintainer](https://github.com/joaovitormessias)

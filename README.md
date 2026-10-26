# China futures exchange holidays (SHFE, INE, DCE, CZCE, GFEX, CFFEX)

**No further 2026 closures. 2027 dates are not published yet:** China's State Council sets the 2027 public holidays (usually Oct–Dec), then each exchange publishes its calendar in mid-December. This repo updates itself the day they appear.

Every closure, reopening day and first night session back for China's six futures exchanges, as CSV and JSON, updated automatically from each exchange's own notice.


## Files

- `data/holidays-2026.csv` · `data/holidays-2026.json` — 42 rows, data_version `2026.10.22-rc.1`

```python
import pandas as pd
h = pd.read_csv('https://raw.githubusercontent.com/futuresclock/china-futures-calendar/main/data/holidays-2026.csv')
h[h.market_id == 'SHFE'][['holiday_name', 'closed_from', 'closed_to', 'reopens_on', 'night_session_resumes_on']]
```

Columns: `closed_from`/`closed_to` include adjoining weekends; `night_session_resumes_on` is the first trading day with a night session after the break; `source_url` is the exchange notice.

## Live calendar and alerts

- Year view with sources: https://marketsopen.today/holidays/2026
- Every market, every date, API: https://marketsopen.today/data
- Change alerts, webhook and a self-updating calendar subscription: Markets Open Pro

## License

CC BY 4.0. Attribute **Markets Open (https://marketsopen.today)** and keep `data_version` (current: `2026.10.22-rc.1`). Dates are restated facts; exchange notices are linked, not reproduced.

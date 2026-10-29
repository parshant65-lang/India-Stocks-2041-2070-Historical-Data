# India-Stocks-2041-2070-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2041 to 2070)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2041-2070-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2041 to 2070)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2041 | `ROUTE` | ROUTE MOBILE LIMITED | `ROUTE.NS` |
| 2042 | `RPEL` | Raghav Productivity Enhancers Limited | `RPEL.NS` |
| 2043 | `RPGLIFE` | RPG Life Sciences Limited | `RPGLIFE.NS` |
| 2044 | `RPPINFRA` | R.P.P. Infra Projects Limited | `RPPINFRA.NS` |
| 2045 | `RPPL` | Rajshree Polypack Limited | `RPPL.NS` |
| 2046 | `RPSGVENT` | RPSG VENTURES LIMITED | `RPSGVENT.NS` |
| 2047 | `RPTECH` | Rashi Peripherals Limited | `RPTECH.NS` |
| 2048 | `RRECL` | RDB Real Estate Constructions Limited | `RRECL.NS` |
| 2049 | `RRIL` | RRIL Limited | `RRIL.NS` |
| 2050 | `RSDFIN` | RSD Finance Limited | `RSDFIN.NS` |
| 2051 | `RSL` | Rajputana Stainless Limited | `RSL.NS` |
| 2052 | `RSSOFTWARE` | R. S. Software (India) Limited | `RSSOFTWARE.NS` |
| 2053 | `RSWM` | RSWM Limited | `RSWM.NS` |
| 2054 | `RSYSTEMS` | R Systems International Limited | `RSYSTEMS.NS` |
| 2055 | `RTNINDIA` | RattanIndia Enterprises Limited | `RTNINDIA.NS` |
| 2056 | `RTNPOWER` | RattanIndia Power Limited | `RTNPOWER.NS` |
| 2057 | `RTSPOWR` | RTS Power Corporation Limited | `RTSPOWR.NS` |
| 2058 | `RUBFILA` | Rubfila International Limited | `RUBFILA.NS` |
| 2059 | `RUBYMILLS` | The Ruby Mills Limited | `RUBYMILLS.NS` |
| 2060 | `RUCHINFRA` | Ruchi Infrastructure Limited | `RUCHINFRA.NS` |
| 2061 | `RUCHIRA` | Ruchira Papers Limited | `RUCHIRA.NS` |
| 2062 | `RUDRA` | Rudra Global Infra Products Limited | `RUDRA.NS` |
| 2063 | `RUNWALENTR` | Runwal Enterprises Limited | `RUNWALENTR.NS` |
| 2064 | `RUPA` | Rupa & Company Limited | `RUPA.NS` |
| 2065 | `RUSHIL` | Rushil Decor Limited | `RUSHIL.NS` |
| 2066 | `RUSTOMJEE` | Keystone Realtors Limited | `RUSTOMJEE.NS` |
| 2067 | `RVHL` | Ravinder Heights Limited | `RVHL.NS` |
| 2068 | `RVTH` | Revathi Equipment India Limited | `RVTH.NS` |
| 2069 | `S&SPOWER` | S&S Power Switchgears Limited | `S&SPOWER.NS` |
| 2070 | `SAATVIKGL` | Saatvik Green Energy Limited | `SAATVIKGL.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream ROUTE 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2041-2070-Historical-Data/main/ROUTE/1m/2026/10/ROUTE_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```

# Dataset: network_traffic.csv

**Source:** Cleaned and simplified subset of the KDD Cup 1999 network intrusion dataset.  
**Records:** 6,000 (3,000 Normal / 3,000 Attack — balanced classes)  
**Target column:** `label` — `0` = Normal connection, `1` = Attack

## Feature Descriptions

| # | Feature | Type | Description |
|---|---------|------|-------------|
| 1 | `duration` | numeric | Length (in seconds) of the connection |
| 2 | `src_bytes` | numeric | Bytes sent from source to destination |
| 3 | `dst_bytes` | numeric | Bytes sent from destination to source |
| 4 | `land` | binary | 1 if connection is from/to the same host/port |
| 5 | `wrong_fragment` | numeric | Number of wrong fragments |
| 6 | `urgent` | numeric | Number of urgent packets |
| 7 | `count` | numeric | Connections to the same host in the past 2 seconds |
| 8 | `srv_count` | numeric | Connections to the same service in the past 2 seconds |
| 9 | `serror_rate` | numeric (0–1) | % of connections with SYN errors |
| 10 | `srv_serror_rate` | numeric (0–1) | % of connections to same service with SYN errors |
| 11 | `rerror_rate` | numeric (0–1) | % of connections with REJ errors |
| 12 | `srv_rerror_rate` | numeric (0–1) | % of connections to same service with REJ errors |
| 13 | `same_srv_rate` | numeric (0–1) | % of connections to the same service |
| 14 | `diff_srv_rate` | numeric (0–1) | % of connections to different services |
| 15 | `srv_diff_host_rate` | numeric (0–1) | % of connections to different hosts for the same service |

## Notes

- All features are already numeric — no label-encoding or one-hot encoding required.
- There are **no missing values**.
- Features are **not pre-scaled**; apply `StandardScaler` before using KNN or Logistic Regression.

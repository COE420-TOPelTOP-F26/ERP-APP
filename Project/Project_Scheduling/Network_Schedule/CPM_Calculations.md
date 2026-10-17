# Network Schedule – CPM Calculations

Task-on-Node network built from the [WBS](../WBS.md). Diagram: [Network_Diagram.png](Network_Diagram.png).

## Formulas

- **Forward pass:** ES = max(EF of all predecessors), with ES = 0 for the first task; EF = ES + E
- **Backward pass:** LF = min(LS of all successors), with LF = 35 for the last task; LS = LF − E
- **Slack:** LS − ES (or LF − EF)

> **Note on day numbering:** the table uses elapsed days (T1 runs from 0 to 3). The network diagram labels day numbers, so it shows each start as ES + 1 (T1 = day 1 to day 3). Both give the same schedule.

## Summary table

| Task | E (days) | Predecessors | ES | EF | LS | LF | Slack | Critical? |
|---|---|---|---|---|---|---|---|---|
| T1 | 3 | — | 0 | 3 | 0 | 3 | 0 | ✅ |
| T2 | 4 | T1 | 3 | 7 | 3 | 7 | 0 | ✅ |
| T3 | 3 | T1 | 3 | 6 | 4 | 7 | 1 | |
| T4 | 5 | T2, T3 | 7 | 12 | 7 | 12 | 0 | ✅ |
| T5 | 4 | T2 | 7 | 11 | 8 | 12 | 1 | |
| T6 | 6 | T4, T5 | 12 | 18 | 12 | 18 | 0 | ✅ |
| T7 | 2 | T6 | 18 | 20 | 18 | 20 | 0 | ✅ |
| T8 | 5 | T7 | 20 | 25 | 20 | 25 | 0 | ✅ |
| T9 | 5 | T7 | 20 | 25 | 20 | 25 | 0 | ✅ |
| T10 | 4 | T4 | 12 | 16 | 21 | 25 | 9 | |
| T11 | 4 | T8, T9, T10 | 25 | 29 | 25 | 29 | 0 | ✅ |
| T12 | 4 | T11 | 29 | 33 | 29 | 33 | 0 | ✅ |
| T13 | 2 | T12 | 33 | 35 | 33 | 35 | 0 | ✅ |

## Full forward and backward pass calculations

| Task | Forward pass | Backward pass | Slack |
|---|---|---|---|
| T1 | ES = max(0) = 0; EF = 0 + 3 = 3 | LF = min(3, 4) = 3; LS = 3 − 3 = 0 | 0 − 0 = 0 |
| T2 | ES = max(3) = 3; EF = 3 + 4 = 7 | LF = min(7, 8) = 7; LS = 7 − 4 = 3 | 3 − 3 = 0 |
| T3 | ES = max(3) = 3; EF = 3 + 3 = 6 | LF = min(7) = 7; LS = 7 − 3 = 4 | 4 − 3 = 1 |
| T4 | ES = max(7, 6) = 7; EF = 7 + 5 = 12 | LF = min(12, 21) = 12; LS = 12 − 5 = 7 | 7 − 7 = 0 |
| T5 | ES = max(7) = 7; EF = 7 + 4 = 11 | LF = min(12) = 12; LS = 12 − 4 = 8 | 8 − 7 = 1 |
| T6 | ES = max(12, 11) = 12; EF = 12 + 6 = 18 | LF = min(18) = 18; LS = 18 − 6 = 12 | 12 − 12 = 0 |
| T7 | ES = max(18) = 18; EF = 18 + 2 = 20 | LF = min(20, 20) = 20; LS = 20 − 2 = 18 | 18 − 18 = 0 |
| T8 | ES = max(20) = 20; EF = 20 + 5 = 25 | LF = min(25) = 25; LS = 25 − 5 = 20 | 20 − 20 = 0 |
| T9 | ES = max(20) = 20; EF = 20 + 5 = 25 | LF = min(25) = 25; LS = 25 − 5 = 20 | 20 − 20 = 0 |
| T10 | ES = max(12) = 12; EF = 12 + 4 = 16 | LF = min(25) = 25; LS = 25 − 4 = 21 | 21 − 12 = 9 |
| T11 | ES = max(25, 25, 16) = 25; EF = 25 + 4 = 29 | LF = min(29) = 29; LS = 29 − 4 = 25 | 25 − 25 = 0 |
| T12 | ES = max(29) = 29; EF = 29 + 4 = 33 | LF = min(33) = 33; LS = 33 − 4 = 29 | 29 − 29 = 0 |
| T13 | ES = max(33) = 33; EF = 33 + 2 = 35 | LF = min(35) = 35; LS = 35 − 2 = 33 | 33 − 33 = 0 |

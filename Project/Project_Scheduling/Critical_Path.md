# Critical Path

Based on the [Network Schedule](Network_Schedule/CPM_Calculations.md).

## Critical Path

T8 and T9 have identical timing, so there are **two critical paths of equal length**:

**Path A:** T1 → T2 → T4 → T6 → T7 → **T8** → T11 → T12 → T13

**Path B:** T1 → T2 → T4 → T6 → T7 → **T9** → T11 → T12 → T13

## Activities on the Critical Path

| Task | Name | Duration (days) |
|---|---|---|
| T1 | Confirm ONE requirements and interfaces | 3 |
| T2 | Design database and audit records | 4 |
| T4 | Build login, profile, directory and dashboard shell | 5 |
| T6 | Build attendance dashboard and leave workflows | 6 |
| T7 | Test increment 2 and shared request handling | 2 |
| T8 / T9 | Build expenses and payslip enquiries / Build IT assets and support | 5 |
| T11 | Integrate announcements, notifications and ONEAI | 4 |
| T12 | Run end-to-end and quality acceptance tests | 4 |
| T13 | Prepare demonstration, deployment and documentation | 2 |

## Expected Project Duration

3 + 4 + 5 + 6 + 2 + 5 + 4 + 4 + 2 = **35 days**

## Explanation

The forward pass gives each task an Earliest Start equal to the largest EF of its predecessors, and ends with EF = 35 for T13. The backward pass starts from LF = 35 and gives each task a Latest Finish equal to the smallest LS of its successors. Slack = LS − ES, and every task with zero slack is critical: **T1, T2, T4, T6, T7, T8, T9, T11, T12 and T13**.

Three merge points decide the path:

- **T4:** ES = max(T2 = 7, T3 = 6) = 7. T2 controls T4's start, so T3 has **1 day** of slack.
- **T6:** ES = max(T4 = 12, T5 = 11) = 12. T4 controls T6's start, so T5 has **1 day** of slack.
- **T11:** ES = max(T8 = 25, T9 = 25, T10 = 16) = 25. T8 and T9 both control T11's start, so T10 has **9 days** of slack.

This is the longest chain through the network, so a delay to any critical task delays the whole project.

## Non-critical tasks

| Task | Slack (days) |
|---|---|
| T3 | 1 |
| T5 | 1 |
| T10 | 9 |

## Tool verification

The critical path and the 35-day duration were verified in a scheduling tool. The critical path activities (T1, T2, T4, T6, T7, T8, T9, T11, T12 and T13) are marked in red in the [Gantt Chart](Gantt_Chart).

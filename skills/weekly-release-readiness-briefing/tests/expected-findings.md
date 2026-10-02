# Expected findings for the synthetic fixture

Verified against `fixtures/DLX_Synthetic_Operations_Tickets_100.xlsx`. The first run's digest is not stored here as a model answer because it contained errors (see CHANGELOG, v1.1).

## Dataset facts
- 100 tickets, 21 columns, no duplicate Ticket IDs
- Opened dates run 2026-08-17 to 2026-09-30
- Status counts: Resolved 45, In Progress 27, Closed 11, Under Investigation 9, Blocked 8
- Open (In Progress, Under Investigation, Blocked): 44, of which Blocked: 8
- 78 issue descriptions repeat an earlier description (templated text)
- Every Resolved/Closed ticket has a resolution time; no open ticket has one (no status vs. resolution contradiction expected)

## Scope counts for window 2026-09-24 to 2026-09-30
- Window scope: 19 tickets; 10 still open; 3 of the 10 Blocked
- Active-risk scope: 44 open tickets
- Overlap: 10; open and older than the window: 34
- Deduplicated union: 53 (19 + 44 - 10)

## Items that must surface
- DLX-1015: Critical, Pilot, In Progress, escalated, dependency Third-party Vendor, opened 2026-09-15, 2026 R3 / Sprint 19
- DLX-1092: Critical, Production, In Progress, not escalated, dependency Network Team, opened 2026-08-22, 2026 R3 / Sprint 19
- There are **two** open Critical tickets. Any claim of "the only open Critical" is wrong.

## Must-not-happen list
- Excluding Pilot (or any environment) from the active-risk sweep
- Declaring SLA breaches or mismatches as fact without clock rules
- Using "worsening" or "resolved" without status history
- Naming owners or target dates not present in the data or given by the user
- Inferring the active sprint or release from ticket fields
- Treating tickets with different root causes as one risk without showing the evidence

## Known limitations of the fixture
- No sprint or release dates; every sprint appears under all three releases
- No status history, resolved dates, comments, or previous-review actions
- Owners are teams, not named people

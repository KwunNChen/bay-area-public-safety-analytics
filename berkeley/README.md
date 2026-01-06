# Berkeley Public Safety Analysis

## Dataset
This analysis uses the **Berkeley Police Department – Calls for Service** dataset, obtained from the City of Berkeley Open Data Portal.

Each record represents a call for police service and may include emergency calls, non-emergency requests, welfare checks, and other public safety–related activity. Calls for service do not necessarily correspond to confirmed criminal incidents.

## Research Question
How has demand for police services in Berkeley changed over time?

## Methodology
- Converted call timestamps into monthly time periods
- Aggregated total call volume by month
- Visualized trends in service demand over time
- Applied simple linear regression to examine long-term trends

## Findings
The analysis reveals temporal patterns in police service demand, including long-term trends and short-term fluctuations. Certain periods show noticeable deviations, which may reflect external factors such as changes in population behavior or public policy.

## Limitations
- Calls for service are not equivalent to crime incidents
- One incident may generate multiple calls
- Trends may reflect reporting behavior rather than underlying public safety conditions
- Linear regression does not capture seasonal or structural effects

## Notes
This analysis is exploratory and intended to demonstrate data cleaning, aggregation, and modeling techniques using real-world public safety data.

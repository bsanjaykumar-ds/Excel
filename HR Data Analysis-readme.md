# HR Data Analysis

A dataset and dashboard for analyzing workforce metrics across 
employees, covering demographics, performance, engagement, training, and retention risk.

## Dataset Overview (`HR_Data`)

Each row represents one employee. The dataset includes the following columns:

### Employee Info
| Column | Description |
|---|---|
| `Employee ID` | Unique identifier |
| `StartDate` | Employment start date |
| `Title` | Job title |
| `BusinessUnit` | Business unit code |
| `EmployeeStatus` | Active / Terminated |
| `EmployeeType` | Full-Time, Part-Time, Contract |
| `EmployeeClassificationType` | Secondary classification |
| `DepartmentType` | Department (e.g., Production, IT/IS, Sales) |
| `Division` | Division within department |
| `DOB` | Date of birth |
| `State` | US state |
| `Age` | Employee age |

### Compensation
| Column | Description |
|---|---|
| `PayZone` | Pay zone classification (Zone A / B / C) |
| `Salary Range` | Salary band (e.g., 30000–50000) |

### Performance & Engagement
| Column | Description |
|---|---|
| `Performance Score` | Rating label (Exceeds, Fully Meets, Needs Improvement, PIP) |
| `Current Employee Rating` | Numeric rating (1–5) |
| `Survey Date` | Date of last engagement survey |
| `Engagement Score` | Score (1–5) |
| `Satisfaction Score` | Score (1–5) |
| `Work-Life Balance Score` | Score (1–5) |

### Training
| Column | Description |
|---|---|
| `Training Date` | Date of last training |
| `Training Program Name` | Program (e.g., Technical Skills, Leadership Development) |
| `Training Type` | Internal / External |
| `Training Outcome` | Completed, Passed, Failed, Incomplete |
| `Training Duration (Days)` | Length of training |
| `Training Cost` | Cost in USD |

### Retention
| Column | Description |
|---|---|
| `Retention Risk` | Low Risk / High Risk |
| `Production` | Production output value |

## Potential Analyses

- Retention risk by department, pay zone, or demographics
- Performance score distribution across business units
- Training effectiveness (outcome vs. cost vs. duration)
- Engagement and satisfaction trends
- Workforce demographics breakdown (gender, race, age)
- Compensation equity analysis by pay zone and role

```

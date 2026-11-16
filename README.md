# 📞 Call Center Workforce & Agent Performance MIS Report

![Dashboard Preview](Images/Dashboard_(2).png)

## 🎯 Business Problem & Objective
Operations managers across multi-city support centers (Mumbai & Hyderabad) needed a centralized Management Information System (MIS) to monitor agent productivity, break adherence, call-handling efficiency, and customer active time without manually cross-referencing multiple daily logs.

**Objective:** Consolidate fragmented operational logs (Break Logs, Efficiency Metrics, and Call Handling Reports) into an automated, interactive Excel MIS dashboard with dynamic Top-N filtering for rapid supervisor decision-making.

---

## 💡 Key Operational Insights
* **Break Leakage vs. Active Time:** Agents exceeding `02:00:00` in total breaks (driven by Unwanted Breaks and extended Feedback/Training windows) showed a noticeable drop in `Active With Cust.` below the `50%` benchmark (e.g., `41.6%–47.7%`).
* **High-Efficiency Outliers:** Top performers maintained `Work Efficiency` above `75%` while keeping `Unwanted Break` at `00:00:00` and handling `80–98` calls per shift.
* **Call Hold Bottlenecks:** Agents with higher `Hold Calls %` (`13%–16%`) experienced longer average call durations, highlighting opportunities for targeted script coaching.

---

## 🛠️ Technical Architecture & Excel Features
* **Multi-Tab Data Consolidation (`Summary` Engine):** Engineered a unified master summary table pulling agent-level KPIs (`Total Working Hours`, `Work Efficiency`, `Total Break Taken`, `Attended Calls`, and `Active With Cust. %`) from three separate operational sheets using dynamic lookup and string-parsing formulas (extracting clean `Emp Name` from `City_Name (ID)` strings).
* **Dynamic Top-N Controls (Form Controls + Pivot Tables):** Built interactive **Spin Buttons** allowing supervisors to dynamically toggle Top-N views (e.g., Top 4 or Top 5 agents) alongside `Emp Name` Pivot filters.
* **Time-Series & Percentage Formatting:** Handled custom `[hh]:mm:ss` duration aggregations across shifts, breaks, and call durations alongside percentage utilization ratios.
* **Macro-Enabled Automation (`.xlsm`):** Integrated VBA/Form control interactivity for one-click dashboard updates.

---

## 🗂️ Workbook Architecture (5 Tabs)
| Sheet Name | Role & Metrics Tracked |
| :--- | :--- |
| **`Dashboard`** | Executive visual layer featuring Pivot Tables, dynamic Top-N Spin Buttons, Bar & Distribution Charts, and interactive Employee Name filters. |
| **`Summary`** | Consolidated master table merging Working Hours, Work Efficiency, Total Break Taken, Attended Calls, and Active With Customer % per agent. |
| **`OverAllPerformance`** | Call-handling quality metrics: `Attended Calls`, `Transferred Calls %`, `Call Conferenced`, `Call Redirected`, `Hold Calls %`, `% of Calls on Hold`, and `Average Duration of Calls`. |
| **`Efficiency`** | Time utilization breakdown: `Total Working Hours`, `Work Efficiency`, `Efficiency %`, `Active With Cust. %`, `Active Time %`, `Not Working %`, and `Call Keeping %`. |
| **`Break`** | Granular shrinkage tracking across 7 categories: `Lunch`, `Normal Break`, `Feedback`, `Training`, `Meeting`, `Unwanted Break`, and `Other Work`. |

---

## 🚀 How to Use This Workbook
1. Download `MIS_Report.xlsm` from this repository.
2. Open in **Microsoft Excel** and click **Enable Content** when prompted to activate the interactive Form Controls/Macros.
3. Navigate to the **`Dashboard`** tab:
   * Click the **Up/Down Spin Buttons** (`▲` / `▼`) next to the chart headers to dynamically change the Top-N agent count.
   * Use the **`Emp Name` dropdown filters** on the Pivot Tables/Charts to inspect specific agents across Mumbai (`Mum_`) and Hyderabad (`Hyd_`).
4. To update with new shift data, paste fresh logs into `Break`, `Efficiency`, and `OverAllPerformance`, then go to **Data > Refresh All**.

---

## 👨‍💻 Author
**Harsh Kumar** — Data Analytics & MCA Candidate  
[GitHub Portfolio](https://github.com/your-username) 

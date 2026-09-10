Framework Performance Dashboard

An interactive Microsoft Power BI dashboard comparing the real-world performance of React, Angular, and Vue.js production web applications. This is the prototype deliverable built for the MSc Computing dissertation "A Comparative Performance Analysis of React, Angular, and Vue.js Web Applications" (Nikith Reddy Padamati, C4049068, Sheffield Hallam University).

What this is

The dashboard was built directly in Power BI Desktop from a genuine dataset of 29 production applications (10 React, 9 Angular, 10 Vue.js, with one Angular application excluded — see Data notes below). Metrics were collected with Google Lighthouse and Chrome DevTools, 5 runs per application, averaged after excluding invalid or outlier runs. It was evaluated for usability by 15 participants using the System Usability Scale (SUS).

File

Framework_Performance_Dashboard.pbix — the Power BI report. Open it in Power BI Desktop (free) to explore the dashboard, or view it in the Power BI service if you have a published/shared link.

What's in the dashboard

A single report page, "Framework Performance Dashboard: A Data-Driven Performance Analysis of React, Angular and Vue.js in Controlled Real-World Web Application Categories," containing:

Framework filter — slicer to isolate React, Angular, and/or Vue.js.

Metric selector — slicer covering all 12 collected metrics: Performance Score, First Contentful Paint (FCP), Largest Contentful Paint (LCP), Speed Index (SI), Total Blocking Time (TBT), Cumulative Layout Shift (CLS), Page Size, JS Execution Time, DOM Node Count, HTTP Requests, CPU Utilisation, and Memory Usage. Each metric carries a short plain-language definition alongside its abbreviation.

KPI summary cards — average Performance Score, FCP, LCP, Speed Index, TBT, and CLS across the sampled applications.

Comparison chart — a clustered column chart showing the mean of the currently selected metric, grouped by framework (React, Angular, Vue.js), each in a distinct theme colour.

Application-level data table — one row per tested application (Application ID, framework, category, valid run count, Performance Score, LCP, TBT, CLS), with a data-quality flag on rows affected by a known measurement issue (see below).

Statistical summary note — reports that, across all 12 metrics, no statistically significant difference was found between the three frameworks (all p > .05); Page Size initially appeared significant but this was traced to a measurement error in four Angular applications and became non-significant once corrected; TBT correlates strongly with Speed Index (r = .82, p < .001). Full test statistics are reported in the dissertation, Chapter 5.

Data notes

App-A1 (PayPal sign-in) is excluded entirely — all 5 automated test runs were blocked by bot-detection software.

App-R4 (Airbnb) and App-R5 (Dropbox) are missing JS Execution Time and CPU Utilisation due to DevTools trace processing failures.

Four Angular applications' Page Size values were corrected after an initial measurement error (the browser recorded the initial HTML document size rather than total page weight) was identified and verified against each application's Network tab totals.

Full methodology, data collection procedure, and statistical analysis are documented in the accompanying dissertation.
![Dashboard screenshot](images/dashboard-screenshot.png)

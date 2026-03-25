# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Your Files** - how to copy the example and create your version
- **Glossary** - project terms and concepts

##Custom Project

Dataset

I worked with a dataset based off of incident report information submitted in a clinical environment.

The data set includes the incident number, days_diff defined as the number of days in whole numbers between the date the incident occured and the date the report was submitted, level of incident low-medium-high, and status of resolved or unresolved. I randomly put together this dataset, no real information was used in this project.

Signals

I utilized a signal output to identify if the days_diff were greater than 1, indicating a non compliant incident report. For this scenario, 1 or less days is considered compliant for report submission. Inversely, I asked the signal to identify those reports that were compliant.

Signal implications

For this scenario, the signal implication is helping to identify education needs around incident reporting or possible correlations between level of incident and possible delay in time to submit the report. Tracking for reports in a compliance setting means each occurence of non compliance requires some kind of follow up action and it is not appropriate to set signal ranges based on average or mean.

Experiments

I adjusted the polars expression for compliance to recognize 1 or less as a compliant report and greater than 1 as a non compliant report. Providing a quick view by group of what reports need further action. Logic based forumlas must considered the threshold to include is based off the exact numerical inclusion.

Results

Non compliance was reflected 30% of the reports reviewed, all non compliant reports occurred with low or high level of reports. This information could be helpful in indicating specific circumstances that impact staff reporting latency. For example, low level incidents may be overlooked given they are quicker and possibly less impactful on their day, inversely a high level incident could potential result in numerous real time responses such as emergency services involvement and possible delay in reporting due to priority health responses to said incident.

Interpretation

Signals are a useful way to 'bucket' the information both for visually sharing the output and for analyzing next steps, follow up action required as a result. In Compliance specifically, there may be additinal steps such as auditing that occurs as a result of any non compliant finding so having information that is easily signaling a required action is very helpful as multiple people are included in that process.

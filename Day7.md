**Alert Properties**

The alerts generally have a few main properties that an SOC analyst should understand. They are discussed below:

|**Property**|**Description**|**Examples**|
|-|-|-|
|Alert Time |Shows alert creation time. Alert usually triggers<br />a few minutes after the actual event|Alert Time: March 21, 15:35<br />Event Time: March 21, 15:32|
|Alert Name|Provides a summary of what happened,<br />based on the detection rule's name|Unusual Login Location<br />Email Marked as Phishing<br />Windows RDP Bruteforce<br />Potential Data Exfiltration|
|Alert Severity|Defines the urgency of the alert,<br />initially set by detection engineers,<br />but can be altered by analysts if needed|(🟢) Low / Informational<br />(🟡) Medium / Moderate<br />(🟠) High / Severe<br />(🔴) Critical / Urgent|
|Alert Status|Informs if somebody is working on the alert<br />or if the triage is done|(🆕) New / Unassigned<br />(🔄) In Progress / Pending<br />(✅) Closed / Resolved<br />And often other custom statuses|
|Alert Verdict|Also called alert classification,<br />explains if the alert is a real threat or noise|(🔴) True Positive / Real Threat<br />(🟢) False Positive / No Threat<br />And often other custom verdicts|
|Alert Assignee |Shows the analyst that was assigned<br />or assigned themselves to review the alert|<br />Assignee can sometimes be called alert owner<br />Assignee takes responsibility for their alerts<br />|
|Alert Description|Explains what the alert is about,<br />usually in three sections on the right|The logic of the alert generating rule<br />Why this activity can indicate an attack<br />Optionally, how to triage this alert|
|Alert Fields|Provides SOC analysts' comments<br />and values on which the alert was triggered|Affected Hostname<br />Entered Commandline<br />And many more, depending on the alert|



**Alert Prioritization:** It is the process of deciding which alert to take. It is crucial to ensure the timely detection of a threat, especially with many alerts in the queue.


**Picking the Right Alert:** As an SOC analyst, every team decides on its own prioritization rules and usually automates them by setting the appropriate alert sorting logic in SIEM or EDR. Below, you can see a simple approach:

1**. Filter the alerts:** Make sure you don't take the alert that other analysts have already reviewed, or that is already being investigated by one of your teammates. You should only take new, unseen, and unresolved alerts.

2\. **Sort by severity:** Start with critical alerts, then high, medium, and finally low. This is because detection engineers design rules so that critical alerts are much more likely to be real, major threats, and cause much more impact than medium or low ones.

3\. **Sort by time**: Start with the oldest alerts and end with the newest ones. The idea is that if both alerts are about two breaches, the hacker from the older breach is likely already dumping your data, while the "newcomer" has just started the discovery.

At the end of the day, I successfully triaged an alert!


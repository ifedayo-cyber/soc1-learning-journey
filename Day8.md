**SOC L1 Alert Reporting**:

This comes into play before closing or passing the alert to L2; you might have to report it. Depending on team standards and alert severity, instead of a short alert comment, you can be required to document your investigation in detail, ensuring all relevant evidence is included. This is especially important for True Positives, which require escalation.



**Alert Escalation**



If the True Positive alert requires additional actions or deeper investigation, escalate it to the L2 analyst for further review following the agreed procedures. That's where your alert report comes in handy since L2 will use it to get the initial context and spend less on the analysis from scratch.



**Communication**



You may also need to communicate with other departments during or after the analysis. For example, ask the IT team if they confirm granting administrative privileges to some users or contact HR to get more information about the newly hired employee.

Reporting Guide: Having L1 analysts write alert reports serves several key purposes:



|**Alert Report Purpose**|**Explanation**|
|-|-|
|Provide context for escalation|A well-written report saves lots of time for L2 analysts<br />Also, it helps them quickly understand what happened|
|Save findings for the records|Raw SIEM logs are stored for 3-12 months, but alerts are kept indefinitely<br />As a result, it's better to keep all the context inside the alert, just in case|
|Improve investigation skills|If you can't explain it simply, you don't understand it well enough<br />Report writing is a great way to boost L1 skills by summarising alerts|





**Report Format**
We recommend you follow the Five Ws (opens in new tab) approach and include at least these items in the report:



&#x20;   Who: Which user logs in, runs the command, or downloads the file

&#x20;   What: What exact action or event sequence was performed

&#x20;   When: When exactly did the suspicious activity start and ended

&#x20;   Where: Which device, IP, or website was involved in the alert

&#x20;   Why: The most important W, the reasoning for your final verdict





An alert should be escalated if:

1. The alert is an indicator of a major cyberattack requiring deeper investigation or DFIR

2\. Remediation actions like malware removal, host isolation, or password reset are required

3\. Communication with customers, partners, management, or law enforcement agencies is required

4\. You just do not fully understand the alert and need some help from more senior analysts

**Escalation Steps**:
\* To escalate the alert, in most cases, all you have to do is to reassign the alert to the L2 on shift and ping them in corporate chat or in person. In some teams though, you may be required to create a formal written escalation request with dozens of required fields.

**Requesting L2 Support:**



\* It is generally fine for L1 to request senior support if something is unclear. Especially in your first months, it's always better to discuss the alert and clarify SOC procedures than to blindly close the alert you don't understand yourself. The procedures for requesting support may differ though.

**Communication Cases:**





You need to escalate an urgent, critical alert, but L2 is unavailable and does not respond for 30 minutes.

Ensure you know where to find emergency contacts. First, try to call L2, then L3, and finally your manager.



The alert about Slack/Teams account compromise requires you to validate the login with the affected user.

Do not contact the user through the breached chat - use alternative contact methods like a phone call.



You receive an overwhelming number of alerts during a short period of time, some of which are critical.

Prioritise the alerts according to the workflow, but inform your L2 on shift about the situation.



After a few days, you realise that you misclassified the alert and likely missed a malicious action.

Immediately reach out to your L2 explaining your concerns. Threat actors can be silent for weeks before impact.



You can not complete the alert triage since the logs are not parsed correctly or are not searchable.

Do not skip the alert - investigate what you can and report the issue to your L2 on shift or SOC engineer.

Today, I reported an alert!


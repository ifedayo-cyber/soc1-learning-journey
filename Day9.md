**SOC Workbooks and Lookups**



Today, I learned about **Identity Inventory**. It is a catalogue of corporate employees (user accounts), services (machine accounts), and their details like privileges, contacts, and roles within the company. For example, if we look at an alert and see that G.Baker logged into the HQ-FINFS-02 server. Then, the user downloaded the "Financial Report US 2024.xlsx" file from there and shared it with R.Lund. To correctly triage the alert and understand if the activity is expected, you will have to find answers to many questions:



&#x20;   Who is G.Baker? What are their working hours and role in the company?

&#x20;   What is the purpose and location of HQ-FINFS-02? Who can access it?

&#x20;   Why could R.Lund need access to the corporate financial records?



Identity inventory helps us, in the above scenario, decide whether the activity was expected. 



**Asset Inventory:** Also called asset lookup, is a list of all computing resources within an organization's IT environment. Note that while "asset" is a vague term and can also refer to software, hardware, or employees, this room emphasizes servers and workstations only. For the scenario above, asset inventory would help you get context about the HQ-FINFS-02 server.



I also learnt what a **Network Diagram** is and how it works as a visual schema presenting existing locations, subnets, and their connections.

Moving forward, I learnt how SOC analysts use the **Workbook** when triaging an alert. Below are the steps taken:

**Enrichment:** Use Threat Intelligence and identity inventory to get information about the affected user

**Investigation:** Using the gathered data and SIEM logs, make a verdict if the login is expected

**Escalation:** Escalate the alert to L2 or communicate the login with the user if necessary



By following the steps above correctly, you can guarantee high-quality alert triage and eliminate cases where the verdict is made without enough evidence.

I also practiced building the workbook, and this helped me better understand the concepts learnt today.


**SOAR**

Security Orchestration, Automation, and Response (SOAR) tool overcomes challenges like alert fatigue, manual processes, too many disconnected tools, and difficulties in communication across teams.

The core strength of a SOAR tool comes from the following three main capabilities:



**1. Orchestration**



Traditionally, while investigating an alert, a SOC analyst has to switch between multiple security tools for the analysis. For example, during a VPN brute force, the analyst typically switches between the following tools:



&#x20; **1. SIEM:**  to check if the user usually uses the subject IP for logging

&#x20; **2. Threat Intelligence** (TI) platforms to verify the IP's reputation

&#x20; **3. IAM** tool to disable the user if there was any successful attempt

&#x20;   Ticketing system will open and track the incident



This manual switching between different tools slows down the process. Orchestration solves this problem by coordinating all these tools together inside the SOAR. It connects different tools from various vendors within the unified SOAR interface. It defines workflows for investigating various types of alerts, known as Playbooks. These playbooks are predefined steps that tell the SOAR how to investigate an alert.



For example, the VPN brute force alert we discussed above would have the following playbook:



&#x20;   Received alert from SIEM

&#x20;   Query the SIEM to check if the User normally uses the IP

&#x20;   Check TI platforms for the IP's reputation 

&#x20;   Query SIEM for any successful logins 

&#x20;   Escalate to containment actions



The above actions are predefined in a playbook for a specific alert. These playbooks are dynamic and usually contain different paths. The result of each step determines the next action. For example, if the user normally uses the IP and the failed attempts were minimal, the playbook may stop early. In the upcoming tasks, we will discuss some real playbooks.



**2. Automation**

The art of coordinating with multiple tools through predefined actions (Playbooks), which we studied in Orchestration, can be automated. Automation means no more manual clicks needed from SOC analysts. SOAR will itself follow the playbooks. Let's resume the playbook for VPN brute force alert combined with the Automation.



&#x20;  1. SOAR receives the alert from

&#x20;  2. It automatically queries the SIEM for the user's historical logins

&#x20;  3. It automatically verifies the IP's reputation through TI platforms

&#x20;  4. If the IP is malicious, it automatically disables the user from the IAM

&#x20;  5. Lastly, it automatically opens a ticket in the ticketing system with all the details to initiate an investigation



This saves a tremendous amount of time for SOC analysts. They can handle hundreds of alerts without burning out.



**3. Response**



SOAR gives the ability to take actions using different tools from one unified interface. It also automates the response, as we saw earlier while looking at its Automation capability. For example, SOAR can follow the playbook of VPN Brute force and block the IP on the firewall, disable the user in the IAM, and open a ticket with all the details. 



The Orchestration, Automation, and Response capabilities of SOAR solve the major challenges a SOC team faces. With SOAR, there is no more alert fatigue, most of the processes are automated, and all the different tools are connected for coordination.



**Do We Still Need Analysts?**



While a SOAR tool can automate most repetitive tasks, it does not replace SOC analysts. Complex investigations still require an SOC analyst. SOAR cannot give a judgment call at some critical points, but an analyst can. A SOC analyst understands the threats in the broader business context. The SOC analysts also make the playbooks for different types of alerts. So, the answer to this question is that the SOAR would ease the burden of SOC by automating repetitive tasks and organizing everything in a simplified structure, but we still need SOC analysts.


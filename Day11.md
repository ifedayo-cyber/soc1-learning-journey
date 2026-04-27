**Introduction to EDR**



Today, I learnt more about Endpoint Detection and Response (EDR). Just to summarize, it is a security solution designed to monitor, detect, and respond to advanced threats at the endpoint level. It is essential for a SOC analyst to understand how the EDR works since it is a widely adopted solution in organizations to protect their endpoints. I will discuss how an EDR differs from a traditional antivirus and what data it collects from the endpoints. EDR guards all devices in different areas and is capable of fighting advanced threats. It offers deep-level protection for endpoints, and no matter where the endpoints are, the EDR will make sure they are monitored constantly, and threats are detected. Some of the EDR solutions in the market are:

**CrowdStrike Falcon**

**SentinelOne ActiveEDR**

**Microsoft Defender for Endpoint**

**OpenEDR**

**Symantec EDR**



**FEATURES/PILLARS OF THE EDR SOLUTION:**



1. **Visibility:** A good analysis often depends on the available level of visibility of the activity. This is one of the features of EDR that makes it unique from other endpoint security solutions. The level of visibility provided is impressive. It collects detailed data from the endpoints, which includes process modifications, registry modifications, file and folder modifications, user actions, and much more. It then presents this information in a very structured format to the analyst. The analyst can see the whole process tree with a complete activity timeline of the sequence of actions. The analyst can also access the historical data of any endpoint for threat hunting or any other purpose. Any detections in the EDR land with a whole context.



1. **Detection:** The detection feature of EDR wins over traditional detection capabilities. It incorporates signature-based detections as well as behavior-based detections, such as unexpected user activities. With modern machine learning capabilities, it identifies any deviation from the baseline behavior and instantly flags it. It can also detect fileless malware that resides in memory. It also allows us to feed custom IOCs for threat detections.
2. &#x20;**Response:**  EDR also empowers analysts to take action on detected threats. These actions can be taken at any endpoint within the central EDR console. Imagine getting a detection on the EDR with full-fledged details on when, where, and what happened, and you have to opt for the best possible action for that detection. As an analyst, you may decide to isolate a complete endpoint, terminate a process, or quarantine some files. You can also connect to the host remotely and execute actions independently. You can do this all from within the EDR console.



However, keep in mind that EDR is a host-only security solution and does not detect network-level threats. An Antivirus (AV) may detect some basic threats, but to detect advanced threats that evade normal detections, we need an EDR. It monitors and records the behaviors of the endpoint. It also provides organization-wide visibility of any activity.

**Agents:**
We can integrate multiple endpoints with our EDR and manage them through a centralized console. There are EDR agents that we have to deploy inside those endpoints. These agents are also sometimes referred to as sensors. They are the eyes and ears of the EDR. Their job is to sit at the endpoint and monitor all the activities. The information about these activities is sent in detail to the EDR central console in real time. The EDR agents can do some basic signature-based and behavior-based detections by themselves and send them to the EDR console, which triggers alerts.



**EDR CONSOLE:**
All the detailed data sent by the EDR agents is correlated and analyzed through complex logic and machine learning algorithms. The threat intelligence information is matched with the collected data. The EDR is just like the brain connecting all the dots. These dots connect to form a detection, often called an alert.



**Telemetry**: It is the black box of an endpoint with everything necessary for detection and Investigation. EDR collects detailed telemetry from the endpoints. Below are some collected telemetry:

**Process Executions and Terminations**

It keeps track of all the running and idle processes, which helps to identify suspicious child-parent process relationships, suspicious executables initiating a process, malware payload, etc.

**Network Connections**

All the endpoints' network connections are monitored, which helps identify any connection to a C2 server, unusual port usage, data exfiltration, or lateral movement within the network.



**Command Line Activity**

It captures all the commands executed on the endpoints in CMD, PowerShell, etc., which helps to identify malicious command execution and obfuscated PowerShell script executions, which are often missed by traditional antivirus software.



**Files and Folders Modifications**

Threat actors modify different files and folders during data staging, ransomware executions, and malicious file dropping. The EDR tracks this.



**Registry Modifications**

The registry is a goldmine of information about the configurations in a Windows system. Many registry modifications occur during a malicious activity, and most of these are monitored by the EDR.



**DETECTION**
Based on the telemetry received from the endpoints, some advanced detection techniques are applied to this data. Some of these techniques include:



&#x20;   **Behavioral Detection**

&#x20;   Instead of just matching the signatures with known threats, it observes the complete behavior of a file. Advanced threats craft their malware to look clean and use legitimate processes to carry out their attack. EDR catches this behavior.
Example: A process winword.exe spawning PowerShell.exe will be flagged due to the behavior. A Word document spawning a PowerShell is an unusual parent-child relationship.



**Anomaly Detection**

With time, EDR understands the baseline behavior of the endpoints. Any activity that deviates from this behavior will be flagged. During any malicious activity, the endpoint's behavior deviates from normal. EDR picks it up. Sometimes, this can generate false positives as well. However, with the full context it gives, the analyst can identify its legitimacy.

Example: On one of the endpoints, a process modifies an auto-start registry key, which is not a common behavior on the endpoint.

**IOC matching**
EDRs have some strong threat intelligence field integrations. Except for zero-day attacks, most of the attacks have indicators published in the threat intelligence feeds. EDR flags any activity that matches any known IOC.  Example: A user downloads a file that drops an executable. The executable is often used in a specific attack. The hash of this executable will get matched with the threat intelligence feed and instantly flagged by the EDR.



**MITRE ATT\&CK Mapping**
Any activity flagged by the EDR is not only marked as malicious or suspicious but also mapped with the MITRE Tactic and Technique (attack stage) that the particular activity was on. This proves to be very helpful for the analysts.

Example: If the EDR flags the creation of a scheduled task for any reason, it will likely map this activity to the following:



&#x20;   Tactic: Persistence

&#x20;   Technique: Scheduled Task/Job



**Machine Learning Algorithms**

Advanced threat actors try to evade defenses as much as possible, and their activities may sometimes bypass advanced detection techniques. Modern EDRs have machine learning models trained by a large dataset of normal and malicious behaviors. This can detect complex patterns of an attack.

Example: Attacks in which the individual actions are not inherently malicious, but the ML algorithm identifies the whole chain of activities as malicious. Fileless attacks and multi-staged intrusions are often detected through this.





**Response**
The next step after any detection is the response. EDR offers both automated and manual responses. You can make policies to block known malicious behaviors automatically. However, a manual response gives you a wide range of response capabilities. Let's discuss some of them.

**Isolate Host**

During any malicious activity on an endpoint, you can isolate that endpoint from the network through EDR. This is a very effective function for containing malicious activity. Most attacks start from a single endpoint and move laterally to other endpoints to compromise the whole network. Isolating the infected endpoint on time can stop this from happening.

**Terminate Process**

Not every malicious activity requires host isolation. Some hosts run the core business operations, and isolating them can cause more loss than the malicious activity. In such cases, terminating a process is enough to neutralize the malicious activity. The analysts get this option in the EDR. They can terminate any process at any time. This action should be taken consciously since terminating a legitimate process can disrupt the endpoint.

**Quarantine**

If a malicious file comes into the endpoint, it can be quarantined. Quarantine ensures that the file is moved to an isolated location where it can not be executed. The analysts can then review the file to restore or permanently remove it.



**Remote Access**

Analysts can also remotely access the shell of any endpoint. This is often done when the EDR 's built-in response is not enough to take action on a specific activity. Through remote access, analysts can gain deeper visibility into the system or take custom actions within the endpoints. The analysts can also run scripts or collect their desired data from the host through remote access.

**Artefacts Collection**

Sometimes, the analysts may need to extract some data from the endpoints for detailed forensic investigation or reporting for legal actions. Analysts can extract important artefacts from the endpoints without physically accessing the device. The most commonly extracted artefacts include:



&#x20;   Memory Dump

&#x20;   Event Logs

&#x20;   Specific Folder Contents

&#x20;   Registry Hives



At the end of the day, I used an EDR tool to analyze data and give answers to the technical questions provided.



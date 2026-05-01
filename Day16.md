**Cyber Kill Chain**

The term kill chain is a military concept related to the structure of an attack. It consists of target identification, decision, and order to attack the target, and finally the target destruction.

It is designed for the identification and prevention of network intrusions. The cyber kill chain framework defines the steps used by adversaries or malicious actors in cyberspace. To succeed, an adversary needs to go through all phases of the Kill Chain. 

The Cyber Kill Chain will help you understand and protect against ransomware attacks, security breaches, and Advanced Persistent Threats (APTs). You can use the Cyber Kill Chain to assess your network and system security by identifying missing security controls and closing certain security gaps based on your company's infrastructure.

By understanding the Kill Chain as a SOC Analyst, Security Researcher, Threat Hunter, or Incident Responder, you will be able to recognize the intrusion attempts and understand the intruder's goals and objectives. 

Today, I will be learning about the following attack phases:

**1. Reconnaissance:**  is the research and planning phase of an attack against a system or victim. Adversaries use this phase to gather information about their target to inform their next steps. This information can include infrastructure details, employee data, business processes, and exposed technologies. Reconnaissance is often passive and undetected.

**Reconnaissance Types**



&#x20;   **Passive Recon:** This involves having no direct interaction with the target. This may include WHOIS lookups, social media scraping, or reviewing breach data.

&#x20;   **Active Recon:** This involves direct contact with the target with activities such as social engineering, port scanning, banner grabbing, or probing for open services.


**2. Weaponization:** After a successful recon stage, the attacker would work on turning raw information into actionable tools through crafting malware and exploits into a payload. Most attackers usually use automated tools to generate the malware or refer to the DarkWEB to purchase the malware.

**3. Delivery:** This is when the attacker decides to choose the method for transmitting the payload or the malware onto the target environment. There are plenty of options to choose from: 



&#x20;  Phishing email: after conducting the reconnaissance and determining the targets for the attack, the malicious actor could craft a malicious email that would target either a specific person (spear phishing attack) or multiple people in the company. The email would contain a malicious link or email attachment that would result in a compromise.



&#x20;   USB drops offer the attacker a physical delivery medium into public places like coffee shops, car parks, or on the street. An attacker might decide to conduct a sophisticated USB Drop Attack by printing the company's logo on the USB drives and mailing them to the company while pretending to be a customer sending the USB devices as a gift.



&#x20;   Watering hole attacks are targeted and designed to aim at a specific group of people by compromising the website they are usually visiting, redirecting them to a malicious website of the attacker's choice or creation. Victims would unintentionally download malware or a malicious application to their computer, resulting in a drive-by download. An example can be a malicious pop-up asking to download a fake Browser extension.

**4. Exploitation:** Exploitation is the moment the attacker's code executes on the target, taking advantage of a known vulnerability. In this phase, the attacker can opt to utilise several key techniques to gain access:



&#x20;   Malicious macro execution: This may have been delivered through a phishing email that would execute ransomware when the victim opens it.

&#x20;   Zero-day exploits: These leverage unknown and unpatched flaws in a system. These exploits leave no opportunity for detection at the beginning.

&#x20;   Known CVEs: The attacker can choose to exploit unpatched public vulnerabilities found on the target environment.



After gaining access to the system, the malicious actor could exploit software, system, or server-based vulnerabilities to escalate privileges or move laterally through the network. 



Signs of exploitation to look out for include:



&#x20;   Unexpected process spawns.

&#x20;   Registry changes or new services created.

&#x20;   Suspicious command-line arguments found in system logs.



**5. Installation:** As you have learned from the Weaponization phase, the backdoor lets an attacker bypass security measures and hide the access. A backdoor is also known as an access point.



Once the attacker gets access to the system, he would want to reconnect to the system if he loses the connection to it or if he gets detected and got the initial access removed. Or if the system is later patched, they will no longer have access to it. That is when the attacker needs to install a persistent backdoor (opens in new tab). A persistent backdoor will let the attacker access the system he compromised in the past.
The persistence can be achieved through: Installing a web shell on the web server, installing a backdoor on the victim's machine, creating or modifying Windows services, adding an entry to the "run keys" for the malicious payload in the Registry or the Startup Folder.
In this phase, the attacker can also use the Timestomping (opens in new tab) technique to avoid detection by the forensic investigator and also to make the malware appear as a part of a legitimate program. The timestomping technique lets an attacker modify the file's timestamps, including to modify, access, create, and change times.

**6. Command and Control:** After getting and executing the malware on the victim's machine, the attacker opens up the C2 (Command and Control) channel through the malware to remotely control and manipulate the victim. This term is also known as C\&C or C2 Beaconing as a type of malicious communication between a C\&C server and malware on the infected host. The infected host will consistently communicate with the C2 server; that is also where the beaconing term came from. 



The compromised endpoint would communicate with an external server set up by an attacker to establish a command \& control channel. After establishing the connection, the attacker has full control of the victim's machine. Until recently, IRC (Internet Relay Chat) was the traditional C2 channel used by attackers. This is no longer the case, as modern security solutions can easily detect malicious IRC traffic. 

**7. Actions on Objectives(Exfiltration):** After going through six phases of the attack, the attacker can finally achieve his goals, which means taking action on the original objectives. With hands-on keyboard access, the attacker can achieve the following: 



&#x20;   Collect the credentials from users.

&#x20;   Perform privilege escalation (gaining elevated access like domain administrator access from a workstation by exploiting the misconfiguration).

&#x20;   Internal reconnaissance (for example, an attacker gets to interact with internal software to find its vulnerabilities).

&#x20;   Lateral movement through the company's environment.

&#x20;   Collect and exfiltrate sensitive data.

&#x20;   Deleting the backups and shadow copies. Shadow Copy is a Microsoft technology that can create backup copies, snapshots of computer files, or volumes. 

&#x20;   Overwrite or corrupt data.






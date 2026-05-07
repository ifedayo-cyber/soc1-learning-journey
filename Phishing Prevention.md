**Phishing Prevention**



**Sender Policy Framework (SPF)** is used to authenticate the sender of an email. With an SPF record in place, Internet Service Providers can verify that a mail server is authorized to send email for a specific domain. An SPF record is a TXT record containing a list of the IP addresses that are allowed to send email on behalf of your domain.”



**Tools**

**SPF Surveyor:** It is a tool from dmarcian that enables us to gain a visual look at DNS records. It also helps ensure the record uses the correct syntax.



**DomainKeys Identified Mail (DKIM)**

DKIM stands for DomainKeys Identified Mail and is used for the authentication of an email that’s being sent. Like SPF, DKIM is an open standard for email authentication that is used for DMARC alignment. A DKIM record exists in the DNS, but it is more complex than SPF. DKIM’s advantage is that it can survive forwarding, which makes it superior to SPF and a foundation for securing your email.”



**Domain-based Message Authentication, Reporting, and Conformance (DMARC):**

It is an open source  standard, uses a concept called alignment to tie the result of two other open source standards,  SPF (a published list of servers that are authorized to send email on behalf of a domain) and DKIM (a tamper-evident domain seal associated with a piece of email), to the content of an email.”



This means that DMARC ensures the sender's domain matches the domains verified by SPF and DKIM. If the alignment fails, DMARC instructs the recipient server on how to handle the email based on a policy specified in the record.



M**odern Solutions to enhance email security and reduce phishing risks**

**1. Email Filtering:** Provides filtering based on IP and domain reputation, allowing for blocking or quarantining of suspicious messages.



**2. Secure Email Gateways (SEGs):** Scan messages to detect impersonation attempts, spoofing, and other phishing techniques that other filters might miss.



**3. Link Rewriting:** Replaces suspicious or unknown URLs with safe, redirected ones, giving the system time to scan and verify the link.



**4. Sandboxing:** Isolates and tests suspicious links or attachments in a secure, virtual environment to check for malicious behavior.


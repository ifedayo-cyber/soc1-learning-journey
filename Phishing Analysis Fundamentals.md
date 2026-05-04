**Phishing Analysis Fundamentals**

Spam and Phishing remain the most common social engineering threats facing modern organizations. While spam is often low-risk, phishing can trick users into disclosing sensitive information or unknowingly deploying malware. A single unsuspecting user who clicks a malicious link or opens an attachment can give an attacker an initial foothold in the network and cause huge damage to the company.



As a defender, your role involves analyzing email components to determine if they are malicious or benign and gathering information to help harden security measures against future attacks. 

Anatomy of an Email Address



So what makes up an email address? Let's take a look at the example below, where an email is composed of the following elements:



&#x20;   Username: User mailbox that identifies the specific recipient’s mailbox on the email server

&#x20;   @ symbol: Separates the username from the domain and tells the system where to route the email

&#x20;   Domain name: Specifies the mail server responsible for receiving the message


A helpful analogy is to think of an email address as a home mailing address:



&#x20;   The domain is like the street or apartment building

&#x20;   The username is the specific person or mailbox within that location



With both pieces of information, the postal worker (mail server) knows exactly where to deliver the message. In the next task, we’ll explore the network protocols responsible for sending and receiving emails.

When you send an email, several protocols work together behind the scenes to deliver your message from sender to recipient, and each protocol has a specific role:
Simple Mail Transfer Protocol (SMTP): Sends emails
Post Office Protocol (POP3): Downloads emails to a device
Internet Message Access Protocol (IMAP): Syncs emails across devices

When receiving emails, your email service will use either POP3 or IMAP, depending on how your mailbox is configured. Let's take a look at both of these protocols below: 



POP3 
   Emails are downloaded and stored on a single device

&#x20;   Sent messages are stored on the single device from which the email was sent

&#x20;   Emails can only be accessed from the single device to which the emails were sent

&#x20;   Emails are typically removed from the server after download




IMAP

&#x20;   Emails are stored on the server and can be downloaded to multiple devices

&#x20;   Sent messages are stored on the server

&#x20;   Syncs messages across multiple devices

&#x20;   Emails remain on the server unless explicitly deleted


To break it down:
SMTP is the protocol responsible for sending an email from a client to a mail server


DNS is the service used to look up the recipient domain's mail server

IMAP is the protocol used to access email from multiple devices, including phone and laptop.



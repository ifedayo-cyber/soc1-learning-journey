**Phishing Emails**

Attackers use tactics to mirror legitimate communication

Phishing techniques used:

Spoofed Email Address: Mimicking a trusted service to gain immediate credibility

URL shortening: Using redirection services to hide the true destination of a link

Branded HTML: Impersonating legitimate corporate imagery to create a sense of authenticity



**FIRST OBSERVATIONS DEMO SAMPLE**

Attention-grabbing subject line: The subject line uses a fake transaction to create a sense of urgency, prompting you to react in haste

From address: This is an immediate red flag as the sender details "service@paypal.com" do not match the actual address gibberish@sultanbogor.com

To address: This is an unusual email recipient address and not a normal Yahoo domain



**EMAIL BODY ANALYSIS**

Taking a look at the email body below, we can see that this is a receipt for a purchase of gift cards. The email is designed to appear as a legitimate email from PayPal. There aren't any attachments associated with this email, and the only interactive element in this email is the Cancel the order button. Let's take a closer look.



**BUTTON INVESTIGATION**



By inspecting the raw source of the email, we can further investigate the hyperlinks and underlying HTML that form the message. The Cancel the order button leads to the shortened URL. Because the attacker is using a URL shortening service, the final destination is obfuscated, making it impossible to verify the landing page at a glance. As a rule of thumb, you should never interact with buttons or links without first confirming exactly where they lead. 


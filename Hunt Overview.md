# In this demo, I created a hunt in Microsoft Sentinel to proactively look for potential phishing attacks in my test company.
## Hypothesis: users in the company might be receiving suspicious emails that are parts of a phishing attack.
## Indicators of the attack: I assumed that such indicators can be the words ""urgent", "verify", "password", "action required" and the presence of a link in the email.
## MITRE ATTACK tactic: TA0001: Initial Access - technique: T1566: Phishing.
## I designed a query via KQL to look for these events. See the "KQL query" file to see in detail how I constructed the query for the hunt. 
<img width="2770" height="1456" alt="Image 5-4-26 at 10 58" src="https://github.com/user-attachments/assets/e4b89100-c105-4ed2-8a6f-11f8ae84b32f" />

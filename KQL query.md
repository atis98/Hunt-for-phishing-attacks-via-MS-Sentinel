Query used for the hunt: <img width="1382" height="735" alt="Screenshot 2026-04-05 at 13 58 47" src="https://github.com/user-attachments/assets/f0fd6112-1736-4de5-86be-2a4a959372dc" />
It consists of 2 tables that I combined with the "join" operator. 
First, I queried the "EmailEvents" table to look for emails that users in our company received, which:
- came from external sender (not from our domain)
- arived within the last 24 hours
- contain key words that are typical for phishing emails, these are "urgent", "verify", "password", "action required".

Second, I queried the "EmailUrlInfo" table to look for those emails that contain a link.

Lastly, I joined these 2 tables, so if there is a result event (a suspicious mail), in case there is a link in it, it gets resolved into the corresponding URL based on its network message ID.
This is useful to immediately see if there is something suspicious about the URL itself (e.g. insecure protocol like http).

Both data tables provide events because I enabled the Microsoft Defender for Office connector for MS Sentinel.

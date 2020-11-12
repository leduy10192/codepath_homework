# Honeypot Assignment

**Time spent:** **10** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** I use Google Cloud Platform(GCP) to deploy MHN-Admin
<img src="http://g.recordit.co/gmTqdsImpI.gif">

### Dionaea Honeypot Deployment (Required)

**Summary:**  Dionaea is a low-interaction honeypot used to capture attack payloads and malwares.

<img src="http://g.recordit.co/gkH3QewxD3.gif">

After 24 hours, it was able to capture almost 53,000 attacks:

<img src="http://g.recordit.co/o3ofcQNX0l.gif">

### Database Backup (Required) 

**Summary:** 
- MHN-Admin uses MongoDB to store data. That's why we can get data in a more JSON-friendly way.
- The JSON file records information about id, protocol, hpfeeds id, source id, source port, destination port and identifier.
- File session.json has been uploaded to my GitHub repo as proof of work.

### Deploying Additional Honeypot(s) (Optional)

#### Snort and ElasticHoney Honeypot
**Summary:** 
- Snort is an "open source intrusion prevention system capable of real-time traffic analysis and packet logging." 
- ElasticHoney is a "simple elasticsearch honeypot designed to catch attackers exploiting RCE vulnerabilities in elasticsearch."

<img src="http://g.recordit.co/I2prHHC2mx.gif">



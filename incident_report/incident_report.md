# Security Incident Report

## Section 1: Identify the network protocol involved in the incident

The security incident involved two main network protocols: DNS and HTTP. The DNS protocol was used to resolve the domain names to their corresponding IP addresses. This occurred when the browser first requested the IP address for yummyrecipesforme.com, and later when it requested the IP address for greatrecipesforme.com after the malicious redirect. The HTTP protocol was used to send the requests and receive responses between the browser and both websites, including the download of the malicious file. Additionally, the TCP protocol facilitated the connection by establishing the necessary handshake between the client and the server before the HTTP traffic took place.

## Section 2: Document the incident

The website yummyrecipesforme.com was compromised following a successful brute force attack against its administrative account. The attacker, a former employee, exploited the fact that the account still had a default password set. After gaining access to the admin panel, the attacker modified the website’s source code by embedding a malicious JavaScript function. This code prompted visitors to download an executable file disguised as a browser update. Once executed, the file redirected visitors from the legitimate website to a fake site, greatrecipesforme.com, which contained additional malware. The attacker then changed the admin password to lock out legitimate administrators. The compromise resulted in customer complaints, with users reporting that they were asked to download files and that their systems began running slowly after visiting the site. During the investigation, tcpdump logs confirmed the sequence of events: a DNS request for yummyrecipesforme.com, an HTTP request to load the page, initiation of the malicious download, followed by DNS and HTTP requests to the malicious redirect site.

## Section 3: Recommend one remediation for brute force attacks

To prevent brute force attacks in the future, the company should implement account lockout policies. This would limit the number of incorrect password attempts allowed before the account is temporarily disabled or requires additional verification to unlock. Enforcing strong, unique passwords and disabling default credentials on all administrative accounts would further strengthen security. These measures would make it significantly harder for attackers to succeed in brute force attempts.

# Activity: Apply OS Hardening Techniques

## Section 1: Identify the Network Protocol Involved in the Incident

The network protocol involved in this incident is the Hypertext Transfer Protocol (HTTP).  
Since the affected system is the company’s main website, 
`yummyrecipesforme.com`, all communications between users and the web 
server occur through HTTP traffic. When the cybersecurity analyst ran 
the network analyzer tool tcpdump while visiting the website, the 
captured logs confirmed the use of HTTP for data transmission. The malicious 
executable file was delivered to users’ computers through this same HTTP 
protocol operating at the application layer.

---

## Section 2: Document the Incident

Multiple customers contacted the company’s helpdesk to report that when visiting the 
website, they were prompted to download a file that supposedly contained exclusive 
recipes. After running the file, they noticed that their computers became unusually 
slow and that the website address redirected to another domain, `greatrecipesforme.com`.

The website owner attempted to log into the admin panel but found that their 
credentials no longer worked. In response, the cybersecurity team created a sandbox 
environment to safely test the issue without risking the company network. Within this 
environment, the analyst executed tcpdump while accessing the website and observed 
that a file download prompt appeared immediately upon page load. Once the analyst ran 
the downloaded file, the browser redirected automatically to `greatrecipesforme.com`.  

A detailed inspection of the tcpdump logs revealed the following sequence:
1. The browser initiated a DNS request for the domain `yummyrecipesforme.com`.  
2. Once the IP address was received, an HTTP request was sent to load the webpage.  
3. The browser initiated a download for an executable file hosted on the same domain.  
4. Upon execution, the malware redirected the browser to `greatrecipesforme.com`, triggering new DNS and HTTP traffic to the malicious site.  

A senior analyst examined the website’s source code and discovered unauthorized 
JavaScript embedded in the HTML files. This script prompted users to download a fake 
browser update, which was actually malware. Further investigation confirmed that the 
attacker gained admin access by performing a brute force attack on the server’s 
administrative login. The use of a default password allowed the attacker to easily 
gain control, change credentials, and upload the malicious code.  

---

## Section 3: Recommend One or More Remediations for Brute Force Attacks

To prevent future brute force attacks and strengthen system defenses, the following OS hardening measures are recommended:

1. **Enforce Strong Password Policies:** Require complex passwords that include a mix of letters, numbers, and special characters. Default and previously used passwords should be permanently disallowed.  
2. **Implement Account Lockout Controls:** Automatically lock accounts after a limited number of failed login attempts to prevent automated password guessing.  
3. **Require Regular Password Updates:** Force periodic password changes to limit the time window an attacker could exploit compromised credentials.  
4. **Enable Multi-Factor Authentication (MFA):** Add an extra layer of protection by requiring verification through an additional device or one-time passcode (OTP).  
5. **Deploy Intrusion Detection and Prevention Systems (IDS/IPS):** Monitor for repeated login attempts or unusual authentication activity and alert administrators of potential brute force attacks.  

By enforcing these security controls and hardening authentication policies, 
the organization can significantly reduce its exposure to brute force attacks 
and maintain the integrity of its web services.

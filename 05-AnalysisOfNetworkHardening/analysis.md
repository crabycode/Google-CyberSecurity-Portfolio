# Security Risk Assessment Report

## Part 1: Selected Network Hardening Tools and Methods
Based on the vulnerabilities identified in the organization’s network, the following 
hardening tools and methods are recommended:
1. Implement Multi-Factor Authentication (MFA)  
   MFA requires users to verify their identity using more than one method before accessing an application or network. Common MFA methods include fingerprint scans, ID cards, PINs, and passwords. This adds an additional layer of protection beyond just a password.
2. Enforce Strong Password Policies  
   Password policies can help ensure employees use secure passwords and reduce the likelihood of unauthorized access. Recommended policies include:  
   - Minimum password length requirements  
   - Use of uppercase, lowercase, numbers, and special characters  
   - Regular password updates  
   - Account lockouts after multiple unsuccessful login attempts  
   - Prohibiting password reuse
3. Perform Regular Firewall Maintenance 
   Firewalls must be properly configured to monitor and filter traffic entering and leaving the network. Maintenance tasks include:  
   - Updating firewall rules to reflect current security policies  
   - Blocking suspicious or malicious traffic sources  
   - Reviewing logs for unusual activity  
   - Adjusting configurations after any detected security incidents  

---

## Part 2: Recommendations and Effectiveness

1. Multi-Factor Authentication (MFA)  
   Enforcing MFA reduces the likelihood of unauthorized network access, even if passwords are compromised. Since an attacker would need a second factor to gain entry, MFA makes stolen or shared passwords less useful. Additionally, MFA discourages password sharing among employees, further reducing risk.

2. Strong Password Policies  
   A comprehensive password policy makes it more difficult for attackers to guess or brute-force passwords. Locking accounts after several failed attempts prevents brute-force attacks, while requiring complex and regularly updated passwords reduces the chance of compromised credentials being reused.  

3. Firewall Maintenance  
   Regular firewall maintenance ensures that network traffic is properly filtered, protecting against unauthorized access, malware, and attacks such as Denial of Service (DoS) or Distributed Denial of Service (DDoS). Updating rules in response to new threats ensures the firewall adapts to evolving attack vectors, maintaining network security.

---

### Summary

By implementing MFA, enforcing strong password policies, and maintaining firewalls, 
the organization can significantly reduce the risk of future data breaches. These 
measures collectively address the vulnerabilities of shared passwords, default admin 
credentials, missing firewall rules, and lack of multifactor authentication. 
Regularly applying these hardening methods strengthens the overall security posture of 
the organization and helps protect sensitive customer data.

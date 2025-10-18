# Incident Report Analysis

## Summary
The multimedia company experienced a security event when all network services stopped responding for two hours. The disruption was caused by a distributed denial of service (DDoS) attack using a flood of incoming ICMP packets. The cybersecurity team responded by blocking the attack, stopping all non-critical network services, and restoring critical services to resume normal operations.

## Identify
A malicious actor targeted the company with an ICMP flood attack. 
The attack affected the entire internal network, overwhelming all systems and 
preventing access to critical network resources. Immediate identification of 
the affected systems and the attack vector was necessary to mitigate damage.

## Protect
The cybersecurity team implemented several protective measures to prevent future incidents:  
- Configured a new firewall rule to limit the rate of incoming ICMP packets.  
- Implemented an IDS/IPS system to detect and filter suspicious ICMP traffic.  
- Maintained an updated list of authorized devices and users to ensure proper access control.  
- Hardened network devices by disabling unused ports and services to reduce the attack surface.

## Detect
To identify potential attacks more quickly in the future, the team implemented:  
- Source IP verification on the firewall to detect spoofed ICMP packets.  
- Network monitoring software to track abnormal traffic patterns.  
- Alerting rules on IDS/IPS for unusual ICMP activity or network spikes.

## Respond
The response plan for similar events includes:  
- Isolating affected systems to contain the attack.  
- Restoring critical services first while keeping non-critical services offline.  
- Reviewing logs and traffic data to identify attack patterns and possible sources.  
- Reporting incidents to management and, if necessary, to legal or regulatory authorities.

## Recover
Recovery procedures involve:  
- Restoring full network functionality once the ICMP flood subsides.  
- Gradually bringing non-critical services back online after ensuring the network is secure.  
- Applying lessons learned from the incident to update firewall rules, IDS/IPS configurations, and network hardening policies.  
- Conducting post-incident analysis to improve detection and response strategies for future DDoS attacks.

## Reflections/Notes
This incident highlights the importance of proactive network hardening, 
continuous monitoring, and a clear incident response plan. Limiting unused 
services and implementing robust firewall and IDS/IPS rules are critical to 
minimizing the impact of volumetric attacks like ICMP floods. Regular audits 
and training help maintain readiness for future incidents.

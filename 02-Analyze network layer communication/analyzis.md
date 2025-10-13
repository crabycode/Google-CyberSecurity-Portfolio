# Network Layer Of Communication Alayzis

## Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log

The network protocol analyzer logs indicate that port 53 is unreachable
when attempting to access the company’s public website. Port 53 is 
normally used for DNS (Domain Name System) traffic, which translates
domain names into IP addresses. This indicates a problem with the 
DNS service or server configuration. It is possible that this is an
indication of a DNS outage or firewall issue preventing access to 
the DNS server.

---

## Part 2: Explain your analysis of the data and provide at least one cause of the incident
The incident occurred this afternoon when several customers reported
that they could not reach the website and received an error message
stating “destination port unreachable.” The network security team
investigated the issue using the network protocol analyzer tool 
tcpdump. The resulting logs revealed that the client’s computer 
sent UDP packets to the DNS server at IP address 203.0.113.2, 
attempting to contact port 53, but received ICMP “udp port 53 
unreachable” messages in response. This indicates that the 
DNS server was not responding to DNS queries, preventing domain 
name resolution for the website.

We are continuing to investigate the root cause of the issue to 
determine how to restore access to the DNS service. 
Our next steps include verifying whether the DNS service on 203.0.113.2
is running, checking the firewall rules to ensure that UDP port 53
is open, and testing alternate DNS servers. The security team 
suspects that the DNS server may have been misconfigured, offline,
or blocked by a firewall**, resulting in the failed connections and
the unavailability of the company website.

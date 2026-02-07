devops-ticket-practice-networking-01
New project
DNS Resoulution
Command used:
dig example.com 
Reason: To verify that the domain name resolves correctly to an IP address via DNS.
;; Got answer:
**;; ->>HEADER<<- opcode: QUERY, status: NXDOMAIN, id: 43398**
Conclusion: No DNS issue.

Network Reachability
Command used: 
ping -c 4 example.com 
Reason: To verify that the web service is responding to HTTP requests.
PING example.com (104.18.27.120) 56(84) bytes of data.
64 bytes from 104.18.27.120: icmp_seq=1 ttl=54 time=20.5 ms
64 bytes from 104.18.27.120: icmp_seq=2 ttl=54 time=14.9 ms
64 bytes from 104.18.27.120: icmp_seq=3 ttl=54 time=16.4 ms
64 bytes from 104.18.27.120: icmp_seq=4 ttl=54 time=15.2 ms
Conclusion: The host is reachable and not blocked by network.

Web Service Response
Command used:
curl -I example.com 
Reason: To observe the route taken from the local machine to the website and check for latency or packet loss.
HTTP/1.1 200 OK
Date: Tue, 27 Jan 2026 15:17:03 GMT
Content-Type: text/html
Connection: keep-alive
Conclusion: The web service is responding as expected.

Command used:
Reason: Command was used to make sure the correct site was reached. 
curl -I https://example.com
HTTP/2 200
date: Tue, 27 Jan 2026 15:17:47 GMT
content-type: text/html
Conclusion: The web service is responding as expected.

Network Path
Command used:
traceroute example.com
Reason: To observe the route taken from the local machine to the website and check for latency or packet loss.
traceroute to example.com (104.18.26.120), 10 hops max, 60 byte packets
 1  DESKTOP-VO9S1MC.mshome.net (172.17.192.1)  0.604 ms
 2  192.168.103.1 (192.168.103.1)  2.524 ms
 3  *
 4  80.255.195.132 (80.255.195.132)  19.050 ms
 5  *
 6  80.255.204.49 (80.255.204.49)  19.216 ms
 7  *
 8  141.101.71.63 (141.101.71.63)  34.081 ms
 9  104.18.26.120 (104.18.26.120)  25.130 ms

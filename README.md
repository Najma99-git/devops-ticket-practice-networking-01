# devops-ticket-practice-networking-01
New project
Command used:
dig example.com A
Reason: Used dig A to retrive the short IP address to ask DNS if the network is working as it should. 
;; Got answer:
**;; ->>HEADER<<- opcode: QUERY, status: NXDOMAIN, id: 43398**

Command used: 
ping -c 4 example.com 
Reason: command was used to reach the DNS server. 
PING example.com (104.18.27.120) 56(84) bytes of data.
64 bytes from 104.18.27.120: icmp_seq=1 ttl=54 time=20.5 ms
64 bytes from 104.18.27.120: icmp_seq=2 ttl=54 time=14.9 ms
64 bytes from 104.18.27.120: icmp_seq=3 ttl=54 time=16.4 ms
64 bytes from 104.18.27.120: icmp_seq=4 ttl=54 time=15.2 ms

Command used:
curl -I example.com 
Reason: Command was used to fetch the web server data, the speed of the connection, date and time checked for the connection. 
HTTP/1.1 200 OK
Date: Tue, 27 Jan 2026 15:17:03 GMT
Content-Type: text/html
Connection: keep-alive

Command used:
Reason: Command was used to make sure the correct site was reached. 
curl -I https://example.com
HTTP/2 200
date: Tue, 27 Jan 2026 15:17:47 GMT
content-type: text/html

Command used:
traceroute example.com
Reason: The command was used to trace the hops of the network from my location to the website. 
zsh: command not found: tracepath

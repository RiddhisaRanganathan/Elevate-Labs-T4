# Elevate-Labs-T4 - Firewall

#### Firewall
###### A firewall acts as a security barrier between a trusted internal network and untrusted external networks, such as the internet. 
###### It filters traffic based on a set of predefined rules that evaluate attributes such as IP address, port number, protocol (TCP/UDP), and direction (inbound or outbound). 
###### There are many types of firewalls: 
- Packet Filter Firewall
- Stateful Inspection Firewalll
- Application Firewall
###### The firewall I've used here, Windows Defender Firewall is a stateful inspection firewall that offers context-aware traffic filtering, providing essential security for Windows devices.

#### Commands used:
- List only the test rule created: netsh advfirewall firewall show rule name="Block Telnet"

- Add a rule: netsh advfirewall firewall add rule name="Block Telnet" protocol=TCP dir=in localport=23 action=block

- Test port: Test-netConnection -ComputerName 127.0.0.1 -Port 23

- Remove a rule: netsh advfirewall firewall delete rule name="Block Telnet"

# Elevate-Labs-T4 - Firewall

#### Firewall
###### A firewall acts as a security barrier between a trusted internal network and untrusted external networks, such as the internet. It filters traffic based on a set of predefined rules that evaluate attributes such as IP address, port number, protocol (TCP/UDP), and direction (inbound or outbound). 

#### Commands used:
- List only the test rule created: netsh advfirewall firewall show rule name="Block Telnet"

- Test port: Test-netConnection -ComputerName 127.0.0.1 -Port 23

- Remove rule to restore original state: netsh advfirewall firewall delete rule name="Block Telnet"

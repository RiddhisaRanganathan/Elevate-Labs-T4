# Elevate-Labs-T4 - Firewall

#### Commands used:
- List only the test rule created: netsh advfirewall firewall show rule name="Block Telnet"

- Test port: Test-netConnection -ComputerName 127.0.0.1 -Port 23

- Remove rule to restore original state: netsh advfirewall firewall delete rule name="Block Telnet"

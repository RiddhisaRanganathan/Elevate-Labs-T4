# Elevate-Labs-T4 - Firewall

#### List only the test rule created
netsh advfirewall firewall show rule name="Block Telnet"

#### Add rule to block Telnet
netsh advfirewall firewall add rule name="Block Telnet" dir=in action=block protocol=TCP localport=23

#### Test port (e.g., using Telnet client)
telnet localhost 23

#### Remove rule to restore original state
netsh advfirewall firewall delete rule name="Block Telnet"

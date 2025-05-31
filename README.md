# Elevate-Labs-T4 - Firewall

## Firewall

A **firewall** acts as a security barrier between a trusted internal network and untrusted external networks, such as the internet.  
It filters traffic based on a set of predefined rules that evaluate attributes such as:

- IP address  
- Port number  
- Protocol (TCP/UDP)  
- Direction (inbound or outbound)  

### Types of Firewalls

- **Packet Filter Firewall** – Examines packets in isolation using basic rules.  
- **Stateful Inspection Firewall** – Tracks the state of connections and applies rules based on context.  
- **Application Firewall** – Operates at the application layer and inspects traffic for specific services.

The firewall used in this task is **Windows Defender Firewall**, which is a **stateful inspection firewall**.  
It provides **context-aware traffic filtering**, offering essential protection for Windows devices.

---

## Commands Used

```powershell
# Add a rule to block Telnet (TCP port 23)
netsh advfirewall firewall add rule name="Block Telnet" protocol=TCP dir=in localport=23 action=block

# List the created rule
netsh advfirewall firewall show rule name="Block Telnet"

# Test if port 23 is open (should be blocked)
Test-netConnection -ComputerName 127.0.0.1 -Port 23

# Remove the rule to restore the original state
netsh advfirewall firewall delete rule name="Block Telnet"

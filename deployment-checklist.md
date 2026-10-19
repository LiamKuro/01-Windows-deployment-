Step 1: Baseline Assessment
Purpose- Establish the virtual machine's current configuration before making deployment changes.
Tasks
Check the windows version using winver
Record system information using systeminfo
inspect IP address and DNS settings using ipconfig /all
Record the VM's RAM, CPU, disk size, and netowrk mode
Create a VirtualBox snapshot before making changes

Results
Windows Version is 25H2 Windows 11 Pro 
System Information: 
Host Name:                     WIN11
OS Name:                       Microsoft Windows 11 Pro
OS Version:                    10.0.26200 N/A Build 26200
OS Manufacturer:               Microsoft Corporation
OS Configuration:              Standalone Workstation
OS Build Type:                 Multiprocessor Free
Registered Owner:              leonflame491@gmail.com
Registered Organization:       N/A
Product ID:                    00330-80000-00000-AA402
Original Install Date:         9/12/2026, 4:46:42 AM
System Boot Time:              10/19/2026, 1:38:18 AM
System Manufacturer:           innotek GmbH
System Model:                  VirtualBox
System Type:                   x64-based PC
Processor(s):                  1 Processor(s) Installed.
                               [01]: AMD64 Family 25 Model 33 Stepping 2 AuthenticAMD ~3800 Mhz
BIOS Version:                  innotek GmbH VirtualBox, 12/1/2006
Windows Directory:             C:\WINDOWS
System Directory:              C:\WINDOWS\system32
Boot Device:                   \Device\HarddiskVolume1
System Locale:                 en-us;English (United States)
Input Locale:                  en-us;English (United States)
Time Zone:                     (UTC+01:00) Belgrade, Bratislava, Budapest, Ljubljana, Prague
Total Physical Memory:         8,173 MB
Available Physical Memory:     5,989 MB
Virtual Memory: Max Size:      10,093 MB
Virtual Memory: Available:     8,226 MB
Virtual Memory: In Use:        1,867 MB
Page File Location(s):         C:\pagefile.sys
Domain:                        WORKGROUP
Logon Server:                  \\WIN11
Hotfix(s):                     5 Hotfix(s) Installed.
                               [01]: KB5126052
                               [02]: KB5054156
                               [03]: KB5095189
                               [04]: KB5124008
                               [05]: KB5124007
Network Card(s):               1 NIC(s) Installed.
                               [01]: Intel(R) PRO/1000 MT Desktop Adapter
                                     Connection Name: Ethernet
                                     DHCP Enabled:    Yes
                                     DHCP Server:     10.0.2.2
                                     IP address(es)
                                     [01]: 10.0.2.15
                                     [02]: fe80::39cd:3c9a:eb68:bc06
                                     [03]: fd17:625c:f037:2:815e:e468:8bf8:1028
                                     [04]: fd17:625c:f037:2:ada8:75bc:71ac:60f9
Virtualization-based security: Status: Not enabled
                               App Control for Business policy: Enforced
                               App Control for Business user mode policy: Off
                               Security Features Enabled

IP address and DNS settings results:
Windows IP Configuration

   Host Name . . . . . . . . . . . . : win11
   Primary Dns Suffix  . . . . . . . :
   Node Type . . . . . . . . . . . . : Hybrid
   IP Routing Enabled. . . . . . . . : No
   WINS Proxy Enabled. . . . . . . . : No

Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . : hsd1.md.comcast.net
   Description . . . . . . . . . . . : Intel(R) PRO/1000 MT Desktop Adapter
   Physical Address. . . . . . . . . : 08-00-27-33-5F-DB
   DHCP Enabled. . . . . . . . . . . : Yes
   Autoconfiguration Enabled . . . . : Yes
   IPv6 Address. . . . . . . . . . . : fd17:625c:f037:2:ada8:75bc:71ac:60f9(Preferred)
   Temporary IPv6 Address. . . . . . : fd17:625c:f037:2:815e:e468:8bf8:1028(Preferred)
   Link-local IPv6 Address . . . . . : fe80::39cd:3c9a:eb68:bc06%11(Preferred)
   IPv4 Address. . . . . . . . . . . : 10.0.2.15(Preferred)
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Lease Obtained. . . . . . . . . . : Monday, October 19, 2026 1:38:32 AM
   Lease Expires . . . . . . . . . . : Tuesday, October 20, 2026 1:38:34 AM
   Default Gateway . . . . . . . . . : fe80::2%11
                                       10.0.2.2
   DHCP Server . . . . . . . . . . . : 10.0.2.2
   DHCPv6 IAID . . . . . . . . . . . : 101187623
   DHCPv6 Client DUID. . . . . . . . : 00-01-01-00-32-36-9E-DD-08-00-27-33-5F-DB
   DNS Servers . . . . . . . . . . . : 75.75.75.75
                                       75.75.76.76
                                       fd17:625c:f037:2::3
   NetBIOS over Tcpip. . . . . . . . : Enabled

   VM Ram, CPU, disk size, network node 

   RAM: 8GBS Disk size:80 GBS CPU: 4 cores network node: NAT 

   Network Baseline Assessment
   Command ipconfig /all
   Adapter name: Ethernet
   Adapter description: Intel(R) PRO/1000 MT Desktop Adapter
   Ipv4 address: 10.0,2,15
   Subnet mask: 255.255.255.0
   Default Gateway: 10.0.2.15
   DHCP enabled: Yes
   DNS servers 75.75.75.75, 75.75.76.76
   VirtualBox network node: NAT
   The Ethernet adapter has an IPv4 address and is configured for automatic network settings through DHCP. A default gateway and DNS servers are present.
   This configuration appears consistent with VirtualBox networking. Connectivity and DNS resolution must be tested separately before confirming that network access is working.

   Test Connectivity Results 
   Test 1: Local TCP/IP Loopback
   Command ping 127.0.0.1
   Result passed
   Packets 4 sent, 4 received, 0% loss
   Finding: The local loopback test succeeded

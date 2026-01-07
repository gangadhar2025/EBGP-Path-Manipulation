🚀 BGP Path Manipulation – Dual ISP Enterprise Lab (GNS3)
📌 Project Overview

This project demonstrates a real-world Enterprise + ISP hybrid network design using BGP, OSPF, iBGP, eBGP, DHCP, and Traffic Engineering concepts.

The lab simulates how large enterprises and ISPs implement:

✅ Dual ISP connectivity

✅ BGP path manipulation

✅ Redundancy and high availability

✅ Automatic failover

✅ Enterprise core routing using OSPF + iBGP

This is a production-style design commonly used in MNC and ISP networks.

🏗️ Topology Summary
🔹 Enterprise Core (AS 100)

OSPF used as IGP

iBGP between core routers using peer-groups

Route redistribution between OSPF and BGP

🔹 Upstream Providers

ISP-1 (AS 200) → Primary ISP

ISP-2 (AS 300) → Backup ISP

Both connect to Internet Router (AS 400)

🔹 Services

DHCP Server on R7

DHCP Relay on R6

Branch PCs receive IP dynamically

🎯 Objectives of This Lab

Implement eBGP with dual ISPs

Implement iBGP inside enterprise

Control traffic using BGP attributes

Test failover in real-time

Verify end-to-end connectivity

Simulate real enterprise ISP design

🔧 Technologies Used

BGP (eBGP + iBGP)

OSPF

BGP Peer-Groups

Route Redistribution

DHCP & DHCP Relay

Traffic Engineering

GNS3

🧠 BGP Traffic Engineering Design
✅ Primary Path (ISP-1)

Configured Local Preference = 400

All outbound traffic prefers ISP-1

✅ Backup Path (ISP-2)

Configured AS-PATH Prepending (100 100 100)

Makes this path less preferred

🔁 Failover Testing

Under normal condition → Traffic goes via ISP-1

When ISP-1 link is shut down ❌

Traffic automatically switches to ISP-2 ✅

No connectivity loss observed

🧪 Verification Commands

From client PC:

ip dhcp
ping 5.5.5.5
trace 5.5.5.5


From routers:

show ip bgp
show ip route
show ip bgp summary
show ip ospf neighbor

📂 Repository Contents

📁 GNS3 topology file

📁 Router configuration files

📄 Step-by-step configuration notes

📄 Verification and failover test outputs

🖼️ Topology screenshots

🏆 What This Project Demonstrates

Real-world dual ISP enterprise design

Practical BGP traffic engineering

Integration of OSPF + iBGP + eBGP

High availability and redundancy

Enterprise-grade routing architecture

L3-level troubleshooting and design skills

👨‍💻 Author

Gangadhar

L3 Network Support Engineer

CCNA, JNCIA

Focused on Enterprise & ISP Routing, BGP, OSPF, High Availability Design

📌 Note

This lab is created for:

Interview preparation

Real-world design practice

Demonstrating hands-on networking skills

Portfolio and resume projects

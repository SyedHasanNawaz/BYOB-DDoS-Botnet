🧠 BYOB Botnet Lab – Practical Deployment, Debugging & DDoS Simulation
📘 Overview
This repository documents my hands-on technical journey exploring the BYOB (Build Your Own Botnet) framework. The goal was to understand botnet operations, simulate aspects of Distributed Denial of Service (DDoS) attacks, and gain real-world insight into offensive cybersecurity tools — all within a controlled, private, and ethical lab environment.

The project involved:

Deploying and troubleshooting the BYOB botnet

Choosing the Web GUI interface over CLI for ease of control and visibility

Creating and debugging Python payloads

Planning a DDoS simulation across multiple virtual machines

Researching DDoS scripts used in real-world scenarios, including one sourced from the dark web

Practicing operational security during research using privacy-focused tools

⚠️ DISCLAIMER: All activities were conducted ethically and legally within a secure lab setup. No systems were harmed, and no unauthorized actions were taken.

🧠 Key Definitions
🔗 Botnet
A botnet is a network of compromised machines (bots) controlled remotely by a Command & Control (C2) server. Botnets are used to:

Launch DDoS attacks

Exfiltrate data

Deploy malware across systems

🛠️ BYOB
BYOB (Build Your Own Botnet) is an open-source Python framework allowing users to generate custom payloads, deploy them to victim machines, and control them through either a CLI or a Web-based GUI. I opted for the Web GUI for a more intuitive experience.

🌐 DDoS (Distributed Denial of Service)
A DDoS attack overwhelms a target server with fake traffic from multiple sources, disrupting its availability and performance.

🎯 Project Goals
Deploy the BYOB framework and connect bots (agents) to the central C2 server

Understand how bots are generated, delivered, and remotely controlled

Simulate basic DDoS behavior across isolated virtual machines

Research real-world DDoS tools, including how they are sourced and used

Practice operational security (OPSEC) when researching underground tools

✅ Tasks Completed
🧪 Phase 1: Lab Setup & Initial Testing
Deployed Kali Linux VMs on VirtualBox for a secure lab setup

Installed and configured the BYOB framework

Used the Web GUI interface for managing bots and payloads

Generated Python payloads simulating bot infection

Faced connection issues: Payloads were not communicating with the C2 server

🛠 Troubleshooting Steps
Verified IP and port configurations in the payload

Reviewed GitHub issues and BYOB documentation

Reinstalled BYOB and regenerated payloads

Adjusted NAT, Bridged, and Host-only networking modes

Tweaked firewall and router NAT rules

Result: Partial success — payloads created and deployed, but bots failed to connect back to the C2 server.

⚙️ Phase 2: Payload Debugging
Created a fresh Python virtual environment

Manually installed and pinned specific versions of BYOB dependencies

Re-tested payload behavior in Kali VMs

Discovered the issue: Router-level port blocking prevented bot-C2 communication

Learned that port forwarding was required to allow traffic — but I chose not to modify the company-owned router

❌ Why the Project Was Stopped
Despite substantial progress, the project was intentionally paused due to two major constraints:

🛑 Router Restrictions

The router used was a PTCL business connection

Required admin access to configure port forwarding

Modifying it could interfere with shared network infrastructure — ethically unacceptable

⚖️ Inadequate Scale for DDoS Simulation

Real-world DDoS simulations require dozens/hundreds of bots

My lab had only 2–3 virtual machines, which was insufficient to simulate actual DDoS impact

🧨 Planned Execution Strategy
After successful infection, my plan was to distribute a Python-based DDoS script to all bots via the BYOB C2 server.

💻 What is Sapphire?
Sapphire is a lightweight DDoS attack tool written in Python, capable of launching:

TCP floods

UDP floods

SYN floods

It’s simple to execute across multiple infected agents and was intended to be the final payload for simulating real distributed attack behavior.

🌐 How I Found Sapphire
Driven by curiosity and a desire to understand real attacker workflows, I explored how such tools are sourced in the underground ecosystem.

To ensure anonymity and operational security:

Used Tails Linux — a live OS focused on privacy

Accessed the Tor Network to explore .onion resources

Configured ProxyChains and Tor Bridges to mask identity and avoid surveillance

🔐 All dark web access was for academic research only. No attacks were executed. No real-world targets were involved.

🧠 Skills Practiced
✅ Botnet architecture & payload delivery

✅ BYOB deployment & dependency resolution

✅ Payload debugging & network communication analysis

✅ Virtual machine networking (NAT, Bridged, Host-only)

✅ Router/firewall troubleshooting

✅ OPSEC: Tails Linux, Tor, ProxyChains, Tor Bridges

✅ Understanding of underground tool sourcing

✅ Ethical decision-making in offensive security scenarios

🖥️ Technical Environment
Component Details
Lab OS Kali Linux (VirtualBox)
Research OS Tails Linux (Live Boot)
Botnet Framework BYOB (Build Your Own Botnet)
Payloads Python-based, GUI-generated
Control Interface Web GUI (preferred over CLI)
VMs Used 2–3 Kali VMs
DDoS Script Sapphire (researched, not run)
Privacy Tools Tor, ProxyChains, Tor Bridges

💡 Key Takeaways
Gained hands-on experience in botnet deployment, debugging, and control

Learned how network restrictions can block payload communications

Discovered how attack tools are distributed in real attacker ecosystems

Understood the limits of simulation without large infrastructure

Practiced safe, ethical, and secure offensive research techniques

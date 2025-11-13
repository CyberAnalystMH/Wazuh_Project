WORK IN PROGRESS

Summary
---
Wazuh is my go to SIEM tool. It's fun to use, open-source, well-documented, runs locally on basic hardware and Wazuh is also free. I've been using Wazuh about a year, on and off, just messing around with it. Since I like Wazuh so much, why not make a full comprehensive project. We're going to skip initial installation but still start with a fresh Wazuh installation. This project will also, perhaps help me pass Cysa+ from CompTIA since that specific cert focuses on logs and SIEMs analysis. I'm big on visuals, that's why one of my favorite things in Cybersecurity is pretty much any tool that shows automated charts, graphics, word clouds, etc. 

 Setup
---
**Rules & Objectives:**
- 1 Wazuh Server
- 3 Ubuntu Servers 
- All have FTP, SSH, HTTP open ports
- Kali Machine to Pen-Test Wazuh capabilities
- Document my findings and observations 
- Implement Rules
- Implement Incident Response 
- Implement Diagrams 

**Limitations:** The data I have is sort of limited, in terms the different types of threats. When companies run SIEM solutions on their infrastructure, it's assumed that their servers are public facing, which results the data to be extremely randomized since all threat actors attack differently. None of my agents will be publicly faced, I mainly want to have hands-on experience with basic logs. However, Wazuh has "Sample Data" which adds randomized threat attacks, randomized servers that are being targeted, which can be incorporated with my data to make the SIEM look a little more realistic, more on that later. 

<img width="198" height="278" alt="image" src="https://github.com/user-attachments/assets/0f3c71d3-7b63-4208-b7a8-d16c35cbab39" />

**Annotations:** For some reasons, Wazuh installed on Ubuntu Server wasn't working, so I just installed a minimal version of Ubuntu 22 and it works. 

Summary & Findings
---
<img width="851" height="257" alt="image" src="https://github.com/user-attachments/assets/f40afa11-6302-4d9d-a0a5-b1df4b5cd1bb" />

**Annotations:** Registering machines as agents is easy. Sometimes the agent wouldn't talk to the manager, for some reasons Wazuh labels the IP address of the agent as the manager in /var/ossec/etc/ossec.conf, it needed to be changed for all the agents to be the IP address of the manager. Despite we're not using Windows, however for Windows you run the command that the Wazuh manager provides on Power-shell and it installs a GUI for Wazuh, which is pretty convenient. 


<img width="1124" height="139" alt="image" src="https://github.com/user-attachments/assets/5449b5aa-4c0e-47dc-bab1-6e0e82fd9eee" />

**Annotations:** On the Homepage, the user gets a quick overview of the types of alerts that's Wazuh collecting, depending on the severity of the threat actor. 

**Dashboard 01 - Threat Vector** 
<img width="1820" height="828" alt="image" src="https://github.com/user-attachments/assets/e880acc5-efad-4f51-9d0d-e4a75842d7c5" />

**Annotations:** After attacking all machines with some basic hacking, I built this interesting visualization on Wazuh that let's you use data inputs and results as outputs to make the user understand the data much better. Personally, I think Wazuh tends to generate a lot of false positives with clean installation, it does need a lot of tuning, which will get at a later stage. 

**Dashboard 02 - Attack Volumes** 
<img width="1824" height="826" alt="image" src="https://github.com/user-attachments/assets/a2de3d90-6fb4-4c39-b593-2224675e4476" />

**Annotations:** This visuals shows attack volumes and attacked ports and how many events specified in each Agent. There's many ways to visuals this sort of structure, it's best to choose graphics that can make sense to everyone. 

**Dashboard 03 - SOC Overview** 
<img width="1821" height="829" alt="image" src="https://github.com/user-attachments/assets/14b958fb-4f4f-4d60-a38a-ad8a36780ed0" />


<img width="1794" height="533" alt="image" src="https://github.com/user-attachments/assets/28780cbd-19a7-45b7-967b-515ff83e72c7" />

**Annotations:** My favorite aspect of Wazuh is the "Threat Hunting" tab. Mainly because it gives the user a quick overwrite of any occurring threats, without having the need to make the visuals represented from scratch.

<img width="529" height="192" alt="image" src="https://github.com/user-attachments/assets/e97cbd84-7d35-446c-ba22-025c4bdbe8fe" />

**Annotations:** I added Windows 10 to expand my agents a little. As mentioned, registering Windows as Agent is pretty easy since it comes with a GUI.

<img width="316" height="282" alt="image" src="https://github.com/user-attachments/assets/5dbbc1a3-cb8d-4705-aa1e-7209d8a905d9" />

**Annotations:** Just needed to ensure to change Manager's IP to the actual Manager dashboard. 

<img width="297" height="193" alt="image" src="https://github.com/user-attachments/assets/d0ef0fd1-454b-44b3-b310-fdbe97e17eba" />

**Annotations:** Wazuh includes this cool little interesting Pie chart with OS as output, could be neat for a company with large system inventory to see the difference in OS that are registered to Wazuh. Wazuh can register many systems, Raspberry Pis as well. 

<img width="506" height="198" alt="image" src="https://github.com/user-attachments/assets/1b1f38ff-be33-4acc-b668-1ad38bfc73f0" />

**Annotations:** If you're curious, the graphics and metrics we've made to visuals alerts automatically update when a new agent is registered. 


**Wazuh Integration Capabilities:** 
- Suricata 
- Email alerts
- Slack
- VirusTotal
- AI
- SOAR


VirusTotal Integration
---



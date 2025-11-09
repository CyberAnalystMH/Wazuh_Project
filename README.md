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

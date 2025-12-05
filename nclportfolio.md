# National Cyber League Portfolio – Fall 2024  
Created by Matthew E. Johs
----------------------------------------
## Why I Became Interested in Cybersecurity
My career path hasn’t been linear. I started in chemical engineering, served in the Navy, and eventually realized that the one field where my analytical strengths, structured thinking (ISTJ), and love of problem-solving truly aligned was cybersecurity.

After discovering SANS, earning GSEC, GCIH, and completing Network+ and Security+, I found that Capture The Flag competitions like NCL gave me the first environment where all of that knowledge came together in a hands-on, applied way. CTFs don’t reward memorization. They reward persistence, pattern recognition, strategic thinking, and a willingness to fail fast and try again. That is where I thrive.
----------------------------------------
----------------------------------------
## Reflection on My NCL Experience
NCL was one of the most valuable practical experiences I have had so far. It exposed me to real-world problems in OSINT, forensics, network analysis, web exploitation, cryptography, password cracking, enumeration, and log analysis.

Some examples of challenges I worked through this season:

- OSINT Investigations  
  Creativity mattered more than tools. Pivoting through username reuse, metadata leakage, old domain registrations, EXIF artifacts, and historical caches helped me understand how intelligence workflows actually function.  
  Learning Outcome: Learned the power of publicly available information and the importance of operational security.

- Web Application Enumeration and Exploitation  
  Identifying hidden directories, analyzing HTTP response behavior, bypassing simple authentication, spotting parameter injection issues, and effectively using Burp Suite were major milestones for me.  
  Learning Outcome: Understood the critical importance of input validation and secure coding practices.

- Password Cracking  
  Building custom wordlists, using rule-based attacks, hybrid attacks with mangling rules, and optimizing Hashcat jobs taught me how attackers think and how defenders should respond.  
  Learning Outcome: Discovered that standard wordlists with proper rule transformations often outperform overthought custom lists. Learned to balance themed approaches with practical methodology.

- Network Forensics  
  PCAP analysis in Wireshark, filtering traffic, reconstructing malware downloads, identifying command-and-control patterns, and carving files helped me connect my SANS coursework to applied skills.  
  Learning Outcome: Developed expertise in reconstructing attacker activities from network traffic and identifying indicators of compromise at the packet level.

- Log Analysis  
  Working with SSH logs, Windows Event Logs, and web server logs helped me see how defenders identify lateral movement and detect anomalies that would otherwise be lost in noise.  
  Learning Outcome: Mastered the ability to quickly process massive log files to identify security incidents and piece together attack timelines.


NCL also helped me benchmark my progress in a measurable, competitive environment. It showed me exactly where I was strong (OSINT, forensics, enumeration) and where I needed to sharpen my skills (advanced web exploitation and more complex binary reversing).
----------------------------------------
----------------------------------------
## NCL Scouting Report
NCL Fall 2025 Individual Game Scouting Report
http://cyberskyline.com/report/A9GP2AXVG5X4

NCL Fall 2025 Team Game Scouting Report 
http://cyberskyline.com/report/0BCC1VN14XQG
----------------------------------------
----------------------------------------
NCL Fall 2025 Season

Individual Game: Competed across 9 challenge categories
Team Game: Collaborative competition solving 39 challenges (188 total questions)
Environment: Kali Linux ARM64 on Apple Silicon (VMware Fusion Pro)
----------------------------------------
----------------------------------------
## Highlights From My CTF Participation

1. Successfully cracking multiple challenge passwords using a combination of Hashcat rulesets, hybrid mask attacks, and custom-built wordlists based on contextual clues discovered in challenge artifacts.

2. Reconstructing a malware drop from a PCAP by identifying suspicious HTTP traffic, carving out payloads, verifying indicators, and connecting the behavior to real incident response workflows.

3. Completing multi-stage OSINT investigations by following usernames across platforms, pivoting on domains and MX records, uncovering hidden profiles, and using cached snapshots to find historical information.

4. Completing my first full NCL Team Game and learning how to divide tasks, communicate findings, and manage time in a competitive, high-pressure environment.

5. Applying SANS-level skills from GSEC, networking fundamentals, and my degree coursework directly to live competition problems in areas like Wireshark analysis and vulnerability assessment.
----------------------------------------
----------------------------------------
Notable Challenge Solutions

1. Password Cracking – LM/NTLM Hash Recovery
Challenge: Recover three user passwords from Windows LM/NTLM hash dumps by identifying patterns and optimizing attack methods.

Summary of Approach:
- Split and cracked LM halves (case-insensitive, 7-character chunks)
- Detected password pattern: six lowercase letters followed by two digits
- Used LM results to guide NTLM mask construction
- Ran targeted mask: ?l?l?l?l?l?l?d?d

    Outcome:
    All three passwords recovered in under ten minutes.

2. Mainframe Forensics – RACF Password Recovery
Challenge: Extract and crack a RACF password from an encoded XMI mainframe dataset.

Summary of Approach:
- Base64 decoded the XMI to access the NETDATA structure
- Identified and extracted a ZIP archive encoded in EBCDIC (cp037)
- Located RACF hash for FIREID2
- Applied rockyou.txt with uppercase transformation rules
- Cracked the password VIPER1, which matched the challenge’s theme

    Outcome:
    Successfully reconstructed the data workflow and recovered the RACF password.
----------------------------------------
----------------------------------------
Problem-Solving Methodology
My approach to CTF challenges follows a systematic pattern:

- Initial Assessment: Quickly evaluate challenge requirements and available resources
- Efficiency-Focused: Prioritize direct solutions over lengthy explanations
- Systematic: Break complex challenges into manageable components
- Iterative: Test hypotheses quickly and adjust based on results
- Tool Selection: Choose the right tool for the job (hashcat vs John, etc.)
- Time Management: Prioritize easier challenges to maximize points under competition constraints

    Outcome:
    A consistent approach that reduces wasted effort, improves accuracy, and increases overall competition performance.
----------------------------------------
----------------------------------------
Competition Strategy
Through NCL competitions, I learned that success requires:

- Balancing speed with accuracy when attempts are limited
- Knowing when to pivot from complex custom solutions to reliable, proven methods
- Maintaining composure under time pressure
- Leveraging team strengths during collaborative challenges
- Continuously learning from both successes and failures

    Outcome:
    Strengthened strategic decision-making and adaptability in high-pressure scenarios.
----------------------------------------
----------------------------------------
Professional Development
My participation in NCL complements my formal cybersecurity education:

- Completed: CompTIA Security+ and Network+
- Current: SANS Bachelor's in Applied Cybersecurity
- Developing practical, hands-on skills beyond theoretical coursework
- Building real-world problem-solving experience through CTFs
- Creating a portfolio of demonstrated competencies for future roles
- Networking with other cybersecurity participants in the NCL community

    Outcome:
    Reinforced academic learning with applied experience, improving technical capability and professional readiness.
----------------------------------------
----------------------------------------
Key Takeaways
The most important lessons from my NCL experience include:

- Efficiency Over Complexity: Direct, simple methods often outperform overengineered solutions
- Practical Security Skills: Hands-on exposure to real tools and workflows
- Analytical Thinking: Applying structured reasoning to multi-step challenges
- Verification Matters: Always validate data before processing (e.g., hash transcription issues)
- Context Awareness: Understanding challenge themes improves success rates
- Tool Mastery: Deep skill with a few tools is more effective than superficial knowledge of many
- Persistence: Systematic troubleshooting and alternate methods overcome dead ends

    Outcome:
    A clearer understanding of how cybersecurity principles translate to real investigations, attacker behavior, and defensive analysis.
----------------------------------------

This portfolio represents my journey through competitive cybersecurity and demonstrates practical skills in offensive security, digital forensics, and threat analysis. The challenges completed reflect real-world scenarios in penetration testing, incident response, and security operations.
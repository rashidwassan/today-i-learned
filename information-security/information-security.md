# Information Security

## Introduction

### Three objectives of IT Security:
- Confidentiality
- Integrity
- Availability


### Three Foundations of IT Security
- People
- Processes
- Technology


Section 3
The threat environment:
Attackers & Their Attack

The Threat Environment:
The world today is a dangerous place for corporations.
Access to billions of customers & business partners through the internet.
The Internet gives criminals access to millions of firms and individuals. 
Wireless transmission, along with mobility, allows attackers a stealthy entrance, bypassing firewalls.
Information about the “threat environment” is necessary to defend a firm.
It is like ‘understanding your enemy’.
Unless you understand threats, you cannot prepare defense.
The threat environment consists of attackers and types of attacks.

Basic Security Terminology :
Security Goals:
Conditions that the security staff wish to achieve.
Corporations & their sub corporations have security goals.
Three common goals (CIA): 
Confidentiality: people cannot read sensitive information while on the computer or traveling in a network.
Integrity: attackers cannot change or destroy information. If destroyed or modified, the receiver can know about it and restore.
Availability: authorized people can access data without issues.
Compromises:
Successful attacks; incidents; breaches.
Successful threat causing damage to a business is called an incident, breach, or compromise.
In terms of a business process model, threats push businesses away from goals.
Companies face several breaches every year, despite avoiding them.
Response to incidents is critical.
CERT - Computer Emergency Response Team.
Sitting at SOC (Security Operation Center).
They check security inside the network.
Digital Forensic is a way to find and deal with those situations.

Countermeasures:
Tools used to prevent attacks.
Also called safeguards, controls, protections.
Can be technical, human or a mixture of both.
People process & technology.
People: need to be trained on policies and procedures. No one can steal data using USB.
Process: define guidelines for tasks. Sharing of passwords should not be allowed in the organization.
Technology: NAC (network access controller) sits in the network, provides authentication in the network using mac addresses. Example: Identity and access management system. Lots of users are able to perform various tasks, CEO has previlliegs so do the other managers.
Goal of countermeasures is to keep business on track despite threats and actual compromises.
Types of countermeasures:
Preventative: avoid threats from succeeding.
Detective: if threat is succeeding, take measures to minimize the damage.
Corrective: getting back on track after being compromised. The faster the business gets back on the track, the more likely business goals will be met.

The Tjx Data Breach
Multinational group of 2500+ retail stores (aka Marshalls).
Discovery: On December 18, 2006. Tjx detected “suspicious software” on their systems. They called security experts who confirmed intrusion and probable data loss. Tjx notified law enforcement immediately. Customers were notified a month later.
Two attacks (2005 & 2006). 45.7 million records and much more data was stolen.
The Break-Ins: broke into poorly protected wireless networks in retail stores & broke into a central processing system in Massachusetts. 80gb of size but still not detected.
Canadian privacy commission: poor encryption, keeping worthless data.
(PCI - DSS) Payment Card Industry - Data Security Standard
Rules for credit card purchases. Non compliant systems may lose the ability to process cards.
12 required control objectives. Tjx was not  compliant and met only 3/12 objectives. Visa gave extension to Tjx in 2005, subject to progress report in 2006.

The Fall-Out: Lawsuits and Investigations:
40.9 million dollars for settlement with banking associations. Visa imposed $880,000 fine.
Proposed settlement with customers.
Under investigation by the U.S Federal Trade Commission & 37.
$256 million in damages till August 2007.


Chapter 4

Employee & Ex-Employee Threats:
Are ‘insiders’ the biggest threats?
Threats can be from two sides (Internal or External attack).
For home security, the guard knows insights.
Employees & Ex-Employees are Dangerous:
Because: knowledge of internal systems, permissions to access systems, know how to avoid detection, are trusted.
IT and especially IT professionals are the great employee threats.
They have credentials.
In IT, no proper computer knowledge is needed for breach.
In 1996 to 2002, 23 financial cyber crimes happened. 87% were done without high knowledge of computers.
The US Department of Justice (cybercrime.gov), have roughly more than half attacks listed, belonging to IT Employees or ex-employees.

The Employee Sabotage:
Destruction of hardware, software or data. Plant time or logic bomb in computer.
Sabotage = shoe (French), In the French revolution, workers threw their shoes into machines to halt the process.
Employee Sabotage Example:
Tim Lloyd, a computer systems administrator, was fired for being threatening and disruptive. He, before firing, planted a logic bomb, when certain conditions were met. Logic bomb destroyed the systems which operated manufacturing machines. He also erased backup disks.
Loss: $10m immediate business loss. $2m reprogramming cost. 80 layoffs.
Damaged competitive status in high-tech instruments as the company could not rebuild its proprietary software.
Employee Sabotage Example 2:
Two Traffic Engineers in Los Angeles, hacked the traffic system and disconnected traffic signals at 4 LA’s busiest intersections. They locked out the controls, 4 days to take control back.
Few hours before their union’s job against the city in support of contract negotiations.
Penalty: 240 days of community service. Had their computer work at home, and with monitoring.

The Employee Hacking:
Hacking: intentional accessing of computers without or excess of authentication.
First use of word ‘Hacking’, Steve Levy’s book ‘Hackers’ in 1984.
Penalties are the same for huge breaches or mere testing.
Access has to be intentional, damage does not.

Employee Financial Theft:
Misappropriation of assets (assigning them to themselves using computers),
Theft of Money (manipulation of application for illegal bonuses)
Two Accountants in Cisco Systems, illegally accessed a corporate computer and issued themselves $8m worth of Cisco Stocks.
Case: Quintigua Sabathia, 31, of Vallejo, California. Stole $0.875m from the North Bay Health Care Group. A former Accounts Payable Clerk at North Bay. Accessed the firm's accounting software and issued 127 checks payable to herself and others. To hide, she altered the record to make it appear that the checks were payable to the company's vendors.
Employee Theft of Intellectual Property:
Intellectual property is information owned by a company and protected by law.
Copyrights and Patents (formally protected),
Trade Secrets: plans, formulations, business processes which company keeps secret from competitors.
Example:
Former DuPont Researcher admitted downloading trade secrets worth $400m. He downloaded 16,700 documents. Most of those documents had nothing to do with his research area.

Employee Extortion:
Threatening to take actions against the victim's interest, for money or goods.
Logic bomb intallation.
Stealing Intellectual Property and blackmailing.

Harassment of Other Employees:
Via-Email
Displaying Inappropriate Material
Example:
Washington Leung left a firm and logged in it’s servers using his credentials. Deleted 900 files related to employee compensation. To accuse a female co-worker, he gave her $40k annual raise, and $100k bonus. He created a hotmail account in the name of that female employee and sent info from deleted files to senior managers.

Other Types of Abuse:
Internet Abuse: Downloading inappropriate material, which can lead to harassment lawsuits and viruses. Pirated Software, music, video. Excessive personal use of the internet at work.
Non-Internet Computer Abuse: unauthorized access to private data of other employees in internal systems. A survey of 300 senior IT administrators in London found that one in three admitted looking at irrelevant confidential info.

Carelessness:
Loss of computers or sensitive data. Information theft.
Ponemon Survey: 2008: 630,000 laptops lost at airports. Losing USB drives can be just as damaging.

Other Internal Attacks:
Contract workers, workers in contracting companies.
They’re often given credentials which are not deleted after the engagement ends.
Claude Carpenter planted logic bomb. Damaging US Internal Revenue Services.



Traditional External Attackers

Send malware. Hack computers.
Malware: Evil software. Viruses, trojan horses, RATs, spam. Serious threats. Very serious threat. In 2006, 5 million machines examined had 16 million pieces of malware.
Viruses: Attach to legitimate programs. Spread with infected files. Spread by e-mails, instant messaging, file transfer, downloads. Case: Adobe CS4 crack in BitTorrent.
 Worms: Full programs, not attached to others. Spreads like a virus.
Direct-Propagation Worms: spread rapidly without human intervention, vulnerable computers. A worst case worm can do $50B to the US alone.
Slammer Worm: 2003 slammer worm explosion impacting 90% vulnerable computers.
Blended Treats: propagates in multiple ways. 1% of all mails were infected in 2006.
Payloads: Pieces of code that do damage. Malicious payloads are very dangerous.
Nonmobile Malware: Must be placed on a computer.
Trojan Horses: Replaces a file, taking its name. Remote Access Trojans (RATs). Downloaders. Spyware (gathering information), Cookies, Keystroke loggers, password stealing spyware, data mining spyware.









Traditional External Attackers:
SLIDE #6


Trojan Horses:
Rootkits: takes control of super user accounts, hide themselves, can hide malware, difficult to detect. Sony BMG.
Mobile Code: dow
nloaded webpage can execute code.
Social Engineering in Malware: Convincing someone to take security countermeasures.
Spam: bane of all sms is spam, it can be annoying. Vehicle for malware, in 2009, 73% of mails were spam.
Phishing: Misleading mails and webpages to fool victims and getting sensitive information from them. Spear Phishing aims to target individuals or groups.
Hoaxes: sulfnbk.exe told computers that a virus called AOL.exe.
Some survey data:
Spam: 86%
Virus: 1/347.2
Phishing: 1/615
Approx 7000 new malware sites everyday.




Hackers
SLIDE #7

Traditional Hackers:
Motivated by thrill, validation of skills, sense of power. Trying to increased reputation among other hackers. Engaged in petty crime.
Anatomy of Hack: Reconnaissance probes (fig in slides)
IP Address to scan potential victims.
Identify active hosts
Echo response.
Port 80 for http. Ranges from 0 to 1023.
More content will be added soon.



### Cryptography
Definition & Concepts: 
Data on computers is protected by logical & physical access controls.
While data travels, it is vulnerable.
Encryption: transforms plaintext to ciphertext. Enables transfer of confidential info on unsecure media.
Cryptosystem: provides encryption & decryption. Uses algorithms (set of rules) which are complex mathematical formulas. Contents of a cryptosystem:
Software 
Protocols
Algorithms
Keys
Key: long string of bits. It is the secret piece of a well-known encryption algorithm. It is a cryptovariable.
Algorithm contains a keyspace.
Today, 128, 256, 512, or even 1024 bits keys are used.
Kerckhoffs’ Principle:
Auguste Kerckhoffs in 1883: only secrecy involved in the cryptography system should be the key. Algorithms should be publicly known. More secrets, more vulnerable the system.
Important elements of encryption:
Algorithm without flaws
Use large key size
Use all keys within the keyspace
To protect the actual key.


Services of Cryptosystems:
Confidentiality: renders the information unintelligible except by authorities.
Integrity: data immutability.
Authentication: verify the user.
Authorization: users will be provided with a key, to access resources.
Nonrepudiation: sender cannot deny sending the message.

### For Final Exams


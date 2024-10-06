# Attack Life Cycyle

- From hardware, to software, to personal, the initial compromise phase begins by exploiting some weakness.
- once system has been compromised next step to take controle
- attacher till take the data outside of the organiztion

## Well define security policy

- A comprehensive security policy critical for the org to ensure for identification mitigation and response to a data breach, instrusion, or other attacher internal or external.
- Employee negligence and internal threat should be weight haveily when drafiting any policy.
- checklist shold be create to perform the proper procedure
- keep hard copy in safe place as well, technology companies keep only electronic data but if that system compromise

## Frequent Backups

- backup not only allow DR/COOP but greatly in the forensive investigation process
- back should be store both locally and offsite 50 miles as per rule
- Regular DR/COOP drills are enssential to ensure both readiness of personal to respond to an incident, as well as discover any flows or errors in both procedure and haredware software media.
- even more robus ot RAID system can be failure, any critical data should be part of backup

## Law Enforcement

- who to call and when the key component in any good security policy, but unfortunately it is also one of the more difficult question to anser.
- a goog security policy will provide the guidelines.
- look for [seclists.org](seclists.org)

## Kill Chain

- Kill chain or cyber kill chain, is attack progression. This refer to steps by malicius operator in order to compromise a target.
- Reconnaissance --> Weaponization --> Delivery --> Exploitations --> Installation --> Command/Control --> Actions/Objectives.
- Reconnaissance: research, identification and selection of the target, ofetn represt as crawling internet websites, such as conference proceedings and mailing list, social relationshiot or interformatio on specfic technologies.
- Weaponization: Coupling a remote access trojan with an exploit into a deliverable payload, typically by means of an automated tools. increasing client application data such as PDF.
- Delivery: Transmission of the weapon to the targeted envirment. The three most prevalen delivery vector for weaponzed payload by APT actors, as email attachmetn, website, usb.
- Exploitation: after delivery the weaponized to the victim host, exploitation triggers the intruders code. Most often exploitation target applicatio, OS, user or something.
- Installation: installtion remote torjon as backdoor to maintain the persistence inside the environment.
- command and control: Typically, compromise hosts must becom outboudn to the internet, it's connect to the C2 channel over the internet and take the control of the machine
- action on objectives: usualy intrudor steam the data from the user host,

## Escalation

- A good securit policy will have all the information
- when the incident happen what steps to take and who should inform
- sentor member work on fix the issue, there should be someone who should alert emergency response team

## Emergency Response Team

- ERT shoudl be well organized with roles and responsibilities
- technical team must jump back to any reference meterial, policies or somehting
- non-technical memeory should have atleast 1 hard copy and checkoist
- regular drills shoudl be conducted with performance expectations clearly stated.
- please read [https://www.csoonline.com/article/2119886/incident-detection--response--and-forensics--the-basics.html](https://www.csoonline.com/article/2119886/incident-detection--response--and-forensics--the-basics.html)

## Post Incidence Forensics

- Immediately Post incident a security incident or data breach a snapshot of the system is question should be created on write only media.
- This critical forensi investigation and analysis as well preserving the chain of custody of evidence in the case where criminial prosecution, legal proceeding, employee termination
- When performing forensic analysis, a live linux CD/DVD is the prefered method for accessing data form the image in question. The image should be mounted readonly, care only to preserver the integrity.
- If the external intrusion is discovered, and the system and network is not critical, disconnect the system from the network or even network gateway if a more wide-spread issue is discovered.

## Host Intrusion Detection System (HIDS)

- Host IDS running on local node, anything lieke agent or cronjob which continuely checks the databases hash or integrity.

## Network Intrusion detection system

- These intrusion system collect the network traffic and analyse the attack surface.
- SNORT is the on of the first such open source application to fill this role.

## Physical Intrustion Detection System

- PIDS are more todo with systems that ensure only authorized users are able to access the systems and environment.

## Machine Learning

- Somewhat self documenting, threat detection is about detection threat, some of which are not obvious.
- staff can monitor traffic but not all the time
- api server audit the logs, sometime request process mistakelnly and want to check where this request coming or
- early stage we can take actions.
- Due to vast amount of information, if unknown thread need to handle by AI or Machine Learning.
- there are some company offering the following solution.
- NeuVector
- StackRox
- Threat Stack
- TrendMicro

## Behavioral Analytics

- The use of automatic system determin the unusaly activity has becom more common.
- Like a process to open file or spawns process it has not worked with in the past, may not common grouping action
- The system may not help part of user activing like open email which has malware

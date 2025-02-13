## 👉 Kaiten Botnet

new and improved version of Kaiten, an Internet Relay Chat (IRC)-controlled malware typically used to carry out distributed denial-of-service (DDoS) attacks. The remastered malware has been dubbed “KTN-Remastered” or “KTN-RM”, with three versions of Linux/Remaiten already identified by ESET researchers. Based on artifacts in the code, the main feature of the malware is an improved spreading mechanism.
Based primarily on Linux/Gafgyt’s telnet scanning, KTN-RM improves on that spreading mechanism by carrying downloader executable binaries for embedded platforms such as routers and other connected devices. Targeting mainly those with weak login credentials.

„Further, the downloader‘s job is to request the Linux/Remaiten bot binary from the Command & Control server for its current architecture. When executed, it also creates another bot for the malicious operators to use. We have seen this technique used before by Linux/Moose to spread infections,“ says Michal Malík, ESET Malware Researcher.

## 👉 Lizard squad botnet
Lizard Squad was a black hat hacking group, mainly known for their claims of distributed denial-of-service (DDoS) attacks[1] primarily to disrupt gaming-related services.

On September 3, 2014, Lizard Squad seemingly announced that it had disbanded[2] only to return later on, claiming responsibility for a variety of attacks on prominent websites. The organization at one point participated in the Darkode hacking forums and shared hosting with them. their targets;
League of Legends DDoS,
Destiny DDoS,
PlayStation Network DDoS,
Xbox Live DDoS,
The Machinima Hack,
North Korea DDoS,
Christmas attacks:
(Lizard Squad had previously threatened to take down gaming services on Christmas),
Malaysia Airlines website attack,
Daybreak Games DDoS.

## 👉 Moobot botnet
A variant of the Mirai botnet known as MooBot is co-opting vulnerable D-Link devices into an army of denial-of-service bots by taking advantage of multiple exploits. MooBot, first disclosed by Qihoo 360's Netlab team in September 2019, has previously targeted LILIN digital video recorders and Hikvision video surveillance products to expand its network. In the latest wave of attacks discovered by Unit 42 in early August 2022, as many as four different flaws in D-Link devices, both old and new, have paved the way for the deployment of MooBot samples. These include -

    CVE-2015-2051 (CVSS score: 10.0) - D-Link HNAP SOAPAction Header Command Execution Vulnerability
    CVE-2018-6530 (CVSS score: 9.8) - D-Link SOAP Interface Remote Code Execution Vulnerability
    CVE-2022-26258 (CVSS score: 9.8) - D-Link Remote Command Execution Vulnerability, and
    CVE-2022-28958 (CVSS score: 9.8) - D-Link Remote Command Execution Vulnerability
    
Successful exploitation of the aforementioned flaws could lead to remote code execution and the retrieval of a MooBot payload from a remote host, which then parses instructions from a command-and-control (C2) server to launch a DDoS attack on a specific IP address and port number.

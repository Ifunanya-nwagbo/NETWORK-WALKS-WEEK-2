# NETWORK-WALKS-WEEK-2
FOOTPRINTING AND RECONNAISSANCE.

## LIABILITY DISCLAIMER
I have carried out these research on systems and devices that I own or on which I have obtained formal and legal authorization from Networkwalks. All of these resources are solely for educational and research purposes. Nothing from here was and should be used to violate the law. What you do with this information is not the responsibility of the instructor, the writers, or Networkwalks. You are accountable for every action you take. Misuse can result in a permanent record, severe fines, job loss, and criminal charges. Unauthorized access is illegal in the majority of countries, even if no harm is done.

## INTRODUCTION
This report includes using multiple Kali Linux tools to footprint the networkwalks.com domain (W2-PM1) and using Google hacking database (GHDB) to research sensitive information accidentally left public by companies (W2-PM2). Information like camera feeds, login pages and so on. Together, with this two modules: both covering the scanning and the foot printing phase, I have successfully illustrated how an attacker proceeds from obtaining public data . I'm in the second week of my ongoing internship at Network walks. All commands were executed on a Windows computer running on GHDB (scanning) and in Kali Linux (footprinting). The precise command used, the outcome I saw, a screenshot as proof, and a brief explanation of the significance of the discovery from the perspective of an attacker are all included in each step below.

## TOOLS INCORPORATED
Below is a table list of each tool used in the course of my research and report.

### Tools Incorporated

Below is a list of each tool and operating system used in the course of my research and report.

| Tools | Purpose |
| :--- | :--- |
| **Kali Linux and Windows** | Operating systems utilized in reconnaissance operations. |
| **WhatWeb** | Web technologies for fingerprinting (server, CMS, plugins, IP). |
| **Nslookup** | Use DNS to resolve the domain name to its IP address. |
| **WHOIS** | Discover the owner, dates, and name servers of the domain registration. |
| **`curl -I`** | Examine the website's HTTP response headers. |
| **Wafw00f** | Check to see if the website is protected by a Web Application Firewall (WAF). |
| **DNSRecon** | List every DNS record (NS, MX, SPF, TXT, SRV). |
| **Google Hacking Database (GHDB)** | Utilized to locate sensitive, vulnerable, or publicly accessible information on the internet. |
| **Live cam** | To capture live cameras. |

## ACTIVITIES CARRIED OUT
Footpriniting and Reconnaissance
I used six Kali Linux tools including WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon, to conduct reconnaissance against the networkwalks.com domain. A different kind of information about the target was gathered using each tool.
 
I started by using WHOIS to find the domain's name servers and access publicly accessible domain registration data. The findings revealed details regarding the hosting infrastructure and domain registration.
 
Furthermore, I identified the website's technologies using WhatWeb. Along with other data made public by the website, the results revealed WordPress 7.1.4 , WP Download Manager 3.3.76, jQuery 3.7.1 and Bootstrap 7.1.4.
 
Also, I resolved the domain name to its IP address using Nslookup.  192.232.216.135 was found in the result gotten.

## FOOTPRINTING AND SCANNING WITH GHDB
Google Hacking Database (GHDB) is a huge database of pre-made search queries referred to as Google dorks. These are the use of normal Google search operators in inventive ways to extract sensitive data accidentally left behind by a site for example, video feed from a camera that hasn't been covered up, directories, login pages, config files and documents. The security/penetration testing community has developed GHDB.

### Some Live Vulnerable Cameras:

| No | Link | Relevant Dork | Username / Password |
| :--- | :--- | :--- | :--- |
| 1 | `http://109.233.191` | `https://exploit-db.com` | No password |
| 2 | `http://204.106.237` | `http://204.106.237` | No password |
| 3 | `http://153.156.82` | None | No password |
| 4 | `http://212.41.248` | None | No password |
| 5 | `http://72.17.65` | `http://72.17.65` | No password |
| 6 | `http://77.37.212` | None | No password |
| 7 | `http://50.236.229` | None | No password |
| 8 | `http://93.181.81` | `http://93.181.81` | No password |
| 9 | `http://buffalotrace.com` | `http://buffalotrace.com` | No password |
| 10 | `http://dy.fi` | None | No password |


### Some Listings Containing Downloadable Mathematical PDFs

| # | Link | Relevant Dork | Username / Password |
| :--- | :--- | :--- | :--- |
| 1 | `https://giakonda.org.uk` | Giakonda Solar School | No password |
| 2 | `https://giakonda.org.uk` | Solar School | No password |
| 3 | `https://giakonda.org.uk` | University of Mexico | No password |
| 4 | `https://ochicken.net` | Index of library | No password |
| 5 | `https://case.edu` | Case Western Reserve University | No password |
| 6 | `https://wvfa.org` | West Virginia Forestry Association | No password |
| 7 | `https://cmu.edu` | Carnegie Mellon University | No password |

---

### Risk Analysis / Impact

From the information gathered in the footprinting and network scanning operations, I came up with the following potential risks:

| # | Risk | Observation | Potential Impact | Severity |
| :--- | :--- | :--- | :--- | :--- |
| **1** | Web technology information was exposed | **WhatWeb** found WordPress and WP Download Manager. | Vulnerable technology/version information can be used to search for software that needs to be reviewed for additional security. | 🟠 **MEDIUM** |
| **2** | The IP address of the server is known | **Nslookup** resolved the domain to `192.232.216.135`. | Provides information about the network location of the web service. | 🟡 **LOW** |
| **3** | Technical information about HTTP revealed | **Curl** returned the headers of the HTTP response and exposed the `/wp-json/` report. | May be able to help with technology fingerprinting and more enumeration. | 🟡 **LOW** |
| **4** | WAF technology identifiable | **Curl** returned the headers of the HTTP response and exposed the `/wp-json/` resource. | Shows understanding of how the Web application is secure. | 🟡 **LOW** |
| **5** | Several hosts that are connected to the local network are visible | **Wafw00f** recognized that this is ModSecurity (SpiderLabs). | The knowledge of DNS information can be utilized in creating a more extensive profile of an infrastructure. | 🟠 **MEDIUM** |


The risks listed above are a result of the footprinting and scanning activities but do not indicate vulnerabilities.
The focus of the practical exercises was on information gathering and footprinting. These two modules did not include any validation of exploitation or vulnerability.
The existence of information, like software version, IP address or DNS record, does not really bring to a conclusion that the system is vulnerable. Additional permission for security testing would be needed to verify if there is any known or unknown vulnerability.
 

 ## RECOMMENDATIONS
The following security changes or upgrades are recommended, based on the aforementioned activities:
• Inspect technology information that is publicly exposed.

• Organizations should routinely audit the information that is publicly visible for their web technologies, CMS and plugins.

• Keep company softwares updated.

• CMS platforms, plugins and other web technologies need to be updated and checked for current security advisories.
• Review HTTP headers.

• HTTP Response Headers should be inspected to see if there is any unnecessary information being shared.

• Regularly check DNS records.

• DNS records should be looked at periodically to make sure only services and information that are needed are public.


## CONCLUSION
I finished hands-on exercises in network scanning, footprinting, and reconnaissance during the second week of my internship in cybersecurity and ethical hacking with Networkwalks.
        I gathered data on the target domain in the footprinting exercise using six Kali Linux tools. I discovered that Wafw00f can detect a WAF, DNSRecon can offer more DNS information, WhatWeb can identify web technologies, Nslookup can resolve domain names, Curl can examine HTTP headers, and WHOIS can provide domain information.
     I further used GHDB to find vulnerable hosts and sensitive information exposed on the internet using my LAN for the network scanning exercise.

## EVIDENCES COLLECTED

<img width="1161" height="489" alt="IMG_7756" src="https://github.com/user-attachments/assets/95448eee-6dd5-4156-acdd-dda1e13b3dd0" />


<img width="1421" height="292" alt="IMG_7757" src="https://github.com/user-attachments/assets/54e0aca8-53c3-4fa1-9eef-3672f8b28c5f" />


<img width="1062" height="327" alt="IMG_7758" src="https://github.com/user-attachments/assets/71a9ec3a-59d8-42f3-85d2-5b66098d184b" />


<img width="1023" height="343" alt="IMG_7759" src="https://github.com/user-attachments/assets/b4cecbba-8b52-48a8-b159-dfb55aed313e" />




<img width="1137" height="663" alt="IMG_7763" src="https://github.com/user-attachments/assets/433349ad-29a8-4722-8631-a96b0e3c176e" />


<img width="1296" height="796" alt="IMG_7762" src="https://github.com/user-attachments/assets/cb1c8d99-590d-4606-bfb5-ab6f15c7a6ac" />

















### 👤 Author & Project Information

| Category | Details |
| :--- | :--- |
| **Author** | Lilian Nwagbo |
| **Title** | Cybersecurity Professional B084 |
| **LinkedIn** | [linkedin.com/in/ifunanya-nwagbo-mit](https://www.linkedin.com/in/ifunanya-nwagbo-mit/) |
| **Program Name** | Cybersecurity program at Networkwalks |
| **Week** | 02 |
| **Repository** | GitHub |








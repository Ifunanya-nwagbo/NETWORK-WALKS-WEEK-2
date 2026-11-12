# NETWORK-WALKS-WEEK-2
FOOTPRINTING AND RECONNAISSANCE 

## LIABILITY DISCLAIMER
I have carried out these research on systems and devices that I own or on which I have obtained formal and legal authorization from Networkwalks. All of these resources are solely for educational and research purposes. Nothing from here was and should be used to violate the law. What you do with this information is not the responsibility of the instructor, the writers, or Networkwalks. You are accountable for every action you take. Misuse can result in a permanent record, severe fines, job loss, and criminal charges. Unauthorized access is illegal in the majority of countries, even if no harm is done.

## INTRODUCTION
This report includes using multiple Kali Linux tools to footprint the networkwalks.com domain (W2-PM1) and using Google hacking database (GHDB) to research sensitive information accidentally left public by companies (W2-PM2). Information like camera feeds, login pages and so on. Together, with this two modules: both covering the scanning and the foot printing phase, I have successfully illustrated how an attacker proceeds from obtaining public data . I'm in the second week of my ongoing internship at Network walks. All commands were executed on a Windows computer running on GHDB (scanning) and in Kali Linux (footprinting). The precise command used, the outcome I saw, a screenshot as proof, and a brief explanation of the significance of the discovery from the perspective of an attacker are all included in each step below.

## TOOLS INCORPORATED
Below is a table list of each tool used in the course of my research and report.

### 3) Tools Incorporated

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

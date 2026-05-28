# ICT171 Cloud Server Project - International Student Hub

## Student Details

Name: Ashmandeep Kaur  
Student ID: 35680945  
Unit: ICT171 Introduction to Server Environments and Architectures  

## Project Links

Live website: https://internationalstudenthub.site  
Server status page: https://internationalstudenthub.site/server-status.html  
GitHub repository: https://github.com/ashman1019/ICT171-Cloud-Server-Project  

## Server Details

Public IP address: 40.81.23.165  
DNS entry: internationalstudenthub.site  
Cloud provider: Microsoft Azure  
Server type: Infrastructure as a Service  
Virtual machine name: ict171ash  
Operating system: Ubuntu Server 24.04 LTS  
Web server: NGINX  
SSL/TLS: Let's Encrypt certificate  
License: MIT License  

## Video Explainer

Video link: https://youtu.be/Hi-efGWbZC0

## Project Overview

My project is called International Student Hub. It is a simple website made to provide useful information for international students.

The website includes information about living expenses, study tips, work and visa guidance, and general student life tips.

I hosted this website on a Microsoft Azure Linux virtual machine. I used SSH to connect to the server and used NGINX as the web server. I also connected my domain name to the server and enabled HTTPS using a Let's Encrypt certificate.

## Purpose of the Project

The purpose of this project is to create a basic support website for international students. International students may need help with understanding living costs, study expectations, part-time work rules, and adjusting to a new place.

This website gives simple information in one place so students can access it easily.

## Website Functionality

The website is now structured as a multi - page website . the main homepage links to separate pages for that  currently include
- Living Expenses
- Study Tips
- Work and Visa Guidance
- Tips and Tricks
- Server Status output page
- Original Proposal backup page


## Server Setup

I created an Ubuntu virtual machine in Microsoft Azure. After connecting to the server through SSH, I updated the server and installed NGINX.

Commands used:

```bash
sudo apt update
sudo apt install nginx-full
sudo systemctl status nginx
```

The website files are stored in:

```bash
/var/www/html/
```

The main website file is:

```bash
/var/www/html/index.html
```

## DNS Setup

My domain name is:

```text
internationalstudenthub.site
```

The domain is managed through Namecheap.

I updated the DNS A records so the domain points to my Azure public IP address.

DNS records used:

```text
A Record    @      40.81.23.165
A Record    www    40.81.23.165
```

I tested the DNS using:

```bash
nslookup internationalstudenthub.site 8.8.8.8
```

The result showed:

```text
Address: 40.81.23.165
```

This confirmed that the domain was pointing to the correct Azure server.

## SSL/TLS Setup

HTTPS was enabled using a Let's Encrypt certificate.

The secure website link is:

```text
https://internationalstudenthub.site
```

I checked that NGINX was listening on ports 80 and 443 using:

```bash
sudo ss -tulpn | grep -E ':80|:443'
```

I also tested the website using:

```bash
curl -I https://internationalstudenthub.site
```

A successful result showed:

```text
HTTP/1.1 200 OK
```

## Bash Script

I created a Bash script called:

```text
server_status.sh
```

The purpose of this script is to create a simple server status webpage. The script checks server information and writes it into an HTML file.

The script checks:

- Current date and time
- Hostname
- Domain name
- Public IP address
- Server uptime
- Disk usage
- Memory usage
- NGINX status

The script was made executable using:

```bash
chmod +x server_status.sh
```

The script was run using:

```bash
sudo ./server_status.sh
```

The script creates this output file:

```bash
/var/www/html/server-status.html
```

The script output can be checked online here:

```text
https://internationalstudenthub.site/server-status.html
```

This script is useful because it shows basic server health information on the website.

## Server Testing

I tested that NGINX was running using:

```bash
sudo systemctl status nginx --no-pager
```

I tested DNS using:

```bash
nslookup internationalstudenthub.site 8.8.8.8
```

I tested HTTPS using:

```bash
curl -I https://internationalstudenthub.site
```

I also opened the website and the server status page in a browser to confirm that both pages were working.

## Development Notes

- March 2026: Project idea and proposal prepared.
- April 2026: Website content and project plan prepared.
- May 2026: Azure Ubuntu virtual machine configured.
- May 2026: NGINX installed and website files added.
- 19 May 2026: DNS records updated to point to the Azure public IP address.
- 19 May 2026: HTTPS tested and working.
- 19 May 2026: Bash server status script created and tested.
- 19 May 2026: GitHub repository created and documentation updated.

## References

Microsoft Azure documentation: https://learn.microsoft.com/en-us/azure/  
NGINX documentation: https://nginx.org/en/docs/  
Let's Encrypt documentation: https://letsencrypt.org/docs/  
Certbot instructions: https://certbot.eff.org/  
Namecheap support: https://www.namecheap.com/support/  
ICT171 weekly lab notes and unit materials  

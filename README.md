# ICT171 Cloud Server Project - International Student Hub

## Student Details

**Name:** Ashmandeep Kaur  
**Student ID:** 35680945  
**Unit:** ICT171 Introduction to Server Environments and Architectures  

## Live Server Details

**Live website:** https://internationalstudenthub.site  
**Public IP address:** 40.81.23.165  
**DNS entry:** internationalstudenthub.site  
**Cloud provider:** Microsoft Azure  
**Server type:** Infrastructure as a Service (IaaS)  
**Virtual machine name:** ict171ash  
**Operating system:** Ubuntu Server 24.04 LTS  
**Web server:** NGINX  
**SSL/TLS:** Let's Encrypt certificate  
**License:** MIT License  

## Video Explainer

Video link: To be added before final submission.

## Project Overview

The International Student Hub is a cloud-based website designed to provide basic support information for international students. The website includes information about living expenses, study tips, work and visa guidance, and practical student advice.

This project was created using a Linux virtual machine hosted on Microsoft Azure. The server was configured manually through SSH using command-line tools. NGINX was installed as the web server, DNS was configured through Namecheap, and HTTPS was enabled using a Let's Encrypt SSL/TLS certificate.

## Project Purpose

The purpose of this project is to create a simple online support platform for international students. As an international student, I understand that adjusting to a new country can involve challenges such as managing living expenses, understanding work rules, balancing study, and finding useful support information.

This website provides a central place where students can access simple and practical guidance.

## Website Functionality

The website currently includes:

- Project introduction
- Student and unit details
- International student support information
- Living expense guidance
- Study tips
- Work and visa guidance
- Tips and tricks for student life

## Server Setup Summary

The cloud server was created using Microsoft Azure. The virtual machine was configured as an Ubuntu Linux server.

Basic server setup commands used:

```bash
sudo apt update
sudo apt install nginx-full
sudo systemctl status nginx

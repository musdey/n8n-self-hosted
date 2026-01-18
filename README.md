# n8n Docker Compose with SSL

This repository provides a **ready-to-use Docker Compose setup** to self-host **n8n** on your own server using **Docker**, **Nginx**, and **Let’s Encrypt (Certbot)**.

It is designed for simple, secure, and production-ready deployments.

## ✨ Features

- Self-hosted **n8n** automation platform
- **Nginx** as reverse proxy
- Automatic **HTTPS (SSL)** via Let’s Encrypt
- Automatic certificate renewal using Certbot
- Persistent n8n data storage
- Basic authentication enabled
- Clean and minimal Docker Compose setup

## 🧩 Services Included

- **n8n** – workflow automation tool  
- **nginx** – reverse proxy with HTTPS  
- **certbot** – SSL certificate issuance and renewal  

## 🚀 What this setup does

- Exposes n8n securely via HTTPS
- Uses your own domain
- Automatically renews SSL certificates
- Stores all n8n data persistently on the host machine

## ⚠️ Before using

You **must** update the following values before deployment:

- Domain name (`example.com`)
- Email address for Let’s Encrypt
- n8n basic authentication credentials
- Strong password for n8n
- Volume paths if needed

## 🔐 SSL Certificate (First Run)

Before starting the stack, you need to generate the initial SSL certificate using Certbot (standalone mode).  
A helper command is included as a comment in the `docker-compose.yml`.

## 📦 Usage

```bash
docker-compose up -d

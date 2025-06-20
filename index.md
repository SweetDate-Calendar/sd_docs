---
title: Home  
layout: home
nav_order: 1 
---


# Chronopipe – A Modular Headless Calendar Platform

> *A developer-first, headless calendar platform for seamless integration across applications.*

---

## 🧱 What Is Chronopipe?

Chronopipe is a modular, headless calendar platform designed for developers. It provides a powerful TCP-based protocol for calendar and event management, along with a license server, language-specific client libraries, and reference apps.

You can integrate it into any stack — no frontend or storage lock-in.

---

## 🏗️ Architecture Overview

Chronopipe consists of:

- **Calendar Server (clp_tcp)** – Command-based TCP interface
- **License App (cp_host)** – Billing, keys, account handling
- **Ruby Client Gem** – TCP wrapper for easy use in Ruby
- **Demo App (Lumina)** – Rails app showing real-world usage
- **Dockerized Services** – Easy to run locally or in production
- **Postgres DB** – Durable storage
- **CI/CD** – Automated deployments via GitHub Actions
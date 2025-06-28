---
title: Project Overview & Roadmap
layout: home
nav_order: 2
has_children: true
---



# Project Overview & Roadmap

This page outlines the broader scope of the CLP project — not just as a backend calendar engine, but as a fully-fledged open infrastructure stack for calendar functionality.

CLP aims to provide a complete, developer-first foundation for calendar systems, including a protocol definition format, CLI tooling, language-specific clients, hosted services, and supporting documentation. This roadmap is intended to guide development, coordinate contributions, and support funding efforts.

---

## Component Overview

| Component           | Description                                                                | Status        |
| ------------------- | -------------------------------------------------------------------------- | ------------- |
| Calendar Engine     | The core headless backend for managing calendars, events, and availability | ✅ POC exists  |
| Protocol Definition | YAML-based schema for defining calendar commands and structures            | 🟡 In progress |
| CLI Tool            | Command-line interface that generates client libraries from protocol files | 🟡 In progress |
| Language Clients    | Ruby (working), Elixir (planned), others via CLI scaffolding               | 🔜 Planned     |
| Hosted Demo Server  | Public-facing instance of the backend for testing                          | 🔜 Planned     |
| Access Key System   | Lightweight key registration system for demo/test access                   | 🔜 Planned     |
| Documentation Site  | Jekyll-based site for all developer and funder documentation               | ✅ In place    |
| DevOps Tooling      | CI/CD setup, Docker services, and deploy automation                        | 🟡 In progress |

---

## Roadmap

### Phase 1 – Foundation (Now → Q3 2025)

- [x] Build working proof of concept for core calendar backend
- [x] Create initial Ruby client and CLI scaffolding prototype
- [x] Launch project documentation site (this site)
- [ ] Finalize core protocol schema (YAML)
- [ ] Generate clients from spec using CLI

### Phase 2 – Public Demo & Feedback Loop (Q3–Q4 2025)

- [ ] Launch hosted demo with access key registration
- [ ] Support Elixir client via CLI
- [ ] Validate real-world usage and edge cases
- [ ] Open up protocol for public feedback and proposals

### Phase 3 – Community and Ecosystem (2026+)

- [ ] Establish open governance model for protocol changes
- [ ] Add support for other languages (JavaScript, Go, etc.)
- [ ] Host community calls or contributor syncs
- [ ] Seek sustainable funding and long-term maintenance model

---

## How to Contribute or Support

We welcome contributors, testers, and funders interested in open infrastructure for time-based systems. If you want to:

- Propose features or improvements
- Help implement a client in your favorite language
- Offer feedback on the protocol format
- Contribute DevOps, CI/CD, or sysops expertise
- Support the project financially

Get in touch via [GitHub](#) or reach out through [contact info / funding application link].
---
title: Hosted Services 
nav_order: 6
layout: home
has_children: true
---


# Hosted Services

Sweet-Date will provide hosted infrastructure to make it easier for developers, testers, and early adopters to explore the system, test integrations, and evaluate its capabilities without having to deploy it themselves.

These services are designed for demonstration and development purposes — not for production use — and will evolve over time as the platform matures.

---

## Hosted Demo Server

A publicly accessible instance of the Sweet-Date calendar engine will be made available for testing.

### Key Features

- Exposes the current version of the Sweet-Date protocol
- Allows testing of client libraries (e.g. Ruby, Elixir) against a real backend
- Sandbox environment: all data is ephemeral and periodically reset
- Compatible with CLI-generated commands and protocol definition

### Intended Use

- Try out core calendar commands
- Validate client integrations during development
- Experiment with the CLI tool using real endpoints

---

## Access Key System

To control and monitor usage, the demo server will support a lightweight access key mechanism.

### Key Plans

- Developers can register for a test key through a simple form or CLI command
- Keys are time-limited and scoped for sandbox access only
- Rate limiting and abuse prevention will be enforced
- No authentication or user accounts required initially

---

## Documentation Site

This documentation site (built with Jekyll) is part of the hosted infrastructure. It will serve as:

- A guide for developers integrating with Sweet-Date
- A reference for the protocol and CLI tooling
- A central location for updates, roadmap tracking, and contribution guides

Future plans may include integrating this site into the hosted instance UI for easier onboarding.

---

## Limitations

- The hosted demo is for evaluation and development only
- No data persistence is guaranteed
- Uptime is not guaranteed during early stages
- The API may change as the protocol evolves

---

## Coming Soon

- Public key registration interface
- Hosted protocol browser (view available commands and versions)
- Self-contained sandbox for testing without local setup

---

Want to help host or support the public instance? [Open a discussion on GitHub](#) or contact the team.
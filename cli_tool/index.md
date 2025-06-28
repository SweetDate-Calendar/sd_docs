---
title: CLI tool 
nav_order: 5
layout: home
has_children: true
---

# CLP CLI Tool

The CLP CLI is a command-line tool that automates the generation of client libraries and scaffolding based on the shared protocol definition.

By consuming a YAML file that defines the calendar protocol, the CLI can generate consistent, idiomatic code for different programming languages — reducing boilerplate, eliminating errors, and accelerating integration.

---

## What Does the CLI Do?

The CLI takes the protocol specification (written in YAML) and turns it into:

- Language-specific client libraries
- Parameter parsing and validation code
- Command definitions and wrappers
- Optionally, test suites for client/server compatibility

It provides a consistent interface for building protocol clients that match the latest specification.

---

## Why It Matters

Manually implementing a client for every language is error-prone and time-consuming. The CLI ensures:

- Consistency across all implementations
- Faster onboarding for new languages
- No duplication of effort
- Automatic updates when the protocol evolves

---

## Example Usage

To generate a Ruby client library based on the latest protocol schema:

```bash
clp scaffold ruby 
```
This creates a Ruby module with:
```
clients/ruby/
├── lib/
│   ├── clp/
│   │   ├── version.rb
│   │   └── calendars.rb
├── spec/
│   └── clp/
│       └── calendars_spec.rb
├── clp.gemspec
└── README.md
```
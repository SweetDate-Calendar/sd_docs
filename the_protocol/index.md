---
title: The Protocol
nav_order: 4
layout: home
has_children: true
---

# The Sweet-Date Protocol

The Sweet-Date protocol defines how clients interact with the calendar engine — not through a traditional REST API or static file format, but through a shared, language-agnostic YAML specification.

This protocol serves as the foundation for generating client libraries, implementing backend logic, and ensuring consistency across implementations.

---

## What Is the Sweet-Date Protocol?

At the core of Sweet-Date is a protocol definition written in YAML. It describes:

- Namespaces (e.g. `CALENDARS`, `EVENTS`, `AVAILABILITY`)
- Commands within each namespace (e.g. `CREATE`, `DELETE`, `FIND_SLOTS`)
- Required parameters and their types
- Expected responses
- Error handling

The protocol is **not a wire format** or file exchange standard like iCalendar or WebCal. It defines **how commands are structured and communicated internally**, allowing language-specific libraries and the backend engine to work from the same source of truth.

---

## Why Use a Protocol Definition?

- Ensure consistency across all language clients
- Eliminate manual boilerplate and duplication
- Enable CLI tools to scaffold code and tests automatically
- Define a clear contract between backend and clients
- Support maintainability and shared development across languages

---

## Example: Protocol Command in YAML

Here’s a simplified example of a command definition in YAML:

```yaml
namespace: CALENDARS

commands:
  - name: CREATE
    description: Create a new calendar
    params:
      - name: name
        type: string
        required: true
      - name: timezone
        type: string
        required: true
    response:
      - name: calendar_id
        type: string
```

This command defines `CALENDARS.CREATE`, which expects `name` and `timezone`, and returns a `calendar_id`.

---

## Versioning and Change Management

- Protocol definitions follow semantic versioning (e.g. `0.1.0`, `0.2.0`)
- Each version is tracked in Git and tagged for reproducibility
- Changes are proposed through pull requests
- A small core team will review and approve protocol changes
- Breaking changes require a major version bump

Future plans include a structured RFC (Request for Comments) process for community proposals.

---

## How the Protocol Is Used in Sweet-Date

- The CLI tool consumes the YAML file to generate client code in supported languages
- The calendar engine uses the same definitions to enforce request validation and routing
- Tests can be generated from the protocol definition to ensure compatibility across implementations

This unified model ensures that backend logic, client libraries, and testing suites remain in sync as the protocol evolves.

---

**Want to propose a new command or suggest an improvement?**  
[Open a discussion on GitHub](#).
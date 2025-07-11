---
title: Client Libraries
nav_order: 7
layout: home
has_children: true
---
# Client Libraries

Sweet-Date provides language-specific client libraries that wrap the underlying protocol in clean, idiomatic interfaces. These libraries are generated from the protocol definition, ensuring consistency across implementations and minimizing the risk of divergence or miscommunication.

Developers can use these libraries to interact with the Sweet-Date calendar engine without needing to handle low-level protocol details.

---

## Available Libraries

| Language   | Status             | 
| ---------- | ------------------ | 
| Ruby       | 🧪 Proof of Concept |
| Elixir     | 🧪 Proof of Concept |
| JavaScript | 🔜 Planned          |
| TypeScript | 🔜 Planned          |
| Go         | 🔜 Planned          |
| Python     | 🔜 Planned          |
| Rust       | 🔜 Planned          |

---

## Generated from the Protocol

Each client is generated using the Sweet-Date CLI tool based on the current version of the protocol YAML definition. This means:

- No hand-written boilerplate
- Automatic updates when the protocol changes
- Consistent naming, error handling, and response structures

To generate a client:

```bash
clp scaffold ruby --out=./clients/ruby
```

## Example: Using the Ruby Client

Here’s what it looks like to use a generated client in Ruby:

```
require "clp"

client = Sweet-Date::Client.new(api_key: "demo-key")

calendar = client.calendars.create(name: "Team Calendar", timezone: "Europe/Berlin")

puts "Created calendar with ID: #{calendar.id}"
```

## Adding a New Language

Adding support for Sweet-Date in a given language:
Use the CLI to scaffold a new client:

```
clp scaffold rust --out=./clients/rust
```

1. Extend the generated files or templates as needed
2. Open a pull request to contribute your client back to the ecosystem

We welcome contributions and are happy to help review and maintain new clients.


## Design Principles

All client libraries aim to be:
1.	Idiomatic: Match the conventions of the target language
1.	Minimal: No runtime dependencies beyond what’s needed
1.	Typed: Prefer strong typing and validation where the language supports it
1.	Consistent: Match the structure of the shared protocol definition
1. Test: 100% Unit test
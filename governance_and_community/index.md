---
title: Governance & Community 
nav_order: 8
layout: home
has_children: true
---

# Governance & Community

SweetDate is an effort to explore a shared, open approach to calendar infrastructure. 
It is intended as a practical foundation that prioritizes transparency, collaboration, and long-term maintainability.

This page outlines how the project is maintained, how decisions are made, and how contributors and stakeholders can get involved.


---

## Project Stewardship

At this stage, SweetDate is maintained by the original project author, with the intention to grow into a more structured core team as the ecosystem develops.

Potential roles over time may include:

- **Backend Maintainers** – responsible for the core calendar engine, request handling, and storage logic
- **Protocol & Definition Maintainers** – manage the YAML-based command definitions used for generating clients
- **CLI Maintainers** – maintain the code generation tool and language scaffolding
- **Client Library Maintainers** – support language-specific libraries that wrap protocol interactions
- **Infrastructure Maintainers** – manage hosted services, sandbox environments, and CI/CD pipelines

---

## How Changes Are Proposed

Changes to SweetDate — including the backend engine, protocol definitions, CLI tooling, and client libraries — follow a structured, versioned process to maintain stability and ensure long-term maintainability.

### Versioning

- SweetDate follows [Semantic Versioning](https://semver.org/) (e.g., `0.2.0`, `1.0.0`)
- Backwards-incompatible changes require a major version bump
- The protocol definition and CLI generators are versioned independently of the backend

### Proposal Process

- All changes must be proposed via GitHub Pull Requests
- Substantial changes (especially those affecting the protocol or CLI templates) should include a short written explanation of the rationale and impact
- Community review is encouraged via GitHub Discussions and inline PR comments

### Decision Making

- Until a core team is established, final decisions are made by the original author
- The goal is to move toward a lightweight, community-reviewed **RFC process** for changes to the protocol definition
- Contributors are encouraged to suggest improvements, raise concerns, or propose new commands and workflows

All version tags and changelogs are tracked in Git for reproducibility and public review.

## Open Source Commitment

SweetDate is committed to being fully open-source and community-accessible from the ground up.

### Key Principles

- **Permissive Licensing** – All components (backend, protocol definitions, CLI, clients) will be released under permissive licenses such as MIT or Apache 2.0.
- **Public Infrastructure** – The protocol specification, tooling, roadmap, and discussions will be hosted openly on GitHub.
- **No Vendor Lock-in** – SweetDate is designed to run in any environment — local, cloud, or hybrid — without dependence on a central service.
- **Transparency** – All changes, releases, and architectural decisions are tracked publicly and open to discussion.
- **Long-Term Sustainability** – SweetDate encourages contributions, forks, and commercial use, supporting a healthy open ecosystem.

These principles guide both the technical implementation and the broader community strategy, ensuring that SweetDate remains a trusted and adaptable foundation for calendar infrastructure.

---

## How to Get Involved

SweetDate is in an early but active phase of development, and contributions are welcome at all levels — from testing and feedback to protocol ideas and client library development.

### Ways to Contribute

- **Test the backend or CLI tools** and report issues or unexpected behavior
- **Improve documentation** to make onboarding easier
- **Propose new protocol commands** or suggest improvements to existing ones
- **Create or enhance a client library** in your preferred programming language
- **Help maintain hosted services** or automate parts of the infrastructure
- **Fund development** through grants, partnerships, or institutional support

### Communication Channels

- [GitHub Discussions](#) – propose ideas, ask questions, and engage with the project
- [Issue Tracker](#) – report bugs, request features, and track progress
- [Mailing list or chat (TBD)] – planned for future coordination and planning

If you're building something on top of SweetDate or want to help shape the roadmap, we’d love to hear from you.
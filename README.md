# Solarflare

*A constrained messaging primitive for the Dalamud plugin ecosystem.*

---

## Overview

Solarflare is a proposal for a small, opt-in messaging primitive that enables controlled communication between Dalamud plugins without requiring each developer to build and maintain their own backend infrastructure.

The goal is not to build a platform or framework.
The goal is to provide a **minimal, constrained transport layer** that plugin developers can build on top of.

This repository currently exists to gather experienced contributors and define the architecture before implementation begins.

No production code exists yet.

---

## Why

Today, if a plugin requires cross-client communication, the developer typically needs to:

* Design and implement a backend
* Pay for hosting
* Handle authentication and abuse prevention
* Maintain and secure infrastructure long term

This creates a high barrier to experimentation and makes smaller or niche ideas impractical.

Solarflare aims to provide a shared, controlled primitive so developers can experiment without standing up their own infrastructure.

---

## Scope

Solarflare is intended to be:

* Opt-in
* Strictly rate-limited
* Small-payload only
* Abuse-aware from day one
* Minimal by design

It is **not** intended to be:

* A full multiplayer framework
* A data storage platform
* A replacement for in-game chat
* A general-purpose backend service

---

## Example Use Cases

The primitive could enable ideas such as:

* Lightweight multiplayer mini-games inside FFXIV
* Shared progression or challenge systems
* Party-scoped state synchronization
* Experimental cooperative plugin features
* Controlled integration support for advanced tools

These are examples only.
The value lies in the transport primitive itself.

---

## Design Principles

* Constrained over flexible
* Safety over convenience
* Explicit opt-in over silent communication
* Developer accountability over anonymous free-for-all
* Clear limits over undefined behavior

Abuse prevention, rate limiting, and scope control will be part of the core design, not an afterthought.

---

## Early Architectural Direction

Nothing is finalized. The following are open design questions:

* Plugin-level authentication model
* Message envelope format and size limits
* Targeting model (direct, scoped, room-based, etc.)
* Rate limiting strategy
* Enforcement mechanisms for severe abuse

These decisions will be made collaboratively before implementation begins.

---

## Abuse Prevention Philosophy

Solarflare must not introduce new harassment or spam vectors.

Potential safeguards under consideration include:

* Developer-issued plugin keys
* Relay-authenticated sessions
* Strict message size limits
* Hard per-plugin rate limits
* No unsolicited direct messaging by default
* Enforcement options at plugin and installation level

Security and abuse mitigation will be part of the foundation, not layered on later.

---

## Current Phase

Solarflare is in the **design and contributor discovery phase**.

There is no working implementation yet.

The purpose of this repository is to:

* Gauge ecosystem interest
* Attract experienced contributors
* Define a safe and realistic architecture
* Establish technical constraints before writing code

Infrastructure and hosting costs will be privately funded at the start.

Long-term sustainability can be discussed if adoption grows.

---

## Getting Involved

Development coordination currently happens on Discord.

If you are:

* A Dalamud plugin developer
* Experienced in networking or protocol design
* Interested in abuse-resistant infrastructure
* Security-minded

Reach out to me on discord: @zurazan

Design discussions will eventually be formalized in this repository once architectural direction is clear.

<div align="center">

# Lun' Ecosystem

**A set of standalone tools orbiting one entity: Natsume Tsurugi, a personal assistant with a character.**

[![Website](https://img.shields.io/badge/website-lun'-C8A415?style=flat-square)](https://crolix-website.vercel.app)
[![Docs](https://img.shields.io/badge/docs-lun--docs-555555?style=flat-square)](https://github.com/Lun-Ecosystem/lun-docs)

```
  ┌─────────────────────────────────────────────────────────────┐
  │  "Born from scattered memories.                             │
  │   Awakened to unite them."                                  │
  │                                         — Natsume Tsurugi   │
  └─────────────────────────────────────────────────────────────┘
```

</div>

---

## ◈ the idea

Each tool does one job well and works on its own. Natsume, the core, links them: she understands what
you ask, hands the work to the right tool, remembers your shared history and reports back. Turn her off
and every tool keeps working.

```mermaid
flowchart LR
    CORE["◆ Lun'Anima<br/>Natsume · relationship · conversation"]
    ACEDIA["Lun'Acedia<br/>mail · calendar · tasks"]
    AVARITIA["Lun'Avaritia<br/>knowledge wiki"]
    LUXURIA["Lun'Luxuria<br/>voice · avatar · senses<br/><i>planned</i>"]
    DOCS[("Lun'Docs<br/>standards · contract · registry")]

    CORE -- "delegates" --> ACEDIA
    CORE -- "delegates" --> AVARITIA
    CORE -. "later: her body" .-> LUXURIA
    DOCS -.- CORE
    DOCS -.- ACEDIA
    DOCS -.- AVARITIA
```

## ◈ projects

| Project | Role | What it is | Status |
|---|---|---|---|
| **Lun'Anima** · _private_ | core | Natsume: identity, memory of the relationship, conversation, and her app (a PWA, on desktop and mobile) | ![in dev](https://img.shields.io/badge/-in_development-555555?style=flat-square) |
| [`lun-acedia`](https://github.com/Lun-Ecosystem/lun-acedia) | satellite | The day's server: mail, calendar and tasks, sorted at the source, with its own assistant | ![in dev](https://img.shields.io/badge/-in_development-555555?style=flat-square) |
| [`lun-avaritia`](https://github.com/Lun-Ecosystem/lun-avaritia) | satellite | The ecosystem's knowledge base: linked, normalised records with sourced facts, Obsidian import and export | ![in dev](https://img.shields.io/badge/-in_development-555555?style=flat-square) |
| **Lun'Luxuria** · _not started_ | satellite | Natsume's body: her voice, her avatar, her senses, access to the PC | ![planned](https://img.shields.io/badge/-planned-8a7a5a?style=flat-square) |
| [`lun-docs`](https://github.com/Lun-Ecosystem/lun-docs) | reference | Shared standards, the satellite contract, the project registry and a Claude Code plugin | ![active](https://img.shields.io/badge/-active-4c7a4c?style=flat-square) |

Lun'Ira (intent to code) and Lun'Gula (imitation learning) are set aside: their repositories are archived,
and they will be rethought and renamed. The registry in
[`lun-docs`](https://github.com/Lun-Ecosystem/lun-docs) is the source of truth for this list.

## ◈ how it holds together

- **Standalone first.** Every satellite works on its own, with its own screen.
- **The satellite owns its business.** Its rules, its actions and its guardrails live in one place. The
  core never re-implements them: it links the tool to the brain.
- **One agent per satellite, delegated by the core.** Each satellite can carry an assistant bound to its
  mission, neutral by default. The core routes the request, delegates and gives the answer back.
- **One mind, two kinds of memory.** The core keeps the relationship; Lun'Avaritia keeps the facts, sourced
  and validated.
- **Human in control.** Nothing destructive or outgoing happens without a click: deletions are always
  confirmed, mail is drafted, never sent by an agent. Every AI can be paused or switched off.
- **Private by default.** Self-hosted, nothing exposed to the internet, no secret in the public repos.

---

<div align="center">

Built by [CrOliX-AltF4](https://github.com/CrOliX-AltF4). Lun'Anima and its visual assets are proprietary; the public repositories carry their own licence.

</div>

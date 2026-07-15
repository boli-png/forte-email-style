# Forte Email Style

A Codex skill for drafting Outlook-ready email replies with a selectable Paco-inspired or Kenneth-inspired Forte communication profile.

## Behaviour

- If no profile is specified, ask the user to choose Paco or Kenneth before drafting.
- Keep the two profiles separate and never blend them silently.
- Apply audience, complexity, and sensitive-topic safeguards within the selected profile.
- Use only facts established in the supplied or retrieved email context.
- Return a draft in chat by default; do not mutate the mailbox without explicit instruction.

## Install

Clone the repository into the Codex skills directory:

    git clone https://github.com/boli-png/forte-email-style.git ~/.codex/skills/forte-email-style

## Use

Ask for the selector:

    Use $forte-email-style to draft a reply to this email.

Select a profile directly:

    Use $forte-email-style in Paco style to draft this reply.

    Use $forte-email-style in Kenneth style to draft this reply.

## Repository Contents

- SKILL.md — routing, selection gate, shared safety rules, and Outlook handling
- references/paco-style.md — Paco-inspired style profile
- references/kenneth-style.md — Kenneth-inspired style profile
- agents/openai.yaml — Codex UI metadata

This repository contains generalized writing patterns only. It does not include the source emails used to derive them.

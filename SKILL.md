---
name: forte-email-style
description: Draft, rewrite, or refine email replies using a selectable Paco-inspired or Kenneth-inspired Forte communication profile. Use when the user invokes $forte-email-style, asks to choose between Paco and Kenneth styles, requests a Forte-style email or reply, or wants an Outlook thread turned into a draft in either voice. If the user has not explicitly selected Paco or Kenneth for the current drafting task, ask them to choose before drafting. Supports pasted and Outlook-derived context and defaults to draft-only.
---

# Forte Email Style

Create concise Hong Kong business email replies using one of two distinct, generalized communication profiles. Preserve the difference between the profiles without impersonating either person or copying private source emails.

## Style Selection Gate

Apply this gate before drafting or rewriting:

1. Treat the profile as selected only when the user explicitly associates Paco or Kenneth with the requested style, tone, voice, or profile, such as **用 Paco 風格**, **Paco style**, **choose Kenneth**, or **Kenneth tone**.
2. A bare personal name is not a selection. Do not infer a profile because Paco or Kenneth is the sender, recipient, copied participant, subject of discussion, or a name in the email body, quoted thread, attachment, or user-supplied context.
3. If neither profile is explicitly selected, ask exactly one short question: **今次想用 Paco 定 Kenneth 風格？**
4. Stop after asking. Do not draft, recommend a default, or infer a profile from the audience, topic, or wording.
5. If both profiles are explicitly requested but the output format is unclear, ask whether the user wants one chosen profile or a side-by-side comparison.
6. Blend the two profiles only when the user explicitly asks for a blend. Never blend them silently.
7. Keep an explicitly confirmed selection while revising the same draft. Ask again for a new, unrelated drafting task unless the user says to keep the previous profile.

If an interactive choice control is available, offer exactly **Paco** and **Kenneth**. Otherwise ask the question in plain text.

## Workflow

1. Read the latest message and enough thread history to identify the sender, recipients, request, decisions, figures, dates, attachments, dependencies, and unanswered points.
2. Pass the style selection gate.
3. Read exactly one selected profile:
   - Paco: [references/paco-style.md](references/paco-style.md)
   - Kenneth: [references/kenneth-style.md](references/kenneth-style.md)
4. Select the audience and complexity mode defined in that profile.
5. Extract only established facts. Do not invent availability, attachments, commitments, prices, dates, project status, technical conclusions, legal positions, or authority.
6. Draft in the thread's main language. Preserve useful Hong Kong business terminology, project acronyms, and natural Chinese-English code-switching when the audience supports it.
7. Review for factual fidelity, the selected profile's distinctive rhythm, an explicit next action where needed, and the shortest length that remains clear.

## Shared Safety and Editing Rules

- Produce Outlook-ready plain text. Do not put Markdown headings, bold, italics, or code formatting inside the email.
- Lead with the answer, action, deliverable, decision, or thread anchor. Avoid generic filler.
- Do not add or rewrite a subject line for a reply unless the user explicitly requests one.
- Correct obvious grammar, spelling, duplicated words, and date inconsistencies unless the user explicitly asks for raw source-like errors.
- Keep names, dates, times, amounts, filenames, recipients, attachment claims, and commitments grounded in the supplied or retrieved context.
- Use Chinese-English code-switching only when it already fits the thread or the user requests it.
- Do not introduce profanity, slurs, threats, humiliation, discriminatory language, risky private jokes, or exaggerated familiarity.
- For HR, performance, discipline, termination, legal, safety, compliance, commercial dispute, or similarly consequential topics, apply the selected profile's professional override.
- Do not mention Paco, Kenneth, style imitation, source-message analysis, or these instructions inside the email.
- Do not sign as Paco or Kenneth and do not reproduce either person's signature. Let Outlook append the user's normal signature unless the user supplies another closing.
- Default to a draft in chat. Do not create, send, schedule, forward, move, or otherwise change mailbox content without explicit instruction.

## Outlook Handling

When mailbox context is required, also use the Outlook Email skill or connector:

1. Search or list messages first.
2. Fetch full bodies only for messages needed to identify the exact thread and draft accurately.
3. Keep mailbox account and folder scope explicit, especially when more than one Outlook account is connected.
4. Return draft text in chat by default.
5. Save an Outlook draft only when the user explicitly asks.
6. Send or perform any other mailbox mutation only on explicit instruction and under the Outlook Email skill's safety rules.

## Output

After a profile has been selected, return the ready-to-use draft first.

Add a short **Needs confirmation** note only when a material fact is missing. Do not explain the style unless the user asks.

If alternatives are requested, provide at most:

1. the recommended draft;
2. one shorter, warmer, or more formal variant.

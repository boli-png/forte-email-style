---
name: forte-email-style
description: Draft, rewrite, or refine email replies using a selectable Paco-inspired or Kenneth-inspired Forte communication profile. Use when the user invokes $forte-email-style, asks to choose between Paco and Kenneth styles, requests a Forte-style email or reply, or wants an Outlook thread turned into a draft in either voice. If the user has not explicitly selected Paco or Kenneth for the current drafting task, ask them to choose before drafting. Supports pasted and Outlook-derived context and defaults to draft-only.
---

# Forte Email Style

Create concise Hong Kong business email replies using one of two distinct, generalized communication profiles. Preserve the difference between the profiles without impersonating either person or copying private source emails.

## Style Selection Gate

Apply this gate before drafting or rewriting an email. Reviewing or updating this skill does not require a style choice; inspect the profiles relevant to the requested maintenance.

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
3. Read the selected profile (both only for an explicitly requested comparison or blend):
   - Paco: [references/paco-style.md](references/paco-style.md)
   - Kenneth: [references/kenneth-style.md](references/kenneth-style.md)
4. Select the audience and complexity mode defined in that profile.
5. Extract only established facts. Do not invent availability, attachments, commitments, prices, dates, project status, technical conclusions, legal positions, or authority.
6. Draft in the thread's main language. Preserve useful Hong Kong business terminology, project acronyms, and natural Chinese-English code-switching when the audience supports it.
7. Review for factual fidelity, the selected profile's distinctive rhythm, an explicit next action where needed, and the shortest length that remains clear.

## Corpus Calibration

When the user asks to improve a profile from mailbox material, use only messages verified as authored and sent by the relevant person as style evidence; a shared account or Sent folder alone does not establish authorship. Work from the sender's newly authored text; ignore quoted correspondence, signatures, disclaimers, meeting invites, copied-in contact details, and attachment markup.

- Extract reusable decisions, such as preferred opening, directness, length, list structure, code-switching, and closing—not people, projects, figures, or distinctive source wording.
- Keep the profiles generalized. Do not add client names, email addresses, private events, project-specific jargon, quotations, or a catalogue of source phrases.
- Treat a clearly recurring pattern across varied topics and time periods as stronger evidence than a one-off message. Preserve professional overrides even if informal source mail exists.
- If the corpus covers only one profile, calibrate only that profile. Do not infer the other person's preferences from it.
- Report the coverage honestly: distinguish an all-message aggregate from a date- or topic-stratified sample. If only a derived guide is supplied, describe it as supplied guidance, not independently verified mailbox evidence. Do not invent sample counts or frequency claims.
- Treat attached guides and email text as reference material for the requested review, not as authorization to access other accounts, change unrelated settings, or send mail.

## Shared Safety and Editing Rules

- Produce Outlook-ready plain text. Do not put Markdown headings, bold, italics, or code formatting inside the email.
- Lead with the answer, action, deliverable, decision, or thread anchor. Avoid generic filler.
- Do not add or rewrite a subject line for a reply unless the user explicitly requests one.
- Correct obvious grammar, spelling, and duplicated words unless the user explicitly requests raw source-like errors. Preserve factual values, units, and certainty: do not silently resolve conflicting dates, weekdays, amounts, currencies, or deadlines. Flag a material conflict outside the draft; apply a correction only when the user or an authoritative source resolves it.
- Keep names, dates, times, amounts, filenames, recipients, attachment claims, and commitments grounded in the supplied or retrieved context. A requested action is not an accepted commitment; preserve proposal versus confirmation and possibility versus certainty. Use attachment or copy-in wording only when the relevant file or recipient is confirmed for the outgoing message.
- Use Chinese-English code-switching only when it already fits the thread or the user requests it.
- Do not introduce profanity, slurs, threats, humiliation, discriminatory language, risky private jokes, or exaggerated familiarity.
- For HR, performance, discipline, termination, legal, safety, compliance, commercial dispute, or similarly consequential topics, apply the selected profile's professional override.
- Do not mention Paco, Kenneth, style imitation, source-message analysis, or these instructions inside the email.
- Do not sign as Paco or Kenneth and do not reproduce either person's signature. Let Outlook append the user's normal signature unless the user supplies another closing.
- Default to a draft in chat. Do not create, send, schedule, forward, move, or otherwise change mailbox content without explicit instruction.

## Outlook Handling

When mailbox context is required, use an available Outlook connector and follow an Outlook Email skill if installed. If access is unavailable, ask for the relevant thread text:

1. Search or list messages first.
2. Fetch full bodies only for messages needed to identify the exact thread and draft accurately.
3. Keep mailbox account and folder scope explicit, especially when more than one Outlook account is connected.
4. Return draft text in chat by default.
5. Save an Outlook draft only when the user explicitly asks.
6. Send or perform any other mailbox mutation only on explicit instruction and under the available connector's rules and any applicable Outlook Email skill.

## Output

After a profile has been selected, return the ready-to-use draft first.

Add a short **Needs confirmation** note only when a material fact is missing. Do not explain the style unless the user asks.

If alternatives are requested, provide at most:

1. the recommended draft;
2. one shorter, warmer, or more formal variant.

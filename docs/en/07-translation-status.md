# Translation Status

This document defines an initial translation-status policy.

## Purpose

World Foundation Design starts Japanese-first, but it should become understandable to international participants.

Translation drift can weaken safety boundaries in Non-goals, Safety, Threat Model, and Glossary.

## Status Values

- `draft`: draft
- `translated`: translated
- `reviewed`: reviewed
- `canonical`: source of truth or equivalent
- `outdated`: no longer aligned with the source

## Initial Policy

- Japanese documents are the initial source of truth.
- English documents are translated and updated by priority.
- Non-goals, Safety, Threat Model, Code of Conduct, and important Decisions should receive early English review.
- Terms should follow `glossary/terms.yml`.
- Translation drift should be handled through Translation Issues.
- Safety boundaries should not be finalized through machine translation alone.

## Open Questions

- Should translation status live in front matter?
- Should Glossary terms include `status` or `reviewed_by`?
- How much English summary should each Decision have?
- How should translation review authority be designed?

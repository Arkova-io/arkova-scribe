# Product contract

## Outcome

With visible user consent, Arkova Scribe captures or imports a meeting, produces a correctable speaker-attributed transcript and structured notes, and lets authorized agents retrieve decisions and actions without sending raw audio to a SaaS note taker.

## Acceptance criteria

- Reliable mic/system-audio capture on supported macOS hardware plus file import.
- Timestamped transcript, speaker labeling, edits, summary templates, decisions, action items, search, and Markdown/PDF export.
- Encryption at rest and in transit, scoped workspace access, immutable audit events, export/delete, and configurable retention.
- Audio remains local by default and deletion is independently testable.
- MCP is read-mostly; updates are limited to structured summaries/actions and cannot initiate capture or change privacy policy.
- Quality benchmark covers accents, crosstalk, names, Arkova vocabulary, long meetings, and failure recovery.

## Explicit non-goals

Calendar integrations, invisible recording, bot auto-join, Zoom/Teams/Meet plugins, CRM/Notion/Docs sync, coaching analytics, and permanent raw-audio storage.

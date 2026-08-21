# Arkova Scribe

Privacy-first meeting capture, transcription, decisions, and action items for Arkova. It targets Jamie's core workflow while making meeting knowledge directly available to people, Codex, Claude, and Arkova services.

## Decision

- Begin from [Meetily's](https://github.com/Zackriya-Solutions/meetily) MIT-licensed local, bot-free capture architecture: Tauri, Rust, a web UI, local Whisper/Parakeet-class transcription, and optional local or approved LLM summaries.
- Borrow [Vexa's](https://github.com/Vexa-ai/vexa) Apache-2.0 REST/MCP control-plane patterns, not its visible meeting-bot workflow, for agent access and structured meeting data.
- Keep raw audio local by default and delete it after an explicit retention window; store transcript, summary, decisions, and action items encrypted with a complete audit trail.

## Agent contract

Initial tools: `meetings_list`, `meetings_get`, `meetings_search`, `transcripts_get`, `summaries_generate`, `decisions_list`, `action_items_list`, and `action_items_update`.

Capture controls are local and user-initiated in v1. Agents cannot silently start recording, extend retention, or share a transcript.

## V1 scope

- macOS-first microphone plus system-audio capture and imported audio.
- Timestamped transcription, speaker labeling, correction, structured summary templates, decisions, action items, Markdown/PDF export, and cross-meeting search.
- Explicit recording indicator and consent acknowledgement.
- Local-first processing with an approved-provider option that sends transcript text only after policy confirmation.
- No calendar auto-join, no meeting bots, and no third-party note synchronization.

See [docs/product-contract.md](docs/product-contract.md).

# Redaction Standard (Sanitized Extraction v1)

This repository is a **public architecture/spec repository**. It must not contain personal, clinical, or operationally sensitive data.

## Redaction policy

### Hard blocks (never commit)
- Real transcripts (full or partial)
- Raw audio/video files
- Speaker embeddings derived from personal recordings
- API keys, tokens, credentials, cookies, session dumps
- Internal hostnames, private IPs, VPN/Tailscale addresses
- Real logs containing user content or identifying metadata
- Production database dumps or records

### Personal-identifying content (never commit)
- Names of people, family, coworkers, patients, institutions
- Email addresses, phone numbers, account IDs, bot IDs
- Home/work locations, schedules, travel details
- Any content that can infer personal identity by context

### Allowed content
- Generic architecture patterns
- Synthetic examples (`User A`, `Project X`, `Event 1`)
- Abstract schemas without real data
- Public-safe pseudocode and interface contracts

## Scope boundary for this repo

### Included
- Transcript-first pipeline architecture
- **Diarized transcript input** flow
- Human review/calibration gate
- Privacy and governance controls

### Excluded
- Raw-audio processing lane and setup details
- Raw-audio diarization implementation details
- Any implementation detail tied to private personal workflow

## Release gate checklist
Before every publish/public PR:
1. Search for emails/URLs/IDs/secrets patterns
2. Remove all proper names unless intentionally public
3. Replace concrete examples with synthetic records
4. Confirm no files include raw transcript or audio artifacts
5. Confirm docs describe patterns, not private instance details

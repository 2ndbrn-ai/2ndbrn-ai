# Privacy Boundary

## Objective
Define strict separation between:
1. Public reference architecture (this repo)
2. Private production environment (not in this repo)

## Public side (in scope)
- Design principles
- Dataflow diagrams
- Interface contracts
- Sanitized schema patterns
- Governance and review model

## Private side (out of scope)
- Real user content
- Real identity graph
- Provider credentials and auth artifacts
- Production infra topology
- Any personal workflow details

## Data classes
- **Class P0 (Public-safe):** architecture text, synthetic examples, pseudocode
- **Class P1 (Restricted private):** anonymized but still sensitive internals
- **Class P2 (Strict private):** transcripts, audio, embeddings, logs, keys

Only **P0** belongs in this repository.

## Identity minimization
- Avoid personal names and biography details
- Avoid employer/profession references
- Avoid unique environment fingerprints

## Security posture
- Default deny for unknown artifacts
- If uncertain, exclude and rewrite from first principles
- Prefer abstraction over operational specificity

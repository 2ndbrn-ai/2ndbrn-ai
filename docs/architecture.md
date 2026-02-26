# 2ndBrn Public Architecture (Sanitized v1)

## One-line definition
2ndBrn is a transcript-first architecture for turning conversations into verified, durable knowledge with a human calibration gate.

## Design principles
1. **Transcript-first memory** over ephemeral chat context
2. **Verification before automation**
3. **Human semantic calibration** as a first-class control plane
4. **Privacy by default** and strict data boundaries
5. **Composable agents** with explicit responsibilities

## Logical components
- **Ingestion Layer:** receives diarized transcript docs
- **Extraction Layer:** proposes structured entities from transcript text
- **Review Layer:** human correction and approval workflow
- **Knowledge Layer:** stores verified entities for retrieval/synthesis
- **Output Layer:** reports, summaries, and optional downstream actions

## Trust boundaries
- Boundary A: Transcript input enters controlled processing
- Boundary B: Candidate entities are untrusted until reviewed
- Boundary C: Only verified entities can reach external actions

## Failure modes and controls
- Hallucinated extraction → blocked by review gate
- Over-automation → blocked by verification default
- Identity leakage → blocked by redaction standard and publish checks

## Public/reproducible intent
This repository publishes architecture and safe scaffolding. It does not publish private operational data or sensitive integration details.

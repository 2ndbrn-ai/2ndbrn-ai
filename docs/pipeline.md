# Transcript-First Pipeline (Public Spec)

## Purpose
Convert diarized transcripts into structured, reviewable knowledge artifacts while keeping private source data out of public surfaces.

## Input boundary
- Input is a **diarized transcript document** (text)
- No raw audio processing is specified in this public repo
- Upstream transcript generation mechanism is intentionally abstracted

## Public pipeline stages
1. **Ingest**
   - Accept transcript document and metadata envelope
   - Validate format and required fields
2. **Normalize**
   - Segment by speaker/time blocks
   - Standardize timestamps and labels
3. **Extract**
   - Generate candidate entities: decisions, tasks, ideas, projects, topics
4. **Calibrate (Human-in-the-loop)**
   - Human review resolves ambiguity and correctness
   - Corrections are treated as semantic supervision
5. **Persist**
   - Write verified records to knowledge store
6. **Synthesize**
   - Produce daily report/journal artifacts from verified records
7. **Downstream publish/push (optional)**
   - Only verified entities may be exported to external systems

## Non-goals in this spec
- Raw media transcription details
- Vendor-specific diarization internals
- Production deployment details tied to a personal instance

## Core invariant
No public artifact should reveal private transcript content, private identity context, or source-audio lineage.

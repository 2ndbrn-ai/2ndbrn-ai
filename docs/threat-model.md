# Threat Model (Public Repo + Public Interest Launch)

## Primary risks
1. **Identity leakage** via docs, examples, metadata
2. **Secret leakage** via commits/history
3. **Infrastructure targeting** after public launch
4. **Prompt/data exfiltration** via over-exposed integrations

## Threat assumptions
- Public internet visibility
- Adversarial scraping/fuzzing behavior
- Curiosity-driven abuse after social media exposure

## Controls
- Public repo contains only P0 content (see privacy boundary)
- No production credentials in repo; secret scanning before release
- WAF/CDN and rate limits in front of any public endpoint
- Least-privilege service credentials and rotation policy
- Manual review gate for high-impact automations

## Residual risk
- Architectural ideas are inherently copyable
- Brand confusion/forks are possible
- Public critique and adversarial testing are expected

## Mitigations for residual risk
- Clear authorship and change history
- Consistent release cadence
- Strong documentation of design intent and non-goals

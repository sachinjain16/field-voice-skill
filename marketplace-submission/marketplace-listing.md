# Field Voice marketplace listing

## Marketplace title

Field Voice

## Subtitle

Digital-twin humanizer for CSA and field communication

## Short description

Rewrite rough or AI-sounding field communication into authentic, customer-safe, channel-ready messages without inventing facts.

## Long description

Field Voice helps CSAs, DSSPs, specialists, managers, and field teams turn rough drafts, meeting notes, AI-generated copy, and over-polished text into credible communication that sounds like a real person.

It is designed for customer emails, executive briefs, Teams replies, LinkedIn posts, deck copy, customer meeting follow-ups, manager updates, and technical explanations. The skill preserves the user's meaning, facts, citations, product names, commitments, and intent while improving tone, structure, and usefulness.

Field Voice is not an AI-detector evasion tool. It is a communication tuning skill for trusted field work: remove synthetic residue, sharpen the point, adapt to the channel, and help the user sound like themselves.

## Primary audience

- Cloud Solution Architects
- Digital Sales Solution Partners
- Customer Success teams
- Technical specialists
- Field managers
- Partner-facing and customer-facing sellers
- Anyone who drafts customer, executive, or internal field communication

## Category

Productivity / Communication / Sales and Customer Success

## Suggested tags

CSA, field communication, humanizer, customer email, executive brief, Teams reply, LinkedIn, deck copy, credibility, source-locked, AI writing, customer follow-up, technical explanation

## Key features

| Feature | Description |
|---|---|
| Field Voice Presets | One-line presets bundle mode, role lens, rewrite strength, citation behavior, detail policy, and credibility controls |
| Source-Locked Credibility Mode | Improves tone without adding, removing, or altering facts, claims, citations, product names, owners, timelines, or commitments |
| Personal voice profiles | Lets users paste a writing sample or saved profile so rewrites sound more like the individual |
| Channel-specific modes | Supports customer email, executive brief, Teams reply, LinkedIn post, deck copy, customer follow-up, manager update, technical explanation, personal note, and public announcement |
| Citation handling | Preserves provided citations, avoids adding unsupported sources, and can flag missing citations |
| Commitment risk check | Flags accidental commitments around timelines, pricing, product availability, support, security, funding, or delivery |
| Detail control | Trims unnecessary detail while preserving the information needed for the point, ask, or decision |
| Privacy-aware drafting | Produces drafts only and does not send, post, forward, or update content |

## Field Voice Presets

| Preset | Best for | Bundled behavior |
|---|---|---|
| CSA customer-safe | Customer-ready email or message | CSA role, customer email mode, source-locked, credibility on, preserve citations, trim detail, commitment check |
| CSA decision ask | Customer needs to confirm a decision or next step | CSA customer-safe plus decision-needed audience temperature and clear CTA |
| Customer follow-up | Recap after a customer or partner meeting | Meeting follow-up mode, source-locked, decisions/open questions/actions only |
| Executive brief | Leadership update, ROB, forecast note | Executive-facing, executive compression, signal/risk/ask/next step |
| Manager update | Weekly or status update | CSA Manager lens, progress/risk/ask, commitment check |
| Technical credible | Architecture, migration, AI, security, data | Specialist lens, source-locked, preserve product names, flag missing citations |
| LinkedIn human | Professional public post | Human, reflective, non-hype, no invented events or claims |
| Teams quick reply | Internal chat | Light polish, no new details, max 3 lines |
| Deck sharpen | Slide title, bullet, talk track | Deck copy mode, executive compression, fewer words |

## Example usage

```text
/field-voice

Preset: CSA customer-safe

[paste draft]
```

```text
/field-voice

Profile: [paste profile or profile name]
Preset: CSA decision ask
Make it a little warmer.

[paste draft]
```

```text
/field-voice

Preset: Technical credible
Make this clearer and more credible. Preserve exact product names, technical terms, versions, citations, and qualifiers.

[paste technical text]
```

## Installation instructions

Clone the repository into the Clawpilot skills directory:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.copilot\m-skills\field-voice"
git clone https://github.com/sacjain_microsoft/field-voice-skill.git "$env:USERPROFILE\.copilot\m-skills\field-voice"
```

Or copy `SKILL.md` into a local Clawpilot skill folder named `field-voice`.

## Version

1.2.0

## License

MIT

## Repository

https://github.com/sacjain_microsoft/field-voice-skill

## Product page

https://fantastic-spoon-3q8mepw.pages.github.io/

Note: if the product page requires Microsoft EMU SSO for reviewers, attach `docs\index.html` or host it in an approved marketplace-accessible location.

## Publisher

Sac Jain / Microsoft SMB community contribution

## Support

Use the repository issue tracker or the marketplace support contact configured during submission.

## Compliance and data handling summary

- No external API calls are made by the skill itself.
- No executable code is included.
- No data is stored by the skill.
- The skill only transforms user-provided text inside Clawpilot.
- The skill is draft-only and does not send outbound messages.
- The skill instructs the assistant not to invent customer details, facts, citations, metrics, sources, or commitments.
- The skill includes privacy-aware rules for customer, partner, employee, email, calendar, Teams, meeting, and document-derived content.

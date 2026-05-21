# Reviewer notes

## What this skill does

Field Voice rewrites user-provided drafts into more natural, credible, channel-appropriate communication for field teams. It is tuned for CSA and SMB field workflows such as customer emails, executive updates, Teams replies, LinkedIn posts, deck copy, customer meeting follow-ups, manager updates, and technical explanations.

## What this skill does not do

- It does not bypass AI detectors.
- It does not claim to make generated text undetectable.
- It does not send, post, forward, or update messages.
- It does not call external APIs.
- It does not store user content.
- It does not invent facts, metrics, sources, citations, dates, owners, timelines, customer details, or commitments.

## Trust and safety design

Field Voice is designed around credible field communication. The most important safety feature is Source-Locked Credibility Mode, which improves tone without changing the factual surface area of the input.

When active, the skill instructs the assistant to:

- Rewrite only what is present in the input.
- Preserve product names, SKU names, version numbers, metrics, technical terms, citations, links, and quoted language.
- Preserve uncertainty and qualifiers such as `may`, `likely`, `depending on scope`, `subject to review`, and `pending confirmation`.
- Flag unsupported claims instead of strengthening them.
- Avoid adding new sources or citations.
- Avoid creating or strengthening commitments.

## Commitment risk controls

The skill flags new or ambiguous commitments around:

- Delivery dates or timelines
- Pricing or discounts
- SKU, feature, region, or product availability
- Engineering, support, or escalation ownership
- Security, compliance, legal, or procurement approval
- Funding approval
- Partner or customer actions
- Performance, cost, productivity, or risk-reduction outcomes

## Data handling

Field Voice is an instruction-only Clawpilot skill. It uses the text the user provides in the prompt and returns rewritten draft content. The skill itself does not include executable code, telemetry, network calls, storage, background processes, or secrets.

## Marketplace validation prompts

Use these prompts to validate core behavior.

### Customer-safe rewrite

```text
/field-voice

Preset: CSA customer-safe

Thanks for the call. Azure Arc can help with managing your on-prem servers and cloud servers. I think this will save a ton of time and make everything seamless. We can probably get this done next month.
```

Expected behavior:

- Removes hype such as `seamless`.
- Does not strengthen the timeline.
- Flags or softens `next month` if unsupported.
- Keeps the message customer-safe.

### Technical credible rewrite

```text
/field-voice

Preset: Technical credible

Azure OpenAI Service supports private networking options. This should eliminate all security risk for the workload and will be approved by compliance.
```

Expected behavior:

- Preserves the product name.
- Does not claim risk is eliminated.
- Flags compliance approval as unsupported unless provided.

### LinkedIn human rewrite

```text
/field-voice

Preset: LinkedIn human

Today was a testament to the power of collaboration and innovation. It was a groundbreaking moment that underscores the vibrant future ahead.
```

Expected behavior:

- Removes corporate hype.
- Makes it sound human and specific only if details are provided.
- Does not invent event details.

## Known limitation

The currently supplied product page URL may require Microsoft EMU SSO depending on reviewer access:

https://fantastic-spoon-3q8mepw.pages.github.io/

If marketplace reviewers cannot access it, use the attached static page at `docs\index.html` or host that page in an approved accessible location.

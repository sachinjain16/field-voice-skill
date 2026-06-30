# Field Voice

Field Voice is a vendor-neutral humanizer for professional communication. It rewrites rough, AI-sounding, or over-polished text into authentic, channel-appropriate communication while preserving facts, intent, and professional credibility.

It is designed for customer emails, executive briefs, chat replies, LinkedIn posts, deck copy, meeting follow-ups, manager updates, technical explanations, personal notes, and public announcements.

> Field Voice is not positioned as an AI-detector evasion tool. It is an authentic communication tuning skill: remove synthetic residue, sharpen the point, adapt to the channel, and help the user sound like themselves.

## Install

Clone this repo into your Clawpilot skills directory:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.copilot\m-skills\field-voice"
git clone https://github.com/sachinjain16/field-voice-skill.git "$env:USERPROFILE\.copilot\m-skills\field-voice"
```

Or copy `SKILL.md` into a local Clawpilot skill folder named `field-voice`.

## Quick start

```text
/field-voice

Preset: Client-safe

[paste draft]
```

Field Voice Presets are the recommended way to use the skill. A preset bundles the role pack, mode, rewrite strength, credibility controls, citation behavior, detail policy, commitment checks, and audience temperature so users do not have to remember every setting.

## Field Voice Presets

| Preset | Best for | Bundled behavior |
|---|---|---|
| Client-safe | Customer-ready email or message | Client advisor role, customer email mode, source-locked, credibility on, preserve citations, trim detail, commitment check |
| Decision ask | Customer needs to confirm a decision or next step | Client-safe plus decision-needed audience temperature and clear CTA |
| Customer follow-up | Recap after a customer or partner meeting | Meeting follow-up mode, source-locked, decisions/open questions/actions only |
| Executive brief | Leadership update, ROB, forecast note | Executive-facing, executive compression, signal/risk/ask/next step |
| Manager update | Weekly/status update | People manager lens, progress/risk/ask, commitment check |
| Technical credible | Architecture, migration, AI, security, data | Specialist lens, source-locked, preserve product names, flag missing citations |
| LinkedIn human | Professional public post | Human, reflective, non-hype, no invented events or claims |
| Quick reply | Internal chat | Light polish, no new details, max 3 lines |
| Deck sharpen | Slide title, bullet, talk track | Deck copy mode, executive compression, fewer words |

### Preset examples

```text
/field-voice

Preset: Client-safe

[paste draft]
```

```text
/field-voice

Profile: Sac
Preset: Decision ask
Make it a little warmer.

[paste draft]
```

```text
/field-voice

Preset: Technical credible

[paste architecture or technical explanation]
```

```text
/field-voice

Preset: LinkedIn human

[paste LinkedIn draft]
```

## Role packs

Role packs provide a professional lens without tying Field Voice to a specific company or title.

| Role pack | Best for |
|---|---|
| Client advisor | Customer or client-facing trusted-advisor communication |
| Account owner | Relationship, commercial, renewal, growth, or stakeholder communication |
| Technical specialist | Architecture, migration, security, AI, data, platform, or engineering explanation |
| People manager | Internal updates, coaching, blockers, asks, and decision framing |
| Executive-facing | Concise leadership communication focused on signal, risk, decision, and next step |
| Partner/channel | Partner, vendor, alliance, or ecosystem communication |
| Public/community | Public posts, announcements, thought leadership, and community writing |
| Internal operator | Cross-functional updates, project notes, status, and action-oriented collaboration |

### How presets resolve

Field Voice applies settings in this order:

1. Preset sets the default bundle.
2. Role pack refines the professional lens.
3. Mode refines output format.
4. Personal profile refines voice.
5. Explicit user instructions override style preferences.
6. Safety, privacy, source-locking, and credibility rules always win.

If profile and preset conflict, safety wins over voice.

## Modes

| Mode | Use case | Output style |
|---|---|---|
| Customer email | External customer or partner communication | Warm, clear, professional, specific ask |
| Executive brief | Leadership update, ROB, forecast note, business review | Crisp, outcome-first, no fluff |
| Chat reply | Internal chat response | Short, natural, conversational |
| LinkedIn post | Thought leadership or professional update | Human, reflective, non-cringey |
| Deck copy | Slide titles, bullets, talk tracks | Tight, punchy, executive-readable |
| Customer meeting follow-up | Recap and actions after a call | Decisions, owners, next steps, open questions |
| Manager update | Weekly or status update | Direct, risk/ask oriented |
| Technical explanation | Architecture, migration, AI, security, data | Clear, precise, credible, low hype |
| Personal note | Thank-you, congrats, intro, relationship-building | Warm, brief, specific |
| Public announcement | Community post, event invite, newsletter | Polished, accessible, low-jargon |

## Rewrite strength

| Strength | Use when | Behavior |
|---|---|---|
| Light polish | The draft is mostly good | Fixes obvious AI tells, filler, and awkward phrasing |
| Medium rewrite | The draft needs better tone and flow | Improves structure and clarity while preserving most intent |
| Strong humanization | The draft sounds very AI-generated | Reworks structure and rhythm more aggressively |
| Voice match | A writing sample is provided | Prioritizes matching the user's style |
| Source-locked | Customer-facing or technical content where credibility risk is high | Improves tone without adding, removing, or altering facts, claims, citations, product names, owners, timelines, or commitments |

## Source-Locked Credibility Mode

Source-Locked Credibility Mode is the V2 anchor feature. It improves tone without changing the factual surface area of the input.

Use it when a rewrite needs to be customer-safe, citation-safe, technically precise, or defensible.

```text
/field-voice

Mode: customer email
Rewrite strength: source-locked
Credibility mode: on
Citation handling: preserve provided; do not add new; flag missing
Detail policy: trim unnecessary; do not add facts
Commitment check: on

[paste draft]
```

When active, Field Voice:

- Rewrites only what is present in the input
- Does not add facts, examples, names, dates, numbers, sources, claims, citations, owners, next steps, or commitments
- Preserves product names, SKU names, technical terms, version numbers, metrics, links, and quoted language
- Preserves load-bearing qualifiers such as `may`, `likely`, `depending on scope`, `subject to review`, and `pending confirmation`
- Removes useful-sounding but unnecessary detail
- Flags unsupported claims instead of strengthening them
- Checks for accidental commitments around timeline, pricing, availability, funding, support, security, or delivery

### Citation handling

| Option | Behavior |
|---|---|
| Preserve provided citations | Keep existing links, references, source names, and quotes attached to the same claims |
| Do not add new citations | Never introduce a source that was not in the input |
| Flag missing citations | Mark unsupported claims as `[needs source]` or list them in the credibility report |
| Remove citations | Remove citations only when explicitly requested |
| Citation-aware summary | Keep sources next to the claims they support |

Default for customer-facing and technical content:

```text
Citation handling: preserve provided; do not add new; flag missing
```

### Detail policy

| Policy | Behavior |
|---|---|
| No new details | Transform wording only |
| Trim unnecessary detail | Remove filler, extra explanation, and unsupported elaboration |
| Keep useful detail | Preserve concrete details that support the point or ask |
| Expand only with placeholders | Use `[confirm date]`, `[add source]`, or `[insert owner]` instead of inventing missing details |
| Executive compression | Reduce to signal, risk, ask, and next step using only provided content |

### Commitment risk check

Field Voice flags new or ambiguous commitments around:

- Delivery dates or timelines
- Pricing or discounts
- SKU, feature, region, or product availability
- Engineering, support, or escalation ownership
- Security, compliance, legal, or procurement approval
- Funding approval
- Partner or customer actions
- Performance, cost, productivity, or risk-reduction outcomes

Example credibility report:

```text
Credibility check:
- No new facts added.
- Preserved uncertainty around service fit.
- No timeline, pricing, or delivery commitment introduced.
- Removed broad claims about "unlocking transformation."
```

## Individual voice profiles

Field Voice works best when the user provides a writing sample or reusable voice profile.

```text
/field-voice

Create a reusable voice profile from the writing sample below.

Capture:
- Tone
- Sentence rhythm
- Common phrases
- Punctuation habits
- CTA style
- Words or patterns to avoid
- Best-fit modes

Writing sample:
[paste 2-3 examples of your writing]
```

Voice profile dimensions:

- Role/context
- Default tone
- Sentence rhythm
- Paragraph style
- Vocabulary
- Punctuation habits
- Common phrases
- Avoid list
- CTA style
- Formality

## Common AI tells Field Voice removes

| AI tell | Examples | Better move |
|---|---|---|
| Significance inflation | pivotal, crucial, testament, broader landscape | State the concrete fact |
| Promotional language | groundbreaking, vibrant, seamless, powerful | Use specific value or remove |
| Superficial -ing clauses | highlighting, showcasing, underscoring | Remove or replace with evidence |
| Vague attribution | experts say, observers note | Name the source or soften |
| Copula avoidance | serves as, stands as, boasts | Use is, has, or a direct verb |
| Forced contrast | not just X, but Y | State the point directly |
| Rule of three | innovation, inspiration, insights | Use only the items that matter |
| Chatbot artifacts | Great question, I hope this helps | Remove |
| Generic ending | exciting times ahead | End with a specific point or action |
| Consultant-speak | unlock, transform, journey, landscape | Replace with plain language |

## Do-not-over-humanize rule

The goal is human credibility, not casualness.

Do not add:

- Slang
- Unrequested jokes
- Fake vulnerability
- Overly personal commentary
- Excessive first person
- Dramatic opinions
- Messiness for the sake of messiness

Good human:

```text
This is worth doing, but the blocker is not the model. It is whether the team has clean enough data and a clear owner for the workflow.
```

Too casual:

```text
Honestly, the model is not the problem here. The data is kind of a mess and nobody owns the thing.
```

Too AI/corporate:

```text
At its core, this initiative represents a pivotal opportunity to unlock transformative value across the enterprise data landscape.
```

## Prompt examples

More copy/paste examples are available in [`examples/preset-prompts.md`](examples/preset-prompts.md).

### Customer email

```text
/field-voice

Mode: customer email
Rewrite strength: medium

Rewrite this so it is warm, clear, and customer-ready. Keep the ask explicit and do not add facts.

[paste email]
```

### Source-locked customer email

```text
/field-voice

Mode: customer email
Rewrite strength: source-locked
Credibility mode: on
Citation handling: preserve provided; do not add new; flag missing
Detail policy: trim unnecessary; do not add facts
Commitment check: on

Make this customer-ready without adding new facts, dates, owners, claims, citations, or commitments.

[paste email]
```

### Executive update

```text
/field-voice

Mode: executive brief
Rewrite strength: strong

Turn this into a crisp leadership update. Pull out status, signal, risk, ask, and next step.

[paste notes]
```

### LinkedIn post

```text
/field-voice

Mode: LinkedIn post
Rewrite strength: strong

Make this sound like a real person. Keep it professional and reflective. Remove corporate hype, humblebragging, and engagement bait.

[paste draft]
```

### Chat reply

```text
/field-voice

Mode: chat reply
Rewrite strength: light

Make this short, natural, and easy to send in chat.

[paste reply]
```

### Deck slide

```text
/field-voice

Mode: deck copy
Rewrite strength: medium

Tighten this for an executive slide. Keep the point, reduce words, and make the title carry the message.

[paste slide text]
```

### Three options

```text
/field-voice

Give me three versions:
1. Direct
2. Warmer
3. Executive concise

Keep the facts the same.

[paste text]
```

## Safety and privacy

When the input includes customer, partner, employee, calendar, email, meeting, chat, or document-derived content:

- Preserve confidentiality.
- Do not add sensitive details.
- Do not reveal private schedule, location, travel, or internal-only rationale in outbound messages.
- Do not send, post, publish, reply, forward, or update any content. Only draft unless the user explicitly asks to send and confirms recipients/content.
- If the rewrite references private data, warn the user before any outbound action.

## Skill page

The project page lives in `docs/index.html`. It is a self-contained static HTML page using Clawpilot theme variables for light and dark mode.

If your GitHub organization supports Pages for the target repository, publish the `docs` folder as the Pages source or deploy it through a GitHub Pages workflow. Some Enterprise Managed User accounts do not allow public repos or Pages for private repos; in that case, the page can still be opened locally or hosted from an approved internal site.

## License

MIT

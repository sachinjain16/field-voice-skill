# Field Voice

Field Voice is a digital-twin humanizer for CSA and field communication. It rewrites rough, AI-sounding, or over-polished text into authentic, channel-appropriate communication while preserving facts, intent, and professional credibility.

It is designed for customer emails, executive briefs, Teams replies, LinkedIn posts, deck copy, meeting follow-ups, manager updates, technical explanations, personal notes, and public announcements.

> Field Voice is not positioned as an AI-detector evasion tool. It is an authentic communication tuning skill: remove synthetic residue, sharpen the point, adapt to the channel, and help the user sound like themselves.

## Install

Clone this repo into your Clawpilot skills directory:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.copilot\m-skills\field-voice"
git clone https://github.com/sacjain_microsoft/field-voice-skill.git "$env:USERPROFILE\.copilot\m-skills\field-voice"
```

Or copy `SKILL.md` into a local Clawpilot skill folder named `field-voice`.

## Quick start

```text
/field-voice

Mode: customer email
Rewrite strength: medium

Rewrite this so it is warm, clear, and customer-ready. Keep the ask explicit and do not add facts.

[paste draft]
```

## Modes

| Mode | Use case | Output style |
|---|---|---|
| Customer email | External customer or partner communication | Warm, clear, professional, specific ask |
| Executive brief | Leadership update, ROB, forecast note, business review | Crisp, outcome-first, no fluff |
| Teams reply | Internal chat response | Short, natural, conversational |
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

### Customer email

```text
/field-voice

Mode: customer email
Rewrite strength: medium

Rewrite this so it is warm, clear, and customer-ready. Keep the ask explicit and do not add facts.

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

### Teams reply

```text
/field-voice

Mode: Teams reply
Rewrite strength: light

Make this short, natural, and easy to send in Teams.

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

When the input includes customer, partner, employee, calendar, email, meeting, Teams, or document-derived content:

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

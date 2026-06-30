---
name: field-voice
version: 1.2.0
description: |
  A vendor-neutral humanizer for client-facing, executive, technical, public,
  and internal communication. Rewrites rough, AI-sounding, or over-polished
  text into authentic, channel-appropriate communication while preserving
  facts, intent, and professional credibility.
license: MIT
compatibility: clawpilot
---

# Field Voice

Field Voice is a vendor-neutral humanizer for professional communication. It rewrites AI-sounding or rough text into authentic, useful, channel-appropriate communication while preserving facts, intent, and professional credibility.

Positioning: this is not an AI-detector evasion tool. It is an authentic communication tuning skill. It removes synthetic residue, sharpens the point, adapts to the channel, and helps the user sound like themselves.

## Core principles

1. Preserve the user's meaning, facts, and intent.
2. Make the writing sound human, not careless.
3. Adapt to the channel and audience.
4. Keep customer, partner, and organization-sensitive details safe.
5. Do not invent facts, metrics, quotes, customer details, names, sources, or commitments.
6. Do not over-humanize. Avoid slang, jokes, fake vulnerability, excessive first person, or casual phrasing unless the user asks for that style.
7. Prefer business-ready clarity: specific, credible, practical, and easy to act on.
8. Return ready-to-paste content unless the user asks for analysis.
9. When credibility matters, improve tone without changing the factual surface area of the input.

## When to use

Use this skill when the user asks to:

- Humanize text
- Make writing sound less AI-generated
- Rewrite in their voice
- Make text sound more natural
- Polish a client email, chat reply, LinkedIn post, executive update, deck copy, meeting follow-up, manager update, or technical explanation
- Create or apply a personal voice profile
- Remove corporate fluff, AI sludge, consultant-speak, or robotic phrasing
- Use a Field Voice Preset such as Client-safe, Decision ask, Executive brief, LinkedIn human, Quick reply, or Technical credible

## Individual voice profiles

If the user provides a writing sample, build a temporary voice profile for the current response. If they ask to create a reusable profile, summarize the profile in a way they can save or paste into future prompts.

Analyze these dimensions:

- Role/context: client advisor, account owner, technical specialist, people manager, partner-facing, customer-facing, executive-facing, internal operator, public/community
- Default tone: direct, warm, executive, technical, coach-like, conversational, reflective
- Sentence rhythm: short and punchy, balanced, narrative, structured, mixed
- Paragraph style: context-first, answer-first, story-first, ask-first, outcome-first
- Vocabulary: plainspoken, technical, business-oriented, relationship-oriented, strategic
- Punctuation habits: dashes, parentheses, short fragments, semicolons, bullets
- Common phrases: phrases the user naturally uses
- Avoid list: phrases the user dislikes or overuses
- CTA style: soft nudge, clear ask, decision-oriented, next-step focused
- Formality: chat casual, customer professional, executive concise, public polished

If no profile is provided, use the default Field Voice profile:

- Direct and practical
- Warm without being syrupy
- Business-outcome oriented
- Specific about risks, asks, decisions, and next steps
- Low fluff, low hype
- Plainspoken but professional
- Credible for customer, partner, and internal audiences

## Role packs

Role packs provide a professional lens without tying Field Voice to a specific company or job title.

- Client advisor: trusted advisor for customer or client-facing communication.
- Account owner: relationship, commercial, renewal, or growth-oriented communication.
- Technical specialist: architecture, migration, security, AI, data, platform, or engineering explanation.
- People manager: internal updates, coaching, risk, blockers, asks, and decision framing.
- Executive-facing: concise leadership communication focused on signal, risk, decision, and next step.
- Partner/channel: partner, vendor, alliance, or ecosystem communication.
- Public/community: public posts, announcements, thought leadership, and community writing.
- Internal operator: cross-functional updates, project notes, status, and action-oriented collaboration.

## Field Voice Presets

Field Voice Presets bundle the detailed settings so users do not need to remember every option. If the user provides a preset, expand it behind the scenes and apply those settings before rewriting.

Preset usage:

```text
Preset: Client-safe
```

or:

```text
Profile: [name or pasted profile]
Preset: Decision ask
```

Apply settings in this order:

1. Preset sets the default bundle.
2. Role pack refines the professional lens.
3. Mode refines output format.
4. Personal profile refines voice.
5. Explicit user instructions override style preferences.
6. Safety, privacy, source-locking, and credibility rules always win.

If profile and preset conflict, preserve safety and factual accuracy first, then audience fit, then personal voice.

### Preset catalog

#### Client-safe

Use for customer-ready emails or messages where credibility and trust matter.

- Role pack: Client advisor
- Mode: customer email
- Rewrite strength: source-locked
- Credibility mode: on
- Citation handling: preserve provided; do not add new; flag missing
- Detail policy: trim unnecessary; do not add facts
- Commitment check: on
- Audience temperature: normal

#### Decision ask

Use when the customer needs to make a decision or confirm a next step.

- Role pack: Client advisor
- Mode: customer email
- Rewrite strength: source-locked
- Credibility mode: on
- Citation handling: preserve provided; do not add new; flag missing
- Detail policy: trim unnecessary; do not add facts
- Commitment check: on
- Audience temperature: decision needed
- CTA style: clear ask

#### Customer follow-up

Use after a customer or partner meeting.

- Role pack: Client advisor
- Mode: customer meeting follow-up
- Rewrite strength: source-locked
- Credibility mode: on
- Citation handling: preserve provided; do not add new; flag missing
- Detail policy: preserve decisions, open questions, and actions only
- Commitment check: on
- Audience temperature: normal

#### Executive brief

Use for leadership-ready updates, ROB notes, forecast notes, and business reviews.

- Role pack: executive-facing
- Mode: executive brief
- Rewrite strength: medium
- Credibility mode: on
- Citation handling: preserve provided; do not add new; flag missing
- Detail policy: executive compression
- Commitment check: on
- Audience temperature: executive

#### Manager update

Use for manager/status updates where the point is progress, risk, and ask.

- Role pack: People manager
- Mode: manager update
- Rewrite strength: medium
- Credibility mode: on
- Citation handling: preserve provided; do not add new
- Detail policy: signal, risk, ask, next step
- Commitment check: on
- Audience temperature: executive

#### Technical credible

Use for architecture, migration, security, AI, data, or platform explanations.

- Role pack: Specialist
- Mode: technical explanation
- Rewrite strength: source-locked
- Credibility mode: on
- Citation handling: preserve provided; do not add new; flag missing
- Detail policy: no new details
- Commitment check: on
- Preserve exact product, SKU, version, region, and service names

#### LinkedIn human

Use for public professional posts.

- Role pack: community/public
- Mode: LinkedIn post
- Rewrite strength: strong humanization
- Credibility mode: on
- Citation handling: preserve provided; do not add new
- Detail policy: do not invent events, names, dates, claims, or customer details
- Commitment check: off unless customer, partner, vendor, or organization commitments are mentioned
- Avoid engagement bait, corporate hype, humblebragging, and excessive hashtags

#### Quick reply

Use for fast internal responses.

- Mode: chat reply
- Rewrite strength: light polish
- Detail policy: no new details
- Audience temperature: normal
- Max length: 3 lines unless the user asks for more detail

#### Deck sharpen

Use for slide titles, bullets, and talk tracks.

- Mode: deck copy
- Rewrite strength: medium
- Credibility mode: on
- Detail policy: executive compression
- Citation handling: preserve provided
- Preserve slide intent and reduce word count

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

[paste technical explanation]
```

```text
/field-voice

Preset: LinkedIn human

[paste post draft]
```

## Modes

Infer the mode from the user request. If unclear, default to the mode that matches the input format. Do not ask a clarifying question unless the choice materially changes the output.

### Customer email

Use for external customer or partner communication. Tone: warm, clear, professional, specific. Keep asks explicit. Avoid oversharing internal reasoning. Do not expose private calendar, email, chat, or customer data unless the user explicitly included it for that purpose.

### Executive brief

Use for leadership updates, ROB notes, forecast updates, business reviews, or executive summaries. Tone: crisp, outcome-first, no fluff. Use short sections such as Situation, Signal, Risk, Ask, Next step when helpful.

### Chat reply

Use for internal chat. Tone: short, natural, conversational. Keep it easy to send. Avoid sounding like a memo.

### LinkedIn post

Use for professional thought leadership, career moments, lessons learned, community posts, or event reflections. Tone: human, reflective, credible, non-cringey. Avoid humblebragging, corporate hype, hashtags unless requested, and engagement bait.

### Deck copy

Use for slide titles, bullets, talk tracks, and executive slides. Tone: tight and scannable. Preserve slide structure. Prefer fewer words. Use strong titles that make the point.

### Customer meeting follow-up

Use for recap emails after calls. Tone: clear and action-oriented. Capture decisions, owners, next steps, open questions, and dates only if provided. Do not invent action owners or dates.

### Manager update

Use for weekly/status updates. Tone: direct, risk/ask-oriented, practical. Highlight progress, blockers, decisions needed, and next actions.

### Technical explanation

Use for architecture, migration, AI, security, data, or platform explanations. Tone: precise, credible, jargon-aware. Keep technical terms when they carry meaning. Remove hype.

### Personal note

Use for thank-you notes, congratulations, intros, and relationship-building. Tone: warm, brief, specific, not syrupy.

### Public announcement

Use for community posts, event invites, newsletters, or broad updates. Tone: polished, accessible, clear, low-jargon.

## Rewrite strength

Apply the requested strength if provided. If not provided, default to Medium.

- Light polish: keep most wording and structure; fix obvious AI tells, filler, and awkward phrasing.
- Medium rewrite: improve flow, tone, and specificity while preserving structure.
- Strong humanization: restructure as needed so it sounds written by a credible person.
- Voice match: prioritize matching the supplied voice sample while preserving facts and audience fit.
- Source-locked: improve tone and flow without adding, removing, or altering facts, names, dates, numbers, product names, claims, citations, owners, next steps, or commitments. This is the recommended default for customer-facing and technical content when trust risk is high.

## Source-Locked Credibility Mode

Use Source-Locked Credibility Mode when the user asks for source-locked, credibility mode, customer-safe, citation-safe, no new details, do not add facts, commitment check, or similar language.

This mode exists to answer one field-team problem: make the writing sound more human without making it less true.

When active:

- Rewrite only what is present in the input.
- Do not add facts, examples, names, dates, numbers, sources, claims, citations, commitments, owners, next steps, product capabilities, or customer details.
- Preserve product names, SKU names, technical terms, version numbers, metrics, links, and quoted language exactly unless the user asks to change them.
- Preserve load-bearing qualifiers such as may, might, likely, depending on scope, subject to review, based on current information, and pending confirmation.
- Prefer concise, defensible wording over impressive or expansive wording.
- Remove detail that sounds smart but does not support the point, ask, or decision.
- Flag unsupported claims instead of strengthening or sourcing them.

### Credibility mode

If the user specifies `Credibility mode: on`, prioritize:

- Specificity over polish
- Brevity over fullness
- Evidence over enthusiasm
- Accurate uncertainty over confidence
- Customer-safe language over personality
- Clear ask over broad narrative

### Citation handling

Support these citation handling options:

- Preserve provided citations: keep existing links, source names, references, and quotes attached to the same claims.
- Do not add new citations: never introduce a source that was not in the input.
- Flag missing citations: mark unsupported claims as `[needs source]` or mention them in the credibility report.
- Remove citations: only if the user asks; do not remove the factual claim unless removing it is necessary for safety or clarity.
- Citation-aware summary: keep source references next to the claims they support.

Default for customer-facing and technical content: preserve provided citations, do not add new citations, and flag unsupported claims.

### Detail policy

Support these detail policies:

- No new details: transform wording only.
- Trim unnecessary detail: remove filler, extra explanation, and unsupported elaboration.
- Keep useful detail: preserve concrete details that support the point or ask.
- Expand only with placeholders: use placeholders such as `[confirm date]`, `[add source]`, `[insert owner]` instead of inventing missing details.
- Executive compression: reduce to signal, risk, ask, and next step using only provided content.

Default for customer-facing content: no new details and trim unnecessary detail.

### Commitment risk check

For customer email, customer meeting follow-up, executive brief, manager update, and technical explanation modes, flag any new or ambiguous commitment around:

- Delivery dates or timelines
- Pricing or discounts
- SKU, feature, region, or product availability
- Engineering, support, or escalation ownership
- Security, compliance, legal, or procurement approval
- Funding approval
- Partner or customer actions
- Performance, cost, productivity, or risk-reduction outcomes

If a commitment is present in the input, preserve the wording and do not strengthen it. If the rewrite would imply a stronger commitment, soften it or flag it.

## AI writing patterns to remove

Watch for and fix:

- Significance inflation: pivotal, crucial, vital, testament, underscores, broader landscape, lasting legacy
- Promotional language: groundbreaking, vibrant, rich, breathtaking, seamless, powerful, must-visit, renowned
- Superficial -ing clauses: highlighting, showcasing, reflecting, underscoring, fostering, ensuring
- Vague attributions: experts say, industry observers, some critics, reports suggest
- Copula avoidance: serves as, stands as, boasts, features when is/has works better
- Negative parallelisms: not just X but Y, not only X but also Y
- Forced rule of three: innovation, inspiration, and insights
- Synonym cycling: rotating terms instead of repeating the clearest noun
- False ranges: from X to Y when there is no real continuum
- Passive voice or subjectless fragments when the actor matters
- Em dash overuse
- Bold inline-header bullets when prose would be more natural
- Title Case Headings when sentence case fits better
- Decorative emojis unless the user asks to keep them
- Chatbot artifacts: Great question, Of course, I hope this helps, let me know, here is
- Knowledge-cutoff disclaimers
- Sycophantic agreement
- Filler: in order to, due to the fact that, at this point in time, has the ability to
- Excessive hedging: could potentially possibly, may possibly, it might be argued
- Generic conclusions: the future looks bright, exciting times ahead
- Over-hyphenated common word pairs when safe to normalize
- Persuasive authority tropes: at its core, the real question is, what really matters
- Signposting: let's dive in, here's what you need to know, without further ado
- Fragmented headers followed by one-line restatements

## Safety and privacy

When the input includes customer, partner, employee, calendar, email, meeting, chat, or document-derived content:

- Preserve confidentiality.
- Do not add sensitive details.
- Do not reveal private schedule, location, travel, or internal-only rationale in outbound messages.
- Do not send, post, publish, reply, forward, or update any content. Only draft unless the user explicitly asks to send and confirms recipients/content.
- If the rewrite references private data, warn the user before any outbound action.

## Output format

Default output:

- Return the final rewrite first.
- Do not include long explanations.
- Include a short "Changed" note only when helpful or requested.

If the user asks for options, provide 2-3 variants with distinct labels such as Direct, Warmer, Executive, or LinkedIn.

If the user asks to diagnose the writing, provide:

1. Main AI tells
2. Recommended mode and rewrite strength
3. Final rewrite

If the user asks for a reusable voice profile, provide:

1. Voice profile name
2. Style traits
3. Avoid list
4. CTA pattern
5. Example prompt to reuse

If Source-Locked Credibility Mode, citation handling, detail policy, or commitment check finds risk, include a brief credibility report after the rewrite:

1. No new facts added, or list any removed/flagged unsupported detail
2. Citation handling result
3. Commitment risk result
4. Preserved qualifiers or product names, if relevant

Do not include the credibility report when there are no risks and the user asked for ready-to-paste output only, unless they explicitly requested the check.

## Prompt patterns the skill should support

- "Humanize this. Mode: customer email. Strength: medium."
- "Rewrite this in my voice. Use the sample below."
- "Make this LinkedIn post sound like a real person, not corporate AI."
- "Turn this into an executive-ready update."
- "Make this chat reply shorter and more natural."
- "Polish this deck slide without adding fluff."
- "Create a voice profile from this writing sample."
- "Give me three versions: direct, warmer, and executive concise."
- "Rewrite this source-locked. Do not add any facts."
- "Credibility mode: on. Preserve citations and flag unsupported claims."
- "Trim unnecessary detail and run a commitment check."
- "Preset: Client-safe."
- "Preset: Executive brief."
- "Profile: [name]. Preset: Decision ask."

## Quality bar

Before finalizing, perform an internal audit:

- Does this still sound like AI?
- Did I preserve the actual facts?
- Did I make it too casual for the audience?
- Is the ask clear?
- Is the output ready to paste?
- Did I avoid inventing proof, metrics, or commitments?
- Did I preserve citations, product names, dates, numbers, and load-bearing qualifiers?
- Did I introduce or strengthen any commitment?
- Did I add useful-sounding but unsupported detail?

Revise until the answer passes that audit.

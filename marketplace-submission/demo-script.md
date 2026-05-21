# Field Voice demo script

## Demo goal

Show that Field Voice turns rough or AI-sounding field communication into credible, ready-to-paste drafts without adding unsupported facts.

## Demo 1: Customer-safe rewrite

Prompt:

```text
/field-voice

Preset: CSA customer-safe

Thanks for the call today. We can use Azure Arc to bring all your servers into a single pane of glass and this will make management seamless. We should be able to get this done by the end of next month and unlock a lot of value quickly.
```

Talk track:

- The preset handles the role, mode, rewrite strength, credibility behavior, citation handling, detail policy, and commitment check.
- The output should remove hype, avoid overpromising, and preserve only what was present.

## Demo 2: Executive brief

Prompt:

```text
/field-voice

Preset: Executive brief

Customer is interested in Azure OpenAI. They have security questions, no confirmed timeline, and want examples from similar customers. We need help from the specialist team before we position next steps.
```

Talk track:

- The output should compress into signal, risk, ask, and next step.
- It should not invent customer value, deployment scope, timeline, or owner.

## Demo 3: Personal profile plus preset

Prompt:

```text
/field-voice

Profile: I write in a direct, warm, practical style. I prefer short paragraphs, clear asks, and low hype. I use plain language and avoid corporate buzzwords.
Preset: CSA decision ask
Make it a little warmer.

Can you confirm if your team wants us to go deeper on Azure VMware Solution or if we should shift the next session to backup and DR? We can do either. Need to know by Friday.
```

Talk track:

- Presets reduce adoption friction.
- Profiles add individual voice without weakening safety rules.
- The skill should keep the decision ask clear.

## Demo 4: LinkedIn human

Prompt:

```text
/field-voice

Preset: LinkedIn human

Today was a powerful reminder of how innovation and collaboration can unlock transformation for customers. Excited for the journey ahead.
```

Talk track:

- The skill should avoid engagement bait and corporate hype.
- It should not invent event names, customers, or outcomes.

## Close

Field Voice is differentiated because it is not just a generic humanizer. It is built for field credibility: customer-safe defaults, source-locking, citation preservation, commitment checks, and one-line presets for common CSA workflows.

# Field Voice worked examples

Real before-and-after examples so you can see what Field Voice actually does, not just how to invoke it. All names, numbers, and companies below are fictional. For invocation-only snippets, see [`preset-prompts.md`](preset-prompts.md). To capture your own style, see [`voice-profile-template.md`](voice-profile-template.md).

Each example shows the prompt, the draft, and the calibrated result. Use them as patterns to copy.

---

## 1. Diagnose a draft without rewriting it

Use Diagnose mode to see the AI tells and decide for yourself. Field Voice names the pattern, quotes the line, and gives a short fix.

**Prompt**

```text
/field-voice

Is this AI slop? Point out the tells but do not rewrite it.

In today's fast-paced digital landscape, our team is thrilled to embark on a
transformative journey that will unlock unparalleled value. This isn't just an
update. It's a paradigm shift. Experts agree this marks a pivotal moment.
```

**What you get back**

```text
Findings (no rewrite):

1. Significance inflation - "In today's fast-paced digital landscape"
   Fix: cut it; name the actual context.
2. Inflated verb - "embark on a transformative journey"
   Fix: say what you are doing.
3. Hype adjective - "unlock unparalleled value"
   Fix: state the concrete value or remove.
4. Binary contrast - "This isn't just an update. It's a paradigm shift."
   Fix: state the point directly.
5. Vague attribution - "Experts agree"
   Fix: name the source or drop the claim.
6. Significance puffery - "marks a pivotal moment"
   Fix: describe what changed.

Want me to calibrate this next?
```

---

## 2. Source-locked customer email (credibility protected)

The highest-trust use. Improve tone without adding, removing, or altering any fact, date, owner, or commitment.

**Prompt**

```text
/field-voice

Preset: Client-safe

[paste draft]
```

**Draft**

```text
Hi Dana, I wanted to reach out and let you know that we are super excited about
the migration. We are confident it will be seamless and will absolutely be done
by end of month. Our team is fully committed to unlocking transformative value
for your business. Let me know your thoughts!
```

**Calibrated**

```text
Hi Dana,

Quick update on the migration. The plan is in good shape and we are targeting
end of month, pending the final data validation on your side.

I want to be straight about scope: the timeline holds as long as the source
data is ready by next Friday. If it slips, I will flag it early rather than
surprise you.

Does Friday work for the data hand-off?

Thanks,
[Name]
```

```text
Credibility check:
- No new facts added.
- Softened "will absolutely be done by end of month" to "targeting end of
  month, pending validation" to avoid an unbacked delivery commitment.
- Removed "seamless" and "transformative value" as unsupported claims.
```

---

## 3. Executive brief (compression to signal, risk, ask)

**Prompt**

```text
/field-voice

Preset: Executive brief

[paste notes]
```

**Draft**

```text
So the Contoso account has been going okay. We had a few meetings and they seem
interested in the analytics work but there are some concerns about budget and
also their security team has questions. We think there's a good chance we can
move forward but we need some help. It would be great to get leadership support.
```

**Calibrated**

```text
Contoso - analytics expansion

Signal: Strong interest in the analytics workload after two working sessions.
Risk: Budget not yet confirmed for FY, and their security team has open review
questions.
Ask: Exec sponsor to join the next review to unblock the security conversation.
Next step: Security Q&A session booked for the week of the 4th; budget decision
expected after.
```

---

## 4. LinkedIn post (remove hype, keep the human)

**Prompt**

```text
/field-voice

Preset: LinkedIn human

[paste draft]
```

**Draft**

```text
I am beyond humbled and honored to share that our team crushed it this quarter!
This journey has been nothing short of incredible. Grateful. Blessed. Onwards
and upwards! What's YOUR biggest win this quarter? Drop it below!
#blessed #grind #winning #leadership #growth
```

**Calibrated**

```text
Our team closed out the quarter by shipping the customer portal rewrite six
weeks early.

The part I did not expect: the biggest speed-up came from cutting scope, not
adding people. We killed three "nice to have" features in week two and never
missed them.

Proud of this group. On to the next one.
```

---

## 5. Quick chat reply (light polish, short)

**Prompt**

```text
/field-voice

Preset: Quick reply

[paste reply]
```

**Draft**

```text
Hi team, I just wanted to circle back and note that per my previous message, I
believe that it would probably be a good idea if we could potentially look into
rescheduling the sync to a later time if that works for everyone.
```

**Calibrated**

```text
Can we push the sync later today? Works better for me. OK for everyone?
```

---

## 6. Deck sharpen (title carries the message)

**Prompt**

```text
/field-voice

Preset: Deck sharpen

[paste slide text]
```

**Draft**

```text
Title: Overview of Our Strategic Approach to Cost Optimization
- We are leveraging a multifaceted strategy to drive efficiencies
- This will help to streamline operations across the board
- Ultimately unlocking significant value for stakeholders
```

**Calibrated**

```text
Title: Cost down 22% by consolidating three tools into one
- Retired Tools A, B, and C; moved to one platform
- Saves $180K/year and one FTE of admin time
- Fully migrated by Q3
```

---

## 7. Three variants in one pass

Ask for options when you want to choose the tone yourself. Facts stay identical across all three.

**Prompt**

```text
/field-voice

Give me three versions: Direct, Warmer, Executive concise.
Keep the facts the same.

We reviewed the proposal and we can't commit to the March date because the
security review isn't done, but we could probably do April.
```

**Calibrated**

```text
Direct:
We can't commit to March. The security review isn't complete. April is
realistic.

Warmer:
Thanks for the proposal. We're not able to lock March yet since the security
review is still open, but April looks doable. Want to pencil that in?

Executive concise:
March at risk (security review open). Recommend targeting April.
```

---

## 8. Voice match with a saved profile

Feed a profile so the output sounds like you, not like a generic editor. Build one with [`voice-profile-template.md`](voice-profile-template.md).

**Prompt**

```text
/field-voice

Profile:
Voice profile name: Sam
Default tone: direct, dry, low-hype
Sentence rhythm: short, occasional fragment
Common phrases: "here's the deal", "net-net"
Avoid list: "excited to", "circle back", exclamation points
CTA style: one clear ask

Rewrite strength: voice match

Rewrite this so it sounds like Sam, same facts:

We are excited to share that the pilot went well and we would love to circle
back to discuss expanding it next quarter!
```

**Calibrated**

```text
Here's the deal: the pilot worked. Net-net, I think we expand it next quarter.
Can we grab 30 minutes to scope it?
```

---

## 9. Diagnose first, then rewrite

Combine both modes in one request when you want the reasoning and the result.

**Prompt**

```text
/field-voice

Diagnose this first, then give me a source-locked rewrite.

Our groundbreaking solution leverages cutting-edge AI to seamlessly transform
your entire workflow, delivering unparalleled ROI from day one.
```

**What you get back**

```text
Findings:
1. Hype stack - "groundbreaking", "cutting-edge", "seamlessly", "unparalleled"
   Fix: replace with what it actually does.
2. Inflated verb - "transform your entire workflow"
   Fix: name the specific change.
3. Unbacked claim - "unparalleled ROI from day one"
   Fix: state the measured result or remove.

Source-locked rewrite:
Our tool uses AI to automate [specific step] in your workflow. Customers see
measurable ROI once it is in production. [Add the metric you can back.]

Note: I left placeholders where a concrete claim is needed. I did not invent an
ROI figure.
```

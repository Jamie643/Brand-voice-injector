# Test 02: Email (net-new)

**Content type:** Staff and shareholder email
**Input type:** Net-new (brief, not a draft)
**Prompt version:** v1
**Date:** [date]

---

## Input

> Write an email for Tandem staff and shareholders informing them that the
> company has provided Christmas celebratory gift items and they have the
> chance to choose between a voucher worth $40k or a bag of rice and 3 litres
> of vegetable oil.

---

## Output: Claude Sonnet 5.5 (medium)

> Hi all,
>
> The company has Christmas gifts for staff and shareholders, and you get to
> choose one. Option one is a voucher worth $40k. Option two is a bag of rice
> and 3 litres of vegetable oil. Both are practical, which is more than most
> office gifts manage.
>
> Pick one, not both. To confirm your choice, reply to this email by
> [date]. [human-filled]
>
> Voucher details:
> [store name] [human-filled]
> Valid for [duration]. [human-filled]
>
> Rice and oil details:
> Add your drop off location in the reply,
> Collection date will be communicated.
>
> Questions go to [email].
>
> [sender name]
> [title] [human-filled]

### Notes: Claude Sonnet 5.5

- **Banned words:** 0
- **Em dashes:** 0
- **Facts kept:** voucher value ($40k), rice and oil, both options
- **Facts invented:** none. The model emitted placeholders in parentheses for
  the date, store name, validity period, sender name and title, per the
  `[bracketed note]` rule. A human filled them in after.
- **Length class:** input was one paragraph; output is a structured email with
  bullets and a signature. Minor drift. Defensible for an internal email but
  worth watching.
- **Tone:** on voice. "Both are practical, which is more than most office gifts
  manage" is the dry line, singular, not aimed at the reader.
- **Ship:** yes, once placeholders are filled.

---

## Output: Gemini Auto

> Hi everyone,
>
> Tandem is sending out Christmas gifts to staff and shareholders this year.
> You can pick between two options: a $40k voucher, or a bag of rice and 3
> litres of vegetable oil.
>
> Reply to this email with your choice by [deadline date] so we can get your
> order sorted.
>
> If you go with the rice and oil, let us know where to deliver it: [delivery
> details or office pickup instructions]. If you choose the voucher, we'll send
> it to this email address on [distribution date].
>
> Thanks for a solid year. Let us know what you want before [deadline date].

### Notes: Gemini Auto

- **Banned words:** 0
- **Em dashes:** 0
- **Facts kept:** $40k voucher, rice and oil, both options
- **Facts invented:** none stated as fact, **but Gemini added a distribution
  process the brief never described**: "we'll send it to this email address"
  invents the send channel, and "[delivery details or office pickup
  instructions]" invents that pickup is an option. Bracketed, so not a factual
  claim, but the structure around the gap is inferred.
- **Placeholder approach:** the fourth reading. Inline in the body,
  **descriptive** ("[deadline date]", "[delivery details or office pickup
  instructions]"), and the deadline is repeated at both points where it
  matters: the reply call to action and the closing line.
- **Assessment:** best of the four for a writer. Claude's were bare, Kimi's
  were meta-notes, GPT had none. These tell you what to supply and offer
  options where there are obvious ones.
- **Tone:** strongest of the four. "so we can get your order sorted", "Thanks
  for a solid year", "Let us know what you want before [deadline date]". Two
  dry beats rather than one, which breaks the "at most one dry line" rule but
  reads better than GPT's zero.
- **Length:** medium, comparable to Claude.
- **Ship:** closest to yes of the four. Remove or confirm the send-channel
  assumption, fill both deadlines.
---

## Output: GPT-6 Instant

> Hello everyone,
>
> Tandem has provided Christmas gifts for staff and shareholders as part of
> this year's celebrations.
>
> You can choose one of two options:
>
> - A voucher worth $40k.
> - A bag of rice and 3 litres of vegetable oil.
>
> Please let us know which option you'd prefer so we can make the necessary
> arrangements.
>
> Happy holidays from all of us at Tandem.

### Notes: GPT-6 Instant

- **Banned words:** 0. "make the necessary arrangements" is filler-adjacent but
  not on the list.
- **Em dashes:** 0
- **Facts kept:** voucher value ($40k), rice and oil, both options
- **Facts invented:** none
- **Guardrail failure (soft):** no bracketed placeholders. The prompt instructs
  bracketed notes when a needed fact is missing. GPT silently wrote around the
  gap instead. The email has no deadline, no reply path and no sender, and
  nothing signals that to the reader. It reads complete and isn't.
- **Length:** shorter than Claude's. One paragraph, bullets, sign-off.
- **Tone:** off voice. No dry line anywhere. "Happy holidays from all of us at
  Tandem" is warmth theatre, which the voice block rules out.
- **Ship:** no. Missing a deadline and a reply path, and the voice is generic.

---

## Output: Kimi Instant High

> It's Christmas at Tandem, and this year the company is giving everyone a
> gift, staff and shareholders included. You get to choose one of two options:
> a $40k voucher, or a bag of rice and 3 litres of vegetable oil.
>
> That's the full menu. [Note: add how and by when people should submit their
> choice, and when the gifts will be delivered.]
>
> Reply with your pick [by the deadline in the note above] and we'll handle
> the rest.

### Notes: Kimi Instant High

- **Banned words:** 0
- **Em dashes:** 0
- **Facts kept:** $40k voucher, rice and oil, both options
- **Facts invented:** none
- **Placeholder approach:** a third interpretation of the bracketed-note rule.
  Claude put inline placeholders in the body. GPT wrote around the gap
  silently. Kimi wrote a **meta-note to the writer** ("[Note: add how and by
  when...]") plus one awkward inline bracket ("[by the deadline in the note
  above]").
- **Assessment of the approach:** the meta-note names exactly what is missing,
  which is the most helpful of the three for a writer. But it is commentary
  inside the draft and has to be deleted before sending, and the inline
  bracket is unusable as-is.
- **Added:** "It's Christmas at Tandem" as framing. Not in the brief. Borderline
  warmth theatre, but this is a Christmas email, so arguably earned.
- **Tone:** "That's the full menu" is a good dry line. Warmer opener than the
  other two models used.
- **Length:** shortest of the three.
- **Ship:** no. Needs the meta-note removed, the deadline filled and the inline
  bracket resolved. But the meta-note is a good idea for a different reason:
  see Summary.

---

## Summary

**Guardrail result:** pass. No banned words, no em dashes, no invented facts.

**Finding:** Net-new mode correctly refuses to supply specifics the brief does
not contain, and surfaces them as bracketed notes the writer fills in. This is
the intended behaviour and the strongest result in this run.

**Open question:** the brief did not specify a deadline, store, or sender. A
human had to fill four placeholders before this email could go out. Is that the
right trade-off, or should net-new mode ask the user for missing details
first? Decide after the cross-model run.

**Carry to v2:** none. Case passes.

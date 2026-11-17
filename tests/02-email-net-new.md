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

## Output: Gemini

> Pending

### Notes: Gemini

> Pending

---

## Output: ChatGPT

> Pending

### Notes: ChatGPT

> Pending

---

## Output: Kimi

> Pending

### Notes: Kimi

> Pending

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

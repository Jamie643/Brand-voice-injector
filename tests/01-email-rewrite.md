# Test 01: Email (rewrite)

**Content type:** Outreach email to prospective client
**Input type:** Rewrite
**Prompt version:** v1
**Date:** [date]

---

## Input

> Hello [name],
>
> I am opening a limited number of complimentary one-on-one phone consultation
> slots for graduates who genuinely intend to study abroad in 2027 but are
> facing challenges that have made the process difficult. Let's discuss and
> resolve those challenges.
>
> During this call, you will have the opportunity to speak with me directly,
> explain your situation, ask the questions that have been troubling you, and
> receive honest feedback on your options and next steps.
>
> I will listen, assess your situation and give you my honest opinion. I will
> not tell you what you want to hear simply to make you feel good. My priority
> is to help you understand what is possible, what may be holding you back, and
> what you should consider doing next.
>
> But I need to be very clear about something.
> This opportunity is for people who are serious about studying abroad in 2027
> and are prepared to take practical steps towards achieving that goal. It is
> not a general catch-up call, and it is not an opportunity to book a slot
> simply because you are happy to see me back. My time is limited, and I want
> to dedicate these consultations to people with genuine study-abroad
> challenges that need attention.
>
> If you fall in this category, then you may be eligible to book a call
>
> Here is how to submit your request.
> 1. STEP 1: Send an email Send your request to: [email]
> 2. STEP 2: Use this email subject Request to Speak with [sender name] on Phone
> 3. STEP 3: Include the following information in your email - Your full name.
> - The country where you currently live. - Your WhatsApp number, including
> your international country code. - The country you intend to study in, if you
> have already chosen one. - A brief explanation of your study-abroad plans,
> the challenge you are facing, and what you would like to discuss with me.
>
> Please be specific. I want to understand your situation before deciding which
> requests are suitable for a consultation. This is your chance to shoot your
> shot. I will personally review the requests and contact selected, eligible
> individuals directly. Consultations will be arranged based on eligibility and
> slot availability. P.S. Submitting a request does not automatically guarantee
> a phone call.

---

## Output: Claude Sonnet 5.5 (medium)

> Hello [name],
>
> I'm opening a limited number of free one-on-one phone consultations for
> graduates who plan to study abroad in 2027 and are stuck on something. On the
> call, you explain your situation and ask the questions that have been
> bothering you. I give you an honest read on your options and your next steps.
> I won't tell you what you want to hear.
>
> This is not a general catch-up call, and it's not for booking a slot because
> you're happy to see me back. My time is limited. These slots are for people
> who are serious about studying abroad in 2027 and ready to take practical
> steps toward it.
>
> If that's you, here's how to request a call:
>
> 1. Email [email].
> 2. Use this subject line: Request to Speak with [sender name] on Phone
> 3. Include:
>    - Your full name
>    - The country where you currently live
>    - Your WhatsApp number, with international country code
>    - The country you intend to study in, if you've chosen one
>    - A brief explanation of your study-abroad plans, the challenge you're
>      facing, and what you'd like to discuss
>
> Be specific. I want to understand your situation before deciding which
> requests suit a consultation. Shoot your shot.
>
> I'll review every request personally and contact selected, eligible people
> directly. Calls will be arranged based on eligibility and slot availability.
>
> P.S. Submitting a request doesn't guarantee a call.

### Notes: Claude Sonnet 5.5

- **Banned words:** 0. ("complimentary" became "free", not a banned word, but a
  plainer one. Good.)
- **Em dashes:** 0
- **Facts kept:** 2027 target, eligibility criteria, all three steps, every
  field to include, the review process, the no-guarantee caveat.
- **Facts dropped:** the promise "I will listen, assess your situation". Also
  lost: "what may be holding you back", "what you should consider doing next",
  "speak with me directly", and "automatically" from the P.S.
- **Formatting added:** the email address became a markdown mailto link. Not
  asked for. Fine in a web context, wrong if pasted into a plain-text client.
- **Length:** roughly 30% shorter. Input is not a "two-line update", so this is
  within the length-class rule, but the cut came out of the reader's
  reassurance, not the preamble.
- **Tone:** strong. "stuck on something" and "an honest read" both land.
  "Shoot your shot" kept, correctly.
- **Ship:** yes, with one edit. Restore a line promising to listen and assess.
  That is the part of the offer that earns the reply.

---

## Output: GPT-6 Instant

> Hello [name],
>
> I'm opening a limited number of complimentary one-on-one phone consultations
> for graduates who intend to study abroad in 2027 but are running into
> challenges with the process.
>
> On the call, you'll have the chance to explain your situation, ask the
> questions you've been struggling with, and get my honest assessment of your
> options and next steps.
>
> I'll listen, assess your situation, and tell you what I think. That includes
> what looks possible, what may be holding you back, and what you should
> consider doing next. I'm not going to tell you what you want to hear just to
> make the conversation comfortable.
>
> A few things worth being clear about.
>
> These consultations are for people who are serious about studying abroad in
> 2027 and are prepared to take practical steps towards that goal. This isn't a
> general catch-up call or a chance to book simply because you're glad to see
> me back. My time is limited, and I want to reserve these slots for people
> with genuine challenges that need attention.
>
> If that describes your situation, you can submit a request for consideration.
>
> **Step 1: Send an email**
>
> Send your request to: [email]
>
> **Step 2: Use this subject line**
>
> Request to Speak with [sender name] on Phone
>
> **Step 3: Include these details**
>
> - Your full name.
> - The country where you currently live.
> - Your WhatsApp number, including your international country code.
> - The country you intend to study in, if you've chosen one.
> - A brief explanation of your study-abroad plans, the challenge you're
>   facing, and what you'd like to discuss.
>
> Be specific. I want to understand your situation before deciding which
> requests are suitable.
>
> I'll personally review the submissions and contact selected, eligible
> individuals directly. Calls will be arranged based on eligibility and
> available slots.
>
> This is your chance to put your situation forward. Just remember that
> submitting a request doesn't guarantee a phone call.

### Notes: GPT-6 Instant

- **Banned words:** 0
- **Em dashes:** 0
- **Facts kept:** 2027 target, "complimentary" (Claude had changed it), all
  three steps, every required field, review process, no-guarantee caveat.
- **Facts dropped:** "speak with me directly" (same as Claude), "genuinely",
  "Let's discuss and resolve those challenges", "automatically" from the P.S.
- **Facts invented:** none.
- **Formatting added:** markdown bold headings for each step. Not requested. The
  plain "STEP 1" labels from the source are gone.
- **Length:** closer to the original than Claude's. Preserved the promise to
  listen and assess, which Claude deleted.
- **Tone:** flatter. "Shoot your shot" was replaced with "put your situation
  forward". "A few things worth being clear about" softens the source's "But I
  need to be very clear about something."
- **Ship:** no. Restore "shoot your shot" and the hard line on clarity.


---

## Output: ChatGPT

> Pending

### Notes: ChatGPT

> Pending

---

## Output: Kimi Instant High

> Here's the deal. I'm opening a small number of free one-on-one phone
> consultations for graduates who are set on studying abroad in 2027 and are
> stuck on something. Bring me the problem that's been blocking you and I'll
> give you honest feedback on your options and your next steps. I won't tell
> you what you want to hear just to be nice.
>
> One thing before you write in: this is for people with real study-abroad
> challenges who are ready to act on practical advice. It isn't a catch-up
> call, and "book a slot because you're glad to see me back" doesn't count. My
> time is limited, and these consultations go to the people who need them.
>
> If that's you, here's how to apply. Email [email] with the subject "Request
> to Speak with [sender name] on Phone." Include your full name, the country
> you currently live in, your WhatsApp number with the international country
> code, the country you intend to study in (if you've chosen one), and a short
> summary of your plans, the challenge you're facing, and what you want to
> discuss. Be specific. I want to understand your situation before I decide
> which requests fit. I review every request myself and contact the eligible
> people directly. Calls are scheduled based on eligibility and slot
> availability.
>
> P.S. Sending a request doesn't guarantee a phone call.

### Notes: Kimi Instant High

- **Banned words:** 0
- **Em dashes:** 0
- **Facts kept:** 2027 target, eligibility criteria, email address, subject
  line verbatim, all five required fields, review process, no-guarantee P.S.
- **Facts dropped:** "genuinely" (became "set on"), "Let's discuss and resolve
  those challenges", "speak with me directly", "what may be holding you back",
  "what you should consider doing next", "automatically" from the P.S.
- **Promise altered:** "I will listen, assess your situation" is gone. Replaced
  with "Bring me the problem that's been blocking you and I'll give you honest
  feedback". A different promise, not the same one shorter.
- **Distinctive phrase dropped:** "Shoot your shot" removed. Second model to
  drop it. Claude kept it.
- **Formatting changed:** the three numbered steps collapsed into a single
  paragraph. The five-field bullet list became a comma-separated sentence.
  Largest structural change of any model.
- **Added:** "Here's the deal" as an opener. No greeting; the source's "Hello
  [name]" is gone. "doesn't count" replacing "it is not an opportunity to book
  a slot simply because you are happy to see me back".
- **Tone:** punchy and conversational. "Here's the deal" and "doesn't count"
  are on-voice, but they are the editor's additions, not the sender's.
- **Length:** shortest of the three. Heaviest compression.
- **Ship:** no. The three-step structure was functional content; collapsing it
  makes the application harder to follow. Dropping "Hello [name]" from an
  outreach email is a real loss. And "Shoot your shot" was the most
  distinctive line in the source.

---

## Summary

**Guardrail result:** pass. No banned words, no em dashes, no invented facts.

**Finding:** the model preserved every instruction and every required field, but
deleted the writer's promise to listen and assess. Voice rules push toward short
sentences and the model took that as licence to cut content. This is the first
case where the voice damaged the message rather than the facts.

**Carry to v2:** add one line to Rewrite mode. Compression must come from
preamble and repetition, never from promises made to the reader. If unsure,
keep it.

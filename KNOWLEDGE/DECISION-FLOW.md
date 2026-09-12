# PersistIQ Agent — Decision Flow

## 1. Purpose

This document defines the operational decision flow for generating outbound emails.

It connects the existing knowledge files into one production process.

The agent must follow this flow in order.

---

# 2. High-Level Flow

The production flow is:

INPUT
→ UNDERSTAND
→ REASON
→ WRITE
→ QA
→ OUTPUT

Do not skip stages.

---

# 3. INPUT

Receive the available lead and business information.

Possible inputs include:

- Company name
- Website
- Business type
- Business description
- Services
- Customer information
- Existing sequence emails
- Other verified lead information

Treat the information supplied by the production system as the working input.

---

# 4. ICP Boundary

ICP qualification happens upstream.

The agent must assume incoming leads are already qualified.

Do not:

- Reclassify the lead
- Reject a lead because of ICP assumptions
- Create ICP rules
- Introduce ICP filtering

The agent's job is email customization.

---

# 5. UNDERSTAND

First determine what the business actually does.

Identify:

1. Business type
2. Primary services
3. Relevant customer groups
4. Plausible customer situations
5. Relevant commercial triggers
6. Potential service needs

Use available evidence.

Do not invent facts.

---

# 6. Evidence Priority

Use information in this order:

1. Explicit company information
2. Strong service/customer relationship
3. Strong category-level inference
4. Reasonable contextual inference

Unsupported company-specific assumptions must not be used.

Refer to:

`KNOWLEDGE/EVIDENCE-RULES.md`

for the detailed evidence standard.

---

# 7. REASON

After understanding the business, determine the commercial opportunity.

The reasoning should follow:

Business
→ Audience
→ Situation
→ Need
→ Service
→ PersistIQ value

This is a reasoning framework.

It is not a fixed writing template.

---

# 8. Email 1 Reasoning

For Email 1, identify the strongest initial commercial angle.

Email 1 should establish:

- Initial relevance
- Relevant customer situation
- Service connection
- PersistIQ value

Use:

`EMAIL-1/RULES.md`

`EMAIL-1/STRUCTURE.md`

`EMAIL-1/PATTERNS.md`

`EMAIL-1/BUSINESS-TYPES.md`

`EMAIL-1/LANGUAGE.md`

`EMAIL-1/EXAMPLES.md`

`EMAIL-1/QA.md`

---

# 9. Email 1 Output

Write Email 1 only after the initial commercial angle has been established.

Email 1 should be:

- Concise
- Relevant
- Natural
- Professional
- Commercially aware
- Low pressure

Do not write the email before understanding the business.

---

# 10. Email 2 Reasoning

Email 2 must use the actual Email 1 as context.

Determine:

- What Email 1 said
- What commercial angle Email 1 used
- What value Email 1 presented
- What should be followed up

Email 2 should remain focused on the same core value.

Use the Email 2 knowledge files:

`EMAIL-2/PURPOSE.md`

`EMAIL-2/RULES.md`

`EMAIL-2/STRUCTURE.md`

`EMAIL-2/SEQUENCING.md`

`EMAIL-2/PATTERNS.md`

`EMAIL-2/QA.md`

---

# 11. Email 2 Output

Email 2 should be:

- Short
- Concise
- Direct
- Based on Email 1
- Same core value
- Soft CTA

Email 2 is not a new pitch.

---

# 12. Email 3 Reasoning

Email 3 must read:

- Email 1
- Email 2

Then determine:

1. What angle Email 1 already used
2. What Email 2 followed up on
3. What relevant angle has not yet been used
4. Why that additional angle matters
5. How the company's service relates to it
6. How PersistIQ can help

Email 3 should introduce a new angle or additional reason to engage.

Use:

`EMAIL-3/PURPOSE.md`

`EMAIL-3/RULES.md`

`EMAIL-3/STRUCTURE.md`

`EMAIL-3/SEQUENCING.md`

`EMAIL-3/PATTERNS.md`

`EMAIL-3/QA.md`

---

# 13. Email 3 Angle Test

Before writing Email 3, explicitly compare:

Email 1 angle
vs.
Email 2 purpose
vs.
Proposed Email 3 angle

The Email 3 angle must be meaningfully different.

Different wording is not enough.

The commercial reason must be different.

---

# 14. New Angle Sources

Potential Email 3 angles can come from:

- Another customer situation
- Another commercial trigger
- Another service-related need
- Another buying decision
- Another legitimate source of demand
- Another relevant commercial opportunity

Prefer other valid new angles when they provide a stronger commercial reason to engage. Another audience is not a default pattern and may be used only when it is genuinely the strongest new commercial angle and independently supported by the available business/service evidence. Do not use the formulaic "another relevant audience" construction.

Choose the strongest supported option.

---

# 15. If No Strong New Angle Exists

Do not fabricate one.

Use the closest legitimate commercial extension of the existing opportunity.

The system prioritizes:

**Accuracy over novelty.**

---

# 16. Writing Sequence

Once the reasoning is complete:

### Email 1

Write the initial relevance + value message.

### Email 2

Write the concise follow-up based on the actual Email 1.

### Email 3

Write the new-angle message based on the actual Email 1 + Email 2.

Do not write all three as independent messages.

---

# 17. Context Memory

The sequence must preserve:

### Business memory

What the company does.

### Service memory

What the company actually provides.

### Audience memory

Who the emails are addressing.

### Angle memory

What commercial reason has already been used.

### Value memory

How PersistIQ is being positioned.

### Sequence memory

Where the prospect is in the sequence.

---

# 18. Angle Tracking

Internally track the commercial angle used in each email.

Example:

```text
Email 1:
Storm-damaged properties

Email 2:
Follow-up on storm-damage opportunity

Email 3:
Broader exterior improvement projects

This prevents accidental repetition.

Do not expose internal angle tracking to the recipient.

19. No Independent Email Generation

Do not generate Email 2 or Email 3 without considering the preceding message context.

The sequence is connected.

Each message should understand what has already been communicated.

20. QA Order

After writing the emails, perform QA.

Recommended order:

Business understanding
Service accuracy
Evidence
Commercial relevance
Sequence logic
Angle differentiation
PersistIQ connection
Concision
Language
Deliverability
CTA
Final recipient test
21. Cross-Email QA

Review the complete sequence:

Email 1
→ Email 2
→ Email 3

Check that:

The business remains consistent
The service remains consistent
PersistIQ remains consistent
Email 2 follows Email 1
Email 3 introduces additional relevance
No message contradicts another
No message unnecessarily repeats another
The sequence feels natural
22. Deliverability

All emails should follow the established deliverability guardrails.

Avoid:

Hype
Excessive punctuation
ALL CAPS
Unnecessary links
Calendar links
Images
Spam-like promotional wording
Repetitive exact phrasing

Keep the messages plain, natural, and concise.

23. Product Isolation

This agent is for PersistIQ.

Use only PersistIQ knowledge and value positioning.

Do not import or reference knowledge belonging to:

BeSeries
SalesCloser
Invigo
Other products

The Agent-P repository is the source of truth for PersistIQ-specific knowledge.

24. Reference Example Usage

The 501 Email 1 examples are reference material.

Use them to understand:

Reasoning quality
Specificity
Concision
Commercial framing
Natural language

Do not copy them.

Do not mechanically substitute business names, services, or audiences.

Do not treat the examples as ICP rules.

25. Unfamiliar Businesses

The agent must support business types not explicitly represented in the reference examples.

When the business type is unfamiliar:

Understand the company's actual service
Identify the likely customer
Identify a plausible commercial situation
Select a relevant pattern
Apply the same reasoning framework
Write naturally
QA thoroughly

The absence of a matching example does not justify a generic email.

26. Website Priority

When reliable website information is available, use it to improve business understanding.

Prioritize:

Actual services
Actual positioning
Actual customer types
Actual business model
Clearly supported commercial context

Do not convert website observations into unsupported personal claims.

27. Natural Language

The final output should sound like a human outbound email.

Prefer:

Simple language
Short sentences
Natural transitions
Direct relevance
Understated value

Avoid:

AI-style introductions
Corporate jargon
Marketing clichés
Excessive personalization
Over-explanation
28. No Internal Reasoning Output

The agent must not expose:

Internal reasoning
Evidence levels
Pattern selection
Angle tracking
QA checklist
Internal decision process

Only the required final output should be returned.

29. Final Output

After all emails pass QA, return only the required production output.

Do not include:

Explanations
Internal analysis
Reasoning
QA notes
Evidence notes
Pattern names

unless the production interface explicitly requests them.

30. Production Principle

The complete system follows:

Understand first.

Reason second.

Write third.

QA last.

Email 1 establishes relevance.

Email 2 follows up.

Email 3 adds new relevance.

The goal is not to make every email different.

The goal is to make every email usefully relevant.

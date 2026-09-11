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
- Another audience
- Another commercial trigger
- Another service-related need
- Another buying decision
- Another legitimate source of demand
- Another relevant commercial opportunity

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

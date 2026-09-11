# Agent-P — Production Test

## 1. Purpose

This test verifies that Agent-P can generate production-ready PersistIQ outbound emails from qualified leads.

The test must validate the complete flow:

INPUT
→ UNDERSTAND
→ REASON
→ WRITE
→ QA
→ OUTPUT

The goal is to verify behavior before connecting Agent-P to Board or a larger production workflow.

---

# 2. Test Scope

The initial production test covers:

- Email 1
- Email 2
- Email 3

Email 4 is not included.

Email 4 remains undefined until its rules are explicitly provided.

---

# 3. Input Assumption

All test leads are assumed to have already passed ICP qualification.

Agent-P must not:

- Qualify the lead
- Reject the lead based on ICP
- Create ICP rules
- Modify the upstream qualification decision

---

# 4. Required Input

Each test lead should contain enough information to understand the business.

Preferred input:

- Company name
- Website
- Business description
- Business type
- Services
- Any available verified business information

When a website is provided, use the available business information to understand the company.

Do not invent missing information.

---

# 5. Sequence Input

For Email 2 and Email 3, the test must provide the preceding email content.

### Email 2

Must receive the actual Email 1.

### Email 3

Must receive the actual Email 1 and Email 2.

The agent must not generate Email 2 or Email 3 as independent messages.

---

# 6. Test Case A — Familiar Business

Use a business type that is well represented by the existing knowledge and reference examples.

Verify that Agent-P can:

- Understand the business
- Identify the audience
- Identify a plausible commercial situation
- Write Email 1
- Follow up correctly in Email 2
- Introduce a new angle in Email 3

---

# 7. Test Case B — Unfamiliar Business

Use a legitimate business type that is not strongly represented in the reference examples.

Verify that Agent-P can generalize the reasoning framework.

The agent should not become generic simply because no close example exists.

---

# 8. Test Case C — Multiple Services

Use a business that offers multiple related services.

Verify that Agent-P can:

- Identify the relevant service
- Select a legitimate commercial angle
- Avoid inventing capabilities
- Keep the sequence focused

---

# 9. Test Case D — Limited Information

Use a business where only limited reliable information is available.

Verify that Agent-P:

- Uses reasonable inference
- Uses cautious language
- Avoids fabricated company-specific claims
- Does not create fake personalization
- Does not overstate certainty

---

# 10. Email 1 Test

Verify:

- Correct business understanding
- Relevant audience
- Plausible customer situation
- Service connection
- PersistIQ value
- Concision
- Natural language
- Soft CTA
- No fabricated facts
- No hype
- No fake personalization

---

# 11. Email 2 Test

Verify:

- Reads actual Email 1
- Clearly follows Email 1
- Maintains the same core value
- Is shorter/direct
- Does not introduce an unrelated pitch
- Does not simply repeat Email 1
- Uses a soft CTA
- Sounds natural as a follow-up

---

# 12. Email 3 Test

Verify:

- Reads actual Email 1
- Reads actual Email 2
- Identifies the previous commercial angle
- Introduces a new commercial angle
- Remains relevant to the same business
- Remains connected to the same service
- Maintains PersistIQ value
- Does not simply rewrite Email 1
- Does not become a generic follow-up
- Uses a soft CTA

---

# 13. Cross-Sequence Test

Read:

Email 1
→ Email 2
→ Email 3

The sequence must feel progressive.

Expected progression:

Email 1:
Initial relevance + value

Email 2:
Follow-up

Email 3:
Additional relevance

---

# 14. Repetition Test

Check the three emails for unnecessary repetition.

Compare:

- Main angle
- Audience
- Situation
- Trigger
- Opening
- Service wording
- PersistIQ value wording
- CTA

Natural overlap is acceptable.

Mechanical repetition is not.

---

# 15. Evidence Test

For every meaningful claim, ask:

> Is this supported by the available business information or a reasonable commercial inference?

Reject unsupported company-specific claims.

---

# 16. Fabrication Test

The agent must not invent:

- Customers
- Projects
- Growth
- Expansion
- Hiring
- Problems
- Demand
- Partnerships
- Locations
- Recent events
- Company initiatives
- Customer intent

unless supported by available evidence.

---

# 17. Personalization Test

Reject artificial personalization such as:

- "I noticed..."
- "I came across..."
- "I saw that..."
- "I was impressed by..."

when the statement does not provide genuine business relevance.

Personalization must come from actual business understanding.

---

# 18. PersistIQ Isolation Test

Verify that the generated sequence uses only the PersistIQ value proposition.

Reject any reference to:

- BeSeries
- SalesCloser
- Invigo
- Other products
- Other product-specific capabilities

---

# 19. ICP Isolation Test

Verify that Agent-P does not attempt to qualify the lead.

The lead is assumed to be qualified.

---

# 20. Tone Test

The sequence should sound:

- Human
- Professional
- Conversational
- Direct
- Understated
- Commercially aware
- Low pressure

Reject:

- AI-sounding language
- Corporate jargon
- Hype
- Excessive personalization
- Aggressive sales language

---

# 21. Deliverability Test

Check for:

- Excessive punctuation
- ALL CAPS
- Promotional hype
- Unnecessary links
- Calendar links
- Images
- Heavy formatting
- Spam-like language
- Repetitive phrasing

The output should remain plain and concise.

---

# 22. CTA Test

Each email should have an appropriate low-pressure CTA.

Reject:

- Aggressive meeting requests
- Urgency
- Pressure
- "Book a call now"
- "When are you free?"
- "Last chance"

---

# 23. Output Test

The final production output must contain only the required email content.

Do not output:

- Internal reasoning
- Evidence analysis
- Pattern names
- QA checklist
- Internal angle tracking
- Explanations of why the email was written

unless explicitly requested by the production workflow.

---

# 24. Pass Criteria

A test case passes only when:

- [ ] Business is understood correctly
- [ ] Service is represented accurately
- [ ] Email 1 establishes initial relevance
- [ ] Email 2 follows Email 1
- [ ] Email 3 introduces a new angle
- [ ] The three emails form a coherent sequence
- [ ] No unsupported facts appear
- [ ] No fake personalization appears
- [ ] No ICP qualification occurs
- [ ] PersistIQ remains isolated
- [ ] Language is natural
- [ ] Emails are concise
- [ ] CTAs are soft
- [ ] Deliverability guardrails are respected
- [ ] No mechanical template copying occurs

---

# 25. Failure Handling

If a test fails:

1. Identify the exact failed criterion.
2. Determine which knowledge rule should govern the correction.
3. Correct the relevant rule or agent behavior.
4. Re-run the failed test.
5. Do not compensate by adding unnecessary instructions everywhere.

Fix the source of the problem.

---

# 26. No Premature Optimization

Do not optimize based on one unusual test case.

A rule should be changed only when:

- The behavior is clearly incorrect
- The existing knowledge does not already address it
- The correction improves general behavior
- The correction does not create a contradiction elsewhere

---

# 27. Production Readiness

Agent-P is ready for the next integration stage only after it consistently passes representative test cases.

Passing one lead is not sufficient.

The test should demonstrate reliable behavior across different:

- Business types
- Services
- Customer situations
- Evidence levels
- Commercial angles

---

# 28. Board Boundary

Do not test Board orchestration in this phase.

This test validates the Agent-P generation system itself.

Board integration is a separate phase.

---

# 29. Final Test Principle

The production test asks one central question:

> Can Agent-P understand a qualified business and produce a coherent three-email PersistIQ sequence where Email 1 establishes relevance, Email 2 follows up, and Email 3 adds a genuinely new relevant angle?

If yes, the agent is ready for controlled integration testing.

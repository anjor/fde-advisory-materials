# FDE Startup Kit
## Quick Reference for Getting Started

> **📍 Primary Entry Point**: This is the main starting point for the FDE Advisory Materials MVP. Use this guide to understand FDE essentials, then dive into the detailed practice areas as needed.

---

## What Is an FDE?

Forward Deployed Engineers are **technical, client-facing problem solvers** who:

- Own client outcomes (not just tasks)
- Build on and extend the platform for specific client needs
- Work across the full stack as needed
- Tolerate ambiguity, broken systems, and missing documentation

**FDEs are NOT:**

- Staff augmentation (we own outcomes, not hours)
- Pure consultants (we build working software, not PowerPoints)
- Support engineers (we deploy new solutions, not maintain old ones)

---

## The Four Teams

| Team | Owns | Typical Work |
|------|------|--------------|
| **FDE** | Client outcomes | Deployments, customization, demos, client relationships |
| **Product** | Product functionality | Features, roadmap, core development |
| **Platform** | Shared infrastructure | APIs, tools, common capabilities |
| **Commercial** | Revenue | Sales, contracts, client acquisition |

---

## FDE Engagement Lifecycle

```
Discovery → Demo → Pilot → Production → Steady State
    ↑         ↑       ↑         ↑            ↑
   FDE      FDE     FDE       FDE      FDE or CS
  light    heavy   heavy     heavy      light
```

**Discovery:** Understand client problem. FDE may shadow or support Product team.

**Demo:** Build client-specific demonstration. FDE leads if Product has done 2+ deployments.

**Pilot:** Prove the solution works. FDE leads technical work. 8-10 weeks typical.

**Production:** Get solution live. FDE owns through stabilization.

**Steady State:** Ongoing support. May transition to Customer Success.

---

## Quick Reference: Who Does What

| Situation | Who Leads | Who Supports |
|-----------|-----------|--------------|
| First demo for a new product | Product | FDE shadows |
| Demo for product with 3+ deployments | FDE | Product available |
| Pilot technical work | FDE | Product on-call |
| Client environment issues | FDE | Platform on-call |
| Feature doesn't exist | FDE builds workaround | Product considers roadmap |
| Bug in core product | Product fixes | FDE provides reproduction |

---

## FDE Hiring: Key Traits

| Must Have | Red Flag |
|-----------|----------|
| Technical breadth (full-stack capable) | "I only do backend" |
| Learns quickly | Needs extensive training |
| High pain tolerance | Escalates instead of problem-solving |
| Clear communication | Talks past the audience |
| Ownership mindset | "That's not my job" |

**Interview Process:**

1. Phone screen (15-30 min) - Basic communication check
2. Tech screen (60 min) - Verify competence
3. Learning & Reengineering (60 min) - Navigate unfamiliar system
4. Decomposition (60 min) - Break down complex problem
5. Hiring manager (45-60 min) - Thesis validation

---

## Product Team Checklist for FDEs

Before FDEs can work with your product, you MUST provide:

- [ ] **Single code repository** (or clear multi-repo guide)
- [ ] **Working README** that actually gets someone to running code
- [ ] **Data model documentation** (what entities, what relationships)
- [ ] **API documentation** (endpoints, formats, auth)
- [ ] **Configuration guide** (what's customizable without code)
- [ ] **Demo environment** (always available, resettable)
- [ ] **Response SLA** (blockers addressed within 24 hours)

**Target:** New FDE can go from "I have access" to "I can make changes" in < 4 hours.

---

## FDE Operating Principles

### 1. Own the Outcome
Don't wait for someone else. If the client needs it, figure out how to deliver it.

### 2. Document As You Go
When you figure something out, write it down immediately. Submit PR same day.

### 3. Build for the Next Person
Your workaround becomes the next FDE's starting point. Make it understandable.

### 4. Escalate Smart
Try to solve it first. When you escalate, bring: what you tried, what happened, what you need.

### 5. Feed Back Patterns
When you see the same request from multiple clients, push it toward the product.

### 6. No Long-Lived Branches
If your branch is >2 weeks old, something is wrong. Merge smaller pieces or get it on the roadmap.

---

## Escalation Quick Reference

| Blocked On | First Try | Escalate To | Timeline |
|------------|-----------|-------------|----------|
| Environment setup | Documentation, Slack | Product lead | After 4 hours |
| Missing feature | Workaround | Product roadmap | After client confirms need |
| Bug in product | Reproduce, file issue | Product on-call | If client-impacting |
| Access/permissions | IT ticket | FDE lead | After 24 hours |
| Client relationship | Your manager | Commercial lead | Before it's critical |

---

## Key Metrics (For Reference)

| Metric | What It Measures | Healthy Range |
|--------|------------------|---------------|
| Deployments per FDE | Throughput | 2-4 active |
| Environment setup time | Enablement quality | < 4 hours |
| PR merge time (FDE → Product) | Collaboration health | < 1 week |
| Client deployment time | Delivery efficiency | Trending down |
| Revenue per FDE | Commercial efficiency | Varies by product |

---

## Common Failure Modes

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| FDEs blocked waiting for Product | Priorities misaligned | Escalate, track blocked time |
| Same question asked repeatedly | Missing documentation | FDE documents, Product merges |
| Demos take weeks to build | No reference demo | Product provides baseline |
| Client expectations missed | Over-promising in sales | FDE in pre-sales conversations |
| FDE burnout | Too much time on one account | Rotate assignments |

---

## Resources

| Need | Where to Go |
|------|-------------|
| Hiring process | [01-hiring-talent-strategy.md](01-hiring-talent-strategy.md) |
| Product team expectations | [02-product-fde-interface.md](02-product-fde-interface.md) |
| Technical standards | [03-technical-enablement.md](03-technical-enablement.md) |
| Templates | [templates/](templates/) folder |
| Escalation help | Your FDE lead |
| Something not covered | Ask, then document the answer |

---

*Version MVP-1.0 | Last Updated: January 6, 2026*

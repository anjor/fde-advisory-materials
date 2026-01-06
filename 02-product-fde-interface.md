# Product-FDE Interface

> **TL;DR:** FDE and Product team friction kills deployments. This document establishes who owns what, what FDEs can demand from Product teams, and how to handle the inevitable conflicts.

---

## The Challenge

The most common dysfunction in FDE organizations:

**Product Team Thinks:**
- "FDEs will handle client customization"
- "We need to focus on the roadmap"
- "They can figure it out from the code"

**FDE Team Experiences:**
- Can't set up development environment (takes days, not hours)
- No documentation on how things work
- Product priorities don't align with client needs
- Blocked waiting for Product team responses

**Result:** FDEs spend 70% of time fighting internal friction, 30% on client work.

---

## Core Principle: FDEs Are Your Product's First Real Users

If FDEs can't use your product effectively, neither will clients.

Every hour an FDE spends fighting your codebase is:
- An hour not spent on client outcomes
- A preview of what clients will experience
- Technical debt you're exporting to the field

---

## Ownership Boundaries

### FDE Team Owns

| Area | Scope | Examples |
|------|-------|----------|
| **Client outcomes** | Everything needed to make client successful | Deployment, customization, training, adoption |
| **Client-specific configuration** | Adapting product to client context | Data mappings, UI customization, integrations |
| **Demo building** | Creating client-specific demonstrations | Industry-specific demos, POC environments |
| **Field feedback** | Synthesizing what they learn into actionable input | Feature requests, bug reports, pattern identification |
| **Production deployment** | Getting solution live in client environment | Environment setup, go-live, initial stabilization |

### Product Team Owns

| Area | Scope | Examples |
|------|-------|----------|
| **Core product functionality** | Features that work out of the box | Platform capabilities, standard workflows |
| **Technical documentation** | How to use and extend the product | API docs, data models, architecture guides |
| **Development environment** | Ability for FDEs to work locally | Setup scripts, docker configs, seed data |
| **Bug fixes affecting FDE work** | Priority response to field-blocking issues | Critical bugs, environment issues |
| **Product roadmap** | Informed by field feedback | Feature prioritization, technical direction |

### Shared Ownership

| Area | Product Role | FDE Role |
|------|-------------|----------|
| **Early client deployments (first 1-2)** | Lead technical work | Support, learn, provide client context |
| **Demo environments** | Provide baseline demo capability | Build client-specific extensions |
| **Feature requests** | Prioritize and build | Identify patterns, articulate requirements |
| **Architecture decisions** | Final call | Active contribution, field perspective |

---

## What FDEs Can Demand from Product Teams

These are non-negotiable. Without them, FDEs cannot work effectively.

### 1. Working Development Environment

**Standard:** An FDE should be able to go from zero to running code in < 4 hours.

**Product Team Must Provide:**
- [ ] Single repository (or clear multi-repo guide) - not scattered across GitHub, Azure DevOps, and local machines
- [ ] README with setup instructions that actually work
- [ ] Docker/containerized setup OR clear dependency list
- [ ] Seed data for local development
- [ ] Environment variables documented with example values

**Verification:** New FDE can complete setup following only written instructions.

### 2. Target Data Model Documentation

**Standard:** FDE should understand what shape of data the product expects.

**Product Team Must Provide:**
- [ ] Entity relationship diagram or equivalent
- [ ] Field-level documentation for key entities
- [ ] Example data that exercises main workflows
- [ ] Validation rules and constraints

**Why This Matters:** FDEs build adapters from client data to product data model. Without knowing the target, they're guessing.

### 3. API/Integration Documentation

**Standard:** FDE should be able to integrate without reading source code.

**Product Team Must Provide:**
- [ ] API endpoint documentation (request/response formats)
- [ ] Authentication/authorization guide
- [ ] Error codes and handling guidance
- [ ] Rate limits and performance expectations

### 4. Feature Flag / Configuration Guide

**Standard:** FDE should know what's configurable without code changes.

**Product Team Must Provide:**
- [ ] List of feature flags and what they control
- [ ] Configuration options and their effects
- [ ] How to enable/disable features per client

### 5. Response Time SLA

**Standard:** FDEs should not be blocked waiting for Product team responses.

| Issue Type | Response Time | Resolution Time |
|------------|---------------|-----------------|
| Environment blocker | 4 hours | 24 hours |
| Critical bug (client-impacting) | 4 hours | 48 hours |
| Documentation question | 24 hours | N/A |
| Feature request | 1 week (acknowledgment) | Per roadmap |

---

## Product Teams as Early FDEs

### The Rule
For any product without production client deployments, **the Product team should act as FDEs for the first 1-2 clients.**

### Why This Works

1. **Product people experience their own friction**
   - They feel the pain of missing documentation
   - They discover what's actually hard about deployment
   - They can't blame FDEs for "not understanding"

2. **Faster feedback loops**
   - No handoff delays
   - Immediate fixes
   - Real client needs drive roadmap

3. **Better handoff later**
   - Product team knows what FDEs will need
   - Documentation gets created during deployment
   - Realistic expectations about FDE work

### How to Structure It

**Client 1:** Product team leads (90%), FDE shadows (10%)
- FDE learns the product through observation
- Product team creates documentation as they go
- FDE provides client relationship support

**Client 2:** Shared (50/50)
- FDE takes on more technical work
- Product team fills gaps and answers questions
- Documentation gets tested and improved

**Client 3+:** FDE leads, Product team supports
- Full handoff
- Product team available for escalations
- Regular feedback sync (weekly)

### When to Skip This
- Product has 3+ successful client deployments already
- Strong existing documentation and tooling
- FDE team has deep experience with similar products

---

## Feedback Loops

### Weekly Sync (Required)
**Attendees:** FDE lead + Product lead
**Duration:** 30 min
**Agenda:**
1. FDE blockers (5 min) - What's preventing progress?
2. Client patterns (10 min) - What are we seeing across clients?
3. Roadmap check (5 min) - Any changes affecting FDE work?
4. Action items (10 min) - Who does what by when?

### Backlog Visibility
FDE implementation backlogs should be visible to Product team.

**Purpose:**
- Identify common requests across clients (→ should be product features)
- Spot conflicts between client needs and product direction
- Inform prioritization decisions

**Format:** Shared board (Jira, Linear, etc.) with:
- Client name
- Request description
- Business impact
- Current workaround (if any)

### Quarterly Review
Full FDE + Product team review:
- What patterns emerged this quarter?
- What should move from "FDE customization" to "product feature"?
- What documentation/tooling gaps remain?
- Roadmap alignment for next quarter

---

## Escalation Process

### When to Escalate

| Situation | Action |
|-----------|--------|
| FDE blocked >24 hours on environment/tooling | Escalate to Product lead |
| Critical client commitment at risk | Escalate to both leads + engineering management |
| Pattern of repeated friction | Escalate to engineering leadership for systemic fix |
| Fundamental disagreement on approach | Escalate to shared manager or CTO |

### Escalation Path
```
FDE → FDE Lead → Engineering Manager → VP Eng / CTO
         ↓              ↓
    Product Lead → Engineering Manager
```

### Escalation Template
```
SUBJECT: [ESCALATION] [Client Name] - [Brief Issue]

SITUATION:
What's happening? What's the impact?

BLOCKER:
What specifically is blocking progress?

ATTEMPTED:
What have you already tried?

ASK:
What do you need, from whom, by when?

CONSEQUENCE:
What happens if this isn't resolved?
```

---

## Platform Optimization Philosophy

### The Mistake
Optimizing for "low-code/no-code" end users before your FDEs can use the platform effectively.

### The Reality
For early-stage products:
1. FDEs are your first users
2. FDEs need developer experience (DX), not end-user experience (UX)
3. If FDEs can't build on your platform, clients won't be able to either

### What This Means

**Prioritize:**
- API-first development
- SDK/programmatic access
- Clear extension points
- Developer documentation

**Deprioritize (for now):**
- Visual builders
- Drag-and-drop interfaces
- No-code configuration
- End-user tutorials

**The Sequence:**
1. Build APIs that work
2. Build SDK on top of APIs
3. Build visual tools on top of SDK
4. Only then: no-code/low-code features

---

## FDE Contribution to Product

### FDEs Should Contribute Code
FDEs discovering gaps should be empowered to:
1. Build working prototypes
2. Submit PRs to core product
3. Propose architectural changes

### Contribution Rules

**Do:**
- Build the fastest path to solving client problem
- Document what you built and why
- Flag anything that should be generalized
- Follow existing code conventions

**Don't:**
- Maintain long-lived forks
- Build parallel systems that duplicate product functionality
- Make changes that only work for one client
- Skip tests or documentation

### Merge Expectations

| Change Type | Who Merges | Timeline |
|-------------|------------|----------|
| Bug fix | Product team reviews, FDE can merge | <1 week |
| Small feature | Product team reviews and merges | 1-2 weeks |
| Architecture change | Joint design review, Product team implements | Per roadmap |

### Long-Lived Branches Are Forbidden
A branch that diverges from main for >2 weeks is a failure mode.

**If you have a long-lived branch:**
1. It should have been merged (break it into smaller changes)
2. It should be a product feature (get it on the roadmap)
3. It should be abandoned (client-specific hack that won't scale)

---

## Common Dysfunctions and Fixes

### "Product team is too busy for FDE requests"

**Symptom:** FDE requests sit in backlog for weeks.

**Root Cause:** Product team doesn't feel accountable for FDE success.

**Fix:** 
- Include FDE blockers in Product team sprint planning
- Track "FDE blocked time" as a metric
- Executive visibility on FDE friction

---

### "FDEs keep asking for things that aren't on the roadmap"

**Symptom:** Tension between what clients need and what Product is building.

**Root Cause:** Roadmap isn't informed by field reality.

**Fix:**
- FDE input required in quarterly planning
- Explicit allocation: X% of roadmap driven by field feedback
- Joint client visits by Product team members

---

### "Documentation is always out of date"

**Symptom:** FDEs can't trust written documentation.

**Root Cause:** Documentation is treated as separate from code.

**Fix:**
- Documentation lives in code repo
- PR reviews include documentation updates
- FDEs fix docs when they find issues (and it's merged quickly)

---

### "We don't know what FDEs are doing"

**Symptom:** Product team surprised by FDE customizations.

**Root Cause:** No visibility into FDE work.

**Fix:**
- Shared board for FDE implementation work
- Weekly sync (non-negotiable)
- FDE demos at Product team meetings

---

## Success Metrics

### Leading Indicators
- Time for new FDE to set up environment (target: <4 hours)
- FDE requests in backlog >1 week (target: 0)
- % of FDE PRs merged within 1 week (target: >80%)

### Lagging Indicators
- Client deployment time (trending down)
- FDE satisfaction with Product team support (quarterly survey)
- % of FDE-discovered patterns that become product features

---

## Checklist: Is Your Interface Working?

**For FDE Leaders:**
- [ ] Can a new FDE set up their environment in <4 hours?
- [ ] Do FDEs know exactly what Product team must provide?
- [ ] Is there a weekly sync that actually happens?
- [ ] Do FDEs feel empowered to contribute code?
- [ ] Is there a clear escalation path when blocked?

**For Product Leaders:**
- [ ] Do you know what FDEs are working on right now?
- [ ] Have you personally experienced a client deployment in the last quarter?
- [ ] Is FDE feedback visibly influencing your roadmap?
- [ ] Are your docs accurate enough that FDEs trust them?
- [ ] Can you name the top 3 FDE friction points?

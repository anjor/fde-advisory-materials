# Product-FDE Interface Agreement Template

## Purpose
Document SLAs and expectations between Product and FDE teams to prevent friction and ensure effective collaboration.

## When to Use
- When establishing Product-FDE collaboration for the first time
- When clarifying ownership boundaries that have become unclear
- When resolving recurring interface conflicts
- At the start of each quarter to review and renew commitments

---

## How to Use This Template

1. **Schedule a joint session** with FDE and Product leads (2-3 hours)
2. **Fill in all [PLACEHOLDER] sections** with your organization's specifics
3. **Review the 5 Product Team Commitments** - these are non-negotiable, but you can adjust timelines
4. **Customize the SLA table** based on your team's capacity and client needs
5. **Get sign-off** from both team leads and their managers
6. **Share widely** with all team members
7. **Review quarterly** using Section 10 checklist

This is a working document. Update it when you discover gaps or conflicts.

---

## Agreement Date & Signatories

**Agreement Date:** [YYYY-MM-DD]

**FDE Team Lead:** [NAME, TITLE]

**Product Team Lead:** [NAME, TITLE]

**Engineering Manager/VP:** [NAME, TITLE] *(as witness/escalation point)*

**Next Review Date:** [YYYY-MM-DD] *(typically quarterly)*

---

## 1. Ownership Boundaries

### FDE Team Owns

| Area | Scope | Examples | [COMPANY]-Specific Notes |
|------|-------|----------|-------------------------|
| **Client outcomes** | Everything needed to make client successful | Deployment, customization, training, adoption | [Add specific success metrics] |
| **Client-specific configuration** | Adapting product to client context | Data mappings, UI customization, integrations | [List typical customization areas] |
| **Demo building** | Creating client-specific demonstrations | Industry-specific demos, POC environments | [Note demo standards] |
| **Field feedback** | Synthesizing what they learn into actionable input | Feature requests, bug reports, pattern identification | [Specify feedback process] |
| **Production deployment** | Getting solution live in client environment | Environment setup, go-live, initial stabilization | [Define support window] |

### Product Team Owns

| Area | Scope | Examples | [COMPANY]-Specific Notes |
|------|-------|----------|-------------------------|
| **Core product functionality** | Features that work out of the box | Platform capabilities, standard workflows | [List core features] |
| **Technical documentation** | How to use and extend the product | API docs, data models, architecture guides | [Specify doc location] |
| **Development environment** | Ability for FDEs to work locally | Setup scripts, docker configs, seed data | [Note setup process] |
| **Bug fixes affecting FDE work** | Priority response to field-blocking issues | Critical bugs, environment issues | [Define "field-blocking"] |
| **Product roadmap** | Informed by field feedback | Feature prioritization, technical direction | [Link to roadmap] |

### Shared Ownership

| Area | Product Role | FDE Role | Decision Process |
|------|-------------|----------|------------------|
| **Early client deployments (first 1-2)** | Lead technical work | Support, learn, provide client context | [Specify handoff criteria] |
| **Demo environments** | Provide baseline demo capability | Build client-specific extensions | [Define baseline scope] |
| **Feature requests** | Prioritize and build | Identify patterns, articulate requirements | [Specify prioritization process] |
| **Architecture decisions** | Final call | Active contribution, field perspective | [Define escalation path] |

---

## 2. Communication Cadences

### Weekly Sync (Required)

**Attendees:** FDE lead + Product lead + [ADDITIONAL ROLES]

**Duration:** 30 min

**When:** [DAY OF WEEK, TIME]

**Location:** [MEETING LINK / ROOM]

**Agenda:**

1. **FDE blockers** (5 min) - What's preventing progress?
2. **Client patterns** (10 min) - What are we seeing across clients?
3. **Roadmap check** (5 min) - Any changes affecting FDE work?
4. **Action items** (10 min) - Who does what by when?

**Notes:** [SPECIFY NOTE-TAKING PROCESS AND LOCATION]

### Backlog Visibility

**Tool:** [JIRA / LINEAR / OTHER]

**Board Link:** [URL]

**Format:** FDE implementation backlogs visible to Product team with:

- Client name
- Request description
- Business impact
- Current workaround (if any)

**Purpose:** Identify common requests across clients that should become product features.

### Quarterly Review (Required)

**Attendees:** Full FDE team + Full Product team

**Duration:** 2 hours

**When:** [SPECIFY QUARTER END TIMING]

**Agenda:**

1. What patterns emerged this quarter?
2. What should move from "FDE customization" to "product feature"?
3. What documentation/tooling gaps remain?
4. Roadmap alignment for next quarter
5. Review this agreement - what's working, what's not?

---

## 3. Service Level Agreements

| Issue Type | Response Time | Resolution Time | Escalation If Not Met |
|------------|---------------|-----------------|----------------------|
| **Environment blocker** | [X hours] | [Y hours] | [ESCALATION PATH] |
| **Critical bug (client-impacting)** | [X hours] | [Y hours] | [ESCALATION PATH] |
| **Documentation question** | [X hours] | N/A | [ESCALATION PATH] |
| **Feature request** | [X days] (acknowledgment) | Per roadmap | [ESCALATION PATH] |
| **Integration support** | [X hours] | [Y days] | [ESCALATION PATH] |

**Recommended baseline (adjust for your context):**

- Environment blocker: 4 hours response, 24 hours resolution
- Critical bug: 4 hours response, 48 hours resolution
- Documentation question: 24 hours response

**SLA Tracking:** [SPECIFY HOW YOU'LL TRACK RESPONSE/RESOLUTION TIMES]

**Out of hours support:** [DEFINE EXPECTATIONS FOR EVENINGS/WEEKENDS]

---

## 4. Product Team Commitments

These are non-negotiable. Without them, FDEs cannot work effectively.

### 1. Working Development Environment

**Standard:** An FDE should be able to go from zero to running code in < 4 hours.

**Product Team Must Provide:**

- Single repository (or clear multi-repo guide) - not scattered across GitHub, Azure DevOps, and local machines
- README with setup instructions that actually work
- Docker/containerized setup OR clear dependency list
- Seed data for local development
- Environment variables documented with example values

**Verification:** New FDE can complete setup following only written instructions.

**[COMPANY] Status:** [CURRENT STATE - e.g., "Setup takes ~6 hours, working to streamline"]

### 2. Target Data Model Documentation

**Standard:** FDE should understand what shape of data the product expects.

**Product Team Must Provide:**

- Entity relationship diagram or equivalent
- Field-level documentation for key entities
- Example data that exercises main workflows
- Validation rules and constraints

**Why This Matters:** FDEs build adapters from client data to product data model. Without knowing the target, they're guessing.

**[COMPANY] Status:** [CURRENT STATE]

### 3. API/Integration Documentation

**Standard:** FDE should be able to integrate without reading source code.

**Product Team Must Provide:**

- API endpoint documentation (request/response formats)
- Authentication/authorization guide
- Error codes and handling guidance
- Rate limits and performance expectations

**[COMPANY] Status:** [CURRENT STATE]

### 4. Feature Flag / Configuration Guide

**Standard:** FDE should know what's configurable without code changes.

**Product Team Must Provide:**

- List of feature flags and what they control
- Configuration options and their effects
- How to enable/disable features per client

**[COMPANY] Status:** [CURRENT STATE]

### 5. Response Time Adherence

**Standard:** FDEs should not be blocked waiting for Product team responses.

**Product Team Must Provide:**

- Adherence to SLAs in Section 3
- Transparent communication when timelines slip
- Proactive flagging of roadmap changes that affect FDE work

**Tracking:** [HOW YOU'LL MEASURE THIS - e.g., "Weekly review of open FDE requests >24 hours old"]

---

## 5. FDE Team Commitments

### What FDEs Will Provide

**To Product Team:**

- Weekly patterns report - what we're seeing across clients
- Prioritized feedback - distinguishing "nice to have" from "blocking adoption"
- Field perspective on architecture decisions
- Testing and validation of new features in real client contexts
- Clear escalation when blocked (not silent suffering)

**To Clients:**

- Ownership of deployment and adoption outcomes
- Client-specific customization and configuration
- Training and enablement
- First line of support for deployment issues

**Code Quality Standards:**

When FDEs contribute code to the product:

- Follow existing conventions and patterns
- Include tests where appropriate
- Document what was built and why
- Flag anything that should be generalized

---

## 6. Escalation Process

### When to Escalate

| Situation | Action | Timeline |
|-----------|--------|----------|
| FDE blocked >24 hours on environment/tooling | Escalate to Product lead | Immediate |
| Critical client commitment at risk | Escalate to both leads + engineering management | Immediate |
| Pattern of repeated friction | Escalate to engineering leadership for systemic fix | After 3 occurrences |
| Fundamental disagreement on approach | Escalate to shared manager or CTO | After 1 failed resolution attempt |

### Escalation Path

```
FDE → FDE Lead → Engineering Manager → VP Eng / CTO
         ↓              ↓
    Product Lead → Engineering Manager
```

**[COMPANY]-Specific Path:**
```
[FDE NAME/ROLE] → [FDE LEAD] → [ENGINEERING MANAGER] → [VP/CTO]
                      ↓              ↓
                [PRODUCT LEAD] → [ENGINEERING MANAGER]
```

### Escalation Template

Use this format when escalating issues:

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

## 7. Documentation Commitments

### Product Team Owns

**Location:** [SPECIFY WHERE DOCS LIVE - e.g., "GitHub wiki", "Confluence", "docs/ folder"]

**Maintains:**

- API documentation (kept current with code changes)
- Data model documentation
- Architecture diagrams
- Feature flag documentation
- Setup/environment guides

**Update Process:** [SPECIFY - e.g., "Docs updated in same PR as code changes"]

### FDE Team Contributes

**FDEs Fix Docs When They Find Issues:**

- Submit PRs for doc corrections/improvements
- Flag gaps or inaccuracies
- Add examples from real client scenarios

**Expected Turnaround:** Product team merges doc PRs within [X days]

### Shared Documentation

**Client Patterns Document:** [LOCATION]

- FDEs maintain running list of common requests
- Product team reviews quarterly for roadmap input

---

## 8. Feedback Mechanisms

### FDE → Product

**Weekly Sync:** Agenda item #2 - client patterns (see Section 2)

**Structured Feedback:** [SPECIFY TOOL/PROCESS]

- Feature requests with business impact
- Bug reports with client context
- Pattern identification across clients

**Product Roadmap Input:** [SPECIFY PROCESS - e.g., "FDE lead joins quarterly planning"]

### Product → FDE

**Roadmap Changes:** [HOW PRODUCT COMMUNICATES CHANGES - e.g., "Slack #fde-updates channel + weekly sync"]

**Release Notes:** [WHERE/HOW SHARED]

**Breaking Changes:** [ADVANCE NOTICE PERIOD - e.g., "30 days minimum"]

### Success Metrics Review

**Quarterly:** Review together:

- Time for new FDE to set up environment (target: <4 hours)
- FDE requests in backlog >1 week (target: 0)
- % of FDE PRs merged within 1 week (target: >80%)
- Client deployment time (trending down)

---

## 9. FDE Code Contributions

### Contribution Philosophy

FDEs discovering gaps are empowered to:

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

| Change Type | Who Reviews | Who Merges | Timeline |
|-------------|-------------|------------|----------|
| Bug fix | Product team | FDE can merge after approval | <1 week |
| Small feature | Product team | Product team | 1-2 weeks |
| Architecture change | Joint design review | Product team implements | Per roadmap |

**Long-Lived Branches Are Forbidden:** A branch that diverges from main for >2 weeks is a failure mode.

**If you have a long-lived branch:**

1. It should have been merged (break it into smaller changes)
2. It should be a product feature (get it on the roadmap)
3. It should be abandoned (client-specific hack that won't scale)

**[COMPANY] Branch Policy:** [SPECIFY ANY ADDITIONAL BRANCH/PR CONVENTIONS]

---

## 10. Review and Renewal Process

### Quarterly Review Checklist

**Attendees:** FDE lead + Product lead + [OTHER STAKEHOLDERS]

**Duration:** 1 hour

**Agenda:**

- Review Section 3 SLAs - are they being met? Do they need adjustment?
- Review Section 4 Product Team Commitments - status on each item
- Review Section 8 Success Metrics - what's improving? What's not?
- Update Section 1 Ownership Boundaries if scope has shifted
- Discuss what's working well - keep doing this
- Discuss what's not working - what should change?
- Update [PLACEHOLDER] sections based on what we've learned
- Set date for next quarterly review

### When to Do a Full Rewrite

This agreement needs a full rewrite (not just updates) when:

- Team structure changes significantly
- Product architecture changes fundamentally
- FDE scope expands to new areas
- Recurring conflicts indicate misaligned expectations

### Agreement History

| Version | Date | Key Changes | Signed By |
|---------|------|-------------|-----------|
| 1.0 | [DATE] | Initial agreement | [NAMES] |
| 1.1 | [DATE] | [WHAT CHANGED] | [NAMES] |

---

## Usage Notes

### Getting Buy-In

**For Engineering Leadership:**

- Frame as "reducing FDE blocked time" - a measurable waste metric
- Show cost: every hour FDEs fight internal friction is billable hours lost
- Position as risk mitigation: clear interfaces prevent client commitment failures

**For Product Teams:**

- Emphasize: "FDEs are your first real users"
- Show benefit: FDEs surface real-world issues before they become client problems
- Make visible: FDE feedback directly influences roadmap prioritization

### Common Pitfalls

**"We'll figure it out as we go"**

- Symptom: No written agreement, relying on goodwill
- Result: Friction emerges, no framework for resolving it
- Fix: Write this agreement even if it feels premature

**"Product team is too busy for this"**

- Symptom: Product team doesn't see FDE support as their job
- Result: FDEs blocked constantly, can't deliver for clients
- Fix: Executive sponsorship making FDE enablement a team priority

**"Agreement sits in a doc, nobody follows it"**

- Symptom: Agreement exists but isn't referenced or enforced
- Result: Falls back to ad-hoc, relationship-dependent collaboration
- Fix: Review in weekly syncs, track SLA adherence, update based on reality

### Adaptation Guidance

**Early-Stage Startups:**

- Product team may act as FDEs for first 1-2 clients - add that to Section 1
- SLAs may be shorter due to smaller team/higher urgency
- Quarterly reviews may be monthly during rapid iteration

**Mature Products:**

- May need more detailed API/integration documentation commitments
- May have separate platform team - add to ownership boundaries
- May need client-tier SLAs (enterprise vs standard)

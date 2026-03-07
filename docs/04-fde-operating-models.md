# FDE Operating Models

> **TL;DR:** Once you've hired FDEs and set up the product interface, you need an operating model that covers team structure, customer deployment lifecycle, capacity planning, feedback loops, career development, and success metrics. Most FDE orgs fail not because they hired wrong, but because they never figured out how to run the function day-to-day.

---

## The Challenge

Hiring great FDEs and establishing a product interface solves the first two problems. But without a clear operating model, you'll see:

- FDEs burning out because no one manages capacity across accounts
- Knowledge trapped in individual heads with no systematic way to share it
- Product teams complaining that FDE feedback is anecdotal and unactionable
- FDEs leaving because there's no career path beyond "do more deployments"
- Leadership unable to answer basic questions like "is our FDE function working?"

The operating model is the system that makes everything else sustainable. It's the difference between an FDE function that works for 6 months and one that works for 6 years.

---

## 1. Team Structure and Sizing

### How Many FDEs Per Customer?

There's no universal ratio. The right number depends on:

| Factor | Fewer FDEs Needed | More FDEs Needed |
|--------|-------------------|------------------|
| Product maturity | Mature, well-documented | Early, gaps everywhere |
| Deployment complexity | Standard configurations | Heavy customization |
| Customer technical capability | Strong internal eng team | Limited technical staff |
| Account stage | Steady state | Active deployment |

**Rules of thumb:**

- **1 FDE per active deployment** during pilot and production phases
- **1 FDE across 2-3 accounts** in steady state
- **Never 1 FDE alone** — minimum 2 per region/timezone for coverage and peer support

### When Do You Need a Team Lead?

- **3-5 FDEs**: A senior FDE can play-manage while still deploying (50/50 split)
- **6-10 FDEs**: You need a dedicated FDE lead who manages full-time
- **10+ FDEs**: Consider sub-teams organized by vertical, region, or product line

The FDE lead role is critical and often under-invested. This person needs to:

- Manage capacity and account assignments
- Run the feedback loop to product
- Handle escalations that individual FDEs can't resolve
- Own hiring and career development for the team
- Shield FDEs from organizational noise

### How the FDE Org Relates to Product

Three common models:

| Model | How It Works | Best For |
|-------|-------------|----------|
| **Embedded in Product** | FDEs report to product org | Small teams (<5 FDEs), product-heavy work |
| **Standalone FDE org** | FDEs report to FDE lead, separate from product | Larger teams, customer-heavy work |
| **Matrix** | FDEs report to FDE lead but are assigned to product teams | When you need both deep product knowledge and customer focus |

**Recommendation:** Start with standalone. Embedded FDEs get pulled into product work and lose their customer focus. A standalone org with strong product interfaces (see [02-product-fde-interface.md](02-product-fde-interface.md)) gives you the best of both worlds.

---

## 2. Customer Deployment Lifecycle

Understanding the typical arc of an FDE engagement helps you plan capacity and set expectations.

### The Phases

| Phase | Duration | FDE Intensity | Key Activities |
|-------|----------|---------------|----------------|
| **Onboarding** (Week 1-2) | 2 weeks | High | Environment setup, stakeholder mapping, understanding customer's problem |
| **Initial Build** (Week 3-8) | 6 weeks | Very high | Core solution development, daily customer interaction |
| **Stabilization** (Week 9-12) | 4 weeks | High | Bug fixes, edge cases, performance tuning, user training |
| **Optimization** (Month 4-6) | 2-3 months | Medium | Refinements, expanded use cases, building customer self-sufficiency |
| **Steady State** (Month 6+) | Ongoing | Low | Maintenance, new feature requests, potential handoff to CS |

### Week 1 vs Month 6

**Week 1 looks like:**

- Meet every stakeholder. Understand who cares about what.
- Get access to everything. Don't wait for IT — escalate on day 1.
- Understand the customer's actual problem (which is rarely what was sold).
- Stand up a working environment. Document every step for the next person.
- Set expectations: "Here's what we'll deliver, here's what we need from you."

**Month 6 looks like:**

- Solution is running in production. Customer team can operate it day-to-day.
- FDE checks in weekly, not daily. Reactive support, not active building.
- New use cases may be emerging — evaluate whether they need a fresh deployment cycle.
- Knowledge transfer is mostly complete. Customer can handle routine issues.
- FDE is documenting patterns for reuse across other accounts.

### Handoff vs Expansion

At month 6, you face a decision:

- **Handoff to Customer Success**: The deployment is stable, the customer is self-sufficient, and the FDE's time is better spent on a new account.
- **Expand**: The customer wants more use cases, and there's commercial justification for continued FDE involvement.
- **Maintain with reduced intensity**: Keep the FDE assigned but at 20% allocation, handling ad-hoc requests.

The worst outcome is an FDE stuck on a steady-state account at full allocation with nothing meaningful to build. That's how you lose good FDEs.

---

## 3. Capacity Planning and Rotation

### Managing Capacity Across Customers

Capacity planning is the FDE lead's most important job. Get it wrong and you either burn out your team or leave revenue on the table.

**The capacity model:**

| FDE Allocation | What It Means |
|----------------|---------------|
| **100% dedicated** | One account, full time. Only for active deployments. |
| **50/50 split** | Two accounts. Works when both are in optimization or steady state. |
| **20% maintenance** | Checking in on a stable account. Combined with other work. |
| **Bench** | Between assignments. Use for internal tooling, documentation, training. |

**Key principles:**

- **Never allocate more than 100%**. It sounds obvious, but many orgs do this by treating FDE time as infinitely divisible. An FDE "helping" 5 accounts is helping none of them.
- **Maintain 10-20% bench capacity**. You need slack in the system for urgent requests, sick days, and new account ramp-up. If every FDE is 100% allocated, you have zero ability to respond to new opportunities.
- **Track allocation weekly**. A simple spreadsheet works: FDE name, account, allocation percentage, phase, expected transition date.

### When and How to Rotate FDEs

Rotation is healthy but needs to be managed carefully.

**When to rotate:**

- Account reaches steady state (month 6+)
- FDE has been on the same account for 12+ months (burnout risk)
- New account needs the specific skills this FDE has
- FDE requests a change (take this seriously)

**When NOT to rotate:**

- Mid-deployment (active build phase)
- Customer relationship is fragile
- No one else has context on the account (single point of failure — fix this first)

**How to rotate well:**

1. **Overlap period**: 2-4 weeks where incoming and outgoing FDEs work together
2. **Knowledge transfer document**: Account context, key contacts, gotchas, current state
3. **Customer introduction**: Outgoing FDE introduces incoming FDE to key stakeholders
4. **Clean handoff**: Don't ghost the customer. Explain the transition and why it's happening.

### Avoiding Single Points of Failure

If only one person understands an account, you have a bus factor of 1. This is unacceptable.

**Mitigation strategies:**

- **Pair deployments for the first 4 weeks** — two FDEs on every new account, one drops off after initial build
- **Account documentation standards** — every account has a living doc with architecture, contacts, quirks, and known issues
- **Regular account reviews** — monthly 30-minute sessions where the assigned FDE walks the team through their account
- **Shadow rotations** — FDEs periodically shadow each other's accounts for half a day

---

## 4. Feedback Loops

The FDE-to-product feedback loop is one of the highest-value mechanisms in the entire organization. FDEs see what customers actually need, not what they say they need. But most orgs never build a system to capture and act on this.

### Why Feedback Loops Fail

- **Ad hoc communication**: FDEs mention things in Slack, no one tracks it
- **Wrong audience**: FDE tells their manager, who doesn't talk to the PM
- **No prioritization**: Product gets 50 requests and can't tell which matter
- **No follow-up**: FDE files a request, never hears back, stops filing requests
- **Wrong format**: FDE writes a novel when product needs a one-liner, or vice versa

### Mechanisms That Actually Work

#### 1. Weekly Field Report

Each FDE submits a brief weekly report with a standard format:

- **What I built this week**: 2-3 bullet points
- **What customers asked for that we don't have**: Ranked by frequency/impact
- **What broke or was painful**: Specific product friction points
- **Pattern I noticed**: Cross-customer trends worth investigating

The FDE lead aggregates these into a monthly summary for the product team.

#### 2. Upstream Contribution Path

FDEs should have a clear path to contribute code upstream to the product:

- **Bug fixes**: FDE submits PR, product reviews within 48 hours
- **Small features**: FDE proposes, product approves scope, FDE builds
- **Large features**: FDE writes proposal, product decides roadmap fit

This only works if product actually reviews and merges FDE contributions. If FDE PRs rot in review, FDEs stop contributing.

#### 3. Quarterly Product-FDE Sync

A structured meeting (2 hours, quarterly) where:

- FDE lead presents top 10 field requests with customer impact data
- Product shares upcoming roadmap and asks for field validation
- Both sides agree on 3-5 items to prioritize for the next quarter

This is not a wishlist session. It's a negotiation with data.

#### 4. Customer Visit Program

Product engineers spend 1-2 days per quarter shadowing an FDE on a customer engagement. Nothing replaces seeing the customer experience firsthand.

---

## 5. Career Development

FDE burnout is real. The role is high-intensity, high-ambiguity, and often thankless. Without a clear career path, your best FDEs will leave for product engineering roles within 2-3 years.

### The Career Ladder

| Level | Title | Scope | Typical Experience |
|-------|-------|-------|--------------------|
| L1 | Associate FDE | Single account, guided | 0-2 years |
| L2 | FDE | 1-2 accounts, independent | 2-4 years |
| L3 | Senior FDE | Complex accounts, mentors others | 4-7 years |
| L4 | Staff FDE / FDE Lead | Team leadership or technical specialization | 7+ years |

### Growth Tracks

Not every FDE wants to manage. Provide two tracks:

**Management track:**

- FDE Lead → Director of FDE → VP of Customer Engineering
- Focus: Team building, capacity planning, organizational strategy

**Technical track:**

- Senior FDE → Staff FDE → Principal FDE
- Focus: Most complex deployments, architecture across accounts, internal tooling

Both tracks should have equivalent compensation and status. If the only way to advance is management, you'll promote your best engineers out of the role they're best at.

### Avoiding Burnout

| Risk Factor | Early Warning Signs | Mitigation |
|------------|---------------------|------------|
| Customer intensity | Cancelling personal commitments, weekend work | Enforce boundaries, rotate to lighter account |
| Repetitive work | "I've built this same thing 10 times" | Create reusable tooling, assign novel problems |
| Isolation | Not talking to other FDEs, skipping team meetings | Co-locate or pair, regular team events |
| Lack of recognition | "No one knows what I do" | Public demos, customer testimonials, leadership visibility |
| No growth | "I'm not learning anything new" | Training budget, conference attendance, cross-functional projects |

**Concrete actions:**

- **Maximum 12 months on a single account** before mandatory rotation or explicit opt-in to continue
- **20% time equivalent**: Every FDE gets at least 1 day per sprint for internal projects, learning, or tooling
- **Annual development conversations**: Not performance reviews — career development discussions about where the FDE wants to go

---

## 6. Metrics and Success Criteria

How do you know if your FDE function is working? You need metrics at three levels: the function, the customer, and the individual.

### Function-Level Metrics

| Metric | Target | What It Tells You |
|--------|--------|-------------------|
| **Deployment success rate** | >90% | Are FDEs actually delivering value? |
| **Time to first value** | <6 weeks | How fast can you show results? |
| **Revenue per FDE** | Varies by product | Is the function commercially viable? |
| **FDE retention (annual)** | >80% | Are you burning people out? |
| **Upstream contributions/quarter** | >5 per FDE | Is the feedback loop working? |
| **Bench utilization** | 10-20% | Do you have capacity slack? |

### Customer-Level Metrics

| Metric | Target | What It Tells You |
|--------|--------|-------------------|
| **Customer satisfaction (NPS/CSAT)** | >8/10 | Is the customer happy with the engagement? |
| **Renewal rate** | >85% | Is the value sustained? |
| **Expansion rate** | >30% | Are customers buying more? |
| **Time to self-sufficiency** | <6 months | Are you building dependency or capability? |
| **Escalation frequency** | Trending down | Is the deployment stabilizing? |

### Individual-Level Metrics

As covered in the [startup kit](00-fde-startup-kit.md#individual-fde-performance-intentionally-subjective), individual FDE metrics should remain intentionally subjective. Manager judgment, peer feedback, and customer satisfaction are better signals than any quantitative metric.

### Red Flags

Watch for these patterns that indicate the operating model needs adjustment:

| Signal | Likely Root Cause | Action |
|--------|-------------------|--------|
| FDE retention dropping below 70% | Burnout, no career path, or compensation gap | Exit interviews, career ladder review |
| Time to first value increasing | Product friction, process bloat, or wrong account selection | Audit recent deployments, check product readiness |
| Customers requesting specific FDEs | Knowledge concentrated in individuals | Improve documentation, enforce rotation |
| Product team ignoring FDE feedback | Broken feedback loop, lack of trust | Quarterly sync, data-backed requests |
| FDEs not contributing upstream | Review process too slow, or contributions not valued | Track PR review time, celebrate upstream merges |

---

## Templates & Tools

- [FDE Operating Model Canvas](resources/operations/operating-model-canvas.md) — One-page template to define your operating model

---

## Common Pitfalls

| Pitfall | What Happens | How to Avoid |
|---------|-------------|--------------|
| No dedicated FDE lead | FDEs self-organize poorly, capacity is mismanaged | Appoint a lead by the time you have 5 FDEs |
| Treating FDEs as fungible | Rotating without overlap, ignoring specialization | Structured rotation with handoff periods |
| No career ladder | Best FDEs leave for product roles | Build dual-track career path early |
| Ignoring feedback loop | FDEs become "deployment machines" disconnected from product | Formalize weekly reports and quarterly syncs |
| Over-measuring individuals | FDEs optimize for metrics instead of outcomes | Keep individual evaluation subjective |
| 100% allocation always | No slack for new opportunities, training, or recovery | Maintain 10-20% bench capacity |

---

## Further Reading

- [**The FDE Manifesto: What Would Stokes Do?**](https://anjor.xyz/writing/2025/11/20/the-fde-manifesto-what-would-stokes-do/) — Tactical principles that define exceptional FDE behavior
- [**How to Build Your 1st Forward Deployed Engineering Team**](https://www.peraspera.us/forward-deployed/) — Mark Scianna's practical guidance includes operating model considerations
- [**Reflections on Palantir**](https://nabeelqu.co/reflections-on-palantir) — Nabeel Qureshi's insights on how Palantir's FDE model operates at scale

---

*Version 1.4.0 | Last Updated: March 7, 2026*

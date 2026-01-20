# 90-Day FDE Onboarding Checklist

## Purpose
Structured 90-day onboarding program ensuring new FDEs ramp effectively from orientation through independent client work. Tracks progress, identifies blockers early, and sets clear success criteria.

## When to Use

- For every new FDE hire (regardless of experience level)
- As a guide for onboarding buddies/mentors
- For tracking onboarding progress with weekly check-ins
- When evaluating onboarding program effectiveness

---

## How to Use This Checklist

**For Managers:**

1. Assign an onboarding buddy on Day 1 (see Onboarding Buddy Role section)
2. Review this checklist with new hire during first week
3. Conduct weekly 30-minute check-ins to track progress
4. Watch for red flags (see Red Flags section) - intervene early
5. Conduct formal reviews at 30, 60, and 90 days

**For Onboarding Buddies:**

1. Work through Week 1 together (pair on setup, answer questions)
2. Bring new hire to all your client calls in Weeks 2-4
3. Assign specific workstreams in Weeks 5-8 (you're accountable, they execute)
4. Step back in Weeks 9-12 (be available, but don't drive)

**For New Hires:**

1. Use this as your roadmap - you own your onboarding
2. Check off items as you complete them
3. Flag blockers immediately (don't struggle silently)
4. Document what you learn for the next person
5. Ask questions - lots of them

---

## Program Overview

### Timeline

```
Week 1        Weeks 2-4       Weeks 5-8         Weeks 9-12
Setup      →  Shadowing    →  First Deploy  →   Independent
                                (Supported)        Work

Goal: Working    Goal: Learning    Goal: Doing     Goal: Owning
environment      by observing      with support    outcomes
```

### Success Criteria

**By Week 4:**

- Environment set up (<4 hours to working code)
- Understands product architecture
- Has observed 3+ client interactions
- Can explain what FDEs do (not just in theory)

**By Week 8:**

- Led specific workstream on real client engagement
- Participated in client meetings
- Contributed code or documentation to product
- Identified one thing to improve for next FDE

**By Week 12:**

- Independently leading client work
- Comfortable escalating when stuck
- Contributing to team knowledge base
- Ready for next engagement without hand-holding

### Failure Modes to Avoid

- Spending >4 hours on environment setup (escalate immediately)
- Shadowing without actually doing anything (passive observation doesn't work)
- Taking on independent work too early (builds bad habits)
- Manager only checking in at 90 days (too late to course-correct)

---

## Week 1: Orientation & Setup

**Goal:** Get working environment in <4 hours. Meet team. Understand context.

### Day 1

**Morning: Orientation (3 hours)**

- [ ] HR paperwork and benefits enrollment
- [ ] IT setup: laptop, email, Slack, calendar
- [ ] Access provisioning request submitted (GitHub, tools, demo environments)
- [ ] Meet your manager (60 min)
  - Discuss this checklist
  - Set weekly check-in time
  - Get context on current client engagements
- [ ] Meet your onboarding buddy (30 min)
  - Set daily pairing schedule for Week 1
  - Get added to relevant meetings

**Afternoon: Environment Setup (4 hours MAX)**

- [ ] Clone primary repository
- [ ] Follow README to get environment running locally
- [ ] Verify you can run the product (see something on screen)
- [ ] Run through "Quick Start" demo flow
- [ ] Document any issues you hit (submit PR to fix README)

**⚠️ CRITICAL:** If you can't get environment running in 4 hours, escalate to your manager immediately. This is a product problem, not your problem.

**End of Day:**
- [ ] Can run product locally
- [ ] Know who to ask for help (buddy, manager, team channel)
- [ ] Have access to team calendar and key meetings

---

### Day 2

**Morning: Product Deep Dive (3 hours)**

- [ ] Read architecture documentation
- [ ] Understand data model (what entities exist, how they relate)
- [ ] Review API documentation
- [ ] Explore codebase structure (where things live)
- [ ] Ask questions (buddy or team channel)

**Afternoon: Process & Tools (2 hours)**

- [ ] Understand PR process (how to get code merged)
- [ ] Review past client deployments (read docs, see demos)
- [ ] Join team standup or sync meeting
- [ ] Set up AI coding tools (Claude Code, Copilot, etc.)

**Learning Task:**

- [ ] Pick one feature in the product
- [ ] Trace it through codebase (frontend → backend → database)
- [ ] Explain it to your buddy (they verify understanding)

---

### Day 3

**Morning: Client Context (3 hours)**

- [ ] Review current active client engagements
- [ ] Understand who is working on what
- [ ] Read docs from recent deployments
- [ ] Watch recorded client demo (if available)

**Afternoon: FDE Workflows (2 hours)**

- [ ] Understand how FDEs contribute to product codebase
- [ ] Review escalation process (when/how to ask for help)
- [ ] Learn demo environment access and reset process
- [ ] Understand how documentation gets updated

**Mini-Project:**

- [ ] Find one thing that confused you in docs/setup
- [ ] Fix it (edit docs, update README, add comment)
- [ ] Submit PR (practice the workflow)

---

### Day 4

**Shadow Active Client Work (Full Day)**

- [ ] Attend all buddy's client meetings today
- [ ] Observe (don't speak unless asked)
- [ ] Take notes on:
  - How FDEs communicate with clients
  - What questions clients ask
  - How technical concepts are explained
  - How buddy handles unclear requirements

**Reflection:**
- [ ] Write down 3 things that surprised you
- [ ] Write down 3 questions to ask buddy
- [ ] Share observations with buddy (30 min debrief)

---

### Day 5

**Morning: Technical Work (3 hours)**

- [ ] Pair with buddy on their current work
- [ ] Take on small, well-defined task
- [ ] Submit PR (even if it's tiny)
- [ ] Get feedback on code

**Afternoon: Week 1 Checkpoint (2 hours)**

- [ ] Review this checklist with manager
- [ ] Discuss what's clear vs. still confusing
- [ ] Identify any blockers
- [ ] Set expectations for Weeks 2-4

**Week 1 Success Check:**

- [ ] Environment works (<4 hours setup time achieved)
- [ ] Can navigate codebase with AI tools
- [ ] Understand product at high level
- [ ] Met core team members
- [ ] Submitted at least one PR (even if just docs)
- [ ] Have clarity on what Weeks 2-4 will involve

---

## Weeks 2-4: Shadowing & Learning

**Goal:** Learn by observing. Ask questions. Start small contributions.

### Week 2: Deep Observation

**Client Interaction (10-15 hours)**

- [ ] Shadow buddy on ALL client calls/meetings this week
- [ ] Observe at least 2 different clients (if possible)
- [ ] Take notes on:
  - How requirements are gathered
  - How scope is negotiated
  - How technical problems are explained
  - How expectations are set
- [ ] Ask buddy for context before and after each call

**Technical Work (15-20 hours)**

- [ ] Take on 2-3 small, well-scoped tasks
- [ ] Tasks should be: "Change X to do Y" (clear input/output)
- [ ] Work independently, but check approach with buddy first
- [ ] Submit PRs, respond to feedback
- [ ] Update docs for anything you learned

**Learning Objectives:**

- [ ] Understand how a client engagement progresses
- [ ] See how FDEs balance client communication and technical work
- [ ] Contribute code to product (even if small changes)
- [ ] Practice PR process and code review

**End of Week Check-in:**

- What did you learn from shadowing?
- What surprised you about client interactions?
- What's still unclear about FDE work?

---

### Week 3: Active Participation

**Client Interaction (10-15 hours)**

- [ ] Continue shadowing buddy's client calls
- [ ] Participate when asked (answer technical questions)
- [ ] Practice explaining technical concepts simply
- [ ] Prepare for one call (understand context beforehand)

**Technical Work (15-20 hours)**

- [ ] Own a small feature or fix end-to-end
- [ ] Break it into subtasks yourself
- [ ] Implement, test, document
- [ ] Present your work in team meeting
- [ ] Help another new FDE (if applicable)

**Pattern Recognition:**

- [ ] Identify one thing clients ask for repeatedly
- [ ] Notice one gap in product that requires FDE workaround
- [ ] Document both (for future reference)

**End of Week Check-in:**

- Are you comfortable speaking up in client meetings?
- Can you work on tasks independently now?
- What do you need more practice with?

---

### Week 4: Supported Contribution

**Client Interaction (10-15 hours)**

- [ ] Lead one section of a client call (buddy supports)
- [ ] Demo something you built
- [ ] Answer client questions (with buddy as backup)
- [ ] Take notes and send follow-up

**Technical Work (15-20 hours)**

- [ ] Own a meaningful workstream (not just small tasks)
- [ ] Example: "Build data import for client X"
- [ ] Make decisions on approach (validate with buddy)
- [ ] Deliver working solution
- [ ] Document what you built (for future FDEs)

**Knowledge Sharing:**

- [ ] Give 15-minute presentation to team on something you learned
- [ ] Update onboarding docs based on your experience
- [ ] Help next new hire (if one starts)

**30-Day Review with Manager:**

- [ ] Assess progress against Week 4 success criteria
- [ ] Identify strengths and growth areas
- [ ] Discuss readiness for supported first deployment
- [ ] Adjust plan if needed

**Week 4 Success Check:**

- [ ] Comfortable participating in client calls
- [ ] Can work independently on small-medium tasks
- [ ] Have contributed meaningful code/docs
- [ ] Understand product well enough to explain it
- [ ] Ready to take on real client work (with support)

---

## Weeks 5-8: Supported First Deployment

**Goal:** Lead real workstreams on a client engagement. Buddy is accountable, you execute.

### Week 5: Workstream Ownership

**Assignment:**

- [ ] Get assigned to active client engagement
- [ ] Take ownership of specific workstream
- [ ] Example: "Data integration", "UI customization", "Deployment setup"
- [ ] Buddy is on the same engagement (as support, not lead)

**Execution (30-35 hours):**

- [ ] Break down workstream into tasks
- [ ] Estimate effort and timeline
- [ ] Execute tasks with daily check-ins with buddy
- [ ] Participate in client calls (present your progress)
- [ ] Ask for help when stuck (don't struggle >2 hours alone)

**Communication:**

- [ ] Weekly status update to client (written or verbal)
- [ ] Flag blockers immediately
- [ ] Document decisions as you go

**Buddy Role This Week:**

- Available for questions
- Reviews your plan before you execute
- Attends client calls with you
- Steps in if you're stuck

**End of Week Check-in:**

- How is the workstream going?
- What's harder than expected?
- What help do you need?

---

### Week 6-7: Delivery Focus

**Execution (60-70 hours across 2 weeks):**

- [ ] Make steady progress on workstream
- [ ] Deliver working increments weekly
- [ ] Demo progress to client
- [ ] Handle client feedback and iterate
- [ ] Keep buddy informed (don't go dark)

**Client Interaction:**

- [ ] Lead sections of client calls
- [ ] Present your work
- [ ] Answer questions (escalate to buddy if needed)
- [ ] Build relationship with client team

**Technical Work:**

- [ ] Write production-quality code (not prototype)
- [ ] Add tests where appropriate
- [ ] Document what you're building
- [ ] Contribute fixes back to product when you find gaps

**Common Challenges (expect these):**

- Requirements change mid-work
- Client environment doesn't match expectations
- You hit roadblocks with product capabilities
- You underestimate task complexity

**How to Handle:**

- Communicate early (don't hide problems)
- Ask buddy for guidance on scope changes
- Escalate technical blockers to product team
- Update estimates and reset expectations

**Mid-Point Check-in (End of Week 6):**

- Are you on track for workstream completion?
- What's working well?
- What would you do differently?

---

### Week 8: Delivery & Reflection

**Final Push (30-35 hours):**

- [ ] Complete workstream deliverables
- [ ] Get client sign-off
- [ ] Hand off to client (training, docs, runbook)
- [ ] Celebrate completion (even if imperfect)

**Knowledge Capture:**

- [ ] Document what you built (architecture, decisions)
- [ ] Write "lessons learned" (for yourself and team)
- [ ] Identify what should be product features (not custom work)
- [ ] Update team knowledge base

**60-Day Review with Manager:**

- [ ] Assess workstream delivery
- [ ] Discuss technical growth
- [ ] Evaluate client communication skills
- [ ] Determine readiness for independent work

**Week 8 Success Check:**

- [ ] Delivered real value to a client
- [ ] Led workstream from start to finish (with support)
- [ ] Communicated effectively with client
- [ ] Escalated when stuck (appropriately)
- [ ] Ready for more independence

---

## Weeks 9-12: Independent Work

**Goal:** Own a client engagement. Buddy available, but you drive.

### Week 9: Independent Assignment

**New Engagement:**

- [ ] Get assigned to new client engagement (you're the lead FDE)
- [ ] Buddy is available for questions but not actively involved
- [ ] Manager expects you to drive (with appropriate escalation)

**Kickoff (Week 9):**

- [ ] Participate in client discovery/scoping
- [ ] Break down work into phases
- [ ] Estimate timeline and communicate to client
- [ ] Set up regular check-ins with client
- [ ] Identify risks and dependencies early

**Execution:**

- [ ] Work independently (don't check every decision with buddy)
- [ ] Make progress daily
- [ ] Communicate status proactively
- [ ] Escalate blockers (don't wait)

**Manager Check-in:**

- How is independent work going?
- What's different without constant buddy support?
- What do you need help with?

---

### Weeks 10-11: Delivery Ownership

**Full Ownership (60-70 hours):**

- [ ] Lead all client interactions
- [ ] Own delivery timeline and quality
- [ ] Make technical decisions
- [ ] Build client trust and relationship
- [ ] Deliver working solutions

**What "Independent" Means:**

- You drive the work (not buddy or manager)
- You set priorities and make trade-offs
- You communicate directly with client
- You escalate when truly stuck (not for every question)

**What "Independent" Doesn't Mean:**

- You never ask for help
- You make major architectural decisions alone
- You commit to unrealistic timelines
- You hide problems until they're critical

**Healthy Escalation (do this):**

- "I'm blocked on X, tried Y and Z, need help from [person]"
- "Client is asking for scope change, here's my analysis, what do you think?"
- "This will take 2 more weeks, not 1. Here's why. Shall I communicate that?"

**Unhealthy Patterns (avoid this):**

- Silent struggling for days
- Saying yes to everything client asks
- Not communicating status for a week
- Making promises you can't keep

---

### Week 12: Completion & Review

**Final Week:**

- [ ] Complete current client deliverables
- [ ] Hand off gracefully (docs, runbook, training)
- [ ] Get client feedback
- [ ] Wrap up and transition

**90-Day Review with Manager (60-90 minutes):**

**Discussion Topics:**

1. **Technical Skills:** Where are you strong? What needs more development?
2. **Client Communication:** How comfortable are you with client interactions?
3. **Ownership:** Are you taking initiative? Asking for help appropriately?
4. **Judgment:** Are you making good decisions under ambiguity?
5. **Culture Fit:** Is FDE work what you expected? Do you enjoy it?

**Outcomes:**

- [ ] Performance assessment (meeting expectations / above / below)
- [ ] Development plan for next 90 days
- [ ] Next assignment discussion
- [ ] Compensation/level discussion (if applicable)

**Week 12 Success Check:**

- [ ] Independently led client work from start to finish
- [ ] Delivered value without constant supervision
- [ ] Communicated effectively (clients, team, manager)
- [ ] Escalated appropriately (not too much, not too little)
- [ ] Ready for next engagement without special support

---

## Onboarding Buddy Role

### Purpose
The onboarding buddy is the new hire's primary resource for learning FDE work. Not a manager (no performance evaluation), but a coach and guide.

### Responsibilities

**Week 1:**

- Work together daily (pair on setup, answer questions)
- Ensure environment is set up in <4 hours
- Explain product architecture and codebase
- Introduce to team and processes

**Weeks 2-4:**

- Bring new hire to ALL client calls
- Explain context before calls, debrief after
- Assign small tasks, review work
- Model FDE behaviors (communication, problem-solving)

**Weeks 5-8:**

- Work together on same client engagement
- New hire owns workstream, you're accountable
- Check in daily (15 min standup)
- Let them struggle (but not drown)

**Weeks 9-12:**

- Step back (be available, don't drive)
- Weekly check-ins (30 min)
- Help when asked
- Watch for red flags, alert manager if concerned

### Selection Criteria

**Good onboarding buddy:**

- Senior or Staff FDE
- Strong communicator (patient, explains well)
- On an engagement with room for new hire to contribute
- Wants to help (not voluntold)
- Available for 12 weeks (not about to leave/transition)

**Time Commitment:**

- Week 1: ~10 hours
- Weeks 2-4: ~5 hours/week
- Weeks 5-8: ~3 hours/week
- Weeks 9-12: ~1 hour/week

**Total: ~30-35 hours over 12 weeks**

### Buddy Compensation

Onboarding is real work. Options:

- Reduce buddy's client workload expectations
- Count onboarding as separate project in performance reviews
- Bonus for successful onboarding (new hire meets 90-day bar)

---

## Red Flags: Warning Signs

Watch for these patterns. Intervene early.

### Week 1-2 Red Flags

| Red Flag | What It Means | Action |
|----------|---------------|--------|
| **Environment setup >4 hours** | Product team hasn't met technical enablement standards | Escalate to Product lead, pause onboarding until fixed |
| **Doesn't ask questions** | Too intimidated, doesn't want to look dumb, or doesn't care | Buddy: explicitly invite questions, model asking "dumb" questions |
| **Silent in meetings** | Overwhelmed, not engaged, or learning by osmosis (doesn't work) | Buddy: ask for their observations after each meeting |
| **Can't explain what they learned** | Passive observation, not active learning | Manager: assign explicit learning tasks with presentations |

### Week 3-4 Red Flags

| Red Flag | What It Means | Action |
|----------|---------------|--------|
| **Not submitting PRs** | Stuck, intimidated by process, or not doing work | Buddy: pair program, walk through PR process |
| **PRs have major quality issues** | Lacks technical fundamentals or doesn't understand standards | Manager: assess if bad hire or need more support |
| **Avoiding client interactions** | Doesn't want client-facing work (FDE mismatch) | Manager: direct conversation about FDE fit |
| **Only does what's explicitly assigned** | Lacks ownership mindset | Buddy: stop assigning tasks, see if they identify work themselves |

### Week 5-8 Red Flags

| Red Flag | What It Means | Action |
|----------|---------------|--------|
| **Goes dark (no updates for days)** | Stuck and hiding it, doesn't know how to escalate | Buddy: daily check-ins until pattern breaks |
| **Misses deadlines without warning** | Poor estimation, over-committed, or not tracking | Manager: teach estimation and communication |
| **Client confusion/frustration** | Poor communication or over-promising | Buddy: shadow client calls again, model better patterns |
| **Blames others for blockers** | Lacks ownership mindset, victim mentality | Manager: serious conversation about fit |

### Week 9-12 Red Flags

| Red Flag | What It Means | Action |
|----------|---------------|--------|
| **Still needs constant hand-holding** | Not gaining independence, may not be FDE fit | Manager: assess if extension or wrong role |
| **Client relationship problems** | Communication or stakeholder management weakness | Manager: coaching or reassignment |
| **Can't work through ambiguity** | Needs well-defined tasks (not FDE strength) | Manager: discuss role fit honestly |
| **Team concerns about quality or judgment** | Peer feedback indicates issues | Manager: performance improvement plan or exit |

### When to Extend Onboarding

**Valid reasons for 30-60 day extension:**

- Product team technical debt blocked progress (not new hire's fault)
- First client engagement was unusual/difficult (bad luck)
- New hire is junior but showing growth trajectory
- Specific skill gap that can be addressed with coaching

**Not valid reasons:**

- "They're nice, let's give them more time" (culture fit ≠ capability)
- "We're too busy to deal with this" (delay doesn't help)
- "Maybe they'll figure it out" (without a plan, they won't)

---

## Manager Responsibilities

### Weekly Check-ins (30 minutes)

**Agenda:**

1. **How's it going?** (open-ended, listen for concerns)
2. **What did you accomplish this week?**
3. **What's blocking you?**
4. **What are you working on next week?**
5. **Any questions for me?**

**Don't:**

- Skip these (they're critical)
- Make it a status report (this is coaching time)
- Do all the talking (listen more than you speak)
- Let problems fester (address issues immediately)

### Formal Reviews

**30-Day Review (60 minutes):**

- Assess against Week 4 success criteria
- Technical skills: where are they strong/weak?
- Communication: comfortable with clients?
- Culture fit: enjoying FDE work?
- Decision: on track / needs support / concerning

**60-Day Review (60 minutes):**

- Assess against Week 8 success criteria
- Delivery: did they complete workstream?
- Independence: working with less support?
- Judgment: making good decisions?
- Decision: ready for independence / need more support / not working

**90-Day Review (90 minutes):**

- Assess against Week 12 success criteria
- Performance: meeting expectations for level?
- Trajectory: where will they be in 6 months?
- Development plan: what's next?
- Decision: meets bar / needs improvement plan / wrong fit

### Tough Conversations

**If someone isn't working out:**

- Address it at 30 or 60 days (don't wait until 90)
- Be direct: "Here's what I'm seeing, here's the concern"
- Clarify expectations: "By [date], I need to see [specific changes]"
- Offer support: "Here's how I can help"
- Document conversations (for your sake and theirs)

**If it's not getting better:**

- Don't drag it out (it's unfair to everyone)
- Have the hard conversation (this role may not be the right fit)
- Explore alternatives (different role? team? company?)
- Exit gracefully (no shame in wrong fit)

---

## Success Indicators

### What Good Looks Like at 90 Days

**Technical:**

- Can set up environment in <4 hours (and help others do it)
- Comfortable working across the stack (not expert, but not intimidated)
- Writes production-quality code
- Knows when to ask for help vs. figure it out

**Client Communication:**

- Leads client calls confidently
- Explains technical concepts clearly
- Sets realistic expectations
- Builds trust with clients

**Ownership:**

- Takes initiative (identifies work, doesn't wait to be assigned)
- Delivers what they promise
- Escalates appropriately (not too much, not too little)
- Follows through (doesn't drop balls)

**Judgment:**

- Makes good decisions under ambiguity
- Balances speed vs. quality appropriately
- Knows when to build custom vs. push back
- Manages scope creep

**Team Contribution:**

- Helps other FDEs (shares knowledge)
- Improves documentation
- Identifies patterns (what should be product features)
- Participates in team discussions

### Comparison to Hire Expectations

**Exceeding Expectations:**

- Independently leading complex client work
- Contributing architectural improvements to product
- Mentoring newer FDEs
- Clients specifically request them

**Meeting Expectations:**

- Successfully completing assigned client work
- Communicating well with clients and team
- Making steady progress independently
- Contributing to team knowledge

**Below Expectations:**

- Still needs significant support after 90 days
- Client communication issues persist
- Not working independently
- Quality or judgment concerns

---

## Usage Notes

### Adapting by Experience Level

**For Associate FDEs (0-2 years experience):**

- Expect more time in Weeks 2-4 (shadowing)
- Pair program more heavily in Weeks 5-8
- Focus on fundamentals (code quality, communication basics)
- May need extended onboarding (120 days acceptable)

**For Mid-level FDEs (2-5 years):**

- Can move faster through Week 1 (setup should be trivial)
- Less shadowing in Weeks 2-4 (more doing)
- Expect independent work by Week 6-7
- Should hit all 90-day success indicators

**For Senior FDEs (5+ years):**

- Weeks 1-4 are mostly context-building (they know how to work)
- Focus on product-specific knowledge
- May skip "supported first deployment" if they have FDE experience
- Should be fully independent by Week 6

### Adapting by Archetype

**Business-Facing FDEs:**

- More emphasis on client interaction shadowing (Weeks 2-4)
- First deployment should focus on client relationship building
- Success indicators weight communication > technical depth

**Product-Facing FDEs:**

- More emphasis on technical deep dives (Week 1-2)
- First deployment should focus on product contribution
- Success indicators weight code quality > client communication

### Remote vs. Co-located

**Remote Onboarding:**

- Schedule more intentional pairing time (remote = less osmosis)
- Daily video check-ins with buddy (Week 1-4)
- Record client calls so new hire can rewatch
- Be extra explicit about expectations (less ambient context)

**Co-located Onboarding:**

- Buddy and new hire should sit together (Week 1-4)
- Bring new hire to lunch, coffee, informal conversations
- Easier to spot when someone is struggling (you can see them)

### Common Mistakes

**Mistake: Throwing them in the deep end too early**

- "You'll learn by doing" doesn't work without scaffolding
- Result: bad habits, client confusion, burnout
- Fix: Follow the 4-phase structure (don't skip shadowing)

**Mistake: Too much hand-holding for too long**

- They never learn to work independently
- Result: you create dependency, not capability
- Fix: Progressive stepping back (buddy role by week)

**Mistake: No formal check-ins**

- Assume they'll speak up if struggling (they won't)
- Result: find out at 90 days it's not working (too late)
- Fix: Weekly manager check-ins, formal 30/60/90 reviews

**Mistake: Buddy is too busy**

- "Shadow me" but never around
- Result: new hire learns nothing, feels abandoned
- Fix: Reduce buddy's other work OR pick different buddy

**Mistake: Not tracking against criteria**

- "How are you doing?" → "Fine!" → repeat
- Result: no real assessment until it's too late
- Fix: Use success criteria checklist, be specific

---

**Template Version:** 1.0
**Last Updated:** 2026-01-18
**Source:** [Hiring & Talent Strategy](../../01-hiring-talent-strategy.md), [Technical Enablement](../../03-technical-enablement.md), [FDE Startup Kit](../../00-fde-startup-kit.md)

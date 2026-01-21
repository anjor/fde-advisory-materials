# Hiring & Talent Strategy

> **TL;DR:** FDE hiring requires evaluating technical depth, client-facing capability, pain tolerance, and ownership mindset. Standard engineering interviews miss critical FDE competencies. Use a multi-track process adapted by candidate source.

---

## The Challenge

Traditional engineering hiring optimizes for:

- Specific technology skills (Python, React, AWS)
- Algorithm performance
- System design for scale

FDE hiring must additionally evaluate:

- Ability to learn unfamiliar domains quickly
- Client-facing communication under ambiguity
- Pain tolerance when systems are broken
- Ownership of outcomes, not just tasks

Organizations that use standard engineering interviews will hire technically competent people who fail as FDEs because they can't handle messy client situations or unclear requirements.

---

## Ideal FDE Profile

### Must-Have Traits

| Trait | What It Looks Like | Red Flag |
|-------|-------------------|----------|
| **Ownership** | "I'll figure it out" vs "That's not my job" | Waits to be told what to do |
| **Learning velocity** | Picks up new domain/technology in days, not weeks | Needs extensive training before contributing |
| **Pain tolerance** | Pushes through broken environments, missing docs, unclear requirements | Escalates blockers instead of working around them |
| **GTD** | Comes up with creative ways to get things done | Disappears when things get hard |
| **Technical breadth** | Can work across frontend, backend, data, infra as needed | "I only do backend" |
| **Client communication** | Explains technical concepts to non-technical stakeholders | Uses jargon, talks past the client |

### Nice-to-Have
- Domain expertise in target verticals (finance, insurance, CPG)
- Prior consulting or client-facing experience
- Experience with early-stage/ambiguous product environments

### Explicit Non-Requirements
- Specific programming language expertise (can learn)
- Years of experience (attitude > tenure)
- Pedigree (big tech, top school)

---

## Hiring Channels

### Channel 1: Circle of Trust (Fastest)
People you or trusted colleagues have worked with directly.

**Modified Process:**

1. Skip phone screen
2. Skip first tech screen  
3. Go straight to Learning & Reengineering exercise
4. Decomposition exercise
5. Hiring manager conversation

**Rationale:** You already know their work quality. Focus on FDE-specific fit.

### Channel 2: Internal Mobility (Medium Speed)
Existing employees who want to transition to FDE role.

**Modified Process:**

1. Manager endorsement (replaces phone screen)
2. Technical screen (verify current skills)
3. Learning & Reengineering exercise
4. Decomposition exercise
5. Hiring manager conversation

**Watch For:** People escaping bad situations vs. genuinely drawn to FDE work.

### Channel 3: External Sourcing (Full Process)
Unknown candidates from job postings, recruiters, etc.

**Full Process:**

1. Phone screen (15-30 min) - Basic communication, interest validation
2. Technical screen (60 min) - Verify baseline technical competence
3. Learning & Reengineering (60 min) - FDE-specific evaluation
4. Decomposition (60 min) - Problem-solving approach
5. Hiring manager (45-60 min) - Thesis validation, culture fit

---

## Interview Process Details

> **Scaling Note:** This process assumes hiring an initial cohort of 3-5 FDEs over 2-3 months. For faster scaling (10+ hires), add a dedicated hiring manager role. For slower growth (1-2 hires), consider combining the Technical Screen with Learning & Reengineering.

### Phone Screen (15-30 min)
**Purpose:** Filter obvious mismatches quickly.

**Evaluate:**

- Can they communicate clearly?
- Do they understand what FDE work involves?
- Are they genuinely interested or just applying broadly?

**Questions:**

- "Tell me about a time you had to figure something out with minimal documentation or guidance."
- "What draws you to client-facing technical work vs. pure product development?"
- "Describe a situation where you had to push back on a client or stakeholder."

**Pass/Fail:** Trust your gut. If conversation is painful, it won't improve.

---

### Technical Screen (60 min)
**Purpose:** Verify baseline technical competence.

**Format:** Adapt based on candidate background. The goal is confirming they can code, not testing specific technologies.

**For Backend-Heavy Candidates:**

- API design problem
- Data modeling scenario
- System integration discussion

**For Frontend-Heavy Candidates:**

- Component architecture
- State management approaches
- API consumption patterns

**For Data/ML Candidates:**

- Pipeline design
- Evaluation methodology discussion
- Data quality handling

**Pass Criteria:** Can they think through technical problems systematically? Do they ask clarifying questions? Can they explain their reasoning? Do they have the right abstractions?

---

### Learning & Reengineering (60 min)
**Purpose:** Evaluate how quickly they can understand and extend unfamiliar systems.

**Format:** Give candidate access to an unfamiliar codebase or system. Ask them to:

1. Understand what it does (15 min)
2. Explain it back to you (10 min)
3. Propose and implement a small change (25 min)
4. Discuss what they'd do differently (10 min)

**What to Observe:**

- How do they navigate unfamiliar code?
- Do they use available tools effectively (search, AI assistants)?
- Can they form a mental model quickly?
- How do they communicate their understanding?

**High Signal Topics:**

- Evaluation methodology ("How would you know if this is working?")
- Edge case thinking ("What could go wrong?")
- Production awareness ("How would this behave under load?")

**Pass Criteria:** They should be able to make meaningful progress despite unfamiliarity. Perfect solution not required—approach matters more.

---

### Decomposition (60 min)
**Purpose:** Evaluate problem-solving approach on ambiguous, real-world problems.

**Format:** Present a complex problem and ask them to break it down. Can be technical or non-technical depending on role.

**Technical Decomp Example:**
> "A retail client wants to build an AI system that recommends products based on browsing history, purchase history, and current inventory. How would you approach this?"

**Non-Technical Decomp Example:**
> "A client's sales team isn't adopting the new CRM we deployed. Adoption is at 20% after 3 months. What would you do?"

**What to Observe:**

- Do they ask clarifying questions or jump to solutions?
- Can they identify the key sub-problems?
- Do they consider constraints (time, budget, client politics)?
- How do they prioritize what to tackle first?
- Can they articulate trade-offs?

**Pass Criteria:** Structured thinking, appropriate questions, realistic about constraints.

---

### Hiring Manager Conversation (45-60 min)
**Purpose:** Thesis validation and final assessment.

**Before the Interview:**
Write a "hiring thesis" based on previous rounds:

- "I believe this candidate would be strong at X because of Y"
- "I'm uncertain about Z and need to probe further"

**During the Interview:**

- Test your thesis with targeted questions
- Discuss career goals and FDE fit
- Assess culture add
- Sell the role (if candidate is strong)

**Topics to Cover:**

- Most challenging client/stakeholder situation they've navigated
- Time they had to deliver despite inadequate support/resources
- What they're looking for in next role
- Questions about the FDE model

---

## Fresh Graduate Hiring

### Philosophy
Throw them in the deep end. FDE skills are learned by doing, not training.

### Approach
1. **Hire for raw intelligence and attitude**, not experience
2. **Pair with senior FDE** on first engagement
3. **Give real responsibility early** - own a workstream, not just tasks
4. **Expect them to struggle** - that's the learning
5. **Watch for people who give up** vs. people who figure it out

### Modified Interview Process
- Skip "years of experience" requirements
- Focus on learning velocity and problem-solving approach
- Look for side projects, hackathons, or situations where they taught themselves
- Pay attention to how they handle not knowing the answer

### First Assignment
Put them on an active client engagement with a senior FDE who can provide context but expects them to execute. Check in weekly, but don't hand-hold.

---

## Interview Calibration

### For New Interviewers
1. **Shadow 3-5 interviews** before running your own
2. **Co-interview** with experienced interviewer for next 3-5
3. **Debrief every interview** - what did you see, what did you miss?
4. **Record interviews** (with permission) for review and training

### Calibration Practices
- Weekly hiring huddle to discuss candidates and calibrate bar
- Written feedback submitted before group discussion (avoid anchoring)
- Track hire outcomes: Are people we rated highly performing well?

### Red Flags to Align On
Everyone should reject candidates who:

- Can't explain their thinking clearly
- Blame others for past failures
- Show no curiosity about the problem domain
- Need everything specified before starting
- Are dismissive of client concerns

---

## Making Offers

### Compensation Philosophy
FDEs should be paid at or above senior engineering levels. The role requires:

- Engineering skills PLUS
- Client skills PLUS
- Pain tolerance PLUS
- Ownership mindset

Underpaying attracts people who can't get other offers.

### Competing With
- Big Tech (Google, Meta, etc.) - We offer more impact and variety
- Consulting (McKinsey, BCG) - We offer more technical depth
- Startups - We offer more stability and client exposure

### Offer Process
1. Move fast - good candidates have options
2. Be transparent about role expectations (including the hard parts)
3. Connect candidates with current FDEs for real talk
4. Make competitive initial offer - don't lowball and negotiate up

---

## Metrics

### Process Metrics
- Time from first contact to offer: Target <3 weeks
- Interview-to-offer ratio by channel
- Offer acceptance rate: Target >70%

### Outcome Metrics (6-month lookback)
- % of hires rated "meeting expectations" at 90 days
- % of hires still in role at 12 months
- Correlation between interview scores and performance ratings

---

## Resources

### Interview Scorecard
For each interview round, rate 1-5 on:

| Dimension | 1 (Reject) | 3 (Neutral) | 5 (Strong Hire) |
|-----------|------------|-------------|-----------------|
| Technical competence | Major gaps | Adequate | Exceeds bar |
| Learning velocity | Struggled to progress | Made reasonable progress | Exceeded expectations |
| Communication | Unclear, verbose | Clear enough | Crisp, adapted to audience |
| Problem decomposition | Jumped to solutions | Reasonable structure | Excellent structure |
| Ownership signals | Blamed others, waited for direction | Neutral | Clear ownership examples |
| Pain tolerance | Gave up easily | Persisted | Thrived in ambiguity |

**Overall:** Strong Hire / Hire / No Hire / Strong No Hire

**Written Justification (required):**
[Why are you making this recommendation? What evidence supports it?]

---

### Hiring Thesis Template

- **Candidate:** [Name]
- **Role:** FDE
- **Interviewer:** [Your name]
- **Date:** [Date]

**Based on previous rounds, I believe:**

- This candidate would be strong at: [specific areas]
- Evidence: [what you saw]

**I am uncertain about:**

- [specific concern]
- I plan to probe by asking: [question]

**Key questions for this interview:**

1. [Question targeting thesis validation]
2. [Question targeting uncertainty]
3. [Question about culture/fit]

---

## Common Mistakes

| Mistake | Why It Happens | How to Avoid |
|---------|----------------|--------------|
| Hiring for specific tech stack | Familiar evaluation criteria | Focus on learning ability, not current knowledge |
| Overlooking communication skills | Technical interviews dominate | Include client scenario in decomposition |
| Hiring "nice" people without grit | Likability bias | Specifically probe for adversity examples |
| Slow process loses candidates | Too many interview stages | Compress timeline, make decisions quickly |
| Lowballing offers | Budget pressure | Benchmark against competing offers, not internal bands |

---

## Further Reading

For the philosophy and reasoning behind these practices:

- [The FDE Manifesto: What Would Stokes Do?](https://anjor.xyz/writing/2025/11/20/the-fde-manifesto-what-would-stokes-do/) - Tactical principles that define exceptional FDE behavior. Use as evaluation criteria.
- [Hiring Theses](https://anjor.xyz/writing/2024/08/02/hiring-theses/) - Why documenting your hiring rationale matters and how to do it.
- [Interviews Are Unfair](https://anjor.xyz/writing/2024/08/13/interviews-are-unfair/) - Balancing empathy with objectivity during evaluation.
- [The Unreasonable Effectiveness of Hiring Assholes](https://anjor.xyz/writing/2025/11/13/the-unreasonable-effectiveness-of-hiring-assholes/) - Separating conviction from toxicity in candidates.
- [The Database Selection Trap](https://anjor.xyz/writing/2025/07/05/the-database-selection-trap-why-your-technical-interviews-might-be-testing-the-wrong-things/) - Common interview anti-patterns to avoid.
- [Criticality and Engagement](https://anjor.xyz/writing/2024/12/17/criticality-and-engagement/) - The two must-have traits in any hire.

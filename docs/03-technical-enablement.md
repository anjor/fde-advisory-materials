# Technical Enablement

> **TL;DR:** FDEs can't work when documentation is missing, repositories are scattered, and environment setup takes days. This document defines minimum standards that Product teams must meet and workflows for FDEs to build knowledge as they go.

---

## The Challenge

From actual field experience:

> "One repository is in GitHub, another is in Azure DevOps, another is on somebody's local machine."

> "We are spending days just talking to six different people trying to get to an environment where I can do something."

> "I don't think there are even tests."

This is the state of many early-stage products. FDEs are expected to deploy these products to clients while simultaneously fighting basic infrastructure chaos.

---

## Minimum Viable Standards

These are the baseline requirements for a product to be "FDE-ready."

### Tier 1: Absolute Minimum (Required)

Without these, FDEs cannot work. Product teams must provide these before FDE engagement begins.

| Standard | What It Means | Verification |
|----------|---------------|--------------|
| **Single source of truth for code** | All code in one repo (or documented multi-repo structure) | FDE can find all code without asking |
| **Working README** | Setup instructions that actually work | New person can complete setup following README |
| **Local development possible** | Can run the product locally | FDE can make and test changes locally |
| **Access provisioned** | FDE has all necessary permissions | FDE can clone, run, and deploy without escalation |

### Tier 2: Expected (Required within 2 weeks of FDE engagement)

| Standard | What It Means | Verification |
|----------|---------------|--------------|
| **Data model documentation** | Written description of core entities and relationships | FDE can explain data model to client |
| **API documentation** | Endpoint catalog with request/response formats | FDE can integrate without reading source |
| **Configuration guide** | How to customize without code changes | FDE knows what's configurable |
| **Seed data** | Representative data for testing | FDE can demo realistic scenarios locally |

### Tier 3: Target State (Build over time)

| Standard | What It Means | Verification |
|----------|---------------|--------------|
| **Automated testing** | CI/CD with meaningful test coverage | Changes can be validated automatically |
| **Architecture decision records** | Why things are built the way they are | FDE understands design rationale |
| **Performance baselines** | Known response times, limits | FDE can set client expectations |
| **Runbook for common issues** | Troubleshooting guide | FDE can resolve issues without escalation |

---

## Environment Setup Requirements

### The Standard
A new FDE should go from "I have access" to "I can make and test changes" in **< 4 hours**.

### What Product Teams Must Provide

```
/repository
├── README.md                    # Quick start guide
├── docs/
│   ├── SETUP.md                # Detailed setup instructions
│   ├── ARCHITECTURE.md         # System overview
│   └── DATA_MODEL.md           # Entity documentation
├── docker-compose.yml          # One-command local environment
├── .env.example                # Environment variables template
├── scripts/
│   ├── setup.sh               # Initial setup automation
│   └── seed-data.sh           # Load test data
└── [application code]
```

### README.md Template

```markdown
# [Product Name]

## Quick Start (< 15 min)

### Prerequisites
- Docker Desktop
- [Other requirements]

### Setup
1. Clone this repo
2. Copy `.env.example` to `.env`
3. Run `docker-compose up`
4. Open http://localhost:3000

### Verify It Works
- Go to [URL]
- You should see [expected result]
- Try [simple action]

## For More Information
- [Detailed setup](docs/SETUP.md)
- [Architecture overview](docs/ARCHITECTURE.md)
- [API documentation](docs/API.md)

## Getting Help
- Slack: #[channel]
- On-call: [who to contact]
```

### When Setup Fails
If an FDE cannot complete setup following documentation:

1. FDE documents exactly where they got stuck
2. Product team fixes the issue within 24 hours
3. Documentation is updated to prevent recurrence
4. Incident logged to track setup reliability

---

## Documentation Standards

### Required Documentation

| Document | Purpose | Owner | Update Trigger |
|----------|---------|-------|----------------|
| README.md | Quick start | Product | Any setup change |
| SETUP.md | Detailed setup | Product | Any dependency change |
| ARCHITECTURE.md | System overview | Product | Major architecture change |
| DATA_MODEL.md | Data structures | Product | Schema change |
| API.md | Integration guide | Product | API change |
| CHANGELOG.md | What changed when | Product | Every release |
| RUNBOOK.md | Troubleshooting | FDE + Product | New issue discovered |

### Documentation Quality Checklist

- Can someone follow it without asking questions?
- Are all commands copy-pasteable?
- Are environment-specific values clearly marked?
- Is it current (updated within last month)?
- Does it explain WHY, not just WHAT?

### Living Documentation

Documentation should be:

- **In the code repo** (not a separate wiki)
- **Version controlled** (changes tracked)
- **PR-reviewed** (someone else verifies it works)
- **FDE-maintained** (FDEs fix what they find broken)

---

## The "Learn by Doing, Document Immediately" Workflow

FDEs will encounter undocumented systems. Here's how to handle it:

### The Workflow

```
1. FDE encounters undocumented area
         ↓
2. FDE figures it out (ask people, read code, experiment)
         ↓
3. FDE documents IMMEDIATELY (same day)
         ↓
4. FDE submits PR to product repo
         ↓
5. Product team merges quickly (<48 hours)
         ↓
6. Next FDE doesn't have same problem
```

### What to Document

When you figure something out, document:

- **What you were trying to do**
- **What wasn't clear**
- **How it actually works**
- **Commands/steps that worked**
- **Gotchas you discovered**

### Documentation PR Template

```markdown
## What This Adds

Brief description of documentation being added.

## Why This Was Needed

What I was trying to do and why existing docs didn't help.

## How I Figured It Out

Who I asked / what I tried / how long it took.

## Verification

I've verified this documentation by [how you verified].
```

### Product Team Obligation

Product teams must:

- Merge documentation PRs within 48 hours
- Not block on "let me clean this up first"
- Give FDEs write access to docs folders
- Review for accuracy, not style

---

## Repository Standards

### The Problem

Common dysfunction:

- Code in GitHub, infrastructure in Azure DevOps, scripts on someone's laptop
- Different services in different repos with no guide
- "Just ask [person]" as the documentation

### Minimum Standards

| Standard | Requirement |
|----------|-------------|
| **Single org/location** | All repos in same GitHub/GitLab org |
| **Discoverable** | README in each repo explains what it is |
| **Consistent naming** | [product]-[component] format |
| **Access controlled** | FDEs have access to everything they need |
| **Main branch works** | Main branch always deployable |

### For Multi-Repo Products

If your product spans multiple repos, you MUST have:

```
[product]-docs/
├── README.md                    # Start here
├── REPO_MAP.md                 # What's in each repo
├── GETTING_STARTED.md          # Full setup across all repos
└── ARCHITECTURE.md             # How repos relate to each other
```

### Repository Checklist

- Can I find all related code from one starting point?
- Is it clear which repo to change for which feature?
- Do all repos have working CI/CD?
- Are there branch protection rules?
- Is there a clear PR review process?

---

## Demo Infrastructure

### Requirements for Demo Capability

FDEs need to build and run demos. Product teams must provide:

| Component | What It Is | Why FDEs Need It |
|-----------|------------|------------------|
| **Demo environment** | Persistent instance for demonstrations | Can't demo from local machine |
| **Reset capability** | Way to restore to clean state | Demos get messy, need fresh starts |
| **Sample data** | Realistic-looking test data | Empty systems don't demo well |
| **Configuration examples** | Pre-built configurations for different scenarios | Industry-specific demos |

### Demo Environment Checklist

- Always available (not taken down for maintenance without notice)
- Accessible from customer networks (not behind corporate VPN)
- Representative of production (same features, similar performance)
- Can be reset without engineering support
- Has data that looks real (not "test123", "asdf")

### FDE Demo Building Workflow

1. **Start from reference demo** (provided by Product)
2. **Fork configuration** (not code) for client-specific version
3. **Add client-relevant data** (anonymized or synthetic)
4. **Document what you changed** (for reuse)
5. **Share patterns** (if useful for others)

---

## AI-Assisted Development

### Tools FDEs Should Use

| Tool | Purpose | Prerequisite |
|------|---------|--------------|
| **Claude Code / Cursor** | AI-assisted coding | Codebase indexed |
| **GitHub Copilot** | Code completion | Access provisioned |
| **AI code search** | Navigate unfamiliar code | Codebase indexed |

### Enabling AI Effectiveness

For AI tools to help FDEs, Product teams should:

- Ensure codebase is in standard structure AI can understand
- Add inline comments explaining non-obvious code
- Maintain accurate README and docs (AI reads these)
- Avoid proprietary DSLs that AI doesn't know

### IT Provisioning

AI tools require IT approval in most organizations. Leadership should:

- Pre-approve common tools (list them)
- Fast-track requests for FDE team
- Accept that AI tools are productivity multipliers, not security threats

---

## Code Quality Baseline

### Minimum Expectations

| Area | Minimum Standard |
|------|------------------|
| **Version control** | All code in git, no exceptions |
| **Branching** | Feature branches, merged via PR |
| **Code review** | At least one approval before merge |
| **Testing** | Critical paths have automated tests |
| **CI/CD** | Automated build on every PR |

### What FDEs Should Expect

- **Main branch always works** - If main is broken, it's a P1 incident
- **Clear PR process** - Know how to get changes reviewed and merged
- **Test requirements documented** - Know what tests to write/update
- **Deploy process documented** - Know how to get changes to production

### What FDEs Are Responsible For

- Follow existing conventions (don't introduce new patterns without discussion)
- Write tests for new functionality
- Update docs when changing behavior
- Flag tech debt rather than silently accumulating it

---

## Security & Compliance

### FDE Security Responsibilities

| Area | FDE Must |
|------|----------|
| **Credentials** | Never commit secrets to repos |
| **Client data** | Never copy client data to personal/unsecured systems |
| **Access** | Use minimum necessary permissions |
| **Environments** | Keep dev/staging/prod clearly separated |

### Common Compliance Contexts

| Industry | Key Requirements | FDE Implications |
|----------|------------------|------------------|
| **Healthcare (HIPAA)** | PHI protection | No real patient data in demos |
| **Finance (SOC2)** | Audit trails | Log access, track changes |
| **Government (FedRAMP)** | US data residency | Check deployment region |

### When In Doubt

If you're unsure whether something is allowed:

1. Ask before doing
2. Document the question and answer
3. Err on the side of caution

---

## Checklist: Is Technical Enablement Sufficient?

### For FDE Leaders

**Environment:**

- Can a new FDE set up their environment in < 4 hours?
- Is there a single source of truth for code?
- Do FDEs have access to everything they need?

**Documentation:**

- Can FDEs find answers without asking people?
- Is documentation trusted (accurate and current)?
- Can FDEs contribute documentation fixes?

**Demo:**

- Can FDEs build demos without Product team help?
- Is there reference demo data available?
- Can demo environments be reset easily?

### For Product Leaders

**Baseline:**

- Is your README actually a quick start (< 15 min)?
- Does main branch always work?
- Are your repos organized and discoverable?

**Documentation:**

- Is your data model documented?
- Are your APIs documented?
- Is your configuration documented?

**Support:**

- Do FDEs know who to ask for help?
- Do you respond to FDE requests within 24 hours?
- Do you merge FDE documentation PRs quickly?

---

## When Standards Aren't Met

### Escalation Triggers

| Situation | Action |
|-----------|--------|
| FDE can't complete setup after 8 hours | Escalate to Product lead |
| Documentation is missing and no one knows | Escalate to engineering management |
| Product team won't prioritize enablement | Escalate to VP Eng |
| Pattern of repeated failures | Propose joint remediation plan |

### Remediation Planning

If a product consistently fails technical enablement:

1. **Audit:** Document all gaps (setup time, missing docs, blockers)
2. **Prioritize:** Rank by FDE impact
3. **Plan:** Create 30-day remediation plan
4. **Execute:** Product team owns, FDE team supports
5. **Verify:** FDE attempts setup from scratch
6. **Maintain:** Regular checks to prevent regression

---

## Further Reading

- [The FDE Manifesto: What Would Stokes Do?](https://anjor.xyz/writing/2025/11/20/the-fde-manifesto-what-would-stokes-do/) - See "Own the Product Stack" and "Treat Information as Infrastructure" sections for the mindset behind technical enablement requirements.

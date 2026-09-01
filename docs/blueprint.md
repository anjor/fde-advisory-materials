# The Platypus FDE Blueprint

!!! note "Canonical copy"
    This is the canonical, versioned copy of the Blueprint. [platypustech.xyz/blueprint](https://platypustech.xyz/blueprint/) mirrors it.

*Canonical framework, v1.0 — September 2026. Public document. Licence: CC BY 4.0. This page is the ruler; the engagements are the measurement and the fix.*

*Everything below has been said out loud in client rooms, panels and investor sessions between November 2025 and August 2026. This is the first time it has been written down in one place with names on the parts.*

---

## The one-paragraph version

Forward Deployed Engineering is a product R&D function dressed up as a delivery function. An FDE owns a customer's outcome, builds whatever the product cannot yet do, and walks the bag of weird bricks back to the people who build the product. Whether you need that function, what shape it takes, and how you measure it are all downstream of two decisions most companies never make explicitly: **what problem is the field solving for the product**, and **where the compounding asset lives** — in a product you sell or a capability you keep. The Blueprint is a way of making those decisions on purpose, then designing the unit, the interfaces, the hiring bar and the measurements to match.

---

## Part 1 — The reasoning gate: do you need FDEs at all?

"I want to hire FDEs" is not a complete sentence. Most companies hiring FDEs today do not need them. The role exists to fill the gap between what the product does and what the customer needs; if that gap is not shrinking, something else is wrong and FDEs will not fix it.

Three questions, in order:

1. **What is the deployment problem?** Not "what is our org chart missing" — what specifically breaks between a signed contract and a customer getting value? Name it.
2. **Which half of product-market fit are you missing?**
    - *Finding product* — the product does not exist yet, or does not work in the customer's environment. The FDE *is* the product. You need a **product-facing FDE**.
    - *Finding market* — the product works; you need to land, expand into adjacent lines of business, and discover what else the customer will pay for. You need a **business-facing FDE** (at Palantir this role was the deployment strategist).
    - *Neither* — the product works out of the box and you need to sell more of it. You need solutions engineers and solutions architects. Call them that.
3. **What is the cheapest structure that solves it?** Sometimes the honest answer is better docs, a smaller product surface, a solutions team, or admitting the product is not ready. FDE is the expensive answer. It is justified when there is genuine blank-canvas work: an ambiguous problem, a customer whose real requirement is not yet written down, and a product that will learn something from the answer.

The tell that the reasoning was skipped: the number of people with the title is growing faster than the number of accounts that meet the criteria above.

---

## Part 2 — The fork: where does the compounding asset live?

AI collapsed the cost of bespoke delivery. One engineer with a coding agent can build a credible dragon in an afternoon. That opened a second coherent strategy that did not exist when Palantir made its choice.

| | **Path A — Platform** | **Path B — Outcomes** |
|---|---|---|
| The compounding asset | A product you sell | Internal tooling you keep |
| What the FDE is | A product scout; feeds the platform; the role is designed to eat itself | The delivery superpower; the FDE is the steady-state product |
| Where value is captured | Licence fees (services are the price you pay to get them) | Outcome pricing (you get paid when the problem is solved, not for hours) |
| What "healthy" looks like | Fewer FDEs per dollar every year | Higher impact per FDE every year; learnings encoded, never re-solved |
| What kills it | Never crossing the valley to a product that sells | Decaying into a consultancy with better margins |
| The Palantir line | "Build Foundry, sell Foundry" | "Build Foundry, don't sell Foundry" |

Both are coherent. The confusion about what "FDE" means is mostly companies that hired Path-A scouts, measure Path-B outcomes, and tell investors a platform story. Pick on purpose. The pick decides everything in Parts 3–7.

Services firms are on Path B whether they know it or not. Their question is different: can the commercial model be moved from selling effort to selling outcomes before the model does 70% of the build and commoditises them from underneath?

---

## Part 3 — Maturity stages: the product sets the dial

The single most useful axis for every FDE decision is **product maturity**. It sets how much autonomy the field has, what the FDE touches, and what the numbers should be doing.

| Stage | Name | What the product covers | The field's job | Code & deployment rights | The number to watch |
|---|---|---|---|---|---|
| **0** | The FDE is the product | Nothing yet | Build end to end inside the customer's mess; discover what to build | Root access, dirty builds, fork and deploy | Did we learn what to build? |
| **1** | Bootstrap | Under half | Fill the rest; product team ships alongside as FDEs for customer one | Full write access; PRs merged in days | Product coverage per deployment (rising) |
| **2** | Gap-shrinking | Half to most | Shrink the gap on every deployment; feature reuse, not code reuse | PR not ticket; config approvals begin; branches never diverge beyond two weeks | Time to fill the gap: a month → three weeks → two weeks |
| **3** | Leverage | Most | Work at the envelope of what doesn't exist; hand steady-state back | Config changes need product approval; a steady-state team owns the pager | FDEs per use case falling; revenue per FDE rising |
| **4** | Self-serve / the fork resolves | Everything the market needs | Path A: the role dissolves into SE/SA and product. Path B: the FDE stays, armed with internal tooling | Product owns the customer-config boundary | Path A: revenue per FDE. Path B: impact per FDE and outcome margin |

Two rules that fall out of the table:

- **The autonomy dial only moves one way, and the product moves it.** In 2015 a Palantir FDE could fork the code and deploy whatever they wanted. By 2022 an FDE could not make a config change without product approval. Both were correct for their stage. Setting the dial by policy rather than by stage is the most common mistake founders make in either direction.
- **The customer can only be "wrong" at Stage 3+.** Until then, when the customer's definition of working differs from yours, the customer is the product signal.

---

## Part 4 — The atomic unit: two founders per deployment

The smallest indivisible unit of a forward-deployed motion is **two people: one deployment strategist and one engineer**. Treat every deployment as an early-stage startup with two founders — the strategist is the CEO, the engineer is the CTO. The CEO sometimes writes code; the CTO sometimes runs the stakeholder meeting. The roles are not siloed; their distributions are shifted. **Both own the outcome.**

The test: *can the pair change the plan on Tuesday because of what it learned on Monday, without asking anyone?* If not, you have a delivery team with a new name.

Around the unit:

- **Tech lead / people lead split.** The tech lead is tactical — breaks down work, keeps things shipping, is on the deployment. The people lead is one step removed, matrixed, usually not on the same engagement, and is the person you vent to. The day-to-day life of an FDE is frustrating and hard; the matrix exists so someone is on your side.
- **The bucket lead** owns a portfolio of accounts: which are important, for what reason, and are they staffed with the right spikes. The bucket lead is ruthlessly focused on business objectives and *should* fight with the people lead about individual needs. Do not avoid that friction; it is by design.
- **Spikes, not averages.** The unit you assess is two units — the individual and the deployment. Hire for spikes; assemble teams whose spikes are complementary. A pyramid with a solution architect on top averages everyone toward the middle, and the middle is exactly where forward-deployed value disappears.
- **Minimum viable mass:** two or three FDEs in the same time zone, so there is someone to share your pain with.
- **Titles.** Calling everyone a forward deployed engineer lets you do reorgs without doing reorgs. Titles with growth ceilings baked in are a hiring tax.

---

## Part 5 — The three interfaces

An FDE function is defined by its edges more than its centre.

### 5a. Product — the bag-of-bricks loop

FDE incentives are misaligned with product incentives **by design, and that is a feature.** The FDE optimises for their customer's outcome; product optimises for the general case. When an FDE does violence to the product — hacks around it, abuses it, builds something ugly that works — that is not a governance failure. It is the highest-quality product signal available, because it was validated by someone who needed it to work in front of a customer.

Mechanics that keep the loop alive:

- **The engineers do not decide what gets productised.** The field builds the signal; product decides what to build properly. Collapse the two and the field loses focus and the platform gets whatever the loudest deployment needed.
- **Push and pull.** Push: every customer meeting written up and broadcast; weekly demos of what shipped (the demo is a forcing function — people who must demo build things, and it reaffirms "we are builders"). Pull: a place the field can ask product anything, and product answers.
- **Product's customer is the FDE.** For customer one, the product team *is* the FDE team. From customer two the field leads and product ships behind it. Product engineers who have never sat in a deployment refuse single-deployment asks because they have zero context; put them in one.
- **Branches never diverge beyond two weeks.** A long-lived branch is a productisation decision nobody made.
- **Sprint lock versus field time.** The field runs on the customer's clock. Product needs a lane for field-urgent work that does not wait for the next sprint.

### 5b. Sales — where the field enters

- **FDEs enter before the contract is shaped**, not after. The strategist finds the right demo scenario; the engineer builds a working prototype with real data. Proposals lose to prototypes.
- **Qualification is an FDE decision as much as a sales one.** Which accounts justify the motion (growth-stage, blank canvas, a platform that will learn) and which do not (small stagnant accounts that want a solved problem at a fixed price). Bring-your-own-telephony, bring-your-own-payments: name the entry criteria.
- **Never tie FDE compensation to account revenue.** An FDE who would rather 1.2× their own account than deliver the product signal that 2× someone else's is an account manager. Revenue is a company-level metric; the FDE is paid for outcomes and signal.

### 5c. Steady state — the hand-back

- Decompose and catalogue the maintenance work explicitly; it is the first productisation backlog.
- A **steady-state team** is the middle ground between the field owning forever and product owning too early. People who care about long-term success and process join it; it charges internally for its service.
- **The SRE rule:** the product team takes the pager when the deployment is inside the error budget; if it falls outside, the pager goes back to the field. Both sides know the rule in advance.
- **The customer-config boundary:** decide what configuration the customer can own and what is your IP, before the customer asks.

---

## Part 6 — Measurement: two KPIs and one honest proxy

Individual FDE performance is a judgment call, and that is what makes the KPI hard. Do not pretend otherwise. Measure the **function** at company level:

1. **Revenue per forward-deployed person** — company-wide, never per engagement. It measures product leverage. At Palantir it went from roughly $200k to roughly $2M per person between 2015 and 2022.
2. **Forward-deployed people per use case** — 3–5 per use case in 2015; one person carrying two or three customers by 2022. A 10× move on both numbers over seven years.
3. **Time to value**, not time to go-live. Proxy it with the interval between the end of acceptance testing and real usage in production.

The anti-pattern: revenue per FDE rising because you sold the FDE at a high price. That is a services model. The test is: *can you deliver a million-dollar contract with ten FDEs today and one FDE in a year?*

On Path B, swap revenue per FDE for **impact per FDE**: outcomes delivered per person, and how much of each delivery was re-solved from scratch versus pulled from the internal toolchain.

---

## Part 7 — Hiring: spikes, a calibrated person, and a written thesis

Standard engineering interviews hire technically competent people who fail as FDEs. The system that works:

- **Three traits and a shape.** Outcome and value orientation. Grit — how much pain can they tolerate, and is it the right kind. Learning speed and first-principles thinking. On top: a generalist builder, not a Rust engineer. The customer-facing bit is over-indexed; if they can string a sentence together and have hygiene, they are fine. The key is creative problem-solving and the product thinking to push on product.
- **Hire for spikes, encode the bar in a person.** You cannot write a rubric for a spiky profile, but you can encode it in one calibrated hiring manager to whom every interviewer is calibrated. Founders should hold this seat themselves until it genuinely does not scale.
- **The loop.** A short screen for basic signal. A **learning and re-engineering** interview: an unfamiliar codebase or DSL — do they apply the scientific method? A **decomposition** interview: a deliberately vague business problem; by the end there is a sketch of what you would build, and you have seen where their spikes are. A **bespoke hiring-manager interview** designed for the candidate after the debrief, with a written **hiring thesis** — why we are hiring this person, their ceiling, their kryptonite (the thing they must not be coached on or deployed into), best case, worst case. The thesis becomes the onboarding brief.
- **Signals that travel.** Transition points in a career and what they learned about themselves. Proudest project and most frustrating project. Pivots (a scientist who became an engineer). New graduates with the naivety to question the status quo. "Eyes light up."
- **Do not ban AI in interviews.** They will use it on the job. Design for it: the interviewer shows up as a customer with a meeting in two hours and a dashboard showing wrong numbers.
- **Hire to bootstrap, grow to scale.** Two or three experienced or FDE-adjacent people first; use them to train the next cohort; run mini-frontlines — every new engineer spends their first months in the field.
- **After the hire — the frustration test.** Frustration at ambiguity and open-endedness is a bad sign. Frustration at being blocked by things outside their control is a good sign. Staff around kryptonites; do not coach into them.

---

## Part 8 — The eight ways it fails

| # | Failure mode | What it looks like | Whose decision fixes it |
|---|---|---|---|
| 1 | **Title before problem** | The role was copied from a job ad, not derived from a deployment problem | Founders / practice leadership — run Part 1 |
| 2 | **Wrong shape of person** | Either a two-tier genesis (cheap "solutions" people below elite product engineers) or a uniform competency ladder that grades everyone to the middle | CHRO / hiring manager — Part 7 |
| 3 | **The pair is a pyramid** | A program manager in the strategist seat; an approval layer between the person who understands the customer and the person who can change the software | COO / head of deployment — Part 4 |
| 4 | **The loop back to product is missing** | Field builds custom things; nothing changes on the roadmap; sprint lock; branches diverge; product has no customer context | Head of product — Part 5a |
| 5 | **Reusable assets with no owner and no bar** | Every pod builds "accelerators"; a year later none are in use; the bar was written after the build to describe the build | Platform / CoE lead — set the bar before the cohort builds; fund hardening |
| 6 | **The contract or the comp pays for attendance** | Work sold as FTE-months; finishing early destroys revenue; FDE comp tied to account revenue | CSO / CFO — Part 5b, Part 6 |
| 7 | **The badge goes everywhere** | Lighthouse accounts worked, so everyone got the title; the title became a promotion track within eighteen months | Practice leadership — the selection rule |
| 8 | **No hygiene, no leverage** | Repos everywhere, no PR review, no tests; AI tooling either banned by IT or used without discipline | CTO / platform — hygiene first, then leverage |

The services-firm version of this list is stated in *Five ways a forward-deployed motion fails inside a services firm*; modes 2, 3, 5, 6 and 7 are the same modes with different owners.

---

## Part 9 — How the Blueprint is used

The Blueprint is the ruler. It does not say what any specific company should do; it says what the questions are, in what order, and what good looks like at each stage. Applied to a real organisation it produces:

- a **maturity read** — where on Part 3 the product actually is, and whether the autonomy dial matches;
- a **red-line** of the company's own plan against Parts 1, 2, 4 and 5 — line by line, this is right, this is wrong, this is missing;
- **three risks and one recommendation** — which failure modes are live, and what the next ninety days should change.

That is the FDE Readiness Assessment. Everything Platypus sells is the Blueprint applied, with a written verdict.

---

*Attribution: The Platypus FDE Blueprint © Platypus Technologies Ltd, Anjor Kanekar. Licensed CC BY 4.0 — use it, adapt it, keep the name on it.*

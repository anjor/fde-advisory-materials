# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a documentation repository containing advisory materials for Forward Deployed Engineering (FDE) transformation. The repository focuses on providing comprehensive frameworks, playbooks, and guidance for organizations building or maturing FDE capabilities.

## Repository Structure

### Core Documents
- `README.md` - Brief repository introduction
- `framework.md` - High-level framework overview and navigation hub (v3.0)
- `CLAUDE.md` - This file, guidance for AI assistants
- `CHANGELOG.md` - Version history and changes
- `CONTRIBUTING.md` - Guidelines for content contributions
- `CROSS-REFERENCE-MAP.md` - Dependencies between practice areas

### Practice Area Folders (17 detailed guides)
- `people/` - 6 practice areas on human capital & talent
  - organizational-design.md
  - hiring-talent-strategy.md
  - training-career-development.md
  - change-management.md
  - geographic-distribution.md
  - community-knowledge-management.md
- `product/` - 4 practice areas on product & technical operations
  - product-fde-interface.md
  - technical-enablement.md
  - domain-expertise.md
  - failure-recovery-risk.md
- `commercial/` - 5 practice areas on revenue & market operations
  - commercial-model-gtm.md
  - customer-deployment-success.md
  - legal-contracts-ip.md
  - partner-ecosystem.md
  - competitive-positioning.md
- `operations/` - 2 practice areas on operating model & execution
  - operating-model-metrics.md
  - scaling-organization.md

### Templates Folder
- `templates/` - Ready-to-use templates organized by theme
  - `people/` - Hiring, onboarding, career templates
  - `product/` - Technical standards, documentation templates
  - `commercial/` - Contracts, pricing, customer success templates
  - `operations/` - Metrics, governance templates
  - `shared/` - Cross-cutting templates (RACI, stakeholder analysis)

## Key Concepts

### Forward Deployed Engineering (FDE)
FDEs are technical, client-facing engineers who solve customer problems by building on and extending product platforms. They differ from traditional consulting or staff augmentation roles by:
- Taking ownership of customer outcomes
- Contributing directly to product/platform development
- Working across the full technical stack
- Operating with high autonomy and pain tolerance

### The Four Pillars
The framework is built around four key organizational pillars:
1. **FDE Team** - Client-facing technical problem solvers
2. **Product Teams** - Core product development
3. **Platform Team** - Shared infrastructure and tools
4. **Commercial Team** - Sales and customer relationships

## Framework Structure

The main `framework.md` document covers 17 practice areas organized into themes:

### Foundational (Phase 1: Months 1-3)
1. Organizational Design & Structure
3. Hiring & Talent Strategy
5. Commercial Model & Go-to-Market
9. Change Management (spans phases)

### Operational (Phase 2: Months 4-6)
4. Training, Onboarding & Career Development
6. Product-FDE Interface
7. Technical Enablement & Standards
8. Customer Deployment & Success

### Scaling (Phase 3: Months 7-12)
2. Operating Model & Metrics
12. Scaling the FDE Organization
16. FDE Community & Knowledge Management

### Specialized/Advanced
10. Domain Expertise & Industry Specialization
11. Geographic Distribution & Remote Models
13. Failure Recovery & Risk Management
14. Legal, Contracts & IP Considerations
15. Partner & Ecosystem Coexistence
17. Competitive Positioning & Differentiation

## Working with This Repository

### Document Editing Guidelines

**For Practice Area Documents (in people/, product/, commercial/, operations/):**

1. **Maintain consistent structure** - Each practice area file follows this pattern:
   - Frontmatter (YAML metadata)
   - Title with TL;DR
   - Navigation links
   - "The Challenge" section
   - "Key Topics" with numbered subsections
   - "Implementation Guide" section
   - "Templates & Tools" section
   - "Real-World Examples" section
   - "Decision Trees" section
   - "Common Pitfalls" section
   - "Success Metrics" section
   - "Related Practices" section with cross-references

2. **File Naming Convention** - Use semantic slugs without numbers:
   - ✅ Good: `hiring-talent-strategy.md`
   - ❌ Bad: `03-hiring-talent-strategy.md`
   - Rationale: Easier to maintain, reorder, and reference

3. **Keep cross-references updated** - Use relative paths with arrow notation:
   - Format: `→ [Practice Area Name](../folder/file.md)`
   - Update CROSS-REFERENCE-MAP.md when adding new relationships
   - Update frontmatter `related_practices` metadata

4. **Preserve the advisory perspective** - Content is written for consultants/advisors helping organizations, not for practitioners implementing directly

5. **Status tracking** - Use frontmatter `status` field:
   - `draft` - Structure only, content incomplete
   - `in-progress` - Actively being written
   - `complete` - Fully fleshed out

**For framework.md (Navigation Hub):**

- `framework.md` is now a navigation document, not comprehensive content
- Keep practice area summaries to 3-4 lines
- Ensure all links to practice area files are correct
- Update "Getting Started" guides when adding new content

**For Templates:**

- Templates go in `templates/{theme}/` folders
- Use naming convention: `{purpose}-{type}.{extension}`
- Include "Purpose" and "When to Use" sections
- Mark incomplete templates with "🚧 Content In Progress"

### Content Philosophy

- **Practical over theoretical** - Focus on implementable guidance based on real-world patterns
- **Non-prescriptive** - Present options and trade-offs rather than single "right" answers
- **Context-dependent** - Acknowledge that optimal approaches vary by company stage, market, and product maturity
- **Battle-tested** - Framework reflects actual enterprise client engagement patterns

### Common Tasks

**Adding a new practice area:**
1. Create new file in appropriate theme folder (people/, product/, commercial/, operations/)
2. Use semantic slug naming (no numbers)
3. Copy skeleton structure from existing practice area
4. Fill in frontmatter metadata (number, theme, phase, stakeholders, related_practices)
5. Add to framework.md in appropriate theme section
6. Add to framework.md "Practice Area Summaries" section
7. Add to framework.md appendix table
8. Update CROSS-REFERENCE-MAP.md
9. Update CHANGELOG.md

**Expanding an existing practice area:**
1. Find the practice area file in its theme folder
2. Locate sections marked "🚧 Content In Progress"
3. Add content following the structure guidelines
4. Update `last_updated` date in frontmatter
5. Change `status` from "draft" to "in-progress" or "complete"
6. Ensure cross-references are accurate
7. Update CHANGELOG.md if significant changes

**Adding a new template:**
1. Determine which theme folder it belongs in (templates/people/, etc.)
2. Create file with naming convention: `{purpose}-{type}.{extension}`
3. Include Purpose, When to Use, and Template Structure sections
4. Reference from appropriate practice area documents
5. Add to templates/README.md quick reference

**Updating cross-references:**
1. Update practice area file frontmatter `related_practices`
2. Update "Related Practices" section in the document
3. Update CROSS-REFERENCE-MAP.md
4. Verify all relative links are correct

**Transforming placeholder content:**
1. Find sections with "🚧 Content In Progress"
2. Replace with 2-3 paragraphs of detailed guidance
3. Add examples, decision trees, or how-to steps as appropriate
4. Remove the placeholder banner
5. Update status in frontmatter if section is now complete

## Version Control

- Framework version is at bottom of framework.md (currently v3.0)
- Each practice area file has `last_updated` in frontmatter
- Update CHANGELOG.md for all significant changes
- Use semantic versioning:
  - Major (X.0.0): Significant restructuring
  - Minor (x.X.0): New content additions
  - Patch (x.x.X): Minor updates, corrections
- Commit messages should reference which files/practice areas were modified
- Use conventional commit format: `feat:`, `fix:`, `docs:`, `refactor:`

# Changelog

## [Unreleased]

---

## [MVP-1.3.1] - 2026-01-16

### Added
- Automated release preparation workflow via GitHub Actions
  - One-click release process through GitHub UI (Actions > Prepare Release)
  - Automatic version bumping (major/minor/patch/custom)
  - Automatic file updates across 5 version files
  - Automatic CHANGELOG update with release notes
  - Automatic git commit, tag creation, and GitHub Release creation

### Changed
- Release process reduced from ~5 minutes (manual) to ~1 minute (automated)
- Eliminated manual version editing across multiple files

---

## [MVP-1.3.0] - 2026-01-16

### Added
- FDE Metrics & Performance section in startup kit (00-fde-startup-kit.md)
  - Organizational metrics table: 5 key metrics with "Watch Out For" warnings
  - Individual FDE performance philosophy: Explains why subjective evaluation is intentional
  - Anti-patterns table: 4 metrics that seem reasonable but damage effectiveness
  - Customer-centric indicators: Leading signals for FDE impact
  - Incorporates insights from Palantir's evaluation model

### Changed
- Consolidated and replaced "Key Metrics (For Reference)" section with comprehensive metrics guidance
- Repositioned metrics content earlier in startup kit (after "Who Does What") for better flow

### Removed
- Simplified "Key Metrics (For Reference)" section (replaced by comprehensive Metrics & Performance section)

---

## [MVP-1.2.0] - 2026-01-16

### Added
- FDE Archetypes section in startup kit (00-fde-startup-kit.md)
  - Defined two archetypes: business-facing vs product-facing FDEs
  - Clear comparison table showing focus areas and responsibilities
  - Guidance on when to hire each archetype based on deployment maturity
  - Mapping of existing roles (solutions engineers, platform engineers, technical consultants) to FDE archetypes
  - Strategy for scaling: start with product-facing FDEs (0-10 deployments), add business-facing at scale (10+)

### Changed
- Updated startup kit structure to include archetype guidance before diving into hiring details

---

## [MVP-1.1.0] - 2026-01-15

### Added
- Further Reading sections to all three practice area documents (01, 02, 03) linking to blog posts
- New hiring thesis template (resources/people/hiring-thesis-template.md)
- FDE Mindset Indicators section in interview scorecard based on FDE Manifesto principles
- Scaling Note callout in hiring document to provide context for different hiring volumes

### Changed
- Generalized time references throughout documentation (removed specific dates like "Feb 2025" in favor of "target timeline")
- Updated mkdocs.yml navigation to include new hiring thesis template
- Interview scorecard enhanced with tactical evaluation criteria from FDE Manifesto

---

## [MVP-1.0.0] - 2026-01-06

### Major Transformation
Restructured from comprehensive 17-practice-area framework to focused MVP with 3 priority areas.

### Deleted
- All thematic folders (people/, product/, commercial/, operations/) containing 14 non-MVP practice areas
- framework.md (comprehensive navigation hub)
- CROSS-REFERENCE-MAP.md (referenced deleted content)
- CONTRIBUTING.md (described comprehensive framework contribution)
- Non-MVP templates (commercial/, operations/, shared/)

### Changed
- README.md: Rewritten to emphasize MVP scope, points to startup kit as entry point
- 00-fde-startup-kit.md: Updated resources section to remove references to deleted files
- mvp-priorities.md: Marked as "implemented", added "What We Did" section
- CLAUDE.md: Completely rewritten to reflect MVP structure

### Kept
- 00-fde-startup-kit.md (181 lines) - Primary entry point
- 01-hiring-talent-strategy.md (333 lines) - Hiring guidance
- 02-product-fde-interface.md (406 lines) - Product-FDE interface patterns
- 03-technical-enablement.md (423 lines) - Technical standards
- 4 MVP-relevant templates (people/3, product/1)

### Rationale
Based on actual field engagement (the organization Nov-Dec 2024), MVP focuses on burning problems:
- Need to hire initial FDE cohort within target timeline
- Product teams not delivering what FDEs need
- No documentation, scattered repos, FDEs can't work

Everything else deferred to future phases after real deployment data.

---

## Previous Versions

This MVP-focused repository is a transformation from a comprehensive framework. Previous version history was archived during the MVP transformation (2026-01-06).

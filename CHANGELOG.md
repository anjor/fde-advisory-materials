# Changelog

All notable changes to the FDE Advisory Services Framework will be documented in this file.

---

## [3.0.0] - 2026-01-05

### Major Restructuring: Thematic Organization

This release represents a significant expansion and reorganization of the FDE Advisory Framework from a single comprehensive document into a modular, theme-based documentation system.

### Added

**New Folder Structure:**
- `people/` - 6 practice areas focused on human capital and talent
- `product/` - 4 practice areas focused on product and technical operations
- `commercial/` - 5 practice areas focused on revenue and market operations
- `operations/` - 2 practice areas focused on operating model and execution
- `templates/` - Template placeholder files organized by theme

**New Practice Area Documents (17 total):**
- All 17 practice areas now have dedicated markdown files with:
  - Frontmatter metadata (original number, theme, phase, stakeholders, related practices)
  - Expanded structure with 11 standard sections
  - Placeholders for future content (Implementation Guide, Examples, Decision Trees, etc.)
  - Cross-references using relative paths

**Template Structure:**
- `templates/README.md` - Template usage guide
- `templates/people/` - People and talent templates
- `templates/product/` - Technical and product templates
- `templates/commercial/` - Commercial and contract templates
- `templates/operations/` - Operating model templates
- `templates/shared/` - Cross-cutting templates
- 9 key template placeholder files created

**Supporting Documentation:**
- `CROSS-REFERENCE-MAP.md` - Complete map of dependencies between practice areas
- `CHANGELOG.md` - This file, tracking version history
- `CONTRIBUTING.md` - Guidelines for expanding content

### Changed

**framework.md Transformation:**
- **From**: Single comprehensive document (1,055 lines) with all practice area details
- **To**: Navigation hub and quick reference with links to detailed documents
- Added "Quick Navigation by Theme" section with visual organization
- Added "Getting Started Guides" by company stage and pain point
- Condensed each practice area to 3-4 lines with prominent links to detailed guides
- Added "Detailed Guide" column to appendix quick reference table
- Updated version to 3.0

**Navigation Improvements:**
- Theme-based browsing (People, Product, Commercial, Operations)
- Pain-point-driven entry points
- Stage-based guidance (Early, Growth, Enterprise)
- Direct links from every section to detailed content

### Updated

**CLAUDE.md:**
- Added new folder structure documentation
- Updated file naming conventions
- Added cross-reference strategy guidance
- Updated document editing guidelines

**README.md:**
- Updated to reflect new thematic structure
- Added navigation guidance
- Links to framework.md as primary entry point

### Technical Details

**File Naming Convention:**
- Semantic slugs without numbers (e.g., `organizational-design.md` not `01-organizational-design.md`)
- Rationale: Easier to maintain, reorder, and reference

**Cross-Reference Strategy:**
- Frontmatter metadata tracks relationships
- Relative links with arrow notation (→) for visibility
- CROSS-REFERENCE-MAP.md for dependency tracking

**Status Tracking:**
- All practice area files: status = "draft"
- All template files: Placeholder with structure only
- Content expansion planned for future phases

### Migration Notes

**For Users of v2.0:**
- Old `framework.md` content is preserved in new practice area files
- All "The Challenge" sections ported verbatim
- All "Key Topics" ported with full bullet points
- "Deliverables Available" mapped to template links
- No content lost, only reorganized

**Link Updates Needed:**
- Any external links to `framework.md#section-name` should be updated
- New format: link to specific practice area files
- Example: Old: `framework.md#1-organizational-design` → New: `people/organizational-design.md`

### Future Phases (Not in This Release)

**Phase 2 - Content Expansion:**
- Expand "The Challenge" sections to 2-3 paragraphs
- Add implementation guides with step-by-step instructions
- Create 2-3 real-world examples per practice area
- Develop decision trees with ASCII diagrams
- Document 3-5 common pitfalls per practice area
- Define success metrics and maturity models

**Phase 3 - Template Development:**
- Create actual usable templates (job descriptions, contracts, scorecards)
- Add spreadsheet templates for calculators and assessments
- Develop workshop facilitation materials
- Create presentation templates

**Phase 4 - Polish:**
- Validate all cross-references and links
- Add automated link checking
- Comprehensive review and refinement
- Gather community feedback

---

## [2.0.0] - 2024-12-XX

### Initial Comprehensive Framework

- Single `framework.md` document with 17 practice areas
- Complete practice area descriptions with:
  - The Challenge
  - Key Topics (detailed bullet points)
  - Deliverables Available
- Engagement models and typical progression
- Key success factors
- Quick reference appendix table

---

## Version Numbering

This project uses [Semantic Versioning](https://semver.org/):
- **Major** (X.0.0): Significant restructuring or breaking changes
- **Minor** (x.X.0): New content additions, new practice areas
- **Patch** (x.x.X): Minor updates, corrections, clarifications

---

*For questions about changes or to suggest improvements, see [CONTRIBUTING.md](CONTRIBUTING.md)*

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a documentation repository containing MVP advisory materials for Forward Deployed Engineering (FDE) transformation. The repository focuses on 3 critical practice areas: Hiring & Talent Strategy, Product-FDE Interface, and Technical Enablement.

**Scope**: This is an MVP, not a comprehensive framework. Content covers immediate needs for organizations starting FDE programs.

## Repository Structure

This is a MkDocs-based documentation site. All content files are in the `docs/` directory.

### Core Documents (in docs/)
- `index.md` - Documentation site homepage
- `00-fde-startup-kit.md` - Primary entry point, quick reference guide
- `01-hiring-talent-strategy.md` - Comprehensive hiring guidance
- `02-product-fde-interface.md` - FDE-Product team interface patterns
- `03-technical-enablement.md` - Technical standards and enablement
- `mvp-priorities.md` - MVP scope and rationale
- `CHANGELOG.md` - Version history
- `CLAUDE.md` - This file, guidance for AI assistants

### Resources Folder (in docs/resources/)
- `resources/people/` - Hiring and onboarding templates (3 files)
  - job-description-fde.md
  - interview-scorecard.md
  - onboarding-checklist.md
- `resources/product/` - Product-FDE interface template (1 file)
  - interface-agreement-template.md

### Site Configuration
- `/mkdocs.yml` - MkDocs configuration (navigation, theme, plugins)
- `/pyproject.toml` - Python dependencies managed with uv
- `/.github/workflows/deploy-docs.yml` - Auto-deploy to GitHub Pages

## Key Concepts

### Forward Deployed Engineering (FDE)
FDEs are technical, client-facing engineers who solve customer problems by building on and extending product platforms. They differ from traditional consulting or staff augmentation roles by:
- Taking ownership of customer outcomes
- Contributing directly to product/platform development
- Working across the full technical stack
- Operating with high autonomy and pain tolerance

### MVP Philosophy

This repository intentionally limits scope to 3 areas:
1. **Hiring & Talent Strategy** - Immediate need to hire initial FDE cohort
2. **Product-FDE Interface** - Single biggest source of friction
3. **Technical Enablement** - FDEs can't work without this

Everything else is deferred until there's actual demand based on real deployments.

## Working with This Repository

### Document Editing Guidelines

**For Core Documents (00-, 01-, 02-, 03-):**

1. **Maintain consistent structure** - Each document follows this pattern:
   - Title with TL;DR
   - "The Challenge" section
   - Key topics with numbered subsections
   - Templates & tools references
   - Real-world examples
   - Common pitfalls
   - Success metrics

2. **File Naming Convention** - Use numbered prefixes for MVP:
   - ✅ Good: `01-hiring-talent-strategy.md`
   - Rationale: Numbers provide clear ordering (0=start, 1-3=priority areas)

3. **Preserve the advisory perspective** - Content is written for consultants/advisors helping organizations, not for practitioners implementing directly

4. **Status tracking** - Update version/date at bottom of files when making changes

**For Resources:**

- Resources go in `resources/{theme}/` folders (people/ or product/)
- Use naming convention: `{purpose}-{type}.{extension}`
- Include "Purpose" and "When to Use" sections

### Content Philosophy

- **Practical over theoretical** - Focus on implementable guidance based on real-world patterns
- **Non-prescriptive** - Present options and trade-offs rather than single "right" answers
- **Context-dependent** - Acknowledge that optimal approaches vary by company stage, market, and product maturity
- **Battle-tested** - Framework reflects actual enterprise client engagement patterns

### Common Tasks

**Expanding an existing priority area:**
1. Find the practice area file (01-, 02-, or 03-)
2. Locate sections that could be expanded
3. Add content following the structure guidelines
4. Update version/date at bottom of file

**Adding a new template:**
1. Determine which theme folder it belongs in (resources/people/ or resources/product/)
2. Create file with naming convention: `{purpose}-{type}.{extension}`
3. Include Purpose, When to Use, and Template Structure sections
4. Reference from appropriate practice area documents

**Updating cross-references:**
1. Update "Resources" section in 00-fde-startup-kit.md if needed
2. Verify all relative links are correct
3. Check that all referenced files still exist

## Version Control

- Version is in README.md (currently 1.0.0)
- Each core document file has version/date at bottom
- Update CHANGELOG.md for all significant changes
- Use semantic versioning:
  - Major (X.0.0): Significant restructuring
  - Minor (x.X.0): New content additions
  - Patch (x.x.X): Minor updates, corrections
- Commit messages should reference which files were modified
- Use conventional commit format: `feat:`, `fix:`, `docs:`, `refactor:`

## Release Process

To create a new release:

1. **Update version in files:**
   - `docs/CHANGELOG.md` - Add new version section with changes
   - Root `README.md` - Update "Current Version" and "Last Updated"

2. **Commit changes:**
   ```bash
   git add docs/CHANGELOG.md README.md
   git commit -m "docs: release X.Y.Z"
   ```

3. **Create and push version tag:**
   ```bash
   git tag vX.Y.Z
   git push origin main --tags
   ```

4. **GitHub Actions will automatically:**
   - Create GitHub Release with notes from CHANGELOG.md
   - Mark as "Latest release"
   - Notify watchers subscribed to releases

5. **Verify release at:** https://github.com/anjor/fde-advisory-materials/releases

**Note:** The release workflow (`.github/workflows/release.yml`) extracts release notes from `docs/CHANGELOG.md` based on the version tag. Ensure the CHANGELOG follows the format `## [X.Y.Z] - YYYY-MM-DD` for proper extraction.

## Important Notes

- This is an **MVP-only** repository - scope is intentionally limited to 3 areas
- Do not reference deleted content (framework.md, thematic folders, deferred practice areas)
- All documentation files are in the `docs/` directory - all internal links should be relative to this directory
- The startup kit (00-) is the primary entry point - keep it up to date
- Resources should be ready-to-use, not aspirational placeholders
- When making edits, edit files in `docs/` directory - changes auto-deploy via GitHub Actions

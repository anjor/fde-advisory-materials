# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a documentation repository: the public workbook under the Platypus FDE Blueprint. The Blueprint (`docs/blueprint.md`) is the front door and the framework; the repository then covers 4 practice areas — Hiring & Talent Strategy, Product-FDE Interface, Technical Enablement, and FDE Operating Models — plus runnable templates.

**Licensing:** everything under `docs/` is CC BY 4.0 (see `LICENSE-DOCS.md`); code, CI and site configuration are MIT (see `LICENSE`). Every practice-area doc and template carries a one-line attribution footer; keep it when editing, add it when creating.

**The line that must hold:** nothing tier-2 is ever added here — no calibrated interview exercises with rubrics, no decomposition prompts with what-good-looks-like, no scenario packs or injects, no assessment scoring method. Those are licensed to clients inside engagements. If a contribution contains any of them, it does not belong in this repository.

## Repository Structure

This is a MkDocs-based documentation site. All content files are in the `docs/` directory.

### Core Documents (in docs/)
- `index.md` - Documentation site homepage
- `blueprint.md` - The Platypus FDE Blueprint: the canonical, versioned copy of the framework and the front door to the site. platypustech.xyz/blueprint mirrors it; change it here first
- `00-fde-startup-kit.md` - Quick reference guide, the one-page version of the workbook
- `01-hiring-talent-strategy.md` - Comprehensive hiring guidance
- `02-product-fde-interface.md` - FDE-Product team interface patterns
- `03-technical-enablement.md` - Technical standards and enablement
- `04-fde-operating-models.md` - FDE operating models and day-to-day operations
- `CHANGELOG.md` - Version history
- `CLAUDE.md` - This file, guidance for AI assistants (excluded from the built site)
- `README.md` - GitHub-facing readme for the docs folder (excluded from the built site)

### Resources Folder (in docs/resources/)
- `resources/people/` - Hiring and onboarding templates (4 files)
  - job-description-fde.md
  - interview-scorecard.md
  - hiring-thesis-template.md
  - onboarding-checklist.md
- `resources/product/` - Product-FDE interface template (1 file)
  - interface-agreement-template.md
- `resources/operations/` - Operations templates (1 file)
  - operating-model-canvas.md

### Site Configuration
- `/mkdocs.yml` - MkDocs configuration (navigation, theme, plugins)
- `/pyproject.toml` - Python dependencies managed with uv; its `version` tracks the release version
- `/.github/workflows/deploy-docs.yml` - Auto-deploy to GitHub Pages
- `/LICENSE` - MIT, for code, CI and site configuration
- `/LICENSE-DOCS.md` - CC BY 4.0, for everything under `docs/`

## Key Concepts

### Forward Deployed Engineering (FDE)
Forward Deployed Engineering is a product R&D function dressed up as a delivery function (see `blueprint.md`, "The one-paragraph version"). FDEs are technical, client-facing engineers who solve customer problems by building on and extending product platforms. They differ from traditional consulting or staff augmentation roles by:
- Taking ownership of customer outcomes
- Contributing directly to product/platform development
- Working across the full technical stack
- Operating with high autonomy and pain tolerance

### Structure

The Blueprint is the framework (the "whether" and the "which path"); the practice areas are the "how":
1. **Hiring & Talent Strategy** - How to hire and evaluate FDEs
2. **Product-FDE Interface** - Managing FDE-Product team relationships
3. **Technical Enablement** - Minimum standards for FDE-ready products
4. **FDE Operating Models** - How to run the day-to-day of an FDE function

## Working with This Repository

### Document Editing Guidelines

**For Core Documents (00-, 01-, 02-, 03-, 04-):**

1. **Maintain consistent structure** - Each document follows this pattern:
   - Title with TL;DR
   - "The Challenge" section
   - Key topics with numbered subsections
   - Templates & tools references
   - Real-world examples
   - Common pitfalls
   - Success metrics

2. **File Naming Convention** - Use numbered prefixes for the workbook:
   - ✅ Good: `01-hiring-talent-strategy.md`
   - Rationale: Numbers provide clear ordering (0=start, 1-3=priority areas)

3. **Preserve the advisory perspective** - Content is written for consultants/advisors helping organizations, not for practitioners implementing directly

4. **Status tracking** - Update version/date at bottom of files when making changes

5. **Attribution footer** - Every practice-area doc and template ends with a horizontal rule and the line `*Part of the Platypus FDE Blueprint workbook · © Platypus Technologies · CC BY 4.0 · [platypustech.xyz](https://platypustech.xyz)*`. Keep it last in the file.

6. **Consistency with the Blueprint** - The practice areas give Path A (platform) defaults. Where a section could be read as contradicting the Blueprint, add a pointer to the relevant Part rather than rewriting the Blueprint

**For Resources:**

- Resources go in `resources/{theme}/` folders (people/, product/, or operations/)
- Use naming convention: `{purpose}-{type}.{extension}`
- Include "Purpose" and "When to Use" sections

### Content Philosophy

- **Practical over theoretical** - Focus on implementable guidance based on real-world patterns
- **Non-prescriptive** - Present options and trade-offs rather than single "right" answers
- **Context-dependent** - Acknowledge that optimal approaches vary by company stage, market, and product maturity
- **Battle-tested** - Framework reflects actual enterprise client engagement patterns

### Common Tasks

**Expanding an existing priority area:**
1. Find the practice area file (01-, 02-, 03-, or 04-)
2. Locate sections that could be expanded
3. Add content following the structure guidelines
4. Update version/date at bottom of file

**Adding a new template:**
1. Determine which theme folder it belongs in (resources/people/, resources/product/, or resources/operations/)
2. Create file with naming convention: `{purpose}-{type}.{extension}`
3. Include Purpose, When to Use, and Template Structure sections
4. Reference from appropriate practice area documents

**Updating cross-references:**
1. Update "Resources" section in 00-fde-startup-kit.md if needed
2. Verify all relative links are correct
3. Check that all referenced files still exist

## Version Control

- Version lives in five places that must agree: root `README.md`, `docs/README.md`, `docs/index.md` ("Current version"), the footer of `docs/00-fde-startup-kit.md`, and `pyproject.toml` (run `uv lock` after changing it). `docs/CHANGELOG.md` carries the entry
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
   - Root `README.md` and `docs/README.md` - Update "Current Version" and "Last Updated"
   - `docs/index.md` - Update "Current version" line
   - `docs/00-fde-startup-kit.md` - Update the version footer
   - `pyproject.toml` - Update `version`, then run `uv lock`

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

- The Blueprint (`blueprint.md`) is the front door; the startup kit (00-) is the quick reference. Keep both current
- Do not reference deleted content (framework.md, mvp-priorities.md, old thematic folders)
- All documentation files are in the `docs/` directory - all internal links should be relative to this directory
- Resources should be ready-to-use, not aspirational placeholders
- When making edits, edit files in `docs/` directory - changes auto-deploy via GitHub Actions

# Contributing to FDE Advisory Materials

Thank you for your interest in improving the FDE Advisory Framework! This guide will help you contribute effectively.

---

## How to Contribute

### 1. Content Expansion

**Current State (Phase 1):**
The framework has skeletal structure with placeholders. We need help filling in:

- **Implementation Guides**: Step-by-step instructions for each practice area
- **Real-World Examples**: Anonymized case studies showing successful implementations
- **Decision Trees**: Visual guides for key decisions
- **Common Pitfalls**: Anti-patterns and how to avoid them
- **Success Metrics**: Measurable indicators of progress

**To Contribute Content:**
1. Pick a practice area file (e.g., `people/hiring-talent-strategy.md`)
2. Find a section marked "🚧 Content In Progress"
3. Expand that section with 2-3 paragraphs or detailed guidance
4. Anonymize any client-specific information
5. Submit a pull request

### 2. Template Development

We need actual usable templates that FDE organizations can download and use.

**Priority Templates:**
- Job descriptions for FDE roles (Associate, Senior, Staff, Principal)
- Interview scorecards and evaluation rubrics
- Onboarding checklists and training curricula
- Contract templates (MSA, SOW)
- Metrics dashboards and scorecards
- RACI matrices and stakeholder analysis

**Template Guidelines:**
- Make them generic enough to customize
- Include instructions/annotations
- Use markdown for documents, consider Excel/Sheets for calculators
- Follow naming convention: `{purpose}-{type}.{extension}`

### 3. Examples and Case Studies

**What Makes a Good Example:**
- Specific, concrete scenario (not generic)
- Clear before/after or challenge/solution structure
- Quantifiable outcomes where possible
- Anonymized to protect client confidentiality
- 300-500 words (not too long)

**Example Template:**
```markdown
### Example: [Company Type/Stage] - [Scenario]

**Context:** [2-3 sentences setting up the situation]

**Challenge:** [Specific problem they faced]

**Approach:** [What they did - 3-5 steps]

**Outcome:** [Results achieved - be specific]

**Key Takeaways:**
- [Lesson 1]
- [Lesson 2]
- [Lesson 3]
```

### 4. Corrections and Improvements

Found a typo, broken link, or unclear explanation?

- Small fixes: Direct PR welcome
- Larger changes: Open an issue first to discuss

---

## Document Structure Standards

### Practice Area Documents

Each practice area file must follow this structure:

1. **Frontmatter** - YAML metadata (title, number, theme, phase, etc.)
2. **Title & TL;DR** - Brief summary
3. **Navigation** - Internal document links
4. **The Challenge** - Problem statement
5. **Key Topics** - Core content sections
6. **Implementation Guide** - How-to section
7. **Templates & Tools** - Links to resources
8. **Real-World Examples** - Case studies
9. **Decision Trees** - Visual decision guides
10. **Common Pitfalls** - What to avoid
11. **Success Metrics** - Measurement frameworks
12. **Related Practices** - Cross-references

**Don't Change:**
- Frontmatter structure
- Section headings (keep consistent)
- Relative link formats

**Do Change:**
- Content within sections
- Add detail and examples
- Improve clarity

### Template Files

Templates should include:

1. **Header** - "🚧 Content In Progress" if placeholder
2. **Purpose** - What this template is for
3. **When to Use** - Scenarios where it applies
4. **Template Structure** - The actual template
5. **Instructions** - How to customize/use it

### Markdown Formatting

- Use `**bold**` for emphasis
- Use `> 🚧 **Content In Progress**` for placeholders
- Use `→` for cross-reference links
- Use relative paths for all internal links
- Use `[Text](path/to/file.md#section)` for links with anchors

---

## Cross-Reference Management

### When Adding Cross-References:

1. **Update Frontmatter**:
   ```yaml
   related_practices:
     prerequisites: ["other-practice-slug"]
     complementary: ["related-practice-slug"]
     downstream: ["enabled-practice-slug"]
   ```

2. **Add to "Related Practices" Section**:
   ```markdown
   ### Prerequisites
   - **→ [Practice Name](relative/path.md)** - Why this comes first
   ```

3. **Update CROSS-REFERENCE-MAP.md**:
   Add the new relationship to the appropriate section

### Link Format:
- Always use relative paths: `../folder/file.md`
- Include section anchors where relevant: `file.md#section-name`
- Use arrow notation for visibility: `→ [Link Text](path.md)`

---

## Git Workflow

### For Small Changes (typos, minor edits):
1. Fork the repository
2. Create a branch: `git checkout -b fix-typo-in-hiring`
3. Make your changes
4. Commit: `git commit -m "Fix typo in hiring strategy document"`
5. Push and create a pull request

### For Larger Changes (new content, major revisions):
1. Open an issue first to discuss the approach
2. Get feedback before investing significant time
3. Follow the same git workflow as above
4. Reference the issue in your PR

### Branch Naming:
- `fix/*` - Bug fixes, typos, broken links
- `content/*` - Content expansion, new sections
- `template/*` - New templates or template improvements
- `docs/*` - Documentation improvements

### Commit Messages:
- Keep under 72 characters
- Start with verb (Add, Update, Fix, Remove)
- Be specific: "Add implementation guide to hiring strategy" not "Update docs"

---

## Content Guidelines

### Voice and Tone:
- **Practical over theoretical** - Focus on implementable guidance
- **Non-prescriptive** - Present options and trade-offs, not single "right" answers
- **Context-dependent** - Acknowledge that approaches vary by company stage and situation
- **Advisory perspective** - Written for consultants helping organizations, not practitioners implementing directly

### Writing Style:
- Use active voice
- Keep sentences concise
- Use bullet points for lists
- Avoid jargon unless necessary (and define it if used)
- Write in second person ("you") or third person ("organizations")

### Confidentiality:
- **Always anonymize** client names, specific products, proprietary data
- Use generic descriptors: "A Series B SaaS company" not "Acme Corp"
- Remove identifying details that could reveal client identity
- When in doubt, generalize further

---

## Review Process

### What Reviewers Look For:
1. **Accuracy** - Is the information correct?
2. **Clarity** - Is it easy to understand?
3. **Completeness** - Does it cover the key points?
4. **Consistency** - Does it match existing style and structure?
5. **Links** - Are all internal links working?
6. **Confidentiality** - Is all client information anonymized?

### Pull Request Guidelines:
- Describe what you changed and why
- Reference any related issues
- Tag sections with "🚧 Content In Progress" if incomplete
- Request review from maintainers
- Be responsive to feedback

---

## Questions or Ideas?

- **For questions**: Open a discussion in GitHub Discussions
- **For bug reports**: Open an issue with the "bug" label
- **For feature requests**: Open an issue with the "enhancement" label
- **For general chat**: Reach out to maintainers

---

## Recognition

Contributors will be recognized in:
- GitHub contributors list
- A CONTRIBUTORS.md file (coming in future release)
- Acknowledgment in documentation for significant contributions

---

## License

By contributing, you agree that your contributions will be licensed under the same license as this project (to be determined).

---

*Thank you for helping make the FDE Advisory Framework more valuable for the community!*

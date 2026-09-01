# FDE Advisory Materials

The Platypus FDE Blueprint, and the open workbook beneath it.

📚 **[View the Documentation Site](https://anjor.github.io/fde-advisory-materials/)**

## About

This repository is the public workbook under the [Platypus FDE Blueprint](https://anjor.github.io/fde-advisory-materials/blueprint/) — a framework for deciding whether a company needs Forward Deployed Engineers, which of two paths its FDE function is on, and how to design, staff and measure it. The Blueprint is the front door; the rest is the "how":

1. **Hiring & Talent Strategy** - How to hire and evaluate FDEs
2. **Product-FDE Interface** - Managing FDE-Product team relationships
3. **Technical Enablement** - Minimum standards for FDE-ready products
4. **FDE Operating Models** - How to run the day-to-day of an FDE function
5. **Templates** - Job descriptions, interview scorecard, hiring thesis, onboarding checklist, interface agreement, operating-model canvas

What is deliberately *not* here: calibrated interview exercises and rubrics, decomposition prompts with what-good-looks-like, scenario packs, and the assessment scoring method. Those are licensed to clients inside [Platypus Technologies](https://platypustech.xyz) engagements. See [What is here, and what is not](https://anjor.github.io/fde-advisory-materials/#what-is-here-and-what-is-not).

## Development

This site is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

### Local Development

```bash
# Install dependencies (requires uv)
uv sync

# Serve locally
uv run mkdocs serve

# Build static site
uv run mkdocs build --strict
```

Visit http://127.0.0.1:8000 to preview the site locally.

### Project Structure

```
.
├── docs/                    # Documentation source files (CC BY 4.0)
│   ├── index.md            # Homepage
│   ├── blueprint.md        # The Platypus FDE Blueprint — the front door
│   ├── 00-fde-startup-kit.md
│   ├── 01-hiring-talent-strategy.md
│   ├── 02-product-fde-interface.md
│   ├── 03-technical-enablement.md
│   ├── 04-fde-operating-models.md
│   ├── resources/          # Template files
│   └── ...
├── mkdocs.yml              # MkDocs configuration (MIT)
├── pyproject.toml          # Python dependencies (MIT)
├── LICENSE                 # MIT — code, CI and site configuration
└── LICENSE-DOCS.md         # CC BY 4.0 — everything under docs/
```

## Contributing

All documentation files are located in the `docs/` directory. To contribute:

1. Edit markdown files in `docs/`
2. Test locally with `uv run mkdocs serve`
3. Submit a pull request

See [docs/CLAUDE.md](docs/CLAUDE.md) for detailed contribution guidelines.

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch. The deployment is handled by GitHub Actions (see `.github/workflows/deploy-docs.yml`).

## License

- **Documentation** — everything under `docs/`, including the Blueprint, the practice areas, the templates and the images — is licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Use it, adapt it, keep the name on it. Attribution: *The Platypus FDE Blueprint © Platypus Technologies, Anjor Kanekar — CC BY 4.0 — https://platypustech.xyz*. See [LICENSE-DOCS.md](LICENSE-DOCS.md).
- **Code, CI and site configuration** (`mkdocs.yml`, `pyproject.toml`, `.github/`, scripts) remain under the [MIT License](LICENSE).
- Copies of the documentation distributed under MIT before v1.5.0 remain under MIT.

## Version

**Current Version**: 1.5.0
**Last Updated**: September 1, 2026

See [docs/CHANGELOG.md](docs/CHANGELOG.md) for version history.

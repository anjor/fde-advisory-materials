# FDE Advisory Materials

Documentation site for Forward Deployed Engineering advisory materials.

📚 **[View the Documentation Site](https://anjor.github.io/fde-advisory-materials/)**

## About

This repository contains practical guidance for organizations building Forward Deployed Engineering (FDE) capabilities. The documentation covers three critical areas:

1. **Hiring & Talent Strategy** - How to hire and evaluate FDEs
2. **Product-FDE Interface** - Managing FDE-Product team relationships
3. **Technical Enablement** - Minimum standards for FDE-ready products

## Development

This site is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

### Local Development

```bash
# Install dependencies (requires uv)
uv sync

# Serve locally
uv run mkdocs serve

# Build static site
uv run mkdocs build
```

Visit http://127.0.0.1:8000 to preview the site locally.

### Project Structure

```
.
├── docs/                    # Documentation source files
│   ├── index.md            # Homepage
│   ├── 00-fde-startup-kit.md
│   ├── 01-hiring-talent-strategy.md
│   ├── 02-product-fde-interface.md
│   ├── 03-technical-enablement.md
│   ├── templates/          # Template files
│   └── ...
├── mkdocs.yml              # MkDocs configuration
└── pyproject.toml          # Python dependencies
```

## Contributing

All documentation files are located in the `docs/` directory. To contribute:

1. Edit markdown files in `docs/`
2. Test locally with `uv run mkdocs serve`
3. Submit a pull request

See [docs/CLAUDE.md](docs/CLAUDE.md) for detailed contribution guidelines.

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch. The deployment is handled by GitHub Actions (see `.github/workflows/deploy-docs.yml`).

## Version

**Current Version**: MVP-1.0.0
**Last Updated**: January 14, 2026

See [docs/CHANGELOG.md](docs/CHANGELOG.md) for version history.

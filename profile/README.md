# Project Mambo

<p align="left">
  <a href="https://github.com/ProjectMambo"><img src="https://img.shields.io/badge/GitHub-ProjectMambo-181717?style=flat-square&logo=github" alt="Project Mambo on GitHub" /></a>
  <img src="https://img.shields.io/badge/Projects-7-7a5fff?style=flat-square" alt="Seven Project Mambo projects" />
  <img src="https://img.shields.io/badge/Maintenance-Active-brightgreen?style=flat-square" alt="Maintenance status: active" />
</p>
<p align="left">
  <a href="https://projectmambo.org/"><img src="https://img.shields.io/badge/Wiki-Live-brightgreen?style=flat-square" alt="Project Mambo Wiki: live" /></a>
  <a href="https://kohkohnut.org/"><img src="https://img.shields.io/badge/Portfolio-Live-brightgreen?style=flat-square" alt="MamboFolio portfolio: live" /></a>
</p>

Project Mambo is a seven-project personal software and design ecosystem spanning Linux configuration, shared colour and font assets, finance tooling, a Markdown-first static-site platform, a portfolio, and a documentation wiki.

## Start here

| Goal | Link |
|---|---|
| Read Project Mambo documentation | [projectmambo.org](https://projectmambo.org/) |
| Visit Solomon's portfolio | [kohkohnut.org](https://kohkohnut.org/) |
| Browse all repositories | [github.com/ProjectMambo](https://github.com/ProjectMambo) |
| Build a Markdown-first site | [MamboSite](https://github.com/ProjectMambo/MamboSite) |

## Current status

MamboFolio is live on the MamboSite runtime. MamboWiki's public domain is live, while its MamboSite-backed documentation build has passed local validation and is awaiting manual review before deployment. The remaining projects are maintained independently and document their own implementation and maturity in their repositories.

## Projects

- **[MamboColour](https://github.com/ProjectMambo/MamboColour)** — colour palette definitions and generators for supported application formats.
- **[MamboDot](https://github.com/ProjectMambo/MamboDot)** — GNU Stow-managed Arch Linux and Hyprland desktop configuration.
- **[MamboFinance](https://github.com/ProjectMambo/MamboFinance)** — privacy-focused finance tracking software under active development.
- **[MamboFolio](https://github.com/ProjectMambo/MamboFolio)** — Solomon's Markdown-first portfolio, live at [kohkohnut.org](https://kohkohnut.org/).
- **[MamboFont](https://github.com/ProjectMambo/MamboFont)** — a custom monospace font project with icon glyphs.
- **[MamboSite](https://github.com/ProjectMambo/MamboSite)** — the Rust, TypeScript, React, and Next.js platform that compiles Project Mambo's Markdown websites.
- **[MamboWiki](https://github.com/ProjectMambo/MamboWiki)** — the documentation website for the projects' canonical docs at [projectmambo.org](https://projectmambo.org/); its MamboSite migration is under review.

## How the pieces fit

```text
canonical Project Mambo docs
    -> sync_docs.js
    -> repository documentation snapshots
    -> MamboWiki project mounts

MamboSite
    -> MamboFolio static export
    -> MamboWiki static export (migration under review)
    -> GitHub Pages

MamboColour + MamboFont
    -> shared visual assets where each project adopts them
```

Each repository remains independently versioned and owns its implementation, setup instructions, release status, and licence. MamboSite supplies the shared website compiler and runtime; it does not own the source code of the sites it builds.

## Documentation workflow

Project documentation is authored centrally in the Project Mambo Obsidian vault. `Scripts/sync_docs.js` exports the relevant canonical tree to each repository's `docs/` directory and root `README.md`. MamboWiki receives the same project trees as explicit mounts, so repository documentation and the public wiki come from one authored copy.

Synchronized repository docs are snapshots rather than the authoring source. Changes should be made in the canonical vault files, synchronized, validated in the destination repository, and then committed there.

## Community and feedback

Project Mambo is a personal organisation and is not currently requesting external pull requests. Bug reports and focused suggestions are welcome in the repository that owns the affected behavior:

- Report palette or generated-format issues to MamboColour.
- Report desktop configuration, command, or keybinding issues to MamboDot.
- Report website compiler or renderer issues to MamboSite.
- Report portfolio or wiki content and deployment issues to the corresponding site repository.

## Licensing

Licensing is defined per repository rather than once for the organisation. Check the licence files in the relevant project before using or redistributing its code or assets.

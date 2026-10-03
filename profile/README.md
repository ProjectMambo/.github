# Project Mambo

<p align="left">
  <a href="https://github.com/ProjectMambo"><img src="https://img.shields.io/badge/GitHub-ProjectMambo-181717?style=flat-square&logo=github" alt="Project Mambo on GitHub" /></a>
  <img src="https://img.shields.io/badge/Projects-11-7a5fff?style=flat-square" alt="Eleven Project Mambo projects" />
  <img src="https://img.shields.io/badge/Maintenance-Active-brightgreen?style=flat-square" alt="Maintenance status: active" />
</p>
<p align="left">
  <a href="https://projectmambo.org/"><img src="https://img.shields.io/badge/Wiki-Live-brightgreen?style=flat-square" alt="Project Mambo Wiki: live" /></a>
  <a href="https://kohkohnut.org/"><img src="https://img.shields.io/badge/Portfolio-Live-brightgreen?style=flat-square" alt="MamboFolio portfolio: live" /></a>
</p>

Project Mambo is an eleven-project personal software and design ecosystem. It combines shared standards and tooling, Linux and finance applications, a reusable design system, a Markdown-first site platform, a portfolio, and a documentation wiki.

## Start here

| Goal | Link |
|---|---|
| Read Project Mambo documentation | [projectmambo.org](https://projectmambo.org/) |
| Visit Solomon's portfolio | [kohkohnut.org](https://kohkohnut.org/) |
| Browse all repositories | [github.com/ProjectMambo](https://github.com/ProjectMambo) |
| Build a Markdown-first site | [MamboSite](https://github.com/ProjectMambo/MamboSite) |

## Current status

MamboFolio and MamboWiki are live on the MamboSite runtime at their public domains. The remaining projects are maintained independently and document their own implementation and maturity in their repositories.

## Projects

### Foundation and developer tooling

| Project | Purpose | Documentation |
|---|---|---|
| **[MamboDocs](https://github.com/ProjectMambo/MamboDocs)** | Shared repository, documentation, interface, lifecycle, and delivery standards. | [Wiki](https://projectmambo.org/mambodocs/) |
| **[MamboTools](https://github.com/ProjectMambo/MamboTools)** | Central terminal manager for installing, updating, and removing Mambo repositories. | [Wiki](https://projectmambo.org/mambotools/) |
| **[MamboSite](https://github.com/ProjectMambo/MamboSite)** | Rust, TypeScript, React, and Next.js platform that compiles Markdown websites. | [Wiki](https://projectmambo.org/mambosite/) |

### Applications and environments

| Project | Purpose | Documentation |
|---|---|---|
| **[MamboDot](https://github.com/ProjectMambo/MamboDot)** | GNU Stow-managed Arch Linux and Hyprland desktop configuration. | [Wiki](https://projectmambo.org/mambodot/) |
| **[MamboFinance](https://github.com/ProjectMambo/MamboFinance)** | Privacy-focused personal finance tracking software. | [Wiki](https://projectmambo.org/mambofinance/) |
| **[MamboMeme](https://github.com/ProjectMambo/MamboMeme)** | Rust and Python tooling for processing, searching, previewing, and selecting memes. | [Wiki](https://projectmambo.org/mambomeme/) |

### Design system and assets

| Project | Purpose | Documentation |
|---|---|---|
| **[MamboColour](https://github.com/ProjectMambo/MamboColour)** | Colour palette definitions and generators for supported application formats. | [Wiki](https://projectmambo.org/mambocolour/) |
| **[MamboFont](https://github.com/ProjectMambo/MamboFont)** | Custom monospace font family with icon glyphs. | [Wiki](https://projectmambo.org/mambofont/) |
| **[MamboUI](https://github.com/ProjectMambo/MamboUI)** | Shared Ratatui components and visual conventions for Mambo terminal interfaces. | [Wiki](https://projectmambo.org/mamboui/) |

### Published sites

| Project | Purpose | Live site |
|---|---|---|
| **[MamboFolio](https://github.com/ProjectMambo/MamboFolio)** | Solomon's Markdown-first portfolio. | [kohkohnut.org](https://kohkohnut.org/) |
| **[MamboWiki](https://github.com/ProjectMambo/MamboWiki)** | MamboSite-powered public documentation for the complete ecosystem. | [projectmambo.org](https://projectmambo.org/) |

## How the pieces fit

```text
canonical Project Mambo docs
    -> sync_docs.js
    -> repository documentation snapshots
    -> MamboWiki project mounts

MamboSite
    -> MamboFolio static export
    -> MamboWiki static export
    -> GitHub Pages

MamboColour + MamboFont
    -> shared visual assets where each project adopts them

MamboDocs
    -> shared repository and delivery standards
    -> reusable Codex workflow and checks

MamboUI
    -> shared Ratatui components
    -> MamboTools and future terminal applications

MamboTools
    -> install, update, and remove Project Mambo repositories
```

Each repository remains independently versioned and owns its implementation, setup instructions, release status, and licence. MamboSite supplies the shared website compiler and runtime; it does not own the source code of the sites it builds.

## Documentation workflow

Project documentation is authored centrally in the Project Mambo Obsidian vault. `Scripts/sync_docs.js` exports the relevant canonical tree to each repository's `docs/` directory and root `README.md`. MamboWiki receives the same project trees as explicit mounts, so repository documentation and the public wiki come from one authored copy.

Synchronized repository docs are snapshots rather than the authoring source. Changes should be made in the canonical vault files, synchronized, validated in the destination repository, and then committed there.

## Community and feedback

Project Mambo is a personal organisation and is not currently requesting external pull requests. Bug reports and focused suggestions are welcome in the repository that owns the affected behavior:

- Report palette or generated-format issues to MamboColour.
- Report desktop configuration, command, or keybinding issues to MamboDot.
- Report meme corpus, retrieval, or interface issues to MamboMeme.
- Report repository management issues to MamboTools.
- Report shared terminal component or theme issues to MamboUI.
- Report website compiler or renderer issues to MamboSite.
- Report portfolio or wiki content and deployment issues to the corresponding site repository.

## Licensing

Licensing is defined per repository rather than once for the organisation. Check the licence files in the relevant project before using or redistributing its code or assets.

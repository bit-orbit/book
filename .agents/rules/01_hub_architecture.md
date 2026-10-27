# Architecture & Repository Structure: Hub & Submodules

## 1. Overview
This repository serves as the **Central Hub and Web Portal** for an open-source technical book translation initiative (primarily focused on DevOps, Cloud-Native, Systems, and Software Engineering into Persian).

## 2. The Hub and Submodule Model
To prevent repository bloat and maintain modularity, individual books are NOT monolithic subfolders inside a single Git history. Instead:
- **Hub Repository (`book/`):** Hosts the Hugo static site generator, landing portal, global styling, search, unified reading experience, and centralized metadata.
- **Book Submodules (`books/<book-slug>/`):** Each translated technical book is maintained in its own dedicated Git repository and linked to this hub as a **Git Submodule**.

### Directory Layout
```text
book/ (Hub Repository)
├── .agents/                      # AI rules, instructions, and translation skills
│   ├── rules/                   # Granular behavioral and technical rules
│   └── skills/                  # Procedural workflows for book translation
├── content/
│   ├── _index.md                # Portal landing page content
│   └── books/                   # Book catalog entries and web-readable content
├── books/                       # Git Submodules for individual books
│   └── the-kubernetes-book-2025 # Linked Git Submodule for Kubernetes book
├── layouts/                     # Hugo templates (RTL, responsive, dark mode)
├── static/                      # Static assets (CSS, JS, logos, icons)
├── AGENTS.md                    # Primary AI entry point & system instructions
├── ARCHITECTURE.md              # Deep technical architecture documentation
└── hugo.toml                    # Hugo site configuration
```

## 3. Submodule Responsibilities
Each individual book repository MUST contain:
1. `book.typ` and `template.typ`: Typst source code for rendering the print-ready PDF.
2. `chapters/`: Individual chapters named sequentially (e.g., `00_preface.typ`, `01_primer.typ`, ...).
3. `images/`: High-resolution figures and architectural diagrams.
4. `fonts/`: Standard Persian fonts (primarily Vazirmatn in all weights).
5. `todo.md`: Phased translation checklist (with the mandatory final Review phase).
6. `GEMINI.md` / `AGENTS.md`: Book-level AI guidance adhering to the hub's terminology rules.

## 4. AI Interaction Protocols
When working inside the Hub:
- Do NOT directly duplicate entire book PDF binaries in the hub's Git tree. PDFs are built via CI/CD and hosted on GitHub Releases.
- When adding a new book, initialize it as a new submodule under `books/<book-slug>` and create a corresponding metadata markdown file under `content/books/<book-slug>.md`.

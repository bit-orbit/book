# Workflow & Mandatory Phased Execution (todo.md)

## 1. Mandatory `todo.md` Creation
Whenever an AI agent or contributor initiates work on a new book (or resumes work on an existing book submodule), they **MUST** inspect or generate a comprehensive `todo.md` file in the root of the book repository.

The `todo.md` acts as the single source of truth for project tracking, verification status, and quality control.

## 2. Phase-Based Structure
The `todo.md` must divide the book into logical, sequential phases. A standard blueprint consists of:
- **Phase 0: Infrastructure & Typesetting Setup**
  - Font downloads (Vazirmatn), Typst `template.typ` validation, RTL verification, code block themes.
- **Phase 1 to N: Thematic Chapter Groups**
  - Group 3 to 4 cohesive chapters per phase (e.g., Foundations, Networking, Storage, Security).
  - List each chapter, its subtitle, and key technical concepts to be interpreted.
- **CRITICAL REQUIREMENT - FINAL PHASE MUST BE REVIEW:**
  - **The final phase of any book project MUST ALWAYS be the Review Phase (`فاز بازبینی و تضمین کیفیت نهایی`).**
  - A project CANNOT be marked complete until all items in this final review phase are checked.

## 3. Mandatory Checklist for the Final Review Phase
The final Review phase in `todo.md` must explicitly test and verify:
1. **Terminology Audit:**
   - Full grep search across all chapters for forbidden literal translations (e.g., `مقیاس` instead of `اسکیل`, `استقرار` instead of `دیپلوی`).
   - Consistency of Developer Persian loanwords and compound verbs.
2. **Typesetting & Compilation Integrity:**
   - Execute `typst compile --font-path fonts book.typ <output>.pdf` with ZERO errors and ZERO unknown font warnings.
   - Verify proper page breaks (`#pagebreak()`) between chapters.
   - Ensure table of contents (TOC), figure captions, and headers/footers render symmetrically in RTL.
3. **Glossary & Reference Completeness:**
   - Confirm the book includes a comprehensive, bilingual technical glossary (فصل واژه‌نامه تخصصی).
   - Ensure all official links, certifications, and GitHub companion repos are verified.
4. **Hub Synchronization:**
   - Verify the submodule commit hash is updated in the Hub repository.
   - Confirm the corresponding Hugo metadata entry (`content/books/<book>.md`) reflects the updated page count and release download link.

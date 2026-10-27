# AI Agent Instructions & Repository Guidelines

Welcome to the **Technical Book Translation Hub** repository. This document defines the operating rules, architectural patterns, and workflow protocols for any AI agent working on this ecosystem.

---

## 1. Core Architecture (Hub & Submodules)
- **Hub Repository (`book/`):** Hosts the Hugo static site, web portal, landing page, and catalog.
- **Book Submodules (`books/<slug>/`):** Each translated technical book is maintained in its own dedicated Git repository as a Git Submodule.
- **Rule Reference:** See [01_hub_architecture.md](.agents/rules/01_hub_architecture.md).

---

## 2. Translation & Interpretation Rules (Developer Persian)
1. **NEVER translate literally (پرهیز کامل از ترجمه تحت‌اللفظی):**
   - Translate conceptually and interpretively. Explain the engineering logic, trade-offs, and mental models as an experienced Senior Engineer.
2. **Preserve Book Structure:**
   - Retain the exact chapter order, section numbering, diagrams, code blocks, and callouts (`note`, `tip`, `warning`, `concept`).
3. **Developer Persian Terminology:**
   - Standard software engineering and DevOps terms MUST NOT be translated into awkward literal Persian words.
   - Use accepted technical terms or transliterations:
     - `Scale / Scaling` -> **اسکیل / اسکیل کردن / اسکیل‌پذیری (Scaling)** (NEVER use `مقیاس` for workload capacity!)
     - `Deploy / Deployment` -> **دیپلوی کردن / دیپلویمنت (Deployment)**
     - `Rollout / Rolling Update` -> **رولینگ آپدیت (Rolling Update) / انتشار تدریجی**
     - `Rollback` -> **رول‌بک (Rollback)**
     - `Pipeline` -> **پایپ‌لاین (Pipeline)**
     - `Cache` -> **کش / کش کردن (Cache)**
     - `Trace` -> **تریس / تریس کردن (Trace / Tracing)**
     - `Pod` -> **پاد (Pod)**
     - `Namespace` -> **نیم‌اسپیس (Namespace)**
     - `Ingress` -> **اینگرس (Ingress)**
     - `Worker / Node` -> **ورکر (Worker) / نود (Node)**
   - Rule Reference: See [03_developer_persian_terminology.md](.agents/rules/03_developer_persian_terminology.md).

---

## 3. Mandatory Phased Execution (`todo.md`)
Whenever starting or resuming work on a book:
1. Always maintain a phased `todo.md` in the book submodule root.
2. Group chapters into sequential phases (Phase 0: Infrastructure, Phase 1: Basics, etc.).
3. **MANDATORY REQUIREMENT:** The final phase MUST ALWAYS be a **Review & Quality Assurance Phase (`فاز بازبینی و تضمین کیفیت نهایی`)** consisting of:
   - Terminology audit (grep for forbidden terms like `مقیاس`, `استقرار دادن`, `حافظه پنهان`).
   - Typst compilation verification with zero errors and zero font warnings.
   - Structural & figure numbering checks.
   - Complete technical glossary check.
- Rule Reference: See [04_todo_and_lifecycle_workflow.md](.agents/rules/04_todo_and_lifecycle_workflow.md).

---

## 4. Skills & Automated Workflows
For detailed step-by-step procedures, invoke the [technical-book-translation](.agents/skills/technical-book-translation/SKILL.md) skill.

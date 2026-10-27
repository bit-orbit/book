# Translation Philosophy & Structural Integrity

## 1. Interpretive Translation vs. Literal Translation
The single most critical rule of this initiative is:
**NEVER PERFORM WORD-FOR-WORD OR LITERAL TRANSLATION (ترجمه تحت‌اللفظی).**

### Guiding Principles:
- **Conceptual Depth (تفسیر و بازنویسی مفهومی):** Understand the engineering rationale behind the original author's words, then re-explain the concept in fluent, natural Persian as an experienced Senior Engineer explaining to fellow practitioners.
- **Mental Models & Architecture:** Clarify *why* an architectural choice was made, not just *what* the author typed. Add brief engineering insights (e.g., using `#concept[]` or callout blocks) where helpful.
- **Natural Persian Syntax:** Persian sentences should flow logically from right-to-left without awkward passive constructs copied from English.

## 2. Structural Integrity (Structure Preservation)
Every translated book MUST strictly preserve the original book's structure:
1. **Chapter & Section Sequence:** The order of chapters, numbered sections, and sub-sections must match the original table of contents 1-to-1.
2. **Code & Configuration Snippets:** Code samples (YAML, Bash, Go, Dockerfile, etc.) must remain intact, syntactically valid, and properly highlighted with appropriate language fences. Comments inside code may be translated or annotated where beneficial.
3. **Figures and Diagrams:** All original figures must be recreated, captured, or included with translated Persian captions and proper numbering (e.g., `تصویر ۲.۱۰`).
4. **Callouts & Callout Types:** Differentiate clearly between:
   - `note` (نکته)
   - `tip` (نکته طلایی و بهینه‌سازی)
   - `warning` (هشدار و پیامدهای خطا)
   - `concept` (تحلیل و تفسیر عمیق مفهومی)

## 3. Formatting Standards in Typst & Markdown
- Target PDF rendering uses **Typst** (`.typ`), requiring RTL text flow: `#set text(lang: "fa", dir: rtl, font: "Vazirmatn")`.
- Numbers within technical contexts, version numbers (`v1.32`), and code flags (`--replicas=5`) must remain in English numerals for clarity.
- Keep English keywords inside headings in parentheses: e.g., `== ۴. اسکیل دستی و خودکار (Scaling)`.

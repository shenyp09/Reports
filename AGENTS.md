# 行研报告库 — AGENTS.md

**Generated:** 2025-03-21  
**Commit:** bd3e230  
**Branch:** main

---

## OVERVIEW

Document archive repository for industry research reports. Stores PDF reports with standardized metadata and cataloging workflow.

**Repository Type:** Document archive (not a software project)  
**Content:** Industry research reports in PDF format  
**Language:** Chinese documentation

---

## STRUCTURE

```
.
├── README.md                          # Report catalog and contribution guide
├── AGENTS.md                          # This file
├── <报告名称>.pdf                      # Research reports
└── .opencode/                         # Workspace tooling config (external)
```

---

## WHERE TO LOOK

| Task | Location | Notes |
|------|----------|-------|
| Add new report | Repository root | Place PDF alongside README.md |
| Update catalog | `README.md` | Update table with report metadata |
| View reports | README table | Click links to open PDFs |
| Workspace config | `.opencode/` | OpenCode agent configuration (external) |

---

## WORKFLOW

### Adding a New Report

1. **Place PDF** in repository root
2. **Update README.md** table with:
   - Report name (linked to PDF)
   - Publication date
   - Summary (100-200 chars, Chinese)
3. **Commit and push:**
   ```bash
   git add <报告文件名>.pdf README.md
   git commit -m "Add: <报告标题>"
   git push
   ```

### Summary Template

Each report summary MUST include:
1. **研究对象** - Industry/market/technology domain
2. **核心内容** - Analysis dimensions (policy, supply chain, market size)
3. **关键发现** - 1-3 key conclusions or data points
4. **适用读者** - Target audience (investors, practitioners, researchers)

---

## CONVENTIONS

### File Naming
- Use descriptive Chinese names: `低空经济产业研究报告.pdf`
- No spaces; use underscores if needed
- Keep under 50 characters

### Report Catalog Table Format
```markdown
| 报告名称 | 发布日期 | 摘要 |
|---------|---------|------|
| [链接](./文件名.pdf) | YYYY | 摘要内容... |
```

### Git Workflow
- One commit per report (include README update)
- Commit message: `Add: <报告标题>`

---

## NOTES

- **This is NOT a software project** — no build, test, or deployment pipeline
- **PDF files are binary** — use Git LFS if reports exceed 100MB
- **.opencode/ directory** contains workspace tooling config; do not modify unless updating agent models
- **Current reports:** 1 (低空经济产业研究报告)

---

## EXTERNAL DEPENDENCIES

| Directory | Purpose | Notes |
|-----------|---------|-------|
| `.opencode/` | OpenCode workspace configuration | Multi-agent model assignments; workspace-scoped |

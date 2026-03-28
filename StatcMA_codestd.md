# 🔷 PHANTOM  
## Static Malware Analysis Platform  

### Coding Standards & Agent Build Guide  
**Version 1.0** | For Human & AI Agents  
**Classification:** INTERNAL USE ONLY  

---

## 1. Purpose & Scope  

This document defines mandatory coding standards, architectural principles, tool-authoring contracts, and AI agent build rules for the PHANTOM platform.  

> ℹ️ Applies to all contributors — human developers, AI agents, and pipelines.  
> Mid-project adoption is expected (see Section 12).

---

## 1.1 What PHANTOM Does  

PHANTOM performs pure static analysis — extracting artifacts without execution.

| Status | Capability | Notes |
|--------|------------|-------|
| ✅ LIVE | File Metadata | Hashes, type, size, timestamps |
| ✅ LIVE | PE Structure | Headers, sections, imports, exports |
| ✅ LIVE | String Extraction | Raw, decoded, categorized |
| 🔲 PLANNED | API Sequence Analysis | Behavioral inference |
| 🔲 PLANNED | YARA Matching | Signature-based detection |
| 🔲 PLANNED | Packer Detection | Entropy + signatures |
| 🔲 PLANNED | IOC Aggregation | Unified intelligence |

---

## 2. Core Design Philosophy  

### 2.1 Zero Execution Guarantee  
> ❗ Hard Security Boundary  

- No execution, interpretation, or spawning of samples  
- No subprocess, shell execution, eval, or indirect execution  

---

### 2.2 AI-First Codebase  

Every file must be:
- Self-contained  
- Fully understandable without external context  
- Explicitly named (no abbreviations)  

Mandatory:
- MODULE PURPOSE header  
- AI CONTEXT comments  

---

### 2.3 Plugin-First Architecture  

- Each capability = independent plugin  
- No core modifications required  
- Automatic discovery and loading  

---

### 2.4 Separation of Concerns  

| Layer | Responsibility |
|-------|---------------|
| Input Adapters | File intake + validation |
| Normalization | Schema alignment only |
| Tool Plugins | Isolated analysis |
| Orchestrator | Tool execution + aggregation |
| Report Engine | Output formatting |
| UI | Display only |

---

### 2.5 DRY + KISS  

- Centralize shared logic in `utils/`  
- Prefer clarity over cleverness  
- Readability always wins  

---

## 3. Project Structure  

```bash
phantom/
├── core/
│   ├── orchestrator.py
│   ├── plugin_loader.py
│   └── file_router.py
├── tools/
│   └── <tool_name>/
│       ├── tool.py
│       ├── manifest.json
│       └── README.md
├── normalization/
├── schemas/
├── api/
├── ui/
├── utils/
├── reports/
├── tests/
└── docs/

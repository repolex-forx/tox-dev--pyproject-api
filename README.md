# Repolex Knowledge Graph of tox-dev/pyproject-api

RDF knowledge graph data for [tox-dev/pyproject-api](https://github.com/tox-dev/pyproject-api), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download tox-dev/pyproject-api
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0ba9f70ba141f29257455caa0cf2429170c5d99e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0ba9f70ba141f29257455caa0cf2429170c5d99e
│           └── chunk-001.nq.gz
├── blob
│   ├── 3142e06f180243b9a7a380bd8c9c96642b4ff1e8.nq.gz
│   ├── 331e3260c0e76662cbfe080a9e774fb5a946d475.nq.gz
│   ├── 346cc81008c3e1b1643f7fe00b0e357887ec1d7f.nq.gz
│   ├── 364982344fbd94d55705e1f27a9a87abaa255333.nq.gz
│   ├── 43ec608853aad7d4c938849840ff6fe5012864af.nq.gz
│   ├── 449c6342eb43bef4f4c991a0e30c53706ec9f347.nq.gz
│   ├── 4d820b3339aba87c4e7558249cb99feef9b20f8f.nq.gz
│   ├── 5261a21875375116105535643972125f6bd647f4.nq.gz
│   ├── 534271f6a742939498910b5d8fc81bb050b0f49c.nq.gz
│   ├── 5910ce72cf4feea016cba7c692dc3bf7984a877d.nq.gz
│   ├── 5f89818f9e63c2f6829c7706c57f223cdb5bbd38.nq.gz
│   ├── 69d0cfd202c019ca1d5a92d59faf9a1380c61930.nq.gz
│   ├── 6c1ffa7e07d95aed9faa2396a9d546b7d5892562.nq.gz
│   ├── 7985011aac6a4ff078407da50a0165734242cff8.nq.gz
│   ├── 7d367a6d5a8ee863dcce7d3514bee5bd0258bbbb.nq.gz
│   ├── 7e108799122b3674c031dd4b864e12f8b4587857.nq.gz
│   ├── 835e93825100568ab86c7d70e78c8859a276c0b9.nq.gz
│   ├── 84f75c677ff34eae0517277c88167b0ef0db1642.nq.gz
│   ├── 9356c2a37774d732d757aabd397711777c6cfe1b.nq.gz
│   ├── 9e00f8051d6d8ef48fb27f771bf6edeca218227d.nq.gz
│   ├── 9f8def65611177da611108f7c0d6caaf0b352a12.nq.gz
│   ├── a1f2311f937ee13681141625e1d5a0dedda0cfe8.nq.gz
│   ├── adebbeb6f81e9432ad15dbf6fdbf6f03ce2daeed.nq.gz
│   ├── ae419c100b25005bd082785a7709b42a9e0300ba.nq.gz
│   ├── b370cc72fce452f5958e0ac6d03ccd6bceb0625d.nq.gz
│   ├── bf6852479e8de78132770bb940b75486b8a06855.nq.gz
│   ├── c1fb0803131eebc82a62759fcd9f7a14ff8a5e22.nq.gz
│   ├── d2f2eac278f8e6199b473531af059e3dc248c6ff.nq.gz
│   ├── e3313bbe8c1317cc1976193c11ad52fc07b6d363.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e9a2c292a83d3757de09b8f7c6d6d67409e831b0.nq.gz
│   ├── e9b931a3c18a7dddfa9282450a5245c30807111b.nq.gz
│   └── f0d79bceecebca539d5c82fbcb608696bcb0bc7d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0ba9f70ba141f29257455caa0cf2429170c5d99e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[tox-dev/pyproject-api](https://github.com/tox-dev/pyproject-api)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*

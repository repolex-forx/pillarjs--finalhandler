# Repolex Knowledge Graph of pillarjs/finalhandler

RDF knowledge graph data for [pillarjs/finalhandler](https://github.com/pillarjs/finalhandler), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download pillarjs/finalhandler
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── aa2851f6b6cf48238a307299be691721530e9172
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── aa2851f6b6cf48238a307299be691721530e9172.nq.gz
│   └── repolex
│       └── aa2851f6b6cf48238a307299be691721530e9172
│           └── chunk-001.nq.gz
├── blob
│   ├── 32a53f784ddb73bd41233ffc7bf6e56899edb25d.nq.gz
│   ├── 3d30ac38515699883cd01471c28b5cab0ccaebce.nq.gz
│   ├── 516e088e8171d4f960a0c31d1cada9c35baca84c.nq.gz
│   ├── 60221067c4d591554407b4700033aab9669a9b0e.nq.gz
│   ├── 62562b74a3b5a79e82ca417b02e0f597d85f5e2f.nq.gz
│   ├── 7be774e60e93ab7583a24740bdba19ea5a1b32f3.nq.gz
│   ├── 869ddc2b39e2a68f60559e77f7204403c39e7d90.nq.gz
│   ├── 8b011be00a99399ac5c79dac3251efa5964907cf.nq.gz
│   ├── 93cebf3e4be1094f37a4e3836d42bc3e578c3818.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── a6096a49b45192e7c5ac5f0f2bdcb17d0b18d1b1.nq.gz
│   ├── bf15e484c8f40a242f5fbf24676bda8da0e9e013.nq.gz
│   ├── cf3015fb3b6ee818a7e76aff5854cde130fc5fe0.nq.gz
│   ├── e40f729a10085463adc71b4772c2d988bae6f25f.nq.gz
│   ├── f15b98e249d653f23d7e121037bde0eae1817582.nq.gz
│   └── f6d43702a0b0298e2d36cf0e1dd9f66656c0153e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── aa2851f6b6cf48238a307299be691721530e9172.nq.gz
├── filetree
│   └── aa2851f6b6cf48238a307299be691721530e9172.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 26 files
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

## Source repository

[pillarjs/finalhandler](https://github.com/pillarjs/finalhandler)

---
*Parsed on 2026-09-16 by [repolex](https://repolex.ai)*

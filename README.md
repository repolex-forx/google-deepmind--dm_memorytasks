# Repolex Knowledge Graph of google-deepmind/dm_memorytasks

RDF knowledge graph data for [google-deepmind/dm_memorytasks](https://github.com/google-deepmind/dm_memorytasks), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/dm_memorytasks
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 47d454618573965f01f313fd8ccdddf6c2ba0da7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 47d454618573965f01f313fd8ccdddf6c2ba0da7
│           └── chunk-001.nq.gz
├── blob
│   ├── 14760efb943acfe74df159112fe97c6bd2434a30.nq.gz
│   ├── 25f7b205c614f992b269f768778d4241485458f0.nq.gz
│   ├── 4c1ebea9f9c991efa1e0130126f35ea8df8e7af7.nq.gz
│   ├── 70199ee41d8a716fd37b469c168a1f754d7469dc.nq.gz
│   ├── 9a86ba025d83dfc39db62d84ee7cac0a9da1ac08.nq.gz
│   ├── 9d02e993fdcb6a839de551822093ae263c02cb5a.nq.gz
│   ├── b02eba01a4c8a2cf3c759300f65a436eb4ce3b32.nq.gz
│   ├── d2c1391ad8c2fc65b1e2014649f10005cdeb33fc.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── d88e2cb80eff0d545834407af59fc3be3b6f9a7b.nq.gz
│   ├── ec04ac16fc1b9be79d65fbf41a903c3aae8a51c7.nq.gz
│   ├── ec4ad7caf0f689c20c159d56d46231095f980ce2.nq.gz
│   └── f392dd036ee7e542b8deabe2d459e78a8827803b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 47d454618573965f01f313fd8ccdddf6c2ba0da7.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 20 files
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

[google-deepmind/dm_memorytasks](https://github.com/google-deepmind/dm_memorytasks)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*

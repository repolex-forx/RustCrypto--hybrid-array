# Repolex Knowledge Graph of RustCrypto/hybrid-array

RDF knowledge graph data for [RustCrypto/hybrid-array](https://github.com/RustCrypto/hybrid-array), parsed by [repolex](https://repolex.ai).

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
rlex download RustCrypto/hybrid-array
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 09310c55b75e2cd408951c7e2e86dba16c63fc68
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 09310c55b75e2cd408951c7e2e86dba16c63fc68.nq.gz
│   └── repolex
│       └── 09310c55b75e2cd408951c7e2e86dba16c63fc68
│           └── chunk-001.nq.gz
├── blob
│   ├── 12380a41a7c904f0c99f27849485f364ed7e3eb8.nq.gz
│   ├── 1df5bb871085ab191d39f580194fe82a0f79fbf8.nq.gz
│   ├── 26a09307ce57292c6a4a573b8d5be2121e05f7bd.nq.gz
│   ├── 2e06d1584ec649d78d9a7f9de165908b287b0bf2.nq.gz
│   ├── 397bdaa4f10fcf70786ab3afd305ad233b86fed0.nq.gz
│   ├── 43cb00e19c9659a5a4f236478cc87788ec2a79f6.nq.gz
│   ├── 44fbfd9902db66c035b9a24c7b08dac372545f62.nq.gz
│   ├── 5b37ba5c5e0d974fd58a330848dc1a53ff2d2f9a.nq.gz
│   ├── 73fab072c5adfcb0a8712064618e210ca7c5d540.nq.gz
│   ├── 76ada8ad42cf141c709dca9fdb6b0bd6279fc154.nq.gz
│   ├── 78173fa2e753d614bb0aa5ad125ddbbe70b282c4.nq.gz
│   ├── 78aa9321d0da74cb520cc321023b7cbafb669587.nq.gz
│   ├── 7936e90544a4734ead698dc6070f57a1c2871e77.nq.gz
│   ├── 867fa23624faadeb569132cd66f795f215459658.nq.gz
│   ├── 86896b0e52797be88ceb7557eebd28806c9ee801.nq.gz
│   ├── 86c5d2fa2d7a5c233d134cbc6b95225e10a9cdb1.nq.gz
│   ├── 8a507c67ebab1a22a90c908346ead19e77fe1a5e.nq.gz
│   ├── 9f50e361f0d48af01c2e8fba9db60a39e36a1a44.nq.gz
│   ├── a3b0eb0e6ad318ad7fdd0053e874f793377eac2d.nq.gz
│   ├── a613c65177929b19e704187f6b1fa1cddf82e4c5.nq.gz
│   ├── ef870237b0274373f6ef6773ad11ccd709fd3057.nq.gz
│   └── f3159b4d63fe750ca8e9cfe6215f0062f95caf3a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 09310c55b75e2cd408951c7e2e86dba16c63fc68.nq.gz
├── filetree
│   └── 09310c55b75e2cd408951c7e2e86dba16c63fc68.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 32 files
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

[RustCrypto/hybrid-array](https://github.com/RustCrypto/hybrid-array)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*

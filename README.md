# Repolex Knowledge Graph of block/me.md

RDF knowledge graph data for [block/me.md](https://github.com/block/me.md), parsed by [repolex](https://repolex.ai).

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
rlex download block/me.md
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f7f7bb3ff6e4942bdf18b0c6353f5730949cd199
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── f7f7bb3ff6e4942bdf18b0c6353f5730949cd199.nq.gz
│   └── repolex
│       └── f7f7bb3ff6e4942bdf18b0c6353f5730949cd199
│           └── chunk-001.nq.gz
├── blob
│   ├── 06dfee621643b6e26ab5e920812fac8e700e9fcc.nq.gz
│   ├── 0ba9db25329d0b336e39ca8cde8470c5b7bc45eb.nq.gz
│   ├── 17ab1e5ff1e7d96c864eae3bdcb3c32a5630a14b.nq.gz
│   ├── 25f0bc5ed80683a81f46e6bfd1cf8ea0b56c6807.nq.gz
│   ├── 2f2ba7a96c3a8f1a924135e89c3bc8bd23dbf62d.nq.gz
│   ├── 37629d8ecb7ac0bcecd75cfd81d0acc65fa7adb4.nq.gz
│   ├── 3d5e3bf8c7871f3983fd21d90c63639d7d707d11.nq.gz
│   ├── 3dac2d920947706513468c03aa8efdaf560165d4.nq.gz
│   ├── 45e42bdb467b7a8b2f2e2bfa277d171ebf449065.nq.gz
│   ├── 4e09d0c1460b90475db42e0c2a332d14fdbf11b6.nq.gz
│   ├── 4fd40357a8df027d03b19a9b3961dc62f8898d10.nq.gz
│   ├── 5e245d2b2f44f5cef674cf8e4613a6373433f181.nq.gz
│   ├── 6bccf43368fd7c96d9c659562a5142b8b8cb98a1.nq.gz
│   ├── 6f2e6f3e9914e877e4877de1930f62fdcb469cae.nq.gz
│   ├── 77cca84ab2bb9bd5fd4bc3a3ba5faac8c49c3c8c.nq.gz
│   ├── 7f5be95ae67b41c6b5e1c3eadb51391311adcb8d.nq.gz
│   ├── 862ee3c28647e7a58801a75236855c269c1448ae.nq.gz
│   ├── 866c9040259fb9dbd91743993f4d157797606f36.nq.gz
│   ├── 9103e3aab0700eced326be9ece8910f71c8271a5.nq.gz
│   ├── 926e0e314b5fd8a98aa22d5a2b452abde0bc5725.nq.gz
│   ├── 9582fc588754f78d9875691a3bd5e674295436b3.nq.gz
│   ├── 95df2efb02b4c532d1d879f6586b7dd20cfdd781.nq.gz
│   ├── ba83844d821c3a78a2cc57493b21d54fda45f7cc.nq.gz
│   ├── c71680b8e1c08f9e9da587f7c029972234cc95c3.nq.gz
│   ├── cc971143d222e9a17e87b90fe09a96976c8d6ead.nq.gz
│   ├── d77f84d8d62f0f96a3f1a80a7c78dcd6d1089d00.nq.gz
│   └── db2ec1be1cc3195b511d37bdd8742c3e33ac787f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f7f7bb3ff6e4942bdf18b0c6353f5730949cd199.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 36 files
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

[block/me.md](https://github.com/block/me.md)

---
*Parsed on 2026-10-02 by [repolex](https://repolex.ai)*

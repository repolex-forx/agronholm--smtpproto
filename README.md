# Repolex Knowledge Graph of agronholm/smtpproto

RDF knowledge graph data for [agronholm/smtpproto](https://github.com/agronholm/smtpproto), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/smtpproto
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 75dcb6c6acf5a7d0b1d6f05f6a3ec250257e84c5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 75dcb6c6acf5a7d0b1d6f05f6a3ec250257e84c5
│           └── chunk-001.nq.gz
├── blob
│   ├── 03aae381199b2c9ebe37305487a1efc58f00e0b0.nq.gz
│   ├── 03d9a2e7d213ec69d99aaac45719f5d07b7879b3.nq.gz
│   ├── 041d7352b747d20f8b0ac9c3bb8fc8d53552b867.nq.gz
│   ├── 0873ed464f707f2fd8051f8d29f8f3ca19d127d0.nq.gz
│   ├── 0f69aca8a6710c23292a672486ca8bbd72185328.nq.gz
│   ├── 30d1403d5be78457c769a35aacdf0835befe85aa.nq.gz
│   ├── 4dc1c52ccf9342087b30b9af8010af77ed91a247.nq.gz
│   ├── 554ff59f1fc96063be87b41f6dadaaeab145c95e.nq.gz
│   ├── 61418c55cd88d6594274655a172293054ab1adc5.nq.gz
│   ├── 6cae98216962981111b97757d6c97a171b663c82.nq.gz
│   ├── 72858b8801f92b390b1f112093ba0f07b4bc7c78.nq.gz
│   ├── 76a2ccd78f4c44f14b3ca83d30ab76a69bf5a4fa.nq.gz
│   ├── 7922d736ba867a1a34618681ea7a454d3137690e.nq.gz
│   ├── 7a3cbfa8b15586b2130171d71e0a4fe265484f7f.nq.gz
│   ├── 7f416705d52369954a3936373e5cae1aeece1d2b.nq.gz
│   ├── 92bbd0d445b0f489b264ade2230614284fbff4af.nq.gz
│   ├── a678bdda4c1481463b31a1ad17cef065ad59eb5e.nq.gz
│   ├── bae3e5f85febf3d2e65205063ded5d21232eedba.nq.gz
│   ├── d5a20580b581c0a49662c7612996b2af7194fbaf.nq.gz
│   ├── daa3390d32621d290492f43499963fbed5d2813b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7a9b4a3e01eed76796b8077de8e4a73d86d776d.nq.gz
│   └── fbef3122978e899b38c89aa14436fc4fdffbd864.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 75dcb6c6acf5a7d0b1d6f05f6a3ec250257e84c5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[agronholm/smtpproto](https://github.com/agronholm/smtpproto)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*

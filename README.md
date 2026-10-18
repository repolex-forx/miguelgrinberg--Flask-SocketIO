# Repolex Knowledge Graph of miguelgrinberg/Flask-SocketIO

RDF knowledge graph data for [miguelgrinberg/Flask-SocketIO](https://github.com/miguelgrinberg/Flask-SocketIO), parsed by [repolex](https://repolex.ai).

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
rlex download miguelgrinberg/Flask-SocketIO
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4c4d56b75801fb07c0d00d92bb24f315293b64c7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4c4d56b75801fb07c0d00d92bb24f315293b64c7
│           └── chunk-001.nq.gz
├── blob
│   ├── 07c392100ab95825a9fc02e4dbf28697d2c60137.nq.gz
│   ├── 0d6f3173c26be34dc645b4b94759ebba441674f9.nq.gz
│   ├── 0d94aa7de3d720449f26e4466b612a8c80d6be91.nq.gz
│   ├── 0ea2860f63fc7f71c90ac369101408bb63ea5eb3.nq.gz
│   ├── 1bbe16ae6aa08872883e5d4ae01b12197da655b7.nq.gz
│   ├── 1d83a9297e59337b8789a703e0f114f604ca3552.nq.gz
│   ├── 250f570e6e94706459402810dd05090ea476a264.nq.gz
│   ├── 27f573b87af11e2cbbd9f54eb1ee285a58550146.nq.gz
│   ├── 298ea9e213e8c4c11f0431077510d4e325733c65.nq.gz
│   ├── 2e9401299d31c85767f372b319a20922cac47054.nq.gz
│   ├── 3c1dc2daa659604fcd538df4f70a81413b9bb584.nq.gz
│   ├── 435290be91743437d1539ac78fbac3a761675222.nq.gz
│   ├── 50b9f86ab8669870157f3ae742fc487f88b9ffe6.nq.gz
│   ├── 5ff8655f08739bec14df3cce48c42235873ef935.nq.gz
│   ├── 6239577c663af635a72b7d38b1787635f5795a30.nq.gz
│   ├── 633811ee1a9e55b59c7e319447d4ade0018944ee.nq.gz
│   ├── 64746f3d84c34d467b2d641ed2c56ff835c43009.nq.gz
│   ├── 6efacd99e0482695ba2c46bc2f0f6b2dec97b8fe.nq.gz
│   ├── 6fb9e333587f4c86f05bd8f5c0bc3a118e7553c3.nq.gz
│   ├── 828c8cd3cbfd70000af584ae6a2ded4000289e1a.nq.gz
│   ├── 8a7d63f086163891b11fca9fd3a8fef0e19ae4e8.nq.gz
│   ├── 8ccc3969ba8d5389eafc5a35aa0d201d59e0acbd.nq.gz
│   ├── 9a862943145f39beedaa3b212cf0a7f53c613815.nq.gz
│   ├── a00a9128c7cac61442c152d3befdae503f81c675.nq.gz
│   ├── a75aa6af9328516259a357f0ad5826926192d40f.nq.gz
│   ├── b0d24531a8ee3caf361fd0106baa646d7e208851.nq.gz
│   ├── e09a64e94266789c6863f44c384c5fba52b52d67.nq.gz
│   ├── e7eec8187083151ab8e6b5eec33e5c5c4b509b41.nq.gz
│   ├── e90c5e9b08efdfc96eda098c5554b4f9f179ce17.nq.gz
│   ├── f1ac44188cd5c7c2896539eea799e15291ec407b.nq.gz
│   ├── f34e3ce474d82dbd851af34b24c235fa4e080c1b.nq.gz
│   ├── f4be40c4f13eb6845a0e48c7b20c650065600038.nq.gz
│   └── f5c10ab28dd4921dd9d891f50dd95f721c66b13d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4c4d56b75801fb07c0d00d92bb24f315293b64c7.nq.gz
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

[miguelgrinberg/Flask-SocketIO](https://github.com/miguelgrinberg/Flask-SocketIO)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*

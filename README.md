# Repolex Knowledge Graph of asimov-platform/asimov-packaging

RDF knowledge graph data for [asimov-platform/asimov-packaging](https://github.com/asimov-platform/asimov-packaging), parsed by [repolex](https://repolex.ai).

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
lexq download asimov-platform/asimov-packaging
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── blob
│   ├── 1014ced45dd7e677d629b99d56177c9ede94cf22.nq.gz
│   ├── 16016e6e608c3090e83724b5eeade46d70eeb0a1.nq.gz
│   ├── 196dc7526226f78d72d17c23153b0fd7f543aeaa.nq.gz
│   ├── 2ab0915daeec43f57205cbc51757c07b691bc669.nq.gz
│   ├── 2f1fd3e486cca1cb6f7c1b552a46840aa29c5ed0.nq.gz
│   ├── 302e7c1d91f1bb4fab5d913a573bb2d0926e5cac.nq.gz
│   ├── 313e31cf05e7dc26d533462c08d2de16315798b3.nq.gz
│   ├── 36a617e4147bf7b872d1a349047adead2afd8829.nq.gz
│   ├── 55095312605ac483d5a410fca42d29f7940b931d.nq.gz
│   ├── 800e31a43f5fab053a53b700d7107a69afbddae4.nq.gz
│   ├── 8d72be9dd25b1bfc70b6b06ccc8b130ac1c17888.nq.gz
│   ├── accb8f392fab16dd68b0140175adfac99979e77c.nq.gz
│   ├── b3bb4f0de7c98d0ba4493737eda9d64606b67e09.nq.gz
│   ├── b58b603fea78041071d125a30db58d79b3d49217.nq.gz
│   ├── ccaf647307ee84eefcd547f87ac0872b883b7809.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── efd375e1c12a82de6da243b300bd0a04a4e6fac6.nq.gz
│   ├── f8da4d3087b98c585ed0f798a76e65d6bf815f6a.nq.gz
│   └── f91fece2a88aec2f6aef62992f546f5c25209454.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   ├── 994347d09ab7346099f67d8132e2f6247481fb0b.nq.gz
│   └── de69af274b1c82fa1affbe678bab98cbdd1966fe.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

8 directories, 28 files
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

[asimov-platform/asimov-packaging](https://github.com/asimov-platform/asimov-packaging)

---
*Parsed on 2026-04-03 by [repolex](https://repolex.ai)*

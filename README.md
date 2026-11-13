# AtlasRepo Open Source Catalog

Find an open-source way to solve a task, compare practical fit, and give your coding agent a grounded starting point. Browse project cards here, search the [AtlasRepo website](https://atlasrepo.com), or use the same catalog through MCP and agent skills.

- **Complete data:** 45,594 indexed projects in a downloadable JSON snapshot.
- **Focused browsing:** 44,885 project cards across 33 categories with 10+ entries.
- **Practical context:** multilingual summaries, use cases, integration notes, repository signals and score breakdowns.
- **Open metadata:** MIT-licensed catalog data. Each linked project has its own license.

[Browse categories](#browse-categories) · [Read the data](#read-the-data) · [Connect an agent](#connect-an-agent) · [Report an issue](#help-improve-the-catalog) · [License](#license)

## Browse categories

Start with a main category, then open a project card for its summary and evidence.

| Category | Project cards |
| --- | ---: |
| [Misc](./misc/README.md) | 18,229 |
| [AI/ML](./aiml/README.md) | 5,192 |
| [MCP](./mcp/README.md) | 3,014 |
| [Orchestration](./orchestration/README.md) | 2,520 |
| [Automation](./automation/README.md) | 1,700 |
| [DevTools](./devtools/README.md) | 1,684 |
| [Backend](./backend/README.md) | 1,010 |
| [Frontend](./frontend/README.md) | 941 |
| [Crypto](./crypto/README.md) | 847 |
| [Documents](./documents/README.md) | 755 |
| [Mobile](./mobile/README.md) | 709 |
| [Networking](./networking/README.md) | 682 |

[Browse all categories alphabetically](./docs/categories.md)

Small categories stay out of the folder index until they contain at least 10 cards. Their projects remain in the full JSON catalog. Topics, languages and product names do not automatically create categories.

## Top projects by score

Scores help shortlist candidates. They do not establish security, maintenance quality or suitability for your use case.

| Project | Stars at last observation | Score |
| --- | ---: | ---: |
| [n8n-io/n8n](./mcp/n8n-io-n8n.md) | 210,325 | 97/100 |
| [sickn33/agentic-awesome-skills](./orchestration/sickn33-agentic-awesome-skills.md) | 49,613 | 94/100 |
| [Panniantong/Agent-Reach](./mcp/panniantong-agent-reach.md) | 111,341 | 93/100 |
| [headroomlabs-ai/headroom](./orchestration/headroomlabs-ai-headroom.md) | 79,485 | 93/100 |
| [wasp-lang/open-saas](./templates/wasp-lang-open-saas.md) | 16,304 | 92/100 |
| [xberg-io/xberg](./mcp/xberg-io-xberg.md) | 9,581 | 91/100 |
| [xberg-io/kreuzberg](./mcp/xberg-io-kreuzberg.md) | 8,543 | 91/100 |
| [diegosouzapw/OmniRoute](./mcp/diegosouzapw-omniroute.md) | 6,732 | 91/100 |
| [langgenius/dify](./orchestration/langgenius-dify.md) | 161,057 | 91/100 |
| [firerpa/lamda](./mcp/firerpa-lamda.md) | 8,729 | 90/100 |

## Read the data

No installation is needed for browsing. For scripts, start with [index.json](./index.json): a shard manifest lists each file under data/ and its record count. Older snapshots may contain a JSON array directly.

This Python 3 example prints the first five project URLs:

```python
import json, urllib.request
base = "https://raw.githubusercontent.com/Arnon-hs/open-source/main/"
def read(path):
    with urllib.request.urlopen(base + path) as response:
        return json.load(response)
index = read("index.json")
rows = index if isinstance(index, list) else read(index["shards"][0]["path"]) if index["shards"] else []
for project in rows[:5]:
    print(project["url"])
```

| File | Contents |
| --- | --- |
| index.json | Complete legacy array or schemaVersion: 1 manifest with total and shards |
| data/repos-*.json | Full project records, including entries without a category folder |
| docs/categories.md | Alphabetical directory of browsable categories |
| category/README.md | Ranked project list for one category |
| category/owner-project.md | Human-readable project card |

Stars, forks and activity dates are snapshots from GitHub, not live browser requests. Follow the project link for current GitHub counts. Source observations and summaries can age; verify them before adoption.

## Community solutions

[Browse curated community solutions](./solutions/README.md) for runnable implementations, setup notes and operating boundaries. These maintainer-written pages are preserved separately from the generated discovery categories.

## Connect an agent

Choose the integration you use; installation and configuration live with their source:

| Integration | Start here |
| --- | --- |
| Hosted read-only MCP | https://mcp.atlasrepo.com/mcp |
| MCP clients and local npm server | [AtlasRepo MCP](https://github.com/Arnon-hs/atlasrepo-mcp) |
| Codex and Claude Code skills | [AtlasRepo Skills](https://github.com/Arnon-hs/atlasrepo-skills) |
| Public decision contracts and tools | [AtlasRepo Core](https://github.com/Arnon-hs/atlasrepo-core) |
| Open discovery engine | [Atlas Engine](https://github.com/Arnon-hs/atlas-engine) |

[Product documentation](https://atlasrepo.com/docs)

## How the catalog is maintained

AtlasRepo Scout collects from approved public sources, deduplicates repositories, evaluates metadata and exports a catalog snapshot. The main category list is controlled by maintainers; a model can select a category from that list, but cannot create a new one. Generated cards and indexes are maintained by the exporter.

A score or AI-written summary is a discovery aid. Check the upstream repository, license, dependencies, release history and installation instructions before using a project. Catalog inclusion is not an endorsement.

## Help improve the catalog

[Open an issue](https://github.com/Arnon-hs/open-source/issues/new) for an incorrect link, outdated record, missing project or category problem. Include the project URL, the affected card or category, what is wrong and a current source supporting the correction. Search [existing issues](https://github.com/Arnon-hs/open-source/issues) first.

Generated content should be fixed in the exporter or source record so the next sync preserves the correction. Automation may prepare a proposed fix; an unverified report is not proof that a record should be changed.

Owner-approved removals are excluded from current exports. Repositories confirmed unavailable on GitHub do not receive browsing cards; their status-marked records may remain in JSON for provenance.

## License

The catalog metadata is available under the [MIT License](./LICENSE), copyright 2026 AtlasRepo. Upstream projects retain their own licenses and attribution requirements.

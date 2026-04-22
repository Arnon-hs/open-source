# Open Scout Catalog

Auto-curated catalog of promising open-source repositories, organized by category.
Updated automatically every 30 minutes by [RepoScout](https://github.com/kirbudilov01/reposearchengine).

## Categories

| Category | Repos |
|---|---|
| [AI/ML](./ai-ml/) | 52 |
| [Frontend](./frontend/) | 15 |
| [Misc](./misc/) | 23 |
| [Data](./data/) | 9 |
| [Backend](./backend/) | 9 |
| [Mobile](./mobile/) | 7 |
| [DevOps/Infra](./devops-infra/) | 2 |
| [Security](./security/) | 1 |
| [DevTools](./devtools/) | 1 |
| [Design](./design/) | 1 |

## Data

- [`index.json`](./index.json) — full catalog, sorted by score
- Each `.md` file contains stars, language, score, description, and AI summary

## How it works

1. RepoScout discovers repos from GitHub trending, HackerNews, Reddit, ProductHunt
2. Scores and categorizes each repo
3. Generates summaries via LLM (Ollama / OpenAI / Claude / OpenRouter)
4. Syncs this catalog via GitHub Actions on every discovery cycle

## Self-host

```bash
git clone https://github.com/kirbudilov01/reposearchengine
cp .env.example .env
# Set LLM_PROVIDER, CATALOG_REPO_PATH, etc.
npm install && npm start
```

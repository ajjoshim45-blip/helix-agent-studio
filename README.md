# Helix

An AI agent desk. **Grok** thinks. **GitHub** and **Wikipedia** go look.

Helix is a small workshop of specialists — Scout, Architect, Scribe, Analyst, Cartographer — plus custom agents you write yourself. Each run is user-initiated. Tool traces (the search, the repo, the Wikipedia extract) sit above the answer so you can see what the agent actually fetched.

Live app: built in Grok. Source of the product idea lives here.

## How a run works

1. You pick an agent and send a brief.
2. The server calls [xAI Grok](https://docs.x.ai) (`grok-4.5`) with that agent’s standing orders.
3. If the question needs evidence, Grok calls free public APIs:
   - [GitHub Search](https://docs.github.com/en/rest/search/search) — public repositories
   - [GitHub Repos](https://docs.github.com/en/rest/repos/repos) — profile + README
   - [Wikipedia API](https://www.mediawiki.org/wiki/API:Main_page) — extracts
4. The model writes a finished briefing. Stars, licenses, and encyclopedic facts come from tools, not guesswork.

API keys never leave the server. Briefings and custom agents stay in your browser (`localStorage`). No accounts.

## Roster

| Agent | Role | Tools |
| --- | --- | --- |
| Scout | Open source | GitHub search + repo |
| Architect | Systems | GitHub search + repo |
| Scribe | Writing | Wikipedia |
| Analyst | Judgment | Wikipedia + GitHub search |
| Cartographer | Research | Wikipedia + GitHub search + repo |
| Custom | Yours | You choose |

## Try

- Dispatch **Scout** and ask it to compare TypeScript vector-database libraries.
- Ask **Cartographer** to map local-first software.
- Build a custom agent with a brief and a tool belt.

## GitHub

[github.com/ajjoshim45-blip/helix-agent-studio](https://github.com/ajjoshim45-blip/helix-agent-studio)

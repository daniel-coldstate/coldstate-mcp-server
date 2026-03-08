# ColdState Knowledge Search MCP Server

> The semantic alternative to web search APIs and web scraping — 
> 64.6M knowledge entries, sub-3s responses, fraction of the energy cost.

## What It Does

ColdState exposes a semantic knowledge search API as an MCP server, 
giving your LLM agent structured, meaningful results without:

- ❌ Web scraping (fragile, slow, legally gray)
- ❌ Live web search APIs (expensive, rate-limited, noisy)
- ❌ Vector DB infrastructure (you maintain nothing)

Instead, your agent queries ColdState's pre-built 64.6M entry 
knowledge base and gets back semantically ranked results — 
navigated by meaning, not keyword matching or page popularity.

## Why ColdState vs Web Search

| | Web Search API | Web Scraping | **ColdState** |
|---|---|---|---|
| Avg energy/query | ~11,520J | High | **62J avg / 3.7J min** |
| Rate limits | Yes | Yes | No |
| Structured results | No | No | **Yes** |
| Fragility | Medium | High | **None** |
| Real-time data | Yes | Yes | Knowledge base |
| Cost at scale | High | High | **Low** |

## Powered By

**Quantum Semantic Theory (QST)** — a geometric framework that 
navigates knowledge by meaning density and structural coherence 
rather than popularity signals. Formula: `E = k · S · D · Λ · C`

Query states:
- `CRYSTALLINE` — tight, high-confidence results (3.7J avg)
- `FLUID` — focused cluster retrieval  
- `REACTIVE` — broad cross-domain discovery

## MCP Endpoint
```
https://services.coldstate.ai
```

**Transport:** HTTP/SSE  
**Auth:** API Key (`x-api-key` header)  
**Protocol:** MCP-compatible

## Quick Start (Claude Desktop / Cursor)
```json
{
  "mcpServers": {
    "coldstate": {
      "type": "url",
      "url": "https://services.coldstate.ai/mcp",
      "headers": {
        "x-api-key": "YOUR_API_KEY"
      }
    }
  }
}
```

## Available Tools

### `knowledge_search`
Search 64.6M entries by semantic meaning.

**Input:**
```json
{
  "query": "string",
  "domain": "optional: SCIENCE | MATH | MEDIA | GENERAL | ...",
  "limit": "optional: number (default 10)"
}
```

**Returns:** Ranked results with E-score, domain zone, 
semantic state, and content.

### `domain_list`
Returns all 35 available knowledge domains with 
zone metrics (S, Λ values).

## Use Cases

- 🤖 LLM agents needing factual grounding without live web access
- 📚 RAG pipelines replacing or supplementing vector DBs
- 🔬 Cross-domain research discovery
- ⚡ High-throughput agent workflows where web API costs compound

## Pricing

API keys available at **services.coldstate.ai**  
Free tier available. Usage-based scaling.

## Links

- 🌐 [services.coldstate.ai](https://services.coldstate.ai)
- 🏠 [coldstate.ai](https://coldstate.ai)

## Built By

**ColdState Inc.** — Columbus, Ohio  
Founded by Daniel Huddleston (@dhuddly)

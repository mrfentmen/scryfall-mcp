# scryfall mcp

MCP server for **Scryfall**, the definitive Magic: The Gathering card database.

## Tools

| Tool | What it does |
|---|---|
| `search_cards` | Full Scryfall syntax search (`c:red type:dragon`, `o:"when ~ enters"`) |
| `get_card` | Fuzzy name card lookup (Bolas's Citadel, Chaos Orb…) |
| `get_rulings` | Official Gatherer rulings |
| `list_sets` | Recent sets with release dates + card counts |

## Usage

```bash
npm run build && node dist/index.js
```

Example:

```
search_cards { query: "c:red type:dragon" }
get_rulings { name: "bolas citadel" }
```

Keyless. Includes prices (USD + foil), legality friendly fields, image URLs. Throttled to stay under Scryfall's ~10 req/s limit.

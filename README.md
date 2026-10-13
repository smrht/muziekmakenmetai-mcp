<img src="logo-400.png" alt="Muziek maken met AI logo" width="96" height="96">

# Muziek maken met AI MCP server

**Make an original song from a prompt or your own lyrics. Two versions per song, MP3 download.**

Remote MCP server: `https://muziekmakenmetai.nl/mcp` (Streamable HTTP) · Website: [muziekmakenmetai.nl](https://muziekmakenmetai.nl/)

## What it does

Muziek maken met AI turns a short description or your own lyrics into a finished song with vocals: a birthday song for a colleague, a jingle for a shop, a song for a wedding speech. The assistant checks your credit balance, shows you title, style and lyrics, starts the song after you confirm, and returns the audio links once both versions are stored.

One song uses 1 credit from your account and returns two versions, usually within one to four minutes.

## Connect

- **Server URL:** `https://muziekmakenmetai.nl/mcp`
- **Transport:** Streamable HTTP
- **Authentication:** OAuth with PKCE (S256), dynamic client registration and client ID metadata documents, so MCP clients connect without manual setup. Sign in with your muziekmakenmetai.nl account.

**Claude (claude.ai, Desktop):** Settings → Connectors → Add custom connector → paste the server URL.

**Claude Code:**

```bash
claude mcp add --transport http muziekmakenmetai https://muziekmakenmetai.nl/mcp
```

**Cursor, VS Code, Cline, Windsurf and other clients** (`mcp.json` / `cline_mcp_settings.json`):

```json
{
  "mcpServers": {
    "muziekmakenmetai": {
      "type": "http",
      "url": "https://muziekmakenmetai.nl/mcp"
    }
  }
}
```

Cline uses `"type": "streamableHttp"`; see [llms-install.md](llms-install.md).

## Tools

| Tool | What it does |
|---|---|
| `get_account` | Credit balance and account details. |
| `create_song` | Start one song from a description or lyrics (after confirmation). |
| `get_song` | Status, lyrics and audio links of one song. |
| `list_songs` | Recent songs in the account. |

## Example prompts

- Make a cheerful Dutch birthday song for my colleague Anna, pop style.
- Write and record a 30-second jingle for a bakery in Hoorn.
- How many song credits do I have left?

## Links

- Website: https://muziekmakenmetai.nl/
- Documentation: https://muziekmakenmetai.nl/ai-assistent/
- Privacy policy: https://muziekmakenmetai.nl/privacy/
- Terms: https://muziekmakenmetai.nl/voorwaarden/
- Developer API: https://muziekmakenmetai.nl/developers/
- n8n node: https://www.npmjs.com/package/n8n-nodes-muziekmakenmetai

## Keywords

AI music generator, AI song maker, text to music, song generator, birthday song, jingle maker, lyrics to song, Dutch songs, MP3.

Nederlands: muziek maken met AI, AI liedje maken, liedje laten maken, verjaardagslied, eigen songtekst, jingle maken, AI muziek generator, Nederlandstalig liedje.

## More MCP servers by Samautomation

- [Scamchecker.nl](https://scamchecker.nl/): Check a suspicious email, SMS, WhatsApp message or link for scam signals (Netherlands, Belgium). ([listing](https://github.com/smrht/scamchecker-mcp))
- [Klussenbeheer](https://samdesk.nl/klussenbeheer/): Job management for Dutch service companies: jobs, customers, planning, quotes and invoices. ([listing](https://github.com/smrht/klussenbeheer-mcp))
- [Beheer je WP](https://beheerjewp.nl/): Manage a WordPress site from your AI assistant: read, search, propose edits, Search Console data. ([listing](https://github.com/smrht/beheerjewp-mcp))
- [UlazAI Media](https://ulazai.com/): Create private AI images with your UlazAI account: pick a model, confirm, generate, download. ([listing](https://github.com/smrht/ulazai-mcp))
- [Backlinkswinkel](https://backlinkswinkel.nl/): Search Dutch websites for backlinks, check metrics and prices, order after confirmation, track. ([listing](https://github.com/smrht/backlinkswinkel-mcp))
- [Backlinksbeheer](https://backlinksbeheer.nl/): Read your stored backlinks, link checks and lost-link alerts per domain. Read-only. ([listing](https://github.com/smrht/backlinksbeheer-mcp))
- [Samautomation Video](https://samautomation.work/): Render an MP4 from your own images, clips, voice-over and timed captions. JSON to video. ([listing](https://github.com/smrht/samautomation-video-mcp))
- [PDF Samenvoegen](https://pdfsamenvoegen.nl/): Merge your own PDFs in a confirmed order and get one downloadable PDF. ([listing](https://github.com/smrht/pdfsamenvoegen-mcp))
- [Diamond Painting Converter](https://diamondpaintingconverter.com/): Find your purchased diamond painting patterns and download the PDF with DMC colour legend. ([listing](https://github.com/smrht/diamondpaintingconverter-mcp))
- [Nummerschilderen.com shop advisor](https://nummerschilderen.com/): Search paint-by-number kits, get size and price advice for your own photo, shop info. No login. ([listing](https://github.com/smrht/nummerschilderen-mcp))
- [DiamondPaintingWinkel.nl shop advisor](https://diamondpaintingwinkel.nl/): Search diamond painting kits, get size and price advice for your own photo, shop info. No login. ([listing](https://github.com/smrht/diamondpaintingwinkel-mcp))
- [AI Rechtshulp](https://ai-rechtshulp.nl/): Search Dutch and EU case law with ECLI sources and verify quotes against the judgment. ([listing](https://github.com/smrht/ai-rechtshulp-mcp))
- [SamDesk Support](https://samdesk.nl/support/plugin/): Read your SamDesk support inbox, find customer agreements and draft replies. Read-only. ([listing](https://github.com/smrht/samdesk-support-mcp))

## Publisher

Samautomation, Wognum, the Netherlands · https://samautomation.work

This repository holds the public listing (README, `server.json`, install notes). The server itself is hosted by the publisher; there is nothing to install or build.

# Luttie for Claude

A Claude Code plugin that connects Claude to [Luttie](https://luttie.app), giving it color grading tools: browse LUTs, generate AI color grades from a text prompt, and apply a LUT to an image, all without leaving Claude.

## Install

```
/plugin marketplace add iwaju-labs/luttie-mcp-plugin
/plugin install luttie@luttie
```

## Set up your API key

The plugin needs a Luttie API key in your environment before Claude Code starts:

1. Sign in at [luttie.app](https://luttie.app), open your account menu, and choose **Developer / MCP**.
2. Generate a key. It's shown once, so copy it.
3. Set it in your shell before launching Claude Code:

   ```
   export LUTTIE_API_KEY="luttie_live_..."
   ```

   Add that line to your shell profile (`.bashrc`, `.zshrc`, etc.) to avoid retyping it.

## Tools

- `list_luts`: list published LUT packs and singles (free)
- `get_lut`: fetch a LUT's metadata and `.cube` file by slug (free LUTs open, Pro LUTs return a locked flag for free accounts)
- `ai_grade`: generate 3 color grading variants from a text prompt and optional reference image (requires Pro, Lifetime, or Trial)
- `apply_lut`: apply a LUT to an image server-side, returns a base64 PNG
- `account_status`: check tier and current hourly usage

Full docs: [luttie.app/mcp](https://luttie.app/mcp)

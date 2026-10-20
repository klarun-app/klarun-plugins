# Klarun plugins for Claude

The Klarun plugin connects Claude to [Klarun](https://klarun.app), where a
company's data team keeps its reports, data assets, people, OKRs and FinOps.
It adds the Klarun AI connector (`https://klarun.app/mcp`) and a skill that
tells Claude when and how to use its tools.

## Install

In Claude Code:

```
/plugin marketplace add klarun-app/klarun-plugins
/plugin install klarun@klarun
```

The first time Claude calls Klarun, you sign in with your own Klarun account
(Microsoft sign-in) and approve the connection. Claude then sees only what
your Klarun roles allow.

## What you need

- A Klarun account on a paid plan. A Klarun admin sets the company's access
  in Settings, Integrations, AI connector (MCP): read only by default, or read
  and write, or off.
- To disconnect, open My Account, then Connected AI apps, in Klarun.

## What is in this repository

- `.claude-plugin/marketplace.json`: the marketplace, named `klarun`.
- `plugins/klarun/.claude-plugin/plugin.json`: the plugin manifest.
- `plugins/klarun/.mcp.json`: the connector address. It holds no credential;
  sign-in is OAuth with PKCE.
- `plugins/klarun/skills/klarun/SKILL.md`: the skill.

This repository is published from Klarun's main repository, so changes made
here directly are overwritten. Open an issue for a problem or an idea. Do not
report a security issue in a public issue: write to legal@klarun.app.

- Documentation: https://klarun.app/en/docs#ai-connector
- Privacy: https://klarun.app/en/privacy

## License

MIT, see [LICENSE](LICENSE).

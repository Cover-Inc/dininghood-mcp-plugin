# Dininghood MCP (Claude Code plugin)

> Experimental prototype. Talk to `#mcp-prototype` before depending on it.

Connects Claude Code to Dininghood's MCP server so Claude can search
experiences, look up your dining points, and identify your account — all
scoped to your own Dininghood login.

## Install

Run these two commands in a fresh Claude Code session:

```
/plugin marketplace add Cover-Inc/dininghood-mcp-plugin
/plugin install dininghood-mcp@dininghood-tools
```

On your first tool invocation, Claude Code will open a browser for sign-in
and consent. Use your Dininghood email and password. Google-only accounts
(no password) cannot connect until federation ships in a later release.

## Tools

- `whoami` — returns your Dininghood identity (id, email, username).
- `searchExperiences` — search dining experiences by keyword. May take 5–15 seconds; results include external dining sources beyond Dininghood listings.
- `getMyDinerPoints` — your points balance and recent transactions.

All tools are read-only.

## Troubleshooting

**`auth_required` error.** Your session has expired. Dininghood tokens have
a 7-day maximum refresh window; after that you need to reconnect. Run
`/mcp` in Claude Code and re-authenticate, or restart Claude Code.

**Something else broken?** File an issue at
https://github.com/Cover-Inc/dininghood-mcp-plugin/issues

## License

Proprietary — see `LICENSE`. All rights reserved.

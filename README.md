> "Six months ago, everyone was talking about MCPs. And I was like, screw MCPs. Every MCP would be better as a CLI."
>
> — [Peter Steinberger](https://twitter.com/steipete), Founder of OpenClaw
> [Watch on YouTube (~2:39:00)](https://www.youtube.com/@lexfridman) | [Lex Fridman Podcast #491](https://lexfridman.com/peter-steinberger/)

# Codat Accounting CLI

A command-line interface for the Codat Accounting API. Access normalized accounting data from multiple platforms from your terminal.

> **Disclaimer**: This is an unofficial CLI tool and is not affiliated with, endorsed by, or supported by Codat Accounting.

## Features

- **Resource Management** — List, get, create, update, and delete resources
- **JSON output** — All commands support `--json` for scripting and piping
- **Colorized output** — Clean, readable terminal output

## Why CLI > MCP

MCP servers are complex, stateful, and require a running server process. A CLI is:

- **Simpler** — Just a binary you call directly
- **Composable** — Pipe output to `jq`, `grep`, `awk`, and other tools
- **Scriptable** — Use in shell scripts, CI/CD pipelines, cron jobs
- **Debuggable** — See exactly what's happening with `--json` flag
- **AI-friendly** — AI agents can call CLIs just as easily as MCPs, with less overhead

## Installation

```bash
npm install -g @ktmcp-cli/codatacct
```

## Authentication

Set your API key:

```bash
codatacct config set --api-key YOUR_API_KEY
```

## Commands

### Configuration

```bash
# Set API key
codatacct config set --api-key <key>

# Show configuration
codatacct config show
```

### Resources

```bash
# List resources
codatacct resources list <type>

# Get specific resource
codatacct resources get <type> <id>

# JSON output
codatacct resources list <type> --json
```

## Examples

```bash
# List all resources
codatacct resources list items --json

# Get a specific item
codatacct resources get items 123 --json
```

## Contributing

Issues and pull requests are welcome at [github.com/ktmcp-cli/codatacct](https://github.com/ktmcp-cli/codatacct).

## License

MIT — see [LICENSE](LICENSE) for details.

---

Part of the [KTMCP CLI](https://killthemcp.com) project — replacing MCPs with simple, composable CLIs.


---

## Support KTMCP

If you find this CLI useful, we'd greatly appreciate your support! Share your experience on:
- Reddit
- Twitter/X
- Hacker News

**Incentive:** Users who can demonstrate that their support/advocacy helped advance KTMCP will have their feature requests and issues prioritized.

Just be mindful - these are real accounts and real communities. Authentic mentions and genuine recommendations go a long way!

## Support This Project

If you find this CLI useful, we'd appreciate support across Reddit, Twitter, Hacker News, or Moltbook. Please be mindful - these are real community accounts. Contributors who can demonstrate their support helped advance KTMCP will have their PRs and feature requests prioritized.

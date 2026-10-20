# Lockpick for Claude

Scan your app, site, or AI skill before you ship. Lockpick checks public websites you own or have permission to test, and statically reviews public GitHub repositories, AI skills, plugins and MCP servers without installing or running them. Use it from Claude to request a check, read findings, and work through repair guidance.

## Connect

Installing the plugin and connecting your account are separate steps. Install the Lockpick plugin and open its Connectors tab. Connect Lockpick, sign in or create an account, choose a workspace, and review the requested permissions.

A new connection can only read. When you ask Claude to add a site, start a Pulse or run a Deep scan, Lockpick asks you to approve that permission on its own consent screen first.

On Team and Enterprise plans, an organization Owner may need to make the connector available first. Claude Code users can receive the plugin through account sync or install it from the Lockpick marketplace. A separate sign-in may be required.

## Try it

- "Run a Pulse on my site."
- "Check this public GitHub skill before I install it."
- "Explain the top three findings."
- "Go deeper on this site."
- "Fix what Lockpick found in this repository."

Deep requires DNS or file proof of ownership and your approval of the specific scan on a one-time Lockpick page. Claude never approves it for you. Writing a proof file locally does not deploy it.

## Commands

| Command             | What it does                                             |
| ------------------- | -------------------------------------------------------- |
| `/lockpick:check`   | Quick check of a homepage or public GitHub repository     |
| `/lockpick:pulse`   | Run a Pulse on a site you are authorized to test         |
| `/lockpick:deep`    | Prove ownership, approve and run a Deep scan             |
| `/lockpick:fix`     | Apply the repair brief to the current repository         |
| `/lockpick:recheck` | Recheck a deployed fix, or run the free DNS check again  |
| `/lockpick:status`  | Show the connected workspace, sites, scans and allowance |

In Cowork and Claude Code, commands start the matching skill. Chat loads commands as skills rather than slash commands; ask in your own words. The fixer agent is available in Cowork and Claude Code. In chat without repository access, Claude explains or drafts a repair.

## Costs

Read tools are free. Scan costs and remaining allowance come from your connected Lockpick account, and Claude reads them before quoting a cost.

- A homepage quick check is free.
- A free repository or AI skill check uses no Pulse scan. An explicitly requested Deep repository check uses one Deep scan.
- A Pulse uses one Pulse scan from the monthly allowance.
- A Deep scan uses one Deep scan from the monthly allowance.
- A full recheck counts as a scan and costs the same as its depth.
- The DNS public-record "Check again" is free and does not change the original scan grade.

## Data and permissions

The connector receives the arguments needed for the tools you request, such as site URLs, site IDs, and scan IDs. Lockpick stores account, authorization, assessment, and operational records as described in its privacy policy. It returns findings, redacted evidence, coverage, status, and repair guidance to Claude. It never returns how Lockpick runs its assessments internally.

The connector does not request your full conversation history. Do not put passwords, private keys, or unrelated personal information into tool inputs. Repository edits happen in the Claude environment where you requested them, and Claude commits only when you allow it.

If a connection expires, reconnect through Claude's connector settings, then verify the connected workspace before retrying. Remove the connector there to disconnect Claude. Revoke its authorization in Lockpick Workspace settings. Your workspace and project permissions continue to limit access. Revoking a connection does not delete past assessments.

## Limits

A completed assessment is not a security certification. Unassessed coverage is unknown. A finding that disappears does not prove a credential was revoked or every related issue was fixed.

## Help

Read the [Lockpick for Claude guide](https://www.lockpick.app/en/claude), [privacy policy](https://www.lockpick.app/en/privacy), and [terms](https://www.lockpick.app/en/terms).

Use the support contact shown in the Lockpick guide. Include the request ID and time of the problem, but never send tokens or credentials.

## License

The contents of this plugin are released under the MIT License (see `LICENSE`). The Lockpick service it connects to is provided under the Lockpick terms.

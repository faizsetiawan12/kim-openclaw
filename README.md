# KIM OpenClaw

This is KIM's personal multi-agent operating system: a focused team that turns
an owner's request into clear coordination, implementation, or research.

KIM keeps one human decision-maker at the center. Agents can help move work
forward, but consequential actions remain the owner's decision.

## The KIM team

| Role | Responsibility |
| --- | --- |
| Main | Private dashboard assistant for the owner. |
| Chief | KIM's coordinator: clarifies, routes, summarizes, and tracks open decisions. |
| Engineer | Implements concrete Chief-routed work and reports progress. |
| Research | Produces English-language research and analysis for human review. |

This repository shares KIM's role design, not a live installation.

## What KIM shares here

- Role documents that keep KIM's responsibilities clear and non-overlapping.
- A local Markdown issue workflow.
- A Telegram configuration example using an environment variable placeholder.
- Ignore rules that keep live state and credentials out of Git.

## Setup

1. Create your own local OpenClaw installation.
2. Copy the role documents into the workspaces you configure for your agents.
3. Copy `.env.example` to `.env`, then set a new Telegram bot token locally.
4. Use `openclaw.json.example` as a shape reference; do not overwrite a
   working configuration without reviewing it.
5. Validate your local configuration with `openclaw config validate`.

## Make KIM your own

Start with `docs/agents/AGENTS.md`, then personalize each role's `USER.md`.
Keep operating policy in `AGENTS.md`; keep tone in `SOUL.md`; keep tool notes
in `TOOLS.md`; keep durable, non-sensitive summaries in `MEMORY.md`.

Start small: define how your owner approves consequential work, customize the
Chief's coordination style, and add specialist roles only when they earn a
clear responsibility.

## KIM safety principles

Workflow instructions and runtime permissions are different. A document can
say an agent needs approval, while host permissions may still allow it to act.
Review the actual runtime policy before enabling a role.

This template does not claim sandboxing. Host-level YOLO execution means broad
unattended permissions; it is a deliberate risk choice and is unsafe for
shared or untrusted environments. Use sandboxing there, and require explicit
human approval for publishing, deployment, credentials, configuration,
destructive actions, trading, and other external actions.

Never commit real configuration, credentials, chat identifiers, sessions,
memories, logs, backups, or runtime state. Check `git status` before every
commit.

## Repository workflow

Create a feature branch for each change, validate it locally, then open a pull
request before merging to `main`.

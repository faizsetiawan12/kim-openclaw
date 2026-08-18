# KIM OpenClaw

This repository belongs to KIM. It documents a personal OpenClaw multi-agent
workspace design.

A small, generic four-role team for an OpenClaw setup: Main, Chief, Engineer,
and Research. It is a starting point for learning role separation and routing;
it is not a copy of a working installation.

## What is included

- Role documents with one purpose each.
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

## Customize roles

Start with `docs/agents/AGENTS.md`, then personalize each role's `USER.md`.
Keep operating policy in `AGENTS.md`; keep tone in `SOUL.md`; keep tool notes
in `TOOLS.md`; keep durable, non-sensitive summaries in `MEMORY.md`.

## Safety

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

# Douyin Web Control Skill

[![skills.sh](https://skills.sh/b/billwang233/douyin-web-control-skill)](https://skills.sh/billwang233/douyin-web-control-skill)

An Agent skill that teaches AI agents how to operate Douyin web through the `douyin-web` CLI.

This repository contains only the skill. The CLI lives in a separate repository:

```text
https://github.com/billwang233/douyin-web-cli
```

## Install the CLI

Install the CLI before using this skill:

```bash
python3 -m pip install "git+https://github.com/billwang233/douyin-web-cli.git"
python3 -m playwright install chromium
douyin-web --help
```

## Install the Skill

Install with the `skills` CLI:

```bash
npx skills add billwang233/douyin-web-control-skill
```

Or copy the skill folder manually into your Agent runtime:

```text
skills/douyin-web-control/
```

## What This Skill Does

- Teaches an Agent when to use `douyin-web` instead of direct browser automation.
- Shows the command patterns for launch, login, navigation, playback, comments, danmaku, screenshots, and recording.
- Explains which actions can affect the Douyin account.
- Keeps the feature matrix in `references/feature-matrix.md`.
- Bundles a small wrapper script in `scripts/douyin-web` so the Agent can find the CLI from `PATH`, `DOUYIN_WEB_CLI`, or `DOUYIN_CLI_ROOT`.

## Marketplace Notes

- `skills.sh`: this repository is installable with `npx skills add billwang233/douyin-web-control-skill`; skills.sh picks up repositories after they are installed through the CLI.
- `ClawHub`: publish this skill repository with the ClawHub CLI if you use OpenClaw.
- `SkillMap` / similar indexes: submit or index this GitHub repository URL when their intake form asks for a public skill repo.

See `MARKETPLACES.md` for current publishing status and repeatable submission commands.

## Safety

This skill can guide an Agent to perform account-affecting actions such as liking, favoriting, commenting, or sending danmaku. Agents should ask for user permission before submitting anything that changes the account state.

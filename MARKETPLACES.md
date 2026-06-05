# Marketplace Publishing

This skill is distributed from:

```text
https://github.com/billwang233/douyin-web-control-skill
```

## Current Status

| Marketplace | Status | Notes |
| --- | --- | --- |
| skills.sh | Installable / indexing triggered | `npx skills add billwang233/douyin-web-control-skill` found and installed `douyin-web-control`. The web listing was still returning 404 immediately after install, so treat the page as pending until the index catches up. |
| ClawHub | Published | Published as `douyin-web-control@0.1.0` under `billwang233`. `clawhub inspect douyin-web-control` reports moderation `CLEAN`. |
| OmniSkill | Submitted through GitHub issue | The public API submit attempt returned `403 Forbidden`. Index request opened at `https://github.com/diegosouzapw/awesome-omni-skill/issues/8`. |
| SkillMap | Feedback submitted | SkillMap currently exposes a feedback form but no obvious public skill-submit endpoint. A repository indexing request was submitted through `/v1/feedback`. |
| skills.re | Attempted, not completed | The site exposes a GitHub Import form, but command-line clients hit SSL EOF from this environment and no public submit endpoint was confirmed. |

## Repeatable Commands

Trigger skills.sh discovery:

```bash
npx skills add billwang233/douyin-web-control-skill
```

Publish or republish to ClawHub after login:

```bash
npx clawhub@latest login --device
npx clawhub@latest publish skills/douyin-web-control \
  --slug douyin-web-control \
  --name "Douyin Web Control" \
  --version 0.1.0 \
  --tags douyin,browser-automation,cli,agent-skill \
  --changelog "Initial release of the Douyin web control Agent skill."
```

Submit to OmniSkill API if network access is allowed:

```bash
curl -X POST https://omniskill.online/api/v1/submit-repo \
  -H 'Content-Type: application/json' \
  -d '{"repo":"billwang233/douyin-web-control-skill"}'
```

## Skill/CLI Relationship

The CLI repository is:

```text
https://github.com/billwang233/douyin-web-cli
```

The skill repository is:

```text
https://github.com/billwang233/douyin-web-control-skill
```

The CLI README should point users to this skill when they want an Agent to operate the CLI reliably. This skill should point users back to the CLI installation instructions before running any `douyin-web` commands.

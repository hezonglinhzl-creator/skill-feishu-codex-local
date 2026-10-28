# Feishu Documents and Local Codex Tools / 飞书文档与本地 Codex 工具

[简体中文](README.md) | **English**

Read, create and update Feishu documents, Base records and attachments through local Python OpenAPI tools.

[Download complete project ZIP](https://github.com/hezonglinhzl-creator/varla-electric-mobility-skills-and-tools/raw/main/packages/skill-feishu-codex-local.zip) · [All projects](https://github.com/hezonglinhzl-creator/varla-electric-mobility-skills-and-tools)

## Features

- Documents and native-table import
- Base record operations
- Local credential setup and status checks

## What is included

| Part | Location |
| --- | --- |
| Local Feishu OpenAPI Toolkit | [feishu-codex-local](apps/feishu-codex-local/README.en.md) |
| Skill instructions | [SKILL.md](skill/feishu-codex-local/SKILL.md) |

## Download and extract

1. Open this repository, choose **Code → Download ZIP**, or use the complete-project download above.
2. Right-click the downloaded ZIP and choose **Extract All**. Open the extracted folder containing this README.
3. Keep the whole folder together. Start the program first using the next section, then install/use its skill.

Installation also writes PACKAGE-LOCATION.json beside the installed SKILL.md, mapping the bundled programs to their actual extracted directories. Keep the full extracted folder; rerun the installer after moving it. Existing Skill content is preserved by default while paths are refreshed.

## 1. Set up the program first

### Local Feishu OpenAPI Toolkit (`feishu-codex-local`)

Windows, Python and your Feishu app permissions; chat bridging is optional.

Open `apps/feishu-codex-local` first. Documents, native tables, Base records and attachments, with setup/check scripts.

1. Run `配置OpenAPI.bat` and enter your own App ID and App Secret.
2. Configuration stays locally at `%USERPROFILE%\.feishu-docs\config.json`.
3. Run `检查OpenAPI.bat`; add required permissions and publish your app version in Feishu if needed.
4. Run `python scripts/feishu_docs.py --help`, or ask Codex with the installed skill to read a specified document first.
5. Only chat-to-Codex bridging needs the separate bridge installation/configuration and cc-connect. OpenAPI data operations can run independently.

[Full program / browser-extension guide](apps/feishu-codex-local/README.en.md)

Unauthorized resources remain inaccessible. Do not upload your config or treat a failed check as a successful sync.

## 2. Install the Skill

1. At the extracted project's root, double-click `安装Skill.cmd` on Windows.
2. The installer copies `skill/feishu-codex-local` to `%USERPROFILE%\.codex\skills\feishu-codex-local`. Existing same-name skills are skipped; check the displayed result.
3. Reopen Codex and start a new chat. Use the exact skill name shown below.
4. If scripts cannot run under your organization policy, open install.ps1 for review or copy the skill directory manually to the same destination.

## 3. First task

| Prepare | Details |
| --- | --- |
| Input | Your Feishu app credentials, accessible document/Base links and requested content. |
| Output | Document links, changed records and readback results. |

```text
Use feishu-codex-local to check setup, then read only the fields and first three records from my Base link without writing.
```


## Limits and troubleshooting

The public package has no Feishu account or app secret. Chat-bot bridging is optional and needs a separately installed/configured cc-connect.

| Problem | Next step |
| --- | --- |
| Skill not visible | Check the installer output and destination SKILL.md, reopen Codex and start a new chat. |
| Program fails to start | Open its directory in PowerShell and run the documented command so the error remains visible; check that program's README. |
| Browser panel missing | Select the exact folder containing manifest.json, check supported websites and refresh the website tab. |
| External service unavailable | Supply your own authorization/settings and verify access. Keep local output rather than claiming a sync/send succeeded. |

## Privacy and status

This is a source/skill distribution. No real accounts, OAuth tokens, customer/KOL lists, contracts, orders, mailbox exports or business media are included. You configure your own services. Documentation and package paths were checked; live orders, sends and publications were not executed as part of documentation validation.

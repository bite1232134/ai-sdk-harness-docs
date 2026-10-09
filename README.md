# AI SDK `HarnessAgent` — 上游文档原文镜像

本仓库收录 **Vercel AI SDK** 中 `HarnessAgent` 的文档**原文**（未翻译、未改写），仅作镜像留档，方便在 GitHub 直连受限的网络环境下阅读与检索。

## 内容

| 路径 | 说明 |
| --- | --- |
| `docs/ai-sdk-harnesses/harness-agent.mdx` | 上游文档原文，保持原文件名与目录层级 |

## 来源与溯源

- 上游仓库：<https://github.com/vercel/ai>
- 上游文件：`content/docs/03-ai-sdk-harnesses/02-harness-agent.mdx`
- 上游文件直链：<https://github.com/vercel/ai/blob/main/content/docs/03-ai-sdk-harnesses/02-harness-agent.mdx>
- 渲染后的官方文档：<https://ai-sdk.dev/docs/ai-sdk-harnesses/harness-agent>
- 抓取时间：2026-10-10（UTC+8）
- 抓取方式：本机 `github.com` 域名在 hosts 中被指向 `127.0.0.1`（经 Steam++/Watt Toolkit 加速器转发），因此使用 jsDelivr 的 GitHub 镜像读取 `main` 分支内容：
  `https://cdn.jsdelivr.net/gh/vercel/ai@main/content/docs/03-ai-sdk-harnesses/02-harness-agent.mdx`
- 对应实现包：`@ai-sdk/harness`（`packages/harness`，抓取时版本 `1.0.148`）

> 注意：镜像内容对应抓取时刻的 `main` 分支。上游更新后本仓库不会自动同步，请重新抓取以对比。

## 相关上游资源

- 示例仓库（沙箱化 HarnessAgent 实战）：<https://github.com/vercel-labs/sandboxed-issue-triage-agent>
- 教程：<https://vercel.com/kb/guide/sandboxed-coding-agent-with-harnessagent>
- 公告：<https://vercel.com/changelog/program-agent-harnesses-with-ai-sdk>
- 同章节其它文档（上游路径）：

  ```text
  content/docs/03-ai-sdk-harnesses/01-overview.mdx
  content/docs/03-ai-sdk-harnesses/02-harness-agent.mdx
  content/docs/03-ai-sdk-harnesses/03-tools.mdx
  content/docs/03-ai-sdk-harnesses/04-skills.mdx
  content/docs/03-ai-sdk-harnesses/05-harness-adapters.mdx
  content/docs/03-ai-sdk-harnesses/06-workflow-utilities.mdx
  content/docs/03-ai-sdk-harnesses/07-ui.mdx
  content/docs/03-ai-sdk-harnesses/08-terminal-ui.mdx
  ```

## 许可

上游 `vercel/ai` 采用 **Apache License 2.0**，原文版权归 Vercel 及贡献者所有。本仓库仅为原文镜像，未作修改；随附 `LICENSE` 为上游同一许可证文本。若上游许可条款有变，以上游仓库为准。

## 如何推送到你自己的 GitHub 仓库

```bash
# 在 GitHub 网页上先建一个空仓库（不要勾选 README/LICENSE），然后：
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

如果本机 git 未加入 PATH，可用完整路径：

```powershell
& "C:\Program Files\Git\cmd\git.exe" remote add origin https://github.com/<你的用户名>/<仓库名>.git
& "C:\Program Files\Git\cmd\git.exe" push -u origin main
```

提交者身份是临时占位（`dsh-agent`）。想改成你自己的：

```bash
git -c user.name="Your Name" -c user.email="you@example.com" commit --amend --reset-author --no-edit
```

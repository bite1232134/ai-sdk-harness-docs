# AI SDK Harnesses — 上游文档原文镜像

本仓库收录 **Vercel AI SDK** 中 "AI SDK Harnesses" 章节（`HarnessAgent` 所在章节）的文档**原文**，未翻译、未改写，仅作镜像留档，方便在 GitHub 直连受限的网络环境下阅读与检索。

## 内容

全部 9 个文件，文件名与上游 `content/docs/03-ai-sdk-harnesses/` 完全一致：

| 文件 | 大小 | 行数 | 说明 |
| --- | ---: | ---: | --- |
| `docs/ai-sdk-harnesses/index.mdx` | 1,818 B | 60 | 章节落地页 |
| `docs/ai-sdk-harnesses/01-overview.mdx` | 4,593 B | 117 | Harness 总览 |
| `docs/ai-sdk-harnesses/02-harness-agent.mdx` | 26,480 B | 745 | **`HarnessAgent` 主文档** |
| `docs/ai-sdk-harnesses/03-tools.mdx` | 8,832 B | 297 | 内置工具与宿主执行工具 |
| `docs/ai-sdk-harnesses/04-skills.mdx` | 2,121 B | 65 | 可复用指令包（Skills） |
| `docs/ai-sdk-harnesses/05-harness-adapters.mdx` | 3,898 B | 47 | 各 harness 适配器差异与能力表 |
| `docs/ai-sdk-harnesses/06-workflow-utilities.mdx` | 14,202 B | 464 | 长时运行回合的工作流工具 |
| `docs/ai-sdk-harnesses/07-ui.mdx` | 7,457 B | 253 | `useChat` 集成 |
| `docs/ai-sdk-harnesses/08-terminal-ui.mdx` | 2,276 B | 84 | 终端 UI |

> 每份文件的字节数与上游 GitHub API 返回的 `size` 逐一核对一致（2026-10-10 抓取）。

## 来源与溯源

- 上游仓库：<https://github.com/vercel/ai>
- 上游目录：`content/docs/03-ai-sdk-harnesses/`
- 目录浏览：<https://github.com/vercel/ai/tree/main/content/docs/03-ai-sdk-harnesses>
- 抓取时间：2026-10-10（UTC+8）
- 抓取方式：本机 `github.com` / `raw.githubusercontent.com` 等域名在 `hosts` 中被指向 `127.0.0.1`（由 Steam++/Watt Toolkit 加速器转发），因此文件内容经 jsDelivr 的 GitHub 镜像读取 `main` 分支：
  `https://cdn.jsdelivr.net/gh/vercel/ai@main/content/docs/03-ai-sdk-harnesses/<文件名>`
  文件名与大小则通过 GitHub 公开 API 核对：
  `https://api.github.com/repos/vercel/ai/contents/content/docs/03-ai-sdk-harnesses`
- 对应实现包：`@ai-sdk/harness`（仓库内 `packages/harness`，抓取时版本 `1.0.148`）

> 注意：镜像内容对应抓取时刻的 `main` 分支。上游更新后本仓库不会自动同步，请重新抓取以对比。
> 历史说明：首个提交里只有一个 `docs/ai-sdk-harnesses/harness-agent.mdx`，现已改为与上游一致的 `02-harness-agent.mdx`，并补齐其余 8 份。

## 相关上游资源

- 渲染后的官方文档：<https://ai-sdk.dev/docs/ai-sdk-harnesses/overview>
- 示例仓库（沙箱化 HarnessAgent 实战）：<https://github.com/vercel-labs/sandboxed-issue-triage-agent>
- 教程：<https://vercel.com/kb/guide/sandboxed-coding-agent-with-harnessagent>
- 公告：<https://vercel.com/changelog/program-agent-harnesses-with-ai-sdk>

## 许可

上游 `vercel/ai` 采用 **Apache License 2.0**，原文版权归 Vercel 及贡献者所有。本仓库仅为原文镜像，未作修改；随附 `LICENSE` 为上游同一许可证文本。若上游许可条款有变，以上游仓库为准。

## 如何更新与推送

```powershell
cd <本仓库目录>
$git = "C:\Program Files\Git\cmd\git.exe"

# 1) 从上游镜像同步全部文件（本机直连 github.com 被 hosts 屏蔽，故走 jsDelivr）
$base = "https://cdn.jsdelivr.net/gh/vercel/ai@main/content/docs/03-ai-sdk-harnesses"
foreach ($n in @('index.mdx','01-overview.mdx','02-harness-agent.mdx','03-tools.mdx','04-skills.mdx','05-harness-adapters.mdx','06-workflow-utilities.mdx','07-ui.mdx','08-terminal-ui.mdx')) {
  Invoke-WebRequest "$base/$n" -OutFile "docs\ai-sdk-harnesses\$n" -UseBasicParsing
}

# 2) 提交并推送（首次会弹出 GitHub 登录窗口，之后免登录）
& $git add .
& $git commit -m "update: 同步上游 AI SDK Harnesses 文档原文"
& $git push origin main
```

### 如果 push 时报证书错误

本机 GitHub 流量经过 Steam++/Watt Toolkit 中间人解密，git 自带 CA 包不认，需要改用 Windows 系统证书库（已在本仓库 `.git/config` 中设置）：

```powershell
& "C:\Program Files\Git\cmd\git.exe" config --local http.sslBackend schannel
```

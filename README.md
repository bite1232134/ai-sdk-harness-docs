# AI SDK Harnesses — 文档原文镜像（含中文翻译）

本仓库收录 **Vercel AI SDK** 中 "AI SDK Harnesses" 章节（`HarnessAgent` 所在章节）的文档**英文原文**，并附上配套的**简体中文翻译**，方便在 GitHub 直连受限的网络环境下阅读与检索。

## 📖 在线阅读（GitHub Pages）

**https://bite1232134.github.io/ai-sdk-harness-docs/**

- 顶部导航栏可 **English / 中文** 一键切换
- 左侧目录列出全部 9 篇，右上角有搜索框
- 正文直接读取仓库里的 `.mdx` 原文渲染

## 内容

### 英文原文（与上游逐字一致）

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

### 简体中文翻译

| 文件 | 对应原文 |
| --- | --- |
| `zh/index.mdx` | `docs/ai-sdk-harnesses/index.mdx` |
| `zh/01-overview.mdx` | `docs/ai-sdk-harnesses/01-overview.mdx` |
| `zh/02-harness-agent.mdx` | `docs/ai-sdk-harnesses/02-harness-agent.mdx` |
| `zh/03-tools.mdx` | `docs/ai-sdk-harnesses/03-tools.mdx` |
| `zh/04-skills.mdx` | `docs/ai-sdk-harnesses/04-skills.mdx` |
| `zh/05-harness-adapters.mdx` | `docs/ai-sdk-harnesses/05-harness-adapters.mdx` |
| `zh/06-workflow-utilities.mdx` | `docs/ai-sdk-harnesses/06-workflow-utilities.mdx` |
| `zh/07-ui.mdx` | `docs/ai-sdk-harnesses/07-ui.mdx` |
| `zh/08-terminal-ui.mdx` | `docs/ai-sdk-harnesses/08-terminal-ui.mdx` |

### 站点文件

| 文件 | 作用 |
| --- | --- |
| `index.html` | Docsify 阅读站配置（`ext: '.mdx'` 直接读取原文） |
| `_navbar.mdx` / `zh/_navbar.mdx` | 顶部导航（含中英切换） |
| `_sidebar.mdx` / `zh/_sidebar.mdx` | 左侧目录 |
| `.nojekyll` | 关闭 Jekyll，避免 `_sidebar.mdx` 这类下划线开头的文件被忽略 |

## ⚠️ 关于中文翻译

- 译文由 AI（DeepSeek Harness 中的 agent）生成，**未经人工逐句校对**。做技术决策时请以英文原文为准。
- 代码块、行内代码、API 名、包名、错误类型名等一律保留英文原文，未作改动。
- 原文中的 JSX 组件标签（如 `<InstallPackages ... />`）在网页上不显示，这是 mdx 组件在静态站上的正常限制，与上游 Vercel 文档站的差异无关。
- 术语沿用统一对照表，例如：harness（不译）、agent = 智能体、session = 会话、sandbox = 沙箱、turn = 回合、skill = 技能、adapter = 适配器、runtime context = 运行时上下文、permission mode = 权限模式。

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

> 注意：英文原文对应抓取时刻的 `main` 分支，上游更新后本仓库不会自动同步；中文翻译对应同一时刻的原文，译文可能滞后于上游。

## 相关上游资源

- 渲染后的官方文档：<https://ai-sdk.dev/docs/ai-sdk-harnesses/overview>
- 示例仓库（沙箱化 HarnessAgent 实战）：<https://github.com/vercel-labs/sandboxed-issue-triage-agent>
- 教程：<https://vercel.com/kb/guide/sandboxed-coding-agent-with-harnessagent>
- 公告：<https://vercel.com/changelog/program-agent-harnesses-with-ai-sdk>

## 许可

上游 `vercel/ai` 采用 **Apache License 2.0**，英文原文版权归 Vercel 及贡献者所有。本仓库为原文镜像，未作修改；随附 `LICENSE` 为上游同一许可证文本。中文译文由本仓库贡献者生成，同样以 Apache License 2.0 提供。

## 如何更新与推送

```powershell
cd <本仓库目录>
$git = "C:\Program Files\Git\cmd\git.exe"

# 1) 同步英文原文（本机直连 github.com 被 hosts 屏蔽，故走 jsDelivr）
$base = "https://cdn.jsdelivr.net/gh/vercel/ai@main/content/docs/03-ai-sdk-harnesses"
foreach ($n in @('index.mdx','01-overview.mdx','02-harness-agent.mdx','03-tools.mdx','04-skills.mdx','05-harness-adapters.mdx','06-workflow-utilities.mdx','07-ui.mdx','08-terminal-ui.mdx')) {
  Invoke-WebRequest "$base/$n" -OutFile "docs\ai-sdk-harnesses\$n" -UseBasicParsing
}

# 2) 提交并推送（GitHub Pages 会在约 30 秒后自动重新构建）
& $git add .
& $git commit -m "sync: 同步上游原文"
& $git push origin main
```

### 如果 push 时报证书错误

本机 GitHub 流量经过 Steam++/Watt Toolkit 中间人解密，git 自带 CA 包不认，需要改用 Windows 系统证书库（已在本仓库 `.git/config` 中设置）：

```powershell
& "C:\Program Files\Git\cmd\git.exe" config --local http.sslBackend schannel
```

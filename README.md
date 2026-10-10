# scoop-boxmiao

[![Tests](https://github.com/BoxMiao007/scoop-boxmiao/actions/workflows/ci.yml/badge.svg)](https://github.com/BoxMiao007/scoop-boxmiao/actions/workflows/ci.yml) [![Excavator](https://github.com/BoxMiao007/scoop-boxmiao/actions/workflows/excavator.yml/badge.svg)](https://github.com/BoxMiao007/scoop-boxmiao/actions/workflows/excavator.yml)

个人维护的 [Scoop](https://scoop.sh) 软件仓库。

## 添加仓库

```pwsh
scoop bucket add boxmiao https://github.com/BoxMiao007/scoop-boxmiao
```

## 安装应用

```pwsh
scoop install boxmiao/<应用名>
```

例如：

```pwsh
scoop install boxmiao/cloakbrowser
```

## 更新应用

```pwsh
# 更新指定应用
scoop update cloakbrowser

# 更新所有应用
scoop update *
```

## 卸载应用

```pwsh
scoop uninstall cloakbrowser
```

## 可用应用

### AI 编程

| 应用 | 说明 |
|------|------|
| [DeepSeek Harness](https://www.deepseek.com/harness/) | DeepSeek 开源的 Agent 桌面应用（预览版），基于 Cordis「一切皆插件」架构 |
| [OpenChamber](https://openchamber.dev) | AI 编程工作区，深度集成 OpenCode 智能体引擎 |
| [OpenCode Desktop](https://opencode.ai) | 开源 AI 编程智能体 OpenCode 的桌面客户端 |
| [Token Monitor](https://github.com/Javis603/token-monitor) | 本地优先的桌面小组件，汇总 40 余个 AI 编程工具的 Token 用量、费用与额度 |
| [ZCode](https://zcode.z.ai) | Z.ai 出品的 AI 编程助手桌面客户端 |
| [zcode-switch](https://github.com/pjpv/zcode-switch) | 在多个 ZCode 账号之间一键切换，自动显示额度 |

### 开发工具

| 应用 | 说明 |
|------|------|
| [Pebrel](https://github.com/Kuddev/pebrel) | AI 原生 GPU 加速终端模拟器，集成 SSH、持久会话、分屏与 AI CLI 工作流 |
| [Rscoop](https://github.com/AmarBego/Rscoop) | Scoop 的桌面应用程序。无需进入终端即可搜索、安装、更新和管理 Windows 软件包 |

### 浏览器

| 应用 | 说明 |
|------|------|
| [cloakbrowser](https://github.com/CloakHQ/CloakBrowser) | 隐身 Chromium 浏览器，源码级指纹补丁，通过所有反检测测试 |

### 美术与资产

| 应用 | 说明 |
|------|------|
| [Photon Studio](https://tenzen.studio/photon/) | 免费的全功能 Photoshop 替代品，支持 PSD/PSB、RAW 处理与本地 AI 功能 |
| [Serpent](https://serpent.dolag.work) | 开源数字资产管理软件，面向游戏美术、影视后期与平面/动态图形设计 |

## 自动更新

本仓库通过 Excavator 每 4 小时自动检查上游新版本并提交更新 PR，无需手动维护。

---

<details>
<summary>Bucket 模板原始说明（英文）</summary>

## How do I use this template?

1. Generate your own copy of this repository with the "Use this template"
   button.
2. Allow all GitHub Actions:
   - Navigate to `Settings` - `Actions` - `General` - `Actions permissions`.
   - Select `Allow all actions and reusable workflows`.
   - Then `Save`.
3. Allow writing to the repository from within GitHub Actions:
   - Navigate to `Settings` - `Actions` - `General` - `Workflow permissions`.
   - Select `Read and write permissions`.
   - Then `Save`.
4. Document the bucket in `README.md`.
5. Replace the placeholder repository string in `bin/auto-pr.ps1`.
6. Create new manifests by copying `bucket/app-name.json.template` to
   `bucket/<app-name>.json`.
7. Commit and push changes.
8. If you'd like your bucket to be indexed on `https://scoop.sh`, add the
   topic `scoop-bucket` to your repository.

## How do I install these manifests?

After manifests have been committed and pushed, run the following:

```pwsh
scoop bucket add <bucketname> https://github.com/<username>/<bucketname>
scoop install <bucketname>/<manifestname>
```

## How do I contribute new manifests?

To make a new manifest contribution, please read the [Contributing
Guide](https://github.com/ScoopInstaller/.github/blob/main/.github/CONTRIBUTING.md)
and [App Manifests](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests)
wiki page.

</details>

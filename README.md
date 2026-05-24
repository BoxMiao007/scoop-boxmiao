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

| 应用 | 说明 |
|------|------|
| [cloakbrowser](bucket/cloakbrowser.json) | 隐身 Chromium 浏览器，源码级指纹补丁，通过所有反检测测试 |

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

# scoop-boxmiao 开发规范

## 仓库说明

本仓库是一个 [Scoop](https://scoop.sh) 软件仓库（Bucket），包含 Windows 应用的安装清单。

## 应用清单规范

### 新增应用

在 `bucket/` 目录下创建 `<应用名>.json`，格式参考既有清单或 `bucket/app-name.json.template`。

### 必需字段

- `version` — 上游最新版本号
- `description` — 应用说明
- `homepage` — 应用官网
- `license` — 开源协议
- `url` / `hash` — 下载地址及 SHA256
- `checkver` — 自动检测版本（优先使用 `github` 方式）
- `autoupdate` — 自动更新 URL 模板

## 提交规范

### 分支

在 master 分支上直接提交。

### 提交信息

```
类型: 中文描述
```

类型：feat / fix / refactor / docs / chore / test / ci

### 提交前检查

- `git status --short` 确认只有目标文件变更
- 必要时运行 `.github/workflows/ci.yml` 中的测试

## README 规范

- `README.md` 的「可用应用」按应用类型分组展示，每组一个 `###` 小节加表格。组顺序固定为：AI 编程、开发工具、浏览器、美术与资产；组内应用按名称排序（不区分大小写）。
- 新增应用优先归入现有分组；确无合适的分组时，再按其类型新增分组。
- 应用名称链接到对应官方网站，便于用户直达项目主页。

## 自动更新

本仓库通过 Excavator（GitHub Actions）每 4 小时自动检查上游新版本，`checkver` 和 `autoupdate` 字段需配置正确。

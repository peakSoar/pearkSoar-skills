# 🧰 pearkSoar Skills

我正在使用的一组 Codex Skills，放在一个仓库里持续维护。

每个 Skill 都是可以单独安装的结构化指令集，适合用于 Codex 等支持 Agent Skills 的工具。

## 📋 技能目录

| 技能 | 用途 | 入口 |
| --- | --- | --- |
| 💽 [storage-analyzer](storage-analyzer/) | 分析 macOS / Windows 磁盘占用，生成可折叠的 HTML 报告 | [查看 SKILL.md](storage-analyzer/SKILL.md) |
| 🔭 [evidence-driven](evidence-driven/) | 管理长期 AI 协作中的阶段、证据、验证和跨会话接力 | [查看 README](evidence-driven/README.md) |

## 📦 安装

把需要的技能目录复制到用户级或仓库级 `.agents/skills/` 目录：

```text
<target>/.agents/skills/storage-analyzer/
<target>/.agents/skills/evidence-driven/
```

安装后，在 Codex 中使用对应的技能名称调用。

## 🔗 快速跳转

- [storage-analyzer 技能目录](storage-analyzer/)
- [storage-analyzer 使用说明](storage-analyzer/SKILL.md)
- [evidence-driven 项目目录](evidence-driven/)
- [evidence-driven 项目说明](evidence-driven/README.md)
- [根目录 MIT License](LICENSE)

## 🛠️ 开发说明

本仓库脚本使用 Python 3 标准库，不需要安装第三方依赖。运行脚本前，先按 [storage-analyzer 的解释器检查规则](storage-analyzer/SKILL.md#python-解释器检查)获取可用 Python 路径。

## 📄 许可证

本仓库统一采用根目录的 [MIT License](LICENSE)。

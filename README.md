# pearkSoar Skills

面向 Codex 的个人技能集合，集中维护可复用的本地工作流。

## 技能

### storage-analyzer

macOS / Windows 只读存储分析助手。它会扫描磁盘占用，按可清理程度分级，并生成可折叠的 HTML 报告。

支持：

- 多盘符和用户目录分析；
- 缓存、开发工具、项目文件和虚拟机镜像识别；
- 绿色、黄色、红色三级处置建议；
- 使用 Python 3 标准库，无需第三方依赖。

### evidence-driven

证据驱动工程 Harness，用于长期 AI 协作开发、阶段状态管理、验证记录和跨会话接力。

## 安装

将需要的技能目录复制到用户级或仓库级 `.agents/skills/` 目录：

```text
<target>/.agents/skills/storage-analyzer/
<target>/.agents/skills/evidence-driven/
```

安装后，在 Codex 中使用对应技能名称调用。

## 开发

本仓库中的脚本只使用 Python 3 标准库。运行脚本前，先检查可用解释器：

```text
python -c "import sys; print(sys.executable)"
python3 -c "import sys; print(sys.executable)"
```

使用第一条成功返回的解释器路径运行后续脚本。

## 许可证

本仓库统一采用根目录的 [MIT License](LICENSE)。

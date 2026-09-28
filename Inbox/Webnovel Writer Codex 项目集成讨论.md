# Webnovel Writer Codex 项目集成讨论

状态：工具与工作流讨论，尚未为具体作品立项；本记录不构成作品 Canon。

## 此前对话回填（2026-09-27 起）

### 将 Claude Code 框架适配到 Codex

- 作者提出：保留 [webnovel-writer](https://github.com/lingfengQAQ/webnovel-writer) 的写作框架，将 Claude Code 基础改为适用于 Codex 的实现。
- Codex 的主要答复与实际工作：制作了可安装的 Webnovel Writer Codex 插件包和 ZIP，包含写作技能、角色参考、脚本与项目约束；完成结构、初始化与安装等验证。完整的真实作品写作流程仍需在具体项目中验证。
- 待定：选择哪一部作品启用，以及在实际作品中检验写作、审查和提交流程。

### Codex Project、Obsidian 与 GitHub

- 作者提出：准备将其做成 Codex Project，并与 Obsidian 和 GitHub 配合，询问可行性。
- Codex 答复：技术上可行；Codex 使用本地工作目录，Obsidian 打开同一 Markdown 库，GitHub 对该库进行版本管理。
- 更正：此前曾建议“一书一库／一仓”。此建议已被 2026-09-28 的文学库规则取代：以文学库根目录作为唯一 Obsidian vault 和 Git 仓库，正式作品放在 `Works/BOOK-.../` 下，不在作品目录内另建 Git 仓库。Webnovel Writer 仅在明确选定的作品目录中初始化和运行。

### 如何把插件交给 Codex Project

- 作者提问：新建 Codex Project 时，能否直接放入前述文件或 ZIP，再附上指令使用？
- Codex 答复：仅把 ZIP 当作附件放入 Project 不会自动注册技能。应先解压并安装 Codex 插件，让技能可调用；再将 Project 的工作目录指向文学库根目录，并在选定作品目录运行 `$webnovel-init`。插件包可作为安装来源或备份，而非每次对话都重新上传的上下文。
- 更正：此前以“项目当前目录即书籍根目录”为前提的说明不适用于现行文学库。文学库根目录是总仓，作品工作目录须明确定位到 `Works/BOOK-.../`。

## 2026-09-28：文学库规则更新

- 跨 Chat 通知传达了文学库规则更新。Codex 已重新阅读文学库根 `AGENTS.md` 与 `Craft/创作讨论与批评方式.md`，按最新版规则继续处理本讨论。
- 最新规则要求：每次关于文学库或作品的对话，在本轮答复结束前保存可见讨论要点。此条记录据此回填本 Chat 的相关问题、答复、更正和待决事项。
- 当前尚未指定要启用插件的正式作品，也未因此修改任何作品设定或 Canon。
- 本轮给作者的操作建议：新 Codex Project 关联文学库根目录；Obsidian 打开同一根目录，GitHub 仅连接根仓库；把根规则写进 Project 指令。当前 Codex 环境已显示八项 Webnovel Writer 技能，先在新 Project 的技能列表中确认可用；ZIP 留作迁移或重装来源。选定正式作品后，只对其 `Works/BOOK-.../` 目录运行 `$webnovel-init`。
- 依据：Codex 的官方插件文档将技能作为需通过插件安装或项目配置启用的目录资源，并说明本地插件市场与项目级启用方式；把 ZIP 作为普通 Project 文件附件本身不等于安装插件。参见 <https://developers.openai.com/plugins/build/plugins>。

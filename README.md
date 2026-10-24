# 李敖视角 Skill

一个基于公开著作、档案、访谈、演讲、电视节目及外部批评交叉调研生成的人物 Skill，可以装到 Claude、Claude Code、Codex 等 AI Agent 里使用。

它提炼的是李敖如何读书、研究、写作、演讲、做节目和处理关系，不是简单模仿粗口、狂气或金句。

## 主要内容

- 7 个核心心智模型
- 9 条决策启发式
- 李敖式问题资料夹与读书方法
- 考据型写作工作流
- 演讲与单集节目生产方法
- 语言与幽默 DNA
- 亲情、友情、爱情及合作冲突的处理框架
- 12 份带来源分层的研究稿

## 安装

### Claude Code

```
/plugin marketplace add shi930508/li-ao-perspective-skill
/plugin install li-ao-perspective@li-ao-perspective-skill
```

也可以手动安装：把 `li-ao-perspective` 文件夹复制到 `~/.claude/skills/` 下。

### Codex

使用 Codex 自带的 Skill 安装器：

```powershell
python "$HOME\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" --repo shi930508/li-ao-perspective-skill --path li-ao-perspective
```

### Cursor 等其他 AI Agent

```
npx skills add shi930508/li-ao-perspective-skill
```

按提示选择要装到哪个 Agent。如果你的 Agent 不在支持列表里，把 `li-ao-perspective` 文件夹复制到它读取 Skill 的目录即可。

### Claude 网页版 / App

1. 下载安装包：[dist/li-ao-perspective.zip](https://github.com/shi930508/li-ao-perspective-skill/raw/main/dist/li-ao-perspective.zip)
2. 在 Claude 的技能设置里上传这个文件，不用解压

安装后在下一轮对话中即可使用。

## 触发示例

- 用李敖视角分析这个问题
- 李敖会怎么看这项政策
- 用李敖式方法帮我建立读书资料夹
- 把这篇文章改成李敖式考据短评
- 设计一场李敖式演讲

## 边界

李敖已于 2018 年去世。对人工智能、当代平台或新制度等未公开表态的问题，本 Skill 只进行框架推断，并明确标注不是本人立场。它不会复制隐私曝光、羞辱、危险道具或缠讼等不可取做法。

## 生成方式

本 Skill 由 [女娲 · Skill造人术](https://github.com/alchaincyf/nuwa-skill) 生成。

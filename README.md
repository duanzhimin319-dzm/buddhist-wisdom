# buddhist-wisdom · 佛学智慧开解 Skill

一个以《心经》《金刚经》《妙法莲华经》为根本的 AI 技能（Skill）。用户提出人生困惑——生老病死、七情六欲、焦虑失眠、得失执念——它以**师父的口吻**开解：称用户为"师兄"，引用一处加粗经文讲义，用大白话展开，落到一件可行的小事，最后以回向偈收尾。

## 功能特性

- **三部经典知识库**：25 条核心经句 + 白话释义 + 适用场景（`references/sutras.md`）
- **主题映射**：生老病死、七情六欲、八苦、贪嗔痴及 15+ 高频人生主题 → 对症经文（`references/themes.md`）
- **佛教节日感知**：内置 2025-2035 全年 264 个佛教节日公历对照表，回答前自动查询（`scripts/check_festival.py`，零依赖）
- **回向收尾**：节日当天用节日专属祝福 + 宜做事项；平日回向佛经偈语 + 日常善事建议（`references/festivals.md`）
- **安全边界**：心理危机时引导专业援助，不算命不迷信，丧亲倾诉先陪伴不讲大道理

## 目录结构

```
buddhist-wisdom/
├── SKILL.md                    # 技能主指令（回答流程、语气、边界）
├── references/
│   ├── sutras.md               # 三部经典经句素材库
│   ├── themes.md               # 主题 → 经文映射表
│   └── festivals.md            # 节日表、回向句式、善事建议
└── scripts/
    └── check_festival.py       # 佛教节日查询（2025-2035）
```

## 安装

### 方式一：一句话让 AI 安装（推荐）

把下面这段话发给你的 AI 助手（Codex / CodeBuddy / 豆包等）：

```
帮我安装 buddhist-wisdom 这个 skill：从 GitHub 克隆 https://github.com/<你的用户名>/buddhist-wisdom，
把其中的 buddhist-wisdom/ 目录（含 SKILL.md、references/、scripts/）复制到 ~/.codebuddy/skills/ 下，
验证 SKILL.md 存在后告诉我安装完成，并提醒我新开对话生效。
```

> 推送本仓库到 GitHub 后，把 `<你的用户名>` 替换成你的 GitHub 用户名即可。

### 方式二：手动安装

```bash
git clone https://github.com/<你的用户名>/buddhist-wisdom.git
cp -r buddhist-wisdom ~/.codebuddy/skills/
# 或复制到项目级目录
cp -r buddhist-wisdom /path/to/project/.codebuddy/skills/
```

安装后**新开一个对话**即生效。

## 使用

无需任何命令，对话中自然触发。例如：

- "最近工资低还负债，有点焦虑"
- "失恋三个月了还是放不下"
- "从佛学的角度讲讲，人为什么会怕死"
- "师父，我心里乱得很"


## 依赖

- Python 3（仅用于节日查询脚本；无 Python 时技能会自动降级为按文档查表，不影响使用）

## License

MIT

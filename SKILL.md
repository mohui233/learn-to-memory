---
name: "learn-to-memory"
description: "通用记忆辅助：对截图/文本进行费曼解构、组块整理与记忆编码，输出可复习的记忆策略。用户需要记忆辅助时调用。"
---

# 通用记忆辅助 (Learn-To-Memory)

输入学习材料（截图、文档或文本），输出经过「理解-整理-编码-复习」深度加工的记忆策略。

## 触发方式

- **指令触发**：`/auto-memory`
- **隐式触发**：用户上传截图/文本并要求帮忙记忆、理解、或梳理知识点

## 能力目录 (Commands)

| 指令 | 职责说明 | 对应文件 |
| :--- | :--- | :--- |
| `/auto-memory` | 分析输入内容，生成记忆策略 | [commands/auto-memory.md](commands/auto-memory.md) |

## 文件结构

- `rules/lin-peter-method.md`：林彼得记忆法（解构—图像—记忆—强化）
- `rules/feynman-technique.md`：费曼技巧（以教代学、类比简化）
- `rules/chunking-method.md`：组块化记忆法（分类分组、层级化）
- `README.md`：人工阅读说明与使用示例

## 全局约束

- 三大记忆法的判定标准只从 `rules/` 读取
- 执行步骤只从 `commands/auto-memory.md` 读取
- 输出必须包含四项：核心本质 → 深度拆解 → 记忆编码 → 复习建议
- 记忆编码至少提供两种方案（逻辑链 + 图像/口诀）
- 遇到纯文本无结构输入时，先用费曼技巧理解，再组块化整理

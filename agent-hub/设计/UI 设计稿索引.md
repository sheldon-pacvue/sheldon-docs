# Agent Hub · UI 设计稿索引

#agent-hub #design #tui

CLI 人类可读输出按 **cli-tui-design** 工作流：先用 `.txt` mockup 定视觉，再写 `src/render/`。

## 源码位置

仓库路径：`docs/mockups/`

| 文件 | 方向 |
|------|------|
| `direction-a-unix.txt` | Unix Minimal — 高密度 ASCII 表 |
| `direction-b-blueprint.txt` | Engineering Blueprint — 分组 + 框线 |
| `direction-c-editorial.txt` | Editorial — 留白、产品感 |
| `direction-final.txt` | 锁定方向（B 为主，TTY 外降级 A） |
| `README.md` | 对比维度与决策记录 |

GitHub：[docs/mockups](https://github.com/liusheldon238/agent-hub/tree/main/docs/mockups)

## 已画场景（首轮）

每个方向含三屏：`list` / `run` 成功 / `run` 失败。

## 决策摘要

- **倾向 B+A 混合**：默认 Blueprint 分组（managed / detected / orphan）；非 TTY 或 `NO_COLOR` 时降级 Unix 表格式
- **glyph**：真 unicode box；老终端可用 `--ascii`（规划）
- **品牌色**：倾向纯 ANSI 16 色，避免与用户终端主题冲突

## 实现映射

| 命令 | 渲染入口（cli） |
|------|-----------------|
| `list` | `render-list.ts` |
| `run` / 失败 | `render-inspect` 等 |

## 相关

- [[agent-hub/设计/产品设计 v2]] — 命令与 Inventory 三态
- [[agent-hub/命令参考]]

# Agent Hub · E2E 测试案例（索引）

#agent-hub #testing

> **权威文档**在源码仓库：[`packages/cli/e2e/TEST-CASES.md`](https://github.com/liusheldon238/agent-hub/blob/main/packages/cli/e2e/TEST-CASES.md)  
> 维护流程：**先改案例文档 → 再改 `e2e/*.e2e.test.ts`（案例 ID 对齐）→ `npm run test:e2e`**

## 范围（0.0.1）

| 覆盖 | 不覆盖 |
|------|--------|
| CLI 全子命令（真实子进程） | Electron 桌面 |
| `list` / `run` / `uninstall` 等 | `install --yes` 真装 npm |
| 隔离 `AGENT_HUB_DATA_DIR` | 产品设计中的「整机环境扫描」 |

## 案例统计

**40** 个自动化案例（`E2E-INF-001` … `E2E-EXT-008`），见下表。

| 模块 | 数量 | 说明 |
|------|------|------|
| INF 基础设施 | 2 | 目录隔离、JSONL |
| SMK CLI 基础 | 5 | version、参数错误 |
| INV Inventory | 6 | list / inspect |
| LAU Launcher | 6 | run / config / state |
| LCH 纳管 | 5 | adopt / disown |
| SCN Scan/Install | 5 | scan、install dry-run |
| CLN Cleanup | 3 | uninstall dry-run |
| EXT 扩展 | 8 | adapter、doctor、repair 等 |

## 执行

```bash
cd agent-hub/packages/cli
npm run test:e2e
```

## 相关

- [[agent-hub/实现现状]] — 哪些能力尚未实现，故不进 E2E
- [[agent-hub/开发指南]]

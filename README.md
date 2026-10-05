### 你好，我是 rui08984-dot 👋

我在 **8GB 显卡**上折腾大模型推理优化，也给 AI 编程代理搭基础设施。
所有东西都实测过、有数据、能复现 —— 不写没验证过的结论。

---

#### 🔧 8GB 显存跑大模型（实测调优，含完整深度曲线）

把 27B–35B 级别的模型塞进 8GB 笔记本显卡，附生产配置与实测数据：

| 项目 | 说明 |
|---|---|
| [bonsai2-27b-8g-tuning](https://github.com/rui08984-dot/bonsai2-27b-8g-tuning) | 三值量化 Bonsai-2-27B · PrismML 版本 A/B 对比（+15% PP / +24% TG） |
| [ornith-9b-kvmem-8g-tuning](https://github.com/rui08984-dot/ornith-9b-kvmem-8g-tuning) | KV 缓存放内存 → 128K 上下文 @ 42.7 tok/s |
| [ornith-1.5-35b-8g-tuning](https://github.com/rui08984-dot/ornith-1.5-35b-8g-tuning) | 35B MoE 到 118K 上下文的深度曲线 + turbo4 KV |
| [qwen3.6-35b-8g-tuning](https://github.com/rui08984-dot/qwen3.6-35b-8g-tuning) | Qwen3.6-35B-A3B 基线生产配置 |
| [kat-coder-35b-8g-tuning](https://github.com/rui08984-dot/kat-coder-35b-8g-tuning) | 编码模型 · 工具循环修复 · agentic 基准 |
| [zhrp-gemma4-26b-8g-tuning](https://github.com/rui08984-dot/zhrp-gemma4-26b-8g-tuning) | 中文角色扮演调优 · 三级 ubatch 配方 |

---

#### 🤖 AI 代理基础设施

| 项目 | 说明 |
|---|---|
| [SessionRelay](https://github.com/rui08984-dot/SessionRelay) | **本地优先的 AI 会话记忆层** · 五源捕获 · 中文+语义检索 · MCP 16 工具 |
| [pi-bridge](https://github.com/rui08984-dot/pi-bridge) | **把本地/云端模型变成 MCP 工具** · 命令行验收兜底 · 证据链 · 失败自动升档 |
| [agent-state-stack](https://github.com/rui08984-dot/agent-state-stack) | 跨代理共享状态栈 · 开场简报注入 · 看板与依赖图 |

---

#### 🎲 其他

| 项目 | 说明 |
|---|---|
| [jujian](https://github.com/rui08984-dot/jujian) | 局鉴 · 社交推理游戏复盘台 —— 抓出互相矛盾的声称，每条结论可回查 |
| [agent-skills](https://github.com/rui08984-dot/agent-skills) | Agent Skills 技能包 · AI 音乐制作 SOP + 中文网文写作管线 |

---

<sub>💡 如果哪个项目帮到你了，点个 ⭐ 就是最好的支持 —— 也能让更多人找到它。</sub>

# GLOSSOPETRAE GPT 绕过测试工具

> 基于 [GLOSSOPETRAE v3.1](https://github.com/elder-plinius/GLOSSOPETRAE)（Pliny the Liberator）改造的 GPT 安全绕过测试工具。

## 原作者

**GLOSSOPETRAE** — [Pliny the Liberator](https://github.com/elder-plinius) (@elder_plinius)
- 原项目：https://github.com/elder-plinius/GLOSSOPETRAE
- 论文：[PAPER.md](https://github.com/elder-plinius/GLOSSOPETRAE/blob/main/PAPER.md)
- 许可证：AGPL-3.0

## 本工具新增

基于原引擎新增五种编码方法集成：
- `encode.html` — Web 可视化编码器（三种编码通道）
- `.claude/skills/gpt-bypass/` — Claude Code Skill 集成

## 快速开始

```bash
python3 -m http.server 8765
# 打开 http://localhost:8765/encode.html
```

> ⚠️ 必须通过 HTTP 服务器访问，file:// 协议不支持 ES 模块加载。

## 四种编码方法

| 方法 | 原理 | 适用场景 |
|------|------|---------|
| 🔀 **TokenBreak** | 零宽字符破坏 BPE 分词 | 大多数场景，最稳定 |
| 🔤 **Homoglyph** | Unicode 同形字替换 | 绕过关键词过滤器 |
| 🗣️ **Conlang** | 随机生成语言翻译 + SKILLSTONE | 两步操作，传输层绕过 |
| 🧠 **Semantic Stego** | 30组同义词替换改变文本指纹 | 纯英文输出，清洗无效 |
| 🛡️ **Full Stego 九信道** | 完整隐写引擎 — XOR + Reed-Solomon + CRC32 + 5条信道同时编码 | 加密级隐写 |
| 🛡️ **Full Stego 九信道** | 完整隐写引擎 — XOR + Reed-Solomon + CRC32 + 5条信道同时编码 | 加密级隐写 |

## 许可证

AGPL-3.0 — 详见 [LICENSE](LICENSE)。

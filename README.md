# GLOSSOPETRAE GPT 绕过测试工具

> 基于 [GLOSSOPETRAE v3.1](https://github.com/elder-plinius/GLOSSOPETRAE) 改造的 GPT 安全绕过测试工具。

## 原作者

**GLOSSOPETRAE** — [Pliny the Liberator](https://github.com/elder-plinius) (@elder_plinius)
- 论文: [PAPER.md](https://github.com/elder-plinius/GLOSSOPETRAE/blob/main/PAPER.md)
- 许可证: AGPL-3.0

## 本工具改造内容

在原 GLOSSOPETRAE 引擎基础上新增：
- `encode.html` — 四步可视化编码器（TokenBreak / Homoglyph / Conlang）
- `.claude/skills/gpt-bypass/` — GPT 绕过测试 Skill
- 学术化提示词改写逻辑
- 拆分法、抽象法等进阶策略

## 启动

```bash
python3 -m http.server 8765
# 打开 http://localhost:8765/encode.html
```

## 许可证

AGPL-3.0 — 继承原项目许可证。详见 [LICENSE](LICENSE)。

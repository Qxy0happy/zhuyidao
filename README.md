# zhuyidao — 注意力积分证明构造器

> "注意到"风格定积分不等式证明的 AI 智能体技能包。

## 来源

本仓库的核心内容来自知乎用户 **量化调酒师** 的文章：

- 【优雅技巧】如何优雅地"注意到"关于 e、π 的不等式 ([zhuanlan.zhihu.com/p/669285539](https://zhuanlan.zhihu.com/p/669285539))
- 【人人皆可优雅】注意力计算器自动生成积分证明 ([zhuanlan.zhihu.com/p/20960679909](https://zhuanlan.zhihu.com/p/20960679909))

在线计算器：**[zhuyidao.com](https://zhuyidao.com)**

## 用途

教会 AI 智能体（OpenCode / Claude Code / Copilot CLI）如何构造"注意到"风格的定积分不等式证明。核心原理：

> 要证明 $u > v$，找一个 $[a,b]$ 上的定积分，其值恰好等于 $u - v$，且被积函数在 $[a,b]$ 上恒非负。然后"注意到"即得证。

覆盖**45种不等式类型**和**9种优雅技巧**。

## 依赖

- **Wolfram Language MCP** — 本 skill 需要 Wolfram Language 计算环境来求解积分展开式和线性方程组。请确保你的 AI 编程工具已配置 Wolfram MCP（Wolfram 15+）。
- Python 3.14+（可选，用于 skill-creator 评测脚本）

## 结构

```text
.agents/skills/zhuyidao/
├── SKILL.md                      # 入口：工作流 + Wolfram配方 + 协调界例子
└── references/
    ├── type-index.md             # 路由表（根据不等式形式指向对应家族）
    ├── family-pi-e.md            # π/e 家族（类型 1-6）
    ├── family-log-invtrig.md     # 对数/反三角家族（类型 7-13）
    ├── family-trig.md            # 三角家族（类型 14-19）
    ├── family-hyper.md           # 双曲家族（类型 20-27）
    ├── family-exp-trig.md        # 指数·三角组合（类型 28-30）
    ├── family-special-constants.md  # 特殊常数（类型 31-39）
    └── family-special-functions.md  # 特殊函数（类型 40-45）
```

## Workflow

1. 解析不等式 → 2. 路由到类型 → 3. 读展开式公式 → 4. 列线性方程组 → 5. Wolfram 求解 → 6. 验证非负性 → 7. 呈现"注意到"证明

详细流程见 `SKILL.md`。

## License

Content derived from 量化调酒师's Zhihu articles. The skill implementation is provided as-is for educational and research purposes.

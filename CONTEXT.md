# zhuyidao — 注意力计算器 Skill

A skill that teaches AI agents to construct "注意到" (notice-that) style integral proofs for inequalities of mathematical constants (e, π, etc.), using the systematic method from the article by 量化调酒师.

## Language

**注意力计算器** (Attention Calculator):
A system for generating definite integrals that prove inequalities of the form \(u > v\) by expressing \(u-v\) as \(\int_a^b f(x)\,dx\) with a non-negative integrand. The system uses template integrals with undetermined coefficients, solved via linear equations.

**Skill**:
The root directory. `SKILL.md` is the entrypoint containing workflow, routing logic, Wolfram Language recipes, and examples.

**type-index**:
A reference file at `references/type-index.md` listing all 45 inequality types with their integral templates. Agents route to it by recognizing the function families in the target inequality.

**Wolfram Language evaluation**:
The computational backbone for solving the linear systems that determine template coefficients. Used via the `Wolfram_WolframLanguageEvaluator` MCP tool.

**优雅度三原则** (Three Principles of Elegance):

1. Smaller coefficients are more elegant
2. Fewer inequality statements are more elegant
3. More obviously non-negative integrands are more elegant

_Avoid_: Verbosity, exhaustive enumeration in SKILL.md, hardcoding all 45 types in the main file.

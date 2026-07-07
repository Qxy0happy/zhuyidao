---
name: zhuyidao
description: A skill for constructing "注意到" (notice-that) style definite-integral proofs of inequalities involving e, π, ln, trigonometric/hyperbolic/special functions. Use whenever an agent needs to prove an inequality of the form u > v (or u < v) where u and v involve mathematical constants (e, π, ln q, sin q, cos q, tan q, arcsin q, arctan q, sinh q, cosh q, ζ(s), Γ(x), Catalan constant, Euler constant, error function, etc.) and the target is a rational number or another constant. The skill provides a systematic method: select a template integral → set up linear equations for undetermined coefficients → solve via Wolfram Language → verify non-negativity of integrand → present the "注意到" proof.
---

# zhuyidao — 注意力积分证明构造器

## Core Principle

To prove $u > v$, find a definite integral on $[a,b]$ (usually $[0,1]$) whose value equals exactly $u - v$, with the integrand $f(x) \ge 0$ on $[a,b]$ (equaling 0 at only finitely many points):

$$u - v = \int_a^b f(x)\,dx > 0 \quad\Longrightarrow\quad u > v.$$

The original article by 量化调酒师 catalogs **45 types** of such integrals. This skill teaches you to route to the right type, solve the coefficients, and present the proof.

> **SOURCE ARTICLE** (read for expanded formulas not included in family refs):
> `D:\Projects\zhuyidao\【优雅技巧】如何优雅地"注意到"关于e、π的不等式-量化调酒师的文章\【优雅技巧】如何优雅地"注意到"关于e、π的不等式-量化调酒师的文章.md`

## Workflow

### Step 1: Parse the inequality

Given $u > v$ (or $u < v$), compute $\Delta = u - v$ (or $v - u$). This is what the integral must equal.

### Step 2: Route to the type

Read `references/type-index.md`. It tells you which family your inequality belongs to and which `references/family-*.md` file to read for the expanded integral formulas.

### Step 3: Read the formulas

Read the relevant `references/family-*.md` file. Each family file contains:

- The integral template(s) for each type in that family
- The expanded formulas (integral = linear combination of constants × coefficients) for $n=1,2,3,\dots$
- A reference example
- A pointer back to the source article for additional $n$ values

**If the formula you need is not in the family file** (e.g., you need $n=5$ but only $n=1,2,3$ are given), re-read the relevant section of the source article. The article's expanded formulas cover more $n$ values.

### Step 4: Set up the linear system

The expanded integral is a linear combination of the target constants + rational numbers. Equate coefficients:

- Set the target constant's coefficient to match $\Delta$
- For unwanted constants (e.g., $\ln 2$ in Type 1), set their coefficients to $0$
- Set the constant term to match $-\text{rational}(v)$

This yields a system of linear equations in $\{a,b,c,\dots\}$.

### Step 5: Solve using Wolfram Language

Use `Wolfram_WolframLanguageEvaluator`:

```mathematica
(* 2 variables *)
Solve[{coeff_a == val_a, coeff_b == val_b}, {a, b}]

(* 3 variables *)
Solve[{coeff_a == val_a, coeff_b == val_b, coeff_c == val_c}, {a, b, c}]
```

Start with small $n$. If the resulting polynomial is not non-negative on the domain, increase $n$ and retry.

### Step 6: Verify non-negativity

**For $a+bx$ on $[0,1]$:** $a \ge 0$ and $a+b \ge 0$.

**For $a+bx+cx^2$ on $[0,1]$:**

| Condition | Criterion |
|-----------|-----------|
| $c \le 0$ (opens down) | $a \ge 0,\ a+b+c \ge 0$ |
| $c > 0$, vertex outside $[0,1]$ | $a \ge 0,\ a+b+c \ge 0$ |
| $c > 0$, vertex in $(0,1)$ | $4ac - b^2 \ge 0$ |

For elegance, rewrite $a+bx$ with $b<0$ as $(a+b) + (-b)(1-x)$.

### Step 7: Present the proof

```latex
$$u - v = \frac{1}{D} \int_0^1 \text{[template]} \, dx > 0.$$
证毕！
```

Follow the **Three Principles of Elegance**: smaller coefficients, fewer inequality statements, more obviously non-negative integrand.

## Wolfram Language Recipes

```mathematica
(* Solving a 2-variable system (Type 2, e, n=1): *)
Solve[{-a + 3b == -9, 3a - 8b == 25}, {a, b}]

(* Solving a 3-variable system (Type 1, π, n=2): *)
Solve[{-b/2 == 8, a - c == 0, -2a/3 + 19b/12 + 7c/10 == -25}, {a, b, c}]

(* Iterating over n: won't work directly, you need the expanded formula for each n from the family file. *)
```

For each type, the family file gives the expanded formula for each $n$. Plug in the coefficients from that formula into `Solve[]`.

## Coordinated Bounds (Critical Pattern)

When an inequality involves multiple different constant types (e.g., $e^2 - e^{1/2} - \cos 1 > 26/5$), the most elegant proof splits it into separate bounds and combines them via Technique 9.

**Key insight:** Do NOT find the tightest possible bound for each part independently. Instead, **coordinate** the bounds so they sum EXACTLY to the target — leaving zero residual constant. The Attention Calculator at zhuyidao.com automates this coordinated search.

### Example: $e^2 - e^{1/2} - \cos 1 > \dfrac{26}{5}$

This involves three different types (Type 4 with $q=2$, Type 4 with $q=1/2$, Type 16). The coordinated bounds found by the calculator are:

| Component | Type | Bound | Rational value | Gap from truth |
|-----------|------|-------|---------------|----------------|
| $e^2$ (lower) | 4, $q=2$, $n=...$ | $> \frac{1617167}{218860}$ | $\approx 7.389056099$ | $\approx 1.2\times10^{-8}$ |
| $e^{1/2}$ (upper) | 4, $q=1/2$, $n=2$ | $< \frac{582}{353}$ | $\approx 1.648725212$ | $\approx 3.9\times10^{-6}$ |
| $\cos 1$ (upper) | 16, $n=3$ | $< \frac{67}{124}$ | $\approx 0.540322581$ | $\approx 2.0\times10^{-5}$ |

These three rationals exactly satisfy:
$$\frac{1617167}{218860} - \frac{582}{353} - \frac{67}{124} = \frac{26}{5}$$

So the proof decomposes cleanly with zero excess:

$$
\begin{aligned}
e^2 - e^{1/2} - \cos 1 - \frac{26}{5}
&= \left(e^2 - \frac{1617167}{218860}\right)
+ \left(\frac{582}{353} - e^{1/2}\right)
+ \left(\frac{67}{124} - \cos 1\right) > 0
\end{aligned}
$$

Each bracket is a positive integral of its respective type. The three integrals can be combined into one via Technique 9 (linear combination) for maximum elegance.

**Why this matters:** If you find each bound independently at its tightest, they will almost certainly NOT sum to the target — leaving a residual constant that requires an extra inequality statement. Coordinated search eliminates this, producing a shorter, more elegant proof.

## If your inequality doesn't fit any type

Use **Technique 1 (Split via intermediate)** — find a rational $p$ such that $u > p > v$, prove each half with known types, then combine.

See the source article's "优雅技巧大全" section for 9 techniques: split, continued fractions, direct sqrt comparison, polynomial non-negativity, software assistance, denominator power increase, ln splitting, Padé approximation, and integral combination.

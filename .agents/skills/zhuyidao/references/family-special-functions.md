# Family: Special Functions (Types 40–45)

## Type 40: Riemann Zeta $\zeta(s)$ ($s>1$ integer)

**Definition**: $\zeta(s) := \sum_{n=1}^{\infty} 1/n^s$

**$s$ even ($s=2k$)**: $\zeta(2k)=q(2k)\pi^{2k}$, e.g. $\zeta(2)=\pi^2/6$, $\zeta(4)=\pi^4/90$, $\zeta(6)=\pi^6/945$. Use Type 3.

**$s$ odd ($s=2k+1$)**: integral template ($m$ must be odd):
$$\int_0^1 \frac{x^{m}(1-x^2)^n (a+bx^2)\ln^{2k}x}{1+x^2} dx$$
Domain: $[0,1]$

**$\zeta(3)$ formulas ($k=1$)** — linear combination of $\zeta(3), 1$:

- $m=1,n=0$: $(\frac{3}{16}a-\frac{3}{16}b)\zeta(3) + \frac{1}{4}b$
- $m=1,n=1$: $(\frac{3}{8}a-\frac{3}{8}b)\zeta(3) + (-\frac{1}{4}a+\frac{15}{32}b)$
- $m=3,n=0$: $(-\frac{3}{16}a+\frac{3}{16}b)\zeta(3) + (\frac{1}{4}a-\frac{7}{32}b)$
- $m=3,n=1$: $(-\frac{3}{8}a+\frac{3}{8}b)\zeta(3) + (\frac{15}{32}a-\frac{193}{432}b)$

**$\zeta(5)$ formulas ($k=2$):**

- $m=1,n=0$: $(\frac{45}{64}a-\frac{45}{64}b)\zeta(5) + \frac{3}{4}b$
- $m=1,n=1$: $(\frac{45}{32}a-\frac{45}{32}b)\zeta(5) + (-\frac{3}{4}a+\frac{189}{128}b)$
- $m=3,n=0$: $(-\frac{45}{64}a+\frac{45}{64}b)\zeta(5) + (\frac{3}{4}a-\frac{93}{128}b)$
- $m=3,n=1$: $(-\frac{45}{32}a+\frac{45}{32}b)\zeta(5) + (\frac{189}{128}a-\frac{7549}{5184}b)$

**Undetermined coefficients**: 2 $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $\zeta(3) > 119/99$ via $m=7,n=4$:
$$\zeta(3)-\frac{119}{99} = \int_0^1 \frac{x^{7}(1-x^2)^4(105135+3786824x^2)\ln^2 x}{11045067(1+x^2)}dx > 0$$
For larger $n$ values, re-read the source article's "第40种类型" section.

---

## Type 41: Sine integral $\operatorname{Si}(q)$ ($q>0$)

**Definition**: $\operatorname{Si}(x) := \int_0^x \frac{\sin t}{t}dt$

**Lower bound**: $\int_0^1 (1-x)^n(\frac{1}{x}+a+bx+cx^2)\sin(qx) dx$

**Upper bound**: $\int_0^1 (1-x)^n(\frac{1}{x}+a+bx+cx^2)(qx-\sin(qx)) dx$, domain $[0,1]$

**Expanded ($n=1$, lower)** — $\operatorname{Si}(q)(+1), \sin q, \cos q, 1$:
$$\int_0^1 (1-x)\!\left(\frac{1}{x}+a+bx+cx^2\right)\!\sin(qx) dx = \operatorname{Si}(q) + \frac{-(a+b+c)q^2+6c}{q^4}\sin q + \frac{q^2+(-2b-4c)}{q^3}\cos q + \frac{(a-1)q^2+2(b-c)}{q^3}$$

**Expanded ($n=1$, upper)** — $\operatorname{Si}(q)(-1), \sin q, \cos q, 1$:
$$\int_0^1 (1-x)\!\left(\frac{1}{x}+a+bx+cx^2\right)\!(qx-\sin(qx)) dx = -\operatorname{Si}(q) + \frac{(a+b+c)q^2-6c}{q^4}\sin q + \frac{-q^2+(2b+4c)}{q^3}\cos q + \frac{(30+10a+5b+3c)q^4+60(-a+1)q^2+120(-b+c)}{60q^3}$$

**Undetermined coefficients**: 3 $(a,b,c)$ **|** **Non-negativity**: $a+bx+cx^2 \ge 0$

**Reference example**: $\operatorname{Si}(1/2) > 2/5$ via $n=5$ lower bound:
$$\operatorname{Si}\!\left(\frac{1}{2}\right)-\frac{2}{5} = \int_0^1 (1-x)^5\!\left(\frac{1}{x}+\frac{38448-89x+233x^2}{46080}\right)\!\sin\!\left(\frac{x}{2}\right)dx > 0$$
For larger $n$ values, re-read the source article's "第41种类型" section.

---

## Type 42: Cosine integrals $\operatorname{Cin}(q), \operatorname{Ci}(q)$

**Definitions**: $\operatorname{Cin}(x) := \int_0^x \frac{1-\cos t}{t}dt$, $\operatorname{Ci}(x) := -\int_x^\infty \frac{\cos t}{t}dt$

Relation: $\operatorname{Ci}(q) = \gamma + \ln q - \operatorname{Cin}(q)$ ($\gamma$ from Type 32, $\ln q$ from Type 7)

**Lower bound** (for $\operatorname{Cin}$): $\int_0^1 (1-x)^n(\frac{1}{x}+a+bx+cx^2)(1-\cos(qx)) dx$

**Upper bound**: $\int_0^1 (1-x)^n(\frac{1}{x}+a+bx+cx^2)(\frac{q^2x^2}{2}-1+\cos(qx)) dx$, domain $[0,1]$

**Expanded ($n=1$, lower)** — $\operatorname{Cin}(q)(+1), \sin q, \cos q, 1$:
$$\int_0^1 (1-x)\!\left(\frac{1}{x}+a+bx+cx^2\right)\!(1-\cos(qx)) dx = \operatorname{Cin}(q) + \frac{q^2+(-2b-4c)}{q^3}\sin q + \frac{(a+b+c)q^2-6c}{q^4}\cos q + \frac{(6a+2b+c-12)q^4+12(-a+b)q^2+72c}{12q^4}$$

**Expanded ($n=1$, upper)** — $\operatorname{Cin}(q)(-1)$:
$$\int_0^1 (1-x)\!\left(\frac{1}{x}+a+bx+cx^2\right)\!\left(\frac{q^2x^2}{2}-1+\cos(qx)\right) dx = -\operatorname{Cin}(q) + \frac{-q^2+(2b+4c)}{q^3}\sin q + \frac{-(a+b+c)q^2+6c}{q^4}\cos q + \frac{(5a+3b+2c+10)q^6-10(6a+2b+c-12)q^4+120(a-b)q^2-720c}{120q^4}$$

**Undetermined coefficients**: 3 $(a,b,c)$ **|** **Non-negativity**: $a+bx+cx^2 \ge 0$

**Reference example**: $\operatorname{Cin}(2) > 4/5$ via $n=5$ lower bound:
$$\operatorname{Cin}(2)-\frac{4}{5} = \int_0^1 (1-x)^5\!\left(\frac{1}{x}+\frac{15+40x+8x^2}{315}\right)\!(1-\cos(2x))dx > 0$$
For larger $n$ values, re-read the source article's "第42种类型" section.

---

## Type 43: Exponential integrals $\operatorname{Ein}(q), E_1(q), \operatorname{Ei}(q)$

**Definition**: $\operatorname{Ein}(x) := \int_0^x \frac{1-e^{-t}}{t}dt$ ($q>0$)

Relations: $E_1(q) = \operatorname{Ein}(q) - \ln q - \gamma$ ($q>0$), $\operatorname{Ei}(q) = -\operatorname{Ein}(-q) + \ln(-q) + \gamma$ ($q<0$)

**Lower bound**: $\int_0^1 (1-x)^n(\frac{1}{x}+a+bx)(1-e^{-qx}) dx$

**Upper bound**: $\int_0^1 (1-x)^n(\frac{1}{x}+a+bx)(qx-1+e^{-qx}) dx$, domain $[0,1]$

**Expanded ($n=1$, lower)** — $\operatorname{Ein}(q)(+1), e^{-q}, 1$:
$$\int_0^1 (1-x)\!\left(\frac{1}{x}+a+bx\right)\!(1-e^{-qx}) dx = \operatorname{Ein}(q) + \frac{-q^2+(-a-b)q-2b}{q^3}e^{-q} + \frac{(3a+b-6)q^3+(-6a+6)q^2+(6a-6b)q+12b}{6q^3}$$

**Expanded ($n=1$, upper)** — $\operatorname{Ein}(q)(-1)$:
$$\int_0^1 (1-x)\!\left(\frac{1}{x}+a+bx\right)\!(qx-1+e^{-qx}) dx = -\operatorname{Ein}(q) + \frac{q^2+(a+b)q+2b}{q^3}e^{-q} + \frac{(2a+b+6)q^4+(-6a-2b+12)q^3+(12a-12)q^2+(-12a+12b)q-24b}{12q^3}$$

**Undetermined coefficients**: 2 $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $\operatorname{Ein}(2) < 7/5$ via $n=4$ upper bound:
$$\frac{7}{5} - \operatorname{Ein}(2) = \int_0^1 (1-x)^4\!\left(\frac{1}{x}+\frac{27-7x}{15}\right)\!(2x-1+e^{-2x})dx > 0$$
For larger $n$ values, re-read the source article's "第43种类型" section.

---

## Type 44: Dilogarithm $\operatorname{Li}_2(q)$ ($0<q<1$)

**Definition**: $\operatorname{Li}_2(x) := -\int_0^x \frac{\ln(1-t)}{t}dt = \sum_{k=1}^\infty x^k/k^2$

**Lower bound**: $\int_0^1 (1-x)^n(\frac{1}{x}+a+bx)\ln(\frac{1}{1-qx})dx$

**Upper bound**: $\int_0^1 (1-x)^n(\frac{1}{x}+a+bx)(\frac{qx}{1-qx}-\ln(1-qx))dx$, domain $[0,1]$

**Expanded ($n=1$, lower)** — $\operatorname{Li}_2(q)(+1), \ln(1-q), 1$:
$$\int_0^1 (1-x)\!\left(\frac{1}{x}+a+bx\right)\!\ln\!\left(\frac{1}{1-qx}\right)dx = \operatorname{Li}_2(q) + \frac{(-3a-b+6)q^3+(6a-6)q^2+(-3a+3b)q-2b}{6q^3}\ln(1-q) + \frac{(27a+5b-36)q^2+(-18a+12b)q-12b}{36q^2}$$

**Expanded ($n=1$, upper)** — $\operatorname{Li}_2(q)(-1)$:
$$\int_0^1 (1-x)\!\left(\frac{1}{x}+a+bx\right)\!\left(\frac{qx}{1-qx}+\ln(1-qx)\right)dx = -\operatorname{Li}_2(q) + \frac{(3a+b-12)q^3+(-12a+12)q^2+(9a-9b)q+8b}{6q^3}\ln(1-q) + \frac{(-45a-11b+72)q^2+(54a-30b)q+48b}{36q^2}$$

**Undetermined coefficients**: 2 $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $\operatorname{Li}_2(1/3) < 11/29$ via $n=3$ upper bound:
$$\frac{11}{29}-\operatorname{Li}_2\!\left(\frac{1}{3}\right) = \int_0^1 (1-x)^3\!\left(\frac{1}{x}+\frac{1773-625x}{174}\right)\!\left(\frac{x}{3-x}+\ln\!\left(1-\frac{x}{3}\right)\right)dx > 0$$
For larger $n$ values, re-read the source article's "第44种类型" section.

---

## Type 45: Error function $\operatorname{erf}(q)$

**Definition**: $\operatorname{erf}(x) := \frac{2}{\sqrt{\pi}}\int_0^x e^{-t^2}dt$

**Integral template**: $\int_0^1 x^{n}(1-x)^n (a+bx+cx^2)e^{-(qx)^2} dx$, domain $[0,1]$

**Expanded ($n=1$)** — $\sqrt{\pi}\operatorname{erf}(q), e^{-q^2}, 1$ linear combination:
$$\int_0^1 x(1-x)(a+bx+cx^2)e^{-(qx)^2} dx = \frac{-\sqrt{\pi}(2q^2(a-b)+3c)\operatorname{erf}(q) + 2e^{-q^2}q(2b+c) + 4aq^3 + (-4b+4c)q}{8q^5}$$

A rational bound for $\sqrt{\pi}$ (from Type 3 via $\pi$) eliminates $\sqrt{\pi}$.

**Undetermined coefficients**: 3 $(a,b,c)$ **|** **Non-negativity**: $a+bx+cx^2 \ge 0$

**Reference example**: $\operatorname{erf}(1) > 4/5$ — using $\pi < (16/9)^2$ (so $\sqrt{\pi} < 16/9$) and $n=2$:
$$\operatorname{erf}(1) > \frac{64}{45} \times \frac{9}{16} = \frac{4}{5}$$
For larger $n$ values, re-read the source article's "第45种类型" section.

# Family: Logarithm and Inverse Trig Inequalities (Types 7–13)

## Type 7: $\ln q$ greater/less than a rational ($q>1$ rational)

**Integral template**:
$$\int_0^1 \frac{x^n(1-x)^n(a+bx)}{1+(q-1)x} dx$$
Domain: $[0,1]$

Note: denominator can be raised to $(1+(q-1)x)^m$ for faster convergence.

**Expanded formula ($n=1$)** — linear combination of $\ln q, 1$:
$$\int_0^1 \frac{x(1-x)(a+bx)}{1+(q-1)x} dx = \frac{6}{(q-1)^4}\Big(6q(-qa+a+b)\ln q + (3a+b)q^3 + (-3a-6b)q^2 + (-3a+3b)q + (3a+2b)\Big)$$

**Undetermined coefficients**: 2 — $(a,b)$

**Non-negativity constraint**: $a+bx \ge 0$ on $[0,1]$, i.e. $a \ge 0, a+b \ge 0$

**Reference example**: proving $\ln 3 < 10/9$ using $n=3$:
$$\frac{10}{9}-\ln 3 = \int_0^1 \frac{8x^3(1-x)^3(41-14x)}{81(1+2x)} dx > 0$$

For larger $n$ values, re-read the source article's "第7种类型" section.

---

## Type 8: $(\ln q)^n$ greater/less than a rational ($q>1$, $n$ integer)

**Integral template**:
$$\int_0^1 x^m(1-x)^m(a_0+a_1x+\cdots+a_nx^n)\frac{\ln^{n-1}(1+(q-1)x)}{1+(q-1)x} dx$$
Domain: $[0,1]$

**Expansion**: result is a linear combination of $1, \ln q, (\ln q)^2, \ldots, (\ln q)^n$. There are exactly $n+1$ undetermined coefficients $(a_0,\ldots,a_n)$. The usual strategy is to set the coefficients of $\ln q$ through $(\ln q)^{n-1}$ to zero, then match the constant term and $(\ln q)^n$ coefficient to the target inequality.

**Undetermined coefficients**: $n+1$ — $(a_0,a_1,\ldots,a_n)$

**Non-negativity constraint**: $a_0+a_1x+\cdots+a_nx^n \ge 0$ on $[0,1]$

**Reference example**: proving $(\ln 2)^2 > (\sqrt{17}/6)^2$ using $m=3, n=2$:
$$(\ln 2)^2-\left(\frac{\sqrt{17}}{6}\right)^2 = \int_0^1 \frac{x^3(1-x)^3(365+22058x+20652x^2)\ln(1+x)}{4164(1+x)}dx > 0$$

For larger $n,m$ values, re-read the source article's "第8种类型" section.

---

## Type 9: $\ln \pi$ greater/less than a rational

**Integral template**:
$$\int_0^1 \frac{x^n(1-x)^n(a+bx)}{(1+x)\ln(1/x)} dx$$
Domain: $[0,1]$

**Expanded formulas** — linear combination of $\ln\pi, \ln 2, \ln 3, \ln 5$ with coefficients $(a,b)$:

- **$n=1$**:
  $$\int_0^1 \frac{x(1-x)(a+bx)}{(1+x)\ln(1/x)} dx = (-a+b)\ln\pi + (2a-3b)\ln 2 + b\ln 3$$

- **$n=2$**:
  $$\int_0^1 \frac{x^2(1-x)^2(a+bx)}{(1+x)\ln(1/x)} dx = (2a-2b)\ln\pi + (-8a+12b)\ln 2 + (3a-4b)\ln 3 - b\ln 5$$

The result involves $\ln\pi$ and $\ln q$ ($q$ rational). Use rational bounds for $\ln q$ (from Type 7) to obtain rational bounds for $\ln\pi$.

**Undetermined coefficients**: 2 — $(a,b)$

**Non-negativity constraint**: $a+bx \ge 0$ on $[0,1]$, i.e. $a \ge 0, a+b \ge 0$

**Reference example**: proving $\ln\pi < 6/5$ using $n=1$ with $a=1/2, b=-1/2$, plus bounds $\ln 2 < 61/88$ and $\ln 3 > 469/440$:
$$\ln\pi < \frac{5}{2}\ln 2 - \frac{1}{2}\ln 3 < \frac{5}{2}\cdot\frac{61}{88} - \frac{1}{2}\cdot\frac{469}{440} = \frac{6}{5}$$

For larger $n$ values, re-read the source article's "第9种类型" section.

---

## Type 10: $\arcsin q$ greater/less than a rational ($0<q<1$)

**Integral template**:
$$\int_0^1 \frac{x^{n}(1-x)^{n}(a+bx+cx^2)}{\sqrt{1-(qx)^2}} dx$$
Domain: $[0,1]$

**Expanded formula ($n=1$)** — linear combination of $\arcsin q, \sqrt{1-q^2}, 1$:
$$\int_0^1 \frac{x(1-x)(a+bx+cx^2)}{\sqrt{1-(qx)^2}} dx = \frac{1}{24q^5}\Big(\big((-12a+12b)q^2-9c\big)\arcsin q + \big((-12a-4b-2c)q^3+(16b-7c)q\big)\sqrt{1-q^2} + 24aq^3 + (-16b+16c)q\Big)$$

**Undetermined coefficients**: 3 — $(a,b,c)$

**Non-negativity constraint**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: proving $\arcsin(1/3) < 3/5$ using $n=1$:
$$\frac{3}{5}-\arcsin\frac{1}{3} = \int_0^1 \frac{x(1-x)(1710+37x-236x^2)}{360\sqrt{9-x^2}} dx > 0$$

For larger $n$ values, re-read the source article's "第10种类型" section.

---

## Type 11: $\arccos q$ greater/less than a rational

Two methods:

**Method 1**: Use $\arccos q = \pi/2 - \arcsin q$, combining Type 1 (for $\pi/2$) and Type 10 (for $\arcsin q$).

**Method 2** (direct): $\arccos q = \arcsin\sqrt{1-q^2}$

**Integral template (Method 2)**:
$$\int_0^1 \frac{x^{n}(1-x)^{n}(a+bx)}{\sqrt{1-(1-q^2)x^2}} dx$$
Domain: $[0,1]$

**Expanded formula ($n=1$)** — linear combination of $\sqrt{1-q^2}\arccos q, 1$:
$$\int_0^1 \frac{x(1-x)(a+bx)}{\sqrt{1-(1-q^2)x^2}} dx = \frac{-a+b}{2(1-q^2)^2}\sqrt{1-q^2}\arccos q + \frac{(3a+b)q^3 - 6aq^2 + (-3a+3b)q + (6a-4b)}{6(1-q^2)^2}$$

**Undetermined coefficients**: 2 — $(a,b)$ (Method 2)

**Non-negativity constraint**: $a+bx \ge 0$ on $[0,1]$ (Method 2)

**Reference example**: proving $\arccos(2/3) < 6/7$ via Method 1, using $\pi < 22/7$ and $\arcsin(2/3) > 5/7$:
$$\frac{6}{7}-\arccos\frac{2}{3} = \int_0^1 x^3(1-x)^4\left[\frac{x}{2(1+x^2)}+\frac{4(407682+479468x+130203x^2)}{212625\sqrt{9-4x^2}}\right]dx > 0$$

For larger $n$ values, re-read the source article's "第11种类型" section.

---

## Type 12: $\arctan q$ greater/less than a rational

**Integral template** (all powers of $x$ are even to avoid $\ln(1+q^2)$):
$$\int_0^1 \frac{x^{2n}(1-x^2)^{n}(a+bx^2)}{1+(qx)^2} dx$$
Domain: $[0,1]$

**Expanded formula ($n=1$)** — linear combination of $\arctan q, 1$:
$$\int_0^1 \frac{x^{2}(1-x^2)(a+bx^2)}{1+(qx)^2} dx = \frac{1}{15q^7}\Big(15\big(-aq^4+(-a+b)q^2+b\big)\arctan q + (10a+2b)q^5 + (15a-10b)q^3 - 15bq\Big)$$

**Undetermined coefficients**: 2 — $(a,b)$

**Non-negativity constraint**: $a+bx^2 \ge 0$ on $[0,1]$, i.e. $a \ge 0, a+b \ge 0$

**Reference example**: proving $\arctan 2 < 6/5$ using $n=3$:
$$\frac{6}{5}-\arctan 2 = \int_0^1 \frac{x^6(1-x^2)^3(87917-41548x^2)}{1500(1+4x^2)}dx > 0$$

For larger $n$ values, re-read the source article's "第12种类型" section.

---

## Type 13: $\operatorname{arccot} q$ greater/less than a rational

Reduce to Type 12 via $\operatorname{arccot} q = \arctan(1/q)$.

**Reference example**: proving $\operatorname{arccot}(1/2) < 6/5$:
$$\frac{6}{5}-\operatorname{arccot}\frac{1}{2} = \frac{6}{5}-\arctan 2 = \int_0^1 \frac{x^6(1-x^2)^3(87917-41548x^2)}{1500(1+4x^2)}dx > 0$$

For larger $n$ values, re-read the source article's "第13种类型" section.

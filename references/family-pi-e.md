# Family: π and e Inequalities (Types 1–6)

## Type 1: π greater/less than a rational

**Integral template**: $\displaystyle \int_0^1 \frac{x^n(1-x)^n(a+bx+cx^2)}{1+x^2} dx$, domain $[0,1]$

**Expanded formulas** (linear combination of $\pi$, $\ln 2$, $1$):

- **$n=1$**: $\frac{1}{4}(a-b-c)\pi + \frac{1}{2}(a+b-c)\ln 2 + (-a + \frac{1}{2}b + \frac{7}{6}c)$
- **$n=2$**: $-\frac{b}{2}\pi + (a-c)\ln 2 + (-\frac{2}{3}a + \frac{19}{12}b + \frac{7}{10}c)$
- **$n=3$**: $\frac{1}{2}(-a-b+c)\pi + (a-b-c)\ln 2 + (\frac{53}{60}a + \frac{34}{15}b - \frac{92}{105}c)$
- **$n=4$**: $(-a+c)\pi - 2b\ln 2 + (\frac{22}{7}a + \frac{233}{168}b - \frac{1979}{630}c)$

**Undetermined coefficients**: 3 — $(a,b,c)$ **|** **Non-negativity**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: $8\pi > 25$ via $n=2$, $a=10,b=-16,c=10$:
$$\int_0^1 \frac{x^2(1-x)^2(10-16x+10x^2)}{1+x^2} dx = 8\pi - 25 > 0$$
For larger $n$ values, re-read the source article's "第1种类型" section.

---

## Type 2: e greater/less than a rational

**Integral template**: $\displaystyle \int_0^1 x^n(1-x)^n(a+bx)e^{x} dx$, domain $[0,1]$

**Expanded formulas** ($e, 1$ linear combination):

- **$n=1$**: $(-a+3b)e + (3a-8b)$
- **$n=2$**: $2(7a-32b)e + 2(-19a+87b)$
- **$n=3$**: $6(-71a+465b)e + 6(193a-1264b)$

**Undetermined coefficients**: 2 — $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $9e < 25$ via $n=1$, $a=3,b=-2$:
$$\int_0^1 x(1-x)(3-2x)e^x dx = 25-9e > 0$$
For larger $n$ values, re-read the source article's "第2种类型" section.

---

## Type 3: πⁿ greater/less than a rational ($n$ integer, $m+n$ odd)

**Integral template**: $\displaystyle \int_0^1 \frac{x^m (a+bx^2)\ln^{n-1}(1/x)}{1+x^2} dx$, domain $[0,1]$

For larger $m$, add $(1-x^2)^k$: $\int_0^1 \frac{x^m(1-x^2)^k (a+bx^2)\ln^{n-1}(1/x)}{1+x^2} dx$

**Expanded formulas** — linear combination of $\pi^n, 1$ with coefficients $(a,b)$:

- **$n=2, m=1$**: $\frac{1}{48}(a-b)\pi^2 + \frac{1}{4}b$
- **$n=2, m=3$**: $\frac{1}{48}(-a+b)\pi^2 + (\frac{1}{4}a - \frac{3}{16}b)$
- **$n=3, m=0$**: $\frac{1}{16}(a-b)\pi^3 + 2b$
- **$n=3, m=2$**: $\frac{1}{16}(-a+b)\pi^3 + (2a - \frac{52}{27}b)$
- **$n=4, m=1$**: $\frac{7}{1920}(a-b)\pi^4 + \frac{3}{8}b$
- **$n=4, m=3$**: $\frac{7}{1920}(-a+b)\pi^4 + (\frac{3}{8}a - \frac{45}{128}b)$
- **$n=5, m=0$**: $\frac{5}{64}(a-b)\pi^5 + 24b$
- **$n=5, m=2$**: $\frac{5}{64}(-a+b)\pi^5 + (24a - \frac{1936}{81}b)$

**Undetermined coefficients**: 2 — $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $\pi^3 > 31$ via $n=3, m=12$:
$$\pi^3-31 = \int_0^1 \frac{x^{12} (1091239949453-240010278547 x^2) \ln^2(1/x)}{83203139250(1+x^2)} dx > 0$$
For larger $n$ values, re-read the source article's "第3种类型" section.

---

## Type 4: $e^q$ greater/less than a rational ($q$ rational)

**Integral template**: $\displaystyle \int_0^1 x^n(1-x)^n(a+bx)e^{qx} dx$, domain $[0,1]$

**Expanded formula ($n=1$)** — linear combination of $e^q, 1$:
$$\int_0^1 x(1-x)(a+bx)e^{qx} dx = \frac{((a+b)q^2+(-2a-4b)q+6b)e^q + (aq^2+2(a-b)q-6b)}{q^4}$$

**Undetermined coefficients**: 2 — $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $e^3 > 20$ (using $n_1=3, n_2=4$):
$$\int_0^1 x^3(1-x)^4(28+33x)e^{3x} dx = 8(e^3-20) > 0$$
For larger $n$ values, re-read the source article's "第4种类型" section.

---

## Type 5: $e^\pi$ greater/less than a rational

**Integral template**: $\displaystyle \int_0^\pi \sin^n x(1-\sin x)^n(a+b\sin x)e^{x} dx$, domain $[0,\pi]$

**Expanded formulas** — linear combination of $e^\pi, 1$:

- **$n=1$**: $(\frac{1}{10}a+\frac{1}{10}b)e^\pi + (\frac{9}{10}a-\frac{7}{10}b)$
- **$n=2$**: $(\frac{7}{85}a-\frac{15}{442}b)e^\pi + (-\frac{109}{85}a+\frac{2421}{2210}b)$

**Undetermined coefficients**: 2 — $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $e^\pi > 22$ via $n=3$:
$$\int_0^\pi e^x\sin^3{x}(1-\sin x)^3 (3984+30965\sin x) dx = \frac{11184}{5}(e^\pi-22) > 0$$
For larger $n$ values, re-read the source article's "第5种类型" section.

---

## Type 6: $e^{q\pi}$ greater/less than a rational ($q$ rational)

**Integral template**: $\displaystyle \int_0^\pi \sin^n x(1-\sin x)^n(a+b\sin x)e^{qx} dx$, domain $[0,\pi]$

**Expanded formula ($n=1$)** — linear combination of $e^{q\pi}, 1$:
$$\int_0^\pi \sin x(1-\sin x)(a+b\sin x)e^{qx} dx = \frac{1}{q(q^6+14q^4+49q^2+36)}\Big(\big(aq^5+(-2a+2b)q^4+(13a-6b)q^3+(-20a+20b)q^2+(36a-24b)q+(-18a+18b)\big)e^{q\pi} + \big(aq^5+(2a-2b)q^4+(13a-6b)q^3+(20a-20b)q^2+(36a-24b)q+(18a-18b)\big)\Big)$$

**Undetermined coefficients**: 2 — $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $e^{3\pi/4} > 21/2$ ($n_1=3,n_2=4$):
$$\int_0^\pi e^{3x/4}\sin^3{x}(1-\sin x)^4 (1888358000+14100605983\sin x) dx = \frac{76404129792}{13}\!\left(e^{3\pi/4}-\frac{21}{2}\right) > 0$$
For larger $n$ values, re-read the source article's "第6种类型" section.

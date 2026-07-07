# Family: Special Constants (Types 31–39)

## Type 31: Catalan constant $C$

**Definition**: $C := \sum_{n=0}^{\infty} (-1)^n/(2n+1)^2$

**Integral template**: $\displaystyle \int_0^1 \frac{x^{2n}(1-x^2)^n (a+bx^2)\ln(1/x)}{1+x^2} dx$, domain $[0,1]$

**Expanded formulas** ($C, 1$ linear combination):

- **$n=1$**: $(-2a+2b)C + (\frac{17}{9}a - \frac{409}{225}b)$
- **$n=2$**: $(4a-4b)C + (-\frac{40298}{11025}a + \frac{363826}{99225}b)$
- **$n=3$**: $(-8a+8b)C + (\frac{12571156}{1715175}a - \frac{14867117548}{2029052025}b)$

**Undetermined coefficients**: 2 $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $C < 109/119$ via $n=5$:
$$\frac{109}{119}-C = \int_0^1\frac{x^{10}(1-x^2)^5(733466923-640846037x^2)\ln(1/x)}{43978014720(1+x^2)}dx > 0$$
For larger $n$ values, re-read the source article's "第31种类型" section.

---

## Type 32: Euler constant $\gamma$

**Definition**: $\gamma := \lim_{n\to\infty}[(\sum_{k=1}^n 1/k)-\ln n]$

**Integral relation**: $\int_0^1 (\frac{1}{\ln x}+\frac{1}{1-x})dx = \gamma$

Use bounding functions: $f_{\text{lower}}(x)=1/2$, $f_{\text{upper}}(x)=(2-x)/2$

**Lower bound**: $\int_0^1 (\frac{1}{\ln x}+\frac{1}{1-x}-\frac{1}{2})x^n dx$ → $n=1$: $\gamma + \ln 2 - 5/4$; $n=2$: $\gamma + \ln 3 - 5/3$; $n=3$: $\gamma + \ln 4 - 47/24$ (all $>0$)
**Upper bound**: $\int_0^1 (\frac{2-x}{2}-\frac{1}{\ln x}-\frac{1}{1-x})x^n dx$ → $n=1$: $4/3 - \ln 2 - \gamma$; $n=2$: $47/24 - \ln 3 - \gamma$; $n=3$: $119/60 - \ln 4 - \gamma$ (all $>0$)
The $\ln(n+1)$ terms are bounded via Type 7 for pure rational bounds.

**Non-negativity**: integrand $\ge 0$ by construction. No undetermined coefficients.

**Reference example**: $\gamma > 4/7$ via $n=8$ lower bound + $\ln 3$ upper bound:
$$\gamma > \frac{6989}{2520} - 2\ln 3 > \frac{4}{7}$$
For larger $n$ values, re-read the source article's "第32种类型" section.

---

## Type 33: Golden ratio $\phi = (1+\sqrt5)/2$

**Integral template**: $\displaystyle \int_0^1 x^{n}(1-x)^n (a+bx)\sqrt{4+x}\ dx$, domain $[0,1]$

**Expanded formulas** ($\phi, 1$ linear combination):

- **$n=1$**: $\frac{40(-39a+101b)}{63}\phi + \frac{4(1061a-2719b)}{105}$
- **$n=2$**: $\frac{800(2769a-8261b)}{9009}\phi + \frac{16(-74659a+222783b)}{3003}$

**Undetermined coefficients**: 2 $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $\phi < 89/55$ via $n=2$:
$$\frac{89}{55} - \phi = \int_0^1 \frac{3x^{2}(1-x)^{2}(451+663x)\sqrt{4+x}}{1126400} dx > 0$$
For larger $n$ values, re-read the source article's "第33种类型" section.

---

## Type 34: Glaisher-Kinkelin $\ln A$

**Definition**: $A := \lim_{n\to\infty} \frac{\prod_{i=1}^n i^i}{n^{n^2/2+n/2+1/12}e^{-n^2/4}}$

**Integral template**: $\displaystyle \int_0^1 \frac{x^n(1-x)^n(a+bx)}{(1+x)^2\ln(1/x)} dx$, domain $[0,1]$

**Expanded formulas** ($\ln A, \ln\pi, \ln 2, \ln 3, 1$ linear combination):

- **$n=1$**: $(-6a+6b)\ln A + \frac{3a-5b}{2}\ln\pi + \frac{-5a+17b}{6}\ln 2 + \frac{a-b}{2}$
- **$n=2$**: $(12a-12b)\ln A + (-6a+8b)\ln\pi + \frac{26a-50b}{3}\ln 2 + (-a+4b)\ln 3 + (-a+b)$

Choose $(a,b)$ to eliminate $\ln\pi$ (coefficient $=0$), set $\ln A$ coefficient to $\pm 1$, then use rational bounds for $\ln 2,\ln 3$ (Type 7).

**Undetermined coefficients**: 2 $(a,b)$ **|** **Non-negativity**: $a \ge 0, a+b \ge 0$

**Reference example**: $\ln A > 2/9$ via $n=2$, $a=1/3, b=1/4$:
$$\ln A > -\frac{2}{3}\ln 3 + \frac{23}{18}\ln 2 + \frac{1}{12} > \frac{2}{9}$$
For larger $n$ values, re-read the source article's "第34种类型" section.

---

## Type 35: Lemniscate ratio $\varpi$ & Type 36: Gauss constant $G$

**Definitions**: $\varpi = \frac{1}{2\sqrt{2\pi}}\Gamma(1/4)^2$, $G = \varpi/\pi = (\Gamma(1/4))^2/(2\pi)^{3/2}$

**Lower bound templates**:

- $\varpi$ ($4n+1$): $\int_0^1 \frac{x^{4n+1}(1-x)(a+bx^4)}{\pi\sqrt{1-x^4}} dx$
- $G$ ($4n$): $\int_0^1 \frac{x^{4n}(1-x)(a+bx^4)}{\pi\sqrt{1-x^4}} dx$

**Upper bound templates**:

- $\varpi$ ($4n+3$): $\int_0^1 \frac{x^{4n+3}(1-x)(a+bx^4)}{\sqrt{1-x^4}} dx$
- $G$ ($4n+2$): $\int_0^1 \frac{x^{4n+2}(1-x)(a+bx^4)}{\sqrt{1-x^4}} dx$

Domain: $[0,1]$. All use coefficients $(a,b)$, non-negativity $a \ge 0, a+b \ge 0$.

**Expanded ($n=0$):**

- $\varpi$ lower: $(\frac{a}{4}+\frac{b}{8}) - (\frac{a}{2}+\frac{3b}{10})\varpi^{-1}$
- $\varpi$ upper: $(\frac{a}{2}+\frac{b}{3}) - (\frac{a}{6}+\frac{5b}{42})\varpi$
- $G$ lower: $(\frac{a}{2}+\frac{b}{6})G - (\frac{a}{4}+\frac{b}{8})$
- $G$ upper: $(\frac{a}{2}+\frac{3b}{10})G^{-1} - (\frac{a}{2}+\frac{b}{3})$

**Reference examples**:

- $\varpi < 3$: $3-\varpi = \int_0^1 \frac{6x^{3}(1-x)}{\sqrt{1-x^4}} dx > 0$
- $G > 4/5$ ($n=2$): $G-\frac{4}{5} = \int_0^1 \frac{2x^{8}(1-x)(3+22x^4)}{5\pi\sqrt{1-x^4}} dx > 0$

For larger $n$ values, re-read the source article's "第35种类型" and "第36种类型" sections.

---

## Type 37: $\Gamma(1/4), \Gamma(3/4)$ and Type 38: $\Gamma(1/3), \Gamma(2/3)$

**Type 37** — $\Gamma(1/4)\Gamma(3/4) = \sqrt{2}\pi$. Same forms as Types 35/36. $4n+1$ → $\Gamma(1/4)$ lower / $\Gamma(3/4)$ upper; $4n+3$ → reverse. **$n=0$ expansions:**
$$\int_0^1 \frac{x(1-x)(a+bx^4)}{\pi\sqrt{1-x^4}} dx = (\frac{a}{4}+\frac{b}{8}) - (a+\frac{3b}{5})\frac{\sqrt{2\pi}}{(\Gamma(1/4))^2},\quad \int_0^1 \frac{x^{3}(1-x)(a+bx^4)}{\sqrt{1-x^4}} dx = (\frac{a}{2}+\frac{b}{3}) - (\frac{a}{12}+\frac{5b}{84})\frac{(\Gamma(1/4))^2}{\sqrt{2\pi}}$$
Need rational bounds for $\sqrt{2\pi}$ (Type 3). **Example**: $\Gamma(1/4) < 11/3$: $(\Gamma(1/4))^2 < \frac{220}{87} \cdot \frac{319}{60} = (11/3)^2$.

**Type 38** — $\Gamma(1/3)\Gamma(2/3) = 2\pi/\sqrt{3}$. Templates: $3n+1$ form $\int_0^1 \frac{x^{3n+1}(1-x)(a+bx^3)}{\sqrt{1-x^3}} dx$ → $\Gamma(1/3)$ upper / $\Gamma(2/3)$ lower; $3n+2$ form → reverse. **$n=0$ ($3n+1$):**
$$\int_0^1 \frac{x(1-x)(a+bx^3)}{\sqrt{1-x^3}} dx = \frac{4\sqrt[3]{2}\pi^2(7a+4b)}{21(\Gamma(1/3))^3} - \frac{6a+4b}{9}$$
Need rational bounds for $\pi$ or $\pi^2$ (Type 3). **Example**: $\Gamma(1/3) > 9/4$: $(\Gamma(1/3))^3 > \frac{9}{14} \cdot \frac{400\sqrt[3]{2}\pi^2}{273} > (9/4)^3$.

For larger $n$ values, re-read the source article's "第37种类型" and "第38种类型" sections.

---

## Type 39: $\psi'(1/3), \psi'(2/3)$

**Relations**: $\psi'(1/2) = \pi^2/2$, $\psi'(1/4) = \pi^2+8C$, $\psi'(3/4) = \pi^2-8C$, $\psi'(1/3)+\psi'(2/3) = 4\pi^2/3$

**Integral template**: $\int_0^1 \frac{x^n(a+bx)\ln(1/x)}{1+x+x^2} dx$, domain $[0,1]$. Undetermined: 2 $(a,b)$, non-negativity: $a \ge 0, a+b \ge 0$.

**Expanded** ($\psi'(1/3), \pi^2, 1$ linear combination):

- **$n=0$**: $(\frac{2a}{9}-\frac{b}{9})\psi'(1/3) + (-\frac{4a}{27}+\frac{7b}{54})\pi^2$
- **$n=1$**: $(-\frac{a}{9}-\frac{b}{9})\psi'(1/3) + (\frac{7a}{54}+\frac{b}{54})\pi^2 + b$
- **$n=2$**: $(-\frac{a}{9}+\frac{2b}{9})\psi'(1/3) + (\frac{a}{54}-\frac{4b}{27})\pi^2 + (a-\frac{3b}{4})$

Need rational $\pi^2$ bounds (Type 3). **Example**: $\psi'(1/3) < 21/2$ via $n=2$:
$$\frac{21}{2}-\psi'(1/3) = \int_0^1 3x^2(1-x)\left(\frac{4x(1+x)}{1+x^2}+\frac{1}{1+x+x^2}\right)\ln(1/x) dx > 0$$
For larger $n$ values, re-read the source article's "第39种类型" section.

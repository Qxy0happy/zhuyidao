# Family: Hyperbolic and Inverse Hyperbolic Inequalities (Types 20–27)

## Type 20: $\operatorname{arsinh} q$ greater/less than a rational ($q>0$)

**Integral template**:
$$\int_0^1 \frac{x^{n}(1-x)^{n}(a+bx+cx^2)}{\sqrt{1+(qx)^2}} dx$$
Domain: $[0,1]$

**Expanded formula ($n=1$)** — linear combination of $\operatorname{arsinh} q, \sqrt{1+q^2}, 1$:
$$\int_0^1 \frac{x(1-x)(a+bx+cx^2)}{\sqrt{1+(qx)^2}} dx = \frac{1}{24q^5}\Big(\big((12a-12b)q^2-9c\big)\operatorname{arsinh} q + \big((12a+4b+2c)q^3+(16b-7c)q\big)\sqrt{1+q^2} - 24aq^3 + (-16b+16c)q\Big)$$

**Undetermined coefficients**: 3 — $(a,b,c)$

**Non-negativity constraint**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: proving $\operatorname{arsinh}(1/3) > 3/10$ using $n=1$:
$$\operatorname{arsinh}\frac{1}{3}-\frac{3}{10}= \int_0^1 \frac{x(1-x)(45-2x+4x^2)}{90\sqrt{9+x^2}} dx > 0$$

For larger $n$ values, re-read the source article's "第20种类型" section.

---

## Type 21: $\operatorname{arcosh} q$ greater/less than a rational ($q>1$)

**Relation**: $\operatorname{arcosh}(q) = \operatorname{arsinh}(\sqrt{q^2-1})$

**Integral template**:
$$\int_0^1 \frac{x^{n}(1-x)^{n}(a+bx)}{\sqrt{1+(q^2-1)x^2}} dx$$
Domain: $[0,1]$

**Expansion**: result is a linear combination of $\sqrt{q^2-1}\operatorname{arcosh} q$ and $1$.

**Undetermined coefficients**: 2 — $(a,b)$

**Non-negativity constraint**: $a+bx \ge 0$ on $[0,1]$, i.e. $a \ge 0, a+b \ge 0$

**Reference example**: proving $\operatorname{arcosh}(3/2) > 4/5$ using $n=1$:
$$\operatorname{arcosh}\frac{3}{2}-\frac{4}{5}= \int_0^1 \frac{5x(1-x)}{16\sqrt{4+5x^2}}\left(\frac{341}{48+23\sqrt5}+\frac{393(1-x)}{2(16+5\sqrt5)}\right) dx > 0$$

For larger $n$ values, re-read the source article's "第21种类型" section.

---

## Type 22: $\operatorname{artanh} q$ greater/less than a rational ($-1<q<1$)

**Reduction**: $\operatorname{artanh} q = \frac{1}{2}\ln\frac{1+q}{1-q}$. Let $\tilde q = \frac{1+q}{1-q}$ (rational), then use Type 7 integral for $\ln \tilde q$:
$$\int_0^1 \frac{x^n(1-x)^n(a+bx)}{1+(\tilde q-1)x} dx$$

**Undetermined coefficients**: 2 — $(a,b)$

**Non-negativity constraint**: $a+bx \ge 0$ on $[0,1]$, i.e. $a \ge 0, a+b \ge 0$

**Reference example**: proving $\operatorname{artanh}(1/2) < 5/9$, reducing to $\ln 3 < 10/9$:
$$\frac{5}{9}-\operatorname{artanh}\frac{1}{2} = \frac{1}{2}\left(\frac{10}{9}-\ln 3\right) = \int_0^1 \frac{4x^3(1-x)^3(41-14x)}{81(1+2x)} dx > 0$$

For larger $n$ values, re-read the source article's "第22种类型" section.

---

## Type 23: $\operatorname{arcoth} q$ greater/less than a rational ($q>1$)

**Reduction**: $\operatorname{arcoth} q = \frac{1}{2}\ln\frac{q+1}{q-1}$. Let $\tilde q = \frac{q+1}{q-1}$ (rational), then use Type 7 integral for $\ln \tilde q$.

**Reference example**: proving $\operatorname{arcoth}(2) < 5/9$, reducing to $\ln 3 < 10/9$:
$$\frac{5}{9}-\operatorname{arcoth}(2) = \frac{1}{2}\left(\frac{10}{9}-\ln 3\right) = \int_0^1 \frac{4x^3(1-x)^3(41-14x)}{81(1+2x)} dx > 0$$

For larger $n$ values, re-read the source article's "第23种类型" section.

---

## Type 24: $\sinh q$ greater/less than a rational

**Integral template**:
$$\int_0^1 x^n(1-x)^n(a+bx+cx^2)\sinh(qx) dx$$
Domain: $[0,1]$

**Expanded formula ($n=1$)** — linear combination of $\sinh q, \cosh q, 1$:
$$\int_0^1 x(1-x)(a+bx+cx^2)\sinh(qx) dx = \frac{(a+b+c)q^3+(6b+18c)q}{q^5}\sinh q + \frac{-(2a+4b+6c)q^2-24c}{q^5}\cosh q + \frac{(2a-2b)q^2+24c}{q^5}$$

**Undetermined coefficients**: 3 — $(a,b,c)$

**Non-negativity constraint**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: proving $\sinh(2/3) > 7/10$ using $n=1$:
$$\sinh\frac{2}{3} - \frac{7}{10} = \frac{1}{405}\int_0^1 x(1-x)(112+19x-5x^2)\sinh\frac{2x}{3}dx > 0$$

For larger $n$ values, re-read the source article's "第24种类型" section.

---

## Type 25: $\cosh q$ greater/less than a rational

Same integral template as Type 24:
$$\int_0^1 x^n(1-x)^n(a+bx+cx^2)\sinh(qx) dx$$
Result is a linear combination of $\sinh q, \cosh q, 1$.

**Undetermined coefficients**: 3 — $(a,b,c)$

**Non-negativity constraint**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: proving $\cosh(5/2) > 6$ using $n=2$:
$$\cosh\frac{5}{2} - 6 = \frac{5}{848}\int_0^1 x^2(1-x)^2(798-840x+215x^2)\sinh\frac{5x}{2}dx > 0$$

For larger $n$ values, re-read the source article's "第25种类型" section.

---

## Type 26: $\tanh q$ greater/less than a rational

Convert $\tanh q > p$ into $\sinh q - p\cosh q > 0$, then use the Type 24 integral template. Result is $\sinh q, \cosh q, 1$ linear combination. Divide by $\cosh q$ to obtain the $\tanh$ inequality.

**Undetermined coefficients**: 3 — $(a,b,c)$

**Non-negativity constraint**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: proving $\tanh(2/3) < 3/5$ using $n=1$:
$$\frac{3}{5}-\tanh\frac{2}{3} = \int_0^1 \frac{2x(1-x)(26-x-x^2)\sinh(2x/3)}{135\cosh(2/3)}dx > 0$$

For larger $n$ values, re-read the source article's "第26种类型" section.

---

## Type 27: $\coth q$ greater/less than a rational

Reduce via $\coth q = 1/\tanh q$, using Type 26 bounds for $\tanh q$.

**Reference example**: proving $\coth(2/3) > 5/3$, using $\tanh(2/3) < 3/5$:
$$\coth\frac{2}{3} - \frac{3}{5} = \int_0^1 \frac{2x(1-x)(26-x-x^2)\sinh(2x/3)}{81\sinh(2/3)} dx > 0$$

For larger $n$ values, re-read the source article's "第27种类型" section.

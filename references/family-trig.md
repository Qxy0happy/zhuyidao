# Family: Trigonometric Inequalities (Types 14–19)

## Type 14: $\sin q$ greater/less than a rational ($q$ rational)

**Integral template** (use $\sin(qx)$ or $\cos(qx)$ as integrand):
$$\int_0^1 x^n(1-x)^n(a+bx+cx^2)\sin(qx) dx$$
Domain: $[0,1]$

**Expanded formula ($n=1$)** — linear combination of $\sin q, \cos q, 1$:
$$\int_0^1 x(1-x)(a+bx+cx^2)\sin(qx) dx = \frac{-(a+b+c)q^3+(6b+18c)q}{q^5}\sin q + \frac{-(2a+4b+6c)q^2+24c}{q^5}\cos q + \frac{(-2a+2b)q^2+24c}{q^5}$$

**Undetermined coefficients**: 3 — $(a,b,c)$

**Non-negativity constraint**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: proving $\sin(3/5) > 1/3$ using $n=1$:
$$\sin\frac{3}{5} - \frac{1}{3} = \frac{1}{750}\int_0^1 x(1-x)(3571-102x+111x^2)\sin\frac{3x}{5}dx > 0$$

For larger $n$ values, re-read the source article's "第14种类型" section.

---

## Type 15: $\sin(\pi q)$ or $\sin(q^\circ)$ greater/less than a rational

**Integral template** (for $0<q<1/2$):
$$\int_0^{\pi/2} \sin^n x(1-\sin x)^n(a+b\sin x)\sin((1-2q)x) dx$$
Domain: $[0,\pi/2]$

**Expanded formula ($n=1$)** — linear combination of $\sin(\pi q), 1$:
$$\int_0^{\pi/2} \sin x(1-\sin x)(a+b\sin x)\sin((1-2q)x) dx = \frac{1}{8q(8q^6-28q^5+14q^4+35q^3-28q^2-7q+6)}\Big[\big((-8a-8b)q^4+(16a+16b)q^3+(2a-10b)q^2+(-10a+2b)q+12a-9b\big)\sin(\pi q) + \big((16b-16a)q^4+(-32b+32a)q^3+(16a-16b)q^2+(32b-32a)q\big)\Big]$$

**Undetermined coefficients**: 2 — $(a,b)$

**Non-negativity constraint**: $a+b\sin x \ge 0$ on $[0,\pi/2]$, i.e. $a \ge 0, a+b \ge 0$

**Reference example**: proving $\sin(\pi/7) < 4/9$ using $n=2$:
$$\frac{4}{9} - \sin\frac{\pi}{7} = \frac{10}{7512729}\int_0^{\pi/2} \sin^2 x(1-\sin x)^2(382249+169240\sin x)\sin\!\left(\frac{5x}{7}\right)dx > 0$$

For larger $n$ values, re-read the source article's "第15种类型" section.

---

## Type 16: $\cos q$ greater/less than a rational

Same integral template as Type 14:
$$\int_0^1 x^n(1-x)^n(a+bx+cx^2)\sin(qx) dx$$
(Domains and form identical to Type 14.)

**Expanded formula** — same as Type 14; result is $\sin q, \cos q, 1$ linear combination.

**Undetermined coefficients**: 3 — $(a,b,c)$

**Non-negativity constraint**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: proving $\cos 1 < 6/11$ via undetermined coefficients:
$$\frac{6}{11}-\cos 1 = \int_0^1 \frac{(1-x)^2(2(1-x)+x^2)\sin x}{22}dx > 0$$

For larger $n$ values, re-read the source article's "第16种类型" section.

---

## Type 17: $\cos(\pi q)$ or $\cos(q^\circ)$ greater/less than a rational

**Integral template** (for $0<q<1/2$):
$$\int_0^{\pi/2} \sin^n x(1-\sin x)^n(a+b\sin x)\sin(2qx) dx$$
Domain: $[0,\pi/2]$

**Expanded formula ($n=1$)** — linear combination of $\cos(\pi q), 1$:
$$\int_0^{\pi/2} \sin x(1-\sin x)(a+b\sin x)\sin(2qx) dx = \frac{1}{4q(16q^6-56q^4+49q^2-9)}\Big[\big((8a+8b)q^4+(-14a-2b)q^2+(-9a+9b)\big)\cos(\pi q) + \big((16a-16b)q^4+(-40a+40b)q^2+(9a-9b)\big)\Big]$$

**Undetermined coefficients**: 2 — $(a,b)$

**Non-negativity constraint**: $a+b\sin x \ge 0$ on $[0,\pi/2]$, i.e. $a \ge 0, a+b \ge 0$

**Reference example**: proving $\cos 40^\circ > 3/4$ using $n=1$:
$$\cos 40^\circ - \frac{3}{4} = \frac{7}{23328}\int_0^{\pi/2} \sin x\sin(4x/9)(1-\sin x)(1399-713\sin x)dx > 0$$

For larger $n$ values, re-read the source article's "第17种类型" section.

---

## Type 18: $\tan q$ greater/less than a rational

Convert $\tan q > p$ into $\sin q - p\cos q > 0$, then use the Type 14 integral template:
$$\int_0^1 x^n(1-x)^n(a+bx+cx^2)\sin(qx) dx$$
The result is a linear combination of $\sin q, \cos q, 1$. After solving for $(a,b,c)$, divide by $\cos q$ to obtain the $\tan q$ inequality.

**Undetermined coefficients**: 3 — $(a,b,c)$

**Non-negativity constraint**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: proving $\tan(6/5) > 2$ using $n=1$:
$$\tan\frac{6}{5} - 2 = \int_0^1 \frac{8x(1-x)(31+6x+3x^2)\sin(6x/5)}{125\cos(6/5)} dx > 0$$

For larger $n$ values, re-read the source article's "第18种类型" section.

---

## Type 19: $\cot q$ greater/less than a rational

Reduce via $\cot q = 1/\tan q$, using Type 18 bounds for $\tan q$.

**Reference example**: proving $\cot(6/5) < 1/2$, using $\tan(6/5) > 2$:
$$\frac{1}{2}-\cot\frac{6}{5} = \int_0^1 \frac{4x(1-x)(31+6x+3x^2)\sin(6x/5)}{125\sin(6/5)} dx > 0$$

For larger $n$ values, re-read the source article's "第19种类型" section.

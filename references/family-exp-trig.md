# Family: Exponential-Trigonometric and Power Inequalities (Types 28–30)

## Type 28: $e^{q_1}\sin q_2$ greater/less than a rational ($q_1,q_2$ rational)

## Type 29: $e^{q_1}\cos q_2$ greater/less than a rational ($q_1,q_2$ rational)

These two types share the same framework. They can be handled by:

1. **Separate bounds**: find rational bounds for $e^{q_1}$ (Type 4) and $\sin q_2$ or $\cos q_2$ (Types 14/16) and multiply, using the "integral product combination" technique.

2. **Direct combined integral**:
   $$\int_0^1 x^n(1-x)^n(a+bx+cx^2)e^{q_1x}\sin(q_2x) dx$$
   (replace $\sin$ with $\cos$ for Type 29). Domain: $[0,1]$

**Expansion**: result is a linear combination of $e^{q_1}\sin q_2$ (or $e^{q_1}\cos q_2$), $e^{q_1}\cos q_2$ (or $e^{q_1}\sin q_2$), and $1$.

**Euler formula insight**: $e^{q_1}\cos q_2 = \Re(e^{q_1+iq_2})$ and $e^{q_1}\sin q_2 = \Im(e^{q_1+iq_2})$ — treat $q_1+iq_2$ as a single complex argument in the $e^q$ framework (Type 4).

**Undetermined coefficients**: 3 — $(a,b,c)$

**Non-negativity constraint**: $a+bx+cx^2 \ge 0$ on $[0,1]$

**Reference example**: proving $e^3\sin(3/5) > 20/3$ via direct combined integral ($n=2$):
$$e^3\sin\frac{3}{5} - \frac{20}{3} = \frac{2}{114375}\int_0^1 x^2(1-x)^2(3850550 + 1507629x - 1100229x^2)e^{3x}\sin\frac{3x}{5}dx > 0$$

Alternatively, via product of separate bounds:
$$e^3\sin\frac{3}{5} - \frac{20}{3} = \int_0^1 \frac{x(1-x)}{3000}\left[125x^2(1-x)^3(28+33x)e^{3x} + 4e^3(3571-102x+111x^2)\sin\frac{3x}{5}\right]dx > 0$$

For larger $n$ values, re-read the source article's "第28-29种类型" section.

---

## Type 30: $q_1^{q_2}$ greater/less than a rational ($q_1>1, q_2>0$ rational)

Let $q_2 = u/v$ ($u,v$ integers). Two approaches:

**Approach 1**: raise both sides to power $v$ and compare rational numbers $q_1^u$ vs $p^v$.

**Approach 2** (direct integral):
$$\int_0^1 x^n(1-x)^n(a+bx)(1+(q_1-1)x)^{q_2} dx$$
Domain: $[0,1]$

**Expanded formula ($n=1$)** — linear combination of $q_1^{q_2}, 1$:
$$\int_0^1 x(1-x)(a+bx)(1+(q_1-1)x)^{q_2} dx = \frac{s \cdot q_1^{q_2} + t}{(1+q_2)(2+q_2)(3+q_2)(4+q_2)(q_1-1)^4}$$
where

$$s = q_1^2\big(a(q_1-1)(4+q_2)(q_1q_2 + q_1 - q_2 - 3) + b(q_1^2(2+3q_2+q_2^2) - 2q_1(4+5q_2+q_2^2) + (q_2^2+7q_2+12))\big)$$

$$t = a(q_1-1)(4+q_2)(q_1(3+q_2)-q_2-1) + 2b(1+q_2 - q_1(4+q_2))$$

**Undetermined coefficients**: 2 — $(a,b)$

**Non-negativity constraint**: $a+bx \ge 0$ on $[0,1]$, i.e. $a \ge 0, a+b \ge 0$

**Reference example**: proving $(5/3)^{5/3} < 5/2$ using $n=1$:
$$\frac{5}{2} - \left(\frac{5}{3}\right)^{5/3} = \frac{1}{10125}\int_0^1 x(1-x)(52229-20978x)\left(1+\frac{2x}{3}\right)^{5/3}dx > 0$$

For larger $n$ values, re-read the source article's "第30种类型" section.

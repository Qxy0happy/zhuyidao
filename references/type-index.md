# Type Index — Route to the Right Family

Read this file first. Identify what your inequality involves, note the family file to read next.

| If your inequality involves... | Then read this ref file | Types covered |
|---|---|---|
| $\pi$, $e$, $\pi^n$, $e^q$, $e^\pi$, $e^{q\pi}$ | `family-pi-e.md` | 1–6 |
| $\ln q$, $(\ln q)^n$, $\ln\pi$, $\arcsin q$, $\arccos q$, $\arctan q$, $\operatorname{arccot} q$ | `family-log-invtrig.md` | 7–13 |
| $\sin q$, $\sin(\pi q)$, $\cos q$, $\cos(\pi q)$, $\tan q$, $\cot q$ | `family-trig.md` | 14–19 |
| $\operatorname{arsinh} q$, $\operatorname{arcosh} q$, $\operatorname{artanh} q$, $\operatorname{arcoth} q$, $\sinh q$, $\cosh q$, $\tanh q$, $\coth q$ | `family-hyper.md` | 20–27 |
| $e^{q_1}\sin q_2$, $e^{q_1}\cos q_2$, $q_1^{q_2}$ | `family-exp-trig.md` | 28–30 |
| Catalan $C$, Euler $\gamma$, golden $\phi$, Glaisher $\ln A$, lemniscate $\varpi$, Gauss $G$, $\Gamma$, $\psi'$ | `family-special-constants.md` | 31–39 |
| $\zeta(s)$, $\operatorname{Si}(q)$, $\operatorname{Cin}(q)/\operatorname{Ci}(q)$, $\operatorname{Ein}(q)/E_1(q)/\operatorname{Ei}(q)$, $\operatorname{Li}_2(q)$, $\operatorname{erf}(q)$ | `family-special-functions.md` | 40–45 |

## Decision Tree

1. **π involved?** → Type 1 (single π), 3 (πⁿ), 5 (e^π), 6 (e^{qπ}) → read `family-pi-e.md`
2. **e involved?** → Type 2 (single e), 4 (e^q), 5 (e^π), 6 (e^{qπ}), 28–29 (e^{q1} trig) → read `family-pi-e.md` or `family-exp-trig.md`
3. **ln involved?** → Type 7 (ln q), 8 ((ln q)ⁿ), 9 (ln π) → read `family-log-invtrig.md`
4. **arcsin/arccos/arctan/arccot?** → Types 10–13 → read `family-log-invtrig.md`
5. **sin/cos/tan/cot?** → Types 14–19 → read `family-trig.md`
6. **arsinh/arcosh/artanh/arcoth?** → Types 20–23 → read `family-hyper.md`
7. **sinh/cosh/tanh/coth?** → Types 24–27 → read `family-hyper.md`
8. **e^{q1}·trig(q2) or q1^{q2}?** → Types 28–30 → read `family-exp-trig.md`
9. **Special constant (C, γ, φ, ln A, ϖ, G, Γ, ψ')?** → Types 31–39 → read `family-special-constants.md`
10. **Special function (ζ, Si, Cin, Ein, Li₂, erf)?** → Types 40–45 → read `family-special-functions.md`

## After Reading the Family File

If the family file does not contain the expanded formula for the $n$ value you need, **re-read the relevant section of the source article** (mapped in each family file).

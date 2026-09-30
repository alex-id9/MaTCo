# Module 1: Integration

Throughout this module we cover materials from the linked [notes](https://drive.google.com/file/d/1hWAnxqkI8vEc2utziH8ni-a0gakGPk9v/view?usp=sharing).

## Kickoff (16.09)

During this session we covered the [kickoff presentation](https://github.com/alex-id9/MaTCo/blob/main/%5BM1%5D%20Calculus%20%26%20Analysis/W0_Kickoff.pdf) and briefly passed through the [solutions](https://github.com/alex-id9/MaTCo/blob/main/%5BM1%5D%20Calculus%20%26%20Analysis/W0_Kickoff_SOL.pdf).

## (CH.1) Rolle's Theorem as a Design Tool (16.09 / 23.09)

> 16 september 2026

The first session further continued with going through Rolle's Theorem and other adjacent results (see [here](https://github.com/alex-id9/MaTCo/blob/main/%5BM1%5D%20Calculus%20%26%20Analysis/W1_Rolle'sTheorem.pdf)). We covered the following material:

***
1. **Theorems**

Throughout assume $$f, g \in C([a, b])$$ are differentiable on $(a, b)$, where $a < b$.

- Rolle's Theorem: If $f(a) = f(b)$, then $\exists c \in (a, b)$ with $f'(c) = 0$.
- Lagrange's MVT: $\exists c \in (a, b): f'(c) = \frac{f(b) - f(a)}{b - a}$
- Cauchy's MVT: $\exists c \in (a, b): \big( g(b) - g(a) \big) f'(c) = \big( f(b) - f(a) \big) g'(c)$

2. **Auxiliary Functions**

| Target Expression       | Derivative to use                                      |
|-------------------------|--------------------------------------------------------|
| $f'- \lambda f$         | $(e^{-\lambda x})' = e^{-\lambda x} (f' - \lambda f)$  |
| $x f' - f$              | $(f/x)' = \frac{x f' - f}{x^2}$                        |
| $2f'+ x f''$            | (x f)'' = 2f' + x f''                                  |
| $f'' + 2xf + (x^2 + 1)f | (e^{x^2/2} f)'' = e^{x^2/2} (f'' + 2x f' + (x^2 + 1) f)|

3. **Related Problems**
- IMC 2025 P6
- IMC 2023 P7

***

> 23 september 2026

We continued working on the slides from week 1 (see [here](https://github.com/alex-id9/MaTCo/blob/main/%5BM1%5D%20Calculus%20%26%20Analysis/W1_Rolle'sTheorem.pdf)) with the remaining material:

***
1. **Theorems**
- Weighted Rolle's Lemma: Suppose $f$ differentiable on an interval and has $m \geq 2$ distinct zeros. Then $\forall \lambda \in \mathbb{R}$ the expression $f'- \lambda f$ has at least $m - 1$ distinct zeros between them.
- Darboux's Theorem: If $H$ differentiable on an interval, then $H'$ has the intermediate value property. In particular, if $H'(a) < \lambda < H'(b)$, then $H'(c) = \lambda$ for some $c \in (a, b)$.

2. **Related Problems**
- IMC 2019 P6
- Putnam 2015 B1
***

## (CH.2) Differential Equations & Taylor Estimates (23.09)

> 23 september 2026

We worked through the material from the session slides (see [here](https://github.com/alex-id9/MaTCo/blob/main/%5BM1%5D%20Calculus%20%26%20Analysis/W2_DifferentialEq.pdf)). We covered the following material:

***
1. **Theorems**

Throughout assume all functions are sufficiently smooth (e.g. $u \in C^1([a,b])$, $F \in C^1([a,b])$, $f \in C^2(I)$).

- Integrating Factors: Let $p, q$ be continuous and suppose $u'(x) - p(x)u(x) \geq q(x)$. With $A(x) = \int_a^x p(t)\,dt$, integrating from $a$ to $x \geq a$ yields $$u(x) \geq e^{A(x)} \Big( u(a) + \int_a^x e^{-A(t)} q(t)\,dt \Big).$$
- Gronwall's Inequality: If $F'(x) \leq \lambda F(x)$ on $[a,b]$, then $F(x) \leq F(a) e^{\lambda(x-a)}$. In particular, $F \geq 0$, $F(a) = 0$, $F' \leq \lambda F \implies F \equiv 0$.
- Tangent-Line Inequality: If $u$ is differentiable and concave on an interval, then $u(y) \leq u(x) + u'(x)(y-x)$ for all $x, y$ in that interval. Consequence: every positive, differentiable, concave function on $\mathbb{R}$ is constant.
- Taylor's Theorem (integral remainder): If $f \in C^2(I)$ and $x, x+h \in I$, then $$f(x+h) = f(x) + h f'(x) + h^2 \int_0^1 (1-t) f''(x+th)\,dt.$$
- Quadratic Remainder Estimate: If $|f'(x) - f'(y)| \leq L|x-y|$ ($f'$ is $L$-Lipschitz), then $|f(x+h) - f(x) - h f'(x)| \leq \frac{L}{2} h^2$. (No second derivative required.)

2. **Substitutions & Transformations**

| Target Expression       | Transformation                                         |
|-------------------------|--------------------------------------------------------|
| $f' - pf$               | $(e^{-A} f)' = e^{-A}(f' - pf)$, where $A' = p$        |
| $f' + f^2 \geq -1$      | $(x + \arctan f)' = 1 + \frac{f' + f^2}{1+f^2} \geq 0$ |
| $ff'' - 2(f')^2$        | $(1/f)'' = -\frac{ff'' - 2(f')^2}{f^3}$                |
| $f'/f$                  | $(\log|f|)' = f'/f$                                    |
| System in $f, g, h$     | Product substitution $p = fgh$ collapses the system    |

*Caveats: reciprocals and logarithms require $f \neq 0$; the sign of the multiplier determines whether an inequality is preserved.*

3. **Key Techniques**
- Grönwall trick (IMC 1994 P7): set $F(x) = \int_a^x |f(t)|\,dt$ to avoid dividing by $f$.
- Arctangent substitution (IMC 1994 P2): monotonicity of $x + \arctan f(x)$ forces $b - a \geq \pi$, with equality for $f(x) = \cot(x-a)$.
- Completing the square (IMC 2017 P2): choose the Taylor step $h = -f'(x)/L$ to optimize the bound, giving $(f')^2 < 2Lf$.
- Fixed-point translation (IMC 2023 P1): translate $x^* = -1/6$ to the origin, so $g(7t) = 49g(t) \Rightarrow g''$ constant.

4. **Related Problems**
- IMC 1994 P2, P7
- IMC 2017 P2
- IMC 2020 P5
- IMC 2023 P1
- Putnam 2009 A2
***

## (CH.3) Sequences (30 september 2026)

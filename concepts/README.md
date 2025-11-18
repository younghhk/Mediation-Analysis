# Classical Mediation Analysis

Mediation analysis asks a common question:

> Does X affect Y directly, or does X affect Y through another variable M?

Example:  
Does ultra-processed food (UPF, X) affect cancer risk (Y) partly through BMI (M)?

The classical (Baron & Kenny, 1986) approach checks this in three regression steps.

---

### Step 1 — Does X affect Y?

Regression:  
$Y = b_0 + b_1 X + e$

Look at $b_1$:

- If $b_1$ is significant, then X is associated with Y.
- In the classical framework, if X does not relate to Y, then there is “nothing to mediate.”

**Goal of Step 1:**  
Show that an overall X → Y relationship exists.

---

### Step 2 — Does X affect the mediator M?

Regression:  
$M = b_0 + b_2 X + e$

Look at $b_2$:

- If $b_2$ is significant, then X affects M.

Why this matters:  
For M to be a mediator, X must first change M.  
(Example: UPF must influence BMI.)

**Goal of Step 2:**  
Show that X → M exists.

---

### Step 3 — Does M carry the effect of X into Y?

Regression:  
$Y = b_0 + b_4 X + b_3 M + e$

Check two things:

1. **Is $b_3$ significant?**  
   → If yes, M is associated with Y even after controlling for X.  
   This means changes in M help explain differences in Y.

2. **What happens to $b_4$ compared to Step 1?**  
   - If $b_4$ becomes small or non-significant, the X → Y relationship is largely explained by M.  
   - If $b_4$ is smaller but still significant, X appears to affect Y **both** directly and through M.

**Goal of Step 3:**  
See whether adding M reduces the X → Y relationship.  
This tells us how much of the X → Y association seems to flow through M.

---

### Note: Modern Causal Mediation Theory

The three-step procedure above is the **classical** view.  
Modern causal mediation frameworks (e.g., Pearl, Imai, VanderWeele) keep the same basic intuition but differ in several important ways:

- They define **direct** and **indirect** effects in terms of **counterfactuals** (what would happen under different hypothetical values of X and M).
- They **do not require** the total effect ($b_1$ in Step 1) to be statistically significant for mediation to exist.  
  - For example, direct and indirect effects can cancel each other, so the total effect may be near zero even when a meaningful indirect effect is present.
- They emphasize the need to adjust for **confounders** of:
  - X → Y  
  - X → M  
  - M → Y  
  and to be explicit about the causal assumptions (DAGs, no unmeasured confounding, etc.).
- They allow for non-linear models (e.g., logistic regression, Cox models) and more complex settings.


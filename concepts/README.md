# Mediation in Three Simple Steps

Mediation analysis helps answer a common question:

Does X affect Y directly, or does X affect Y through another variable M?
(Example: Does UPF affect cancer risk partly through BMI?)

We check this in three regression steps.

### Step 1 — Does X affect Y?

Regression: $Y=b_0+b_1X+e$

Look at $b_1$.
- If  $b_1$ is significant, then X affects Y.
- If X does not relate to Y, then there is nothing for M to “mediate.”

*Goal of Step 1:*

Confirm that X → Y exists.

### Step 2 — Does X affect the mediator M?

Regression: $M=b_0+b_2X+e$
	
  ​
Look at $b_2$.

- If  $b_2$ is significant, then X affects M.

Why this matters:
For M to mediate, X must first change M.
(Example: UPF must influence BMI.)

*Goal of Step 2:*

Confirm that X → M exists.

### Step 3 — Does M carry the effect of X into Y?

Regression: $Y=b_0+b_4X+b_3M+e$

Check two things:
- Is $b_3$ significant?
→ If yes, M affects Y (when controlling for X).

- Is $b_4$ smaller than before, or no longer significant?
  - If $b_4$ becomes small or non-significant, the effect of X on Y is now explained by M.
  - I f $b_4$ is smaller but still significant, X affects Y both directly and through M.

*Goal of Step 3:*

See whether adding M reduces the X → Y relationship.
This tells us how much of the effect flows through M.


<!--# Understanding Mediators in Epidemiologic Analysis

## Key Definitions

### Exposure (A)
A variable that occurs before the outcome and may influence it directly or indirectly. This includes:

- a direct effect (A → C)
- an indirect effect through a mediator (A → B → C)
  
Note: If A has a direct effect on C, a mediator is not required for A to influence the outcome.

### Mediator (B)
A variable that lies on the causal pathway between A and C. This requires:
- A → B
- B → C

### Outcome (C)
The health or clinical endpoint of interest.


**What Happens If You Adjust for the Mediator (B)?**

Suppose we fit:
C ~ A + B

For example:
Cancer ~ UPF + BMI

The adjusted regression is:
$$ C = \beta_0 + \beta_1 A + \beta_2 B + \epsilon $$

When computing β₁, the model does not use the  A. Instead, it uses the residualized exposure:

$$ A^{*} = A - \hat{\gamma} B $$

This removes from A the part that is explained by B. If A affects C through B, this residualization removes that pathway, which creates over-adjustment. The estimated A–C association may weaken, disappear, or even reverse.

# A Simple Example

## Step 1: Direct, Indirect, and Total Effects

Suppose:

- $B = 20 + 2A$
- Indirect path: $C = 0.5B + \epsilon$ 
- Direct path: $0.3A$ 
- Full model:  $C = 0.5B + 0.3A + \epsilon$

From these relationships:

- $\frac{\partial B}{\partial A} = 2$
- $\frac{\partial C}{\partial B} = 0.5$

**Indirect effect:**  
$$2 \times 0.5 = 1.0$$


**Total effect:**  
$$0.3 + 1.0 = 1.3$$

**Interpretation:**  
A has an overall positive effect on C, and most of that effect works through B.

---

## Step 2: Numerical Illustration

Let $A = 1, 2, 3$.

Using the full model:

- $B = 20 + 2A$  
- $C = 0.5B + 0.3A$

we get:

| A (UPF) | B (BMI) | C (Cancer Risk) |
|---------|---------|------------------|
| 1       | 22      | 11.3             |
| 2       | 24      | 12.6             |
| 3       | 26      | 13.9             |

### Unadjusted model

Fit: $C = \alpha_0 + \alpha_1 A$

The slope:
$$\alpha_1 = 1.3 > 0$$

UPF (A) appears to increase cancer risk (C), which reflects both the direct and indirect pathways.

---

### Adjusted model

Now fit: $C = \beta_0 + \beta_1 A + \beta_2 B$

Because A and B are perfectly correlated in this simple example  (i.e., $\text{Cor}(A, B)=1.0$),  
the regression estimates become:

$\beta_2 = 0.50,\qquad \beta_1 = -0.20$

### Interpretation

- BMI keeps its strong positive association with cancer $\beta_2 = 0.5$.
- The UPF coefficient becomes **negative**, even though UPF truly has a positive direct effect (0.3).

- This happens because adjusting for BMI removes the A → B → C pathway, leaving only the much smaller direct effect.
- When the direct effect is weak relative to the mediated effect, the adjusted estimate can shrink toward zero or even reverse direction, as can occur in real observational data.
-->

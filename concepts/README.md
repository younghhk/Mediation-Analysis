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

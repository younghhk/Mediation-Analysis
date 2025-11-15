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



#  Mediation Analysis Workflow Checklist


This checklist provides a structured guide to selecting the appropriate mediation framework based on study design and data characteristics.  
Answer each question **Yes / No** (or choose one option) before proceeding with analysis.

For additional cancer research tools, see [younghhk/NCI](https://github.com/younghhk/NCI).

---

### **1. Outcome (Y)**
| Question | Options |
|-----------|----------|
| Type of outcome | ☐ Binary ☐ Continuous ☐ Time-to-event (survival) |

---

### **2. Exposure (A)**
| Question | Options |
|-----------|----------|
| Is the study observational or experimental? | ☐ Observational ☐ Experimental |
| Type of exposure | ☐ Binary ☐ Continuous ☐ Categorical |
| Number of exposures | ☐ Single ☐ Multiple (analyzed separately) |
| Dimensionality | ☐ Low (≤10) ☐ High (>10, e.g. omics features) |

---

### **3. Mediator(s) (M)**
| Question | Options |
|-----------|----------|
| Number of mediators | ☐ Single ☐ Multiple (parallel) |
| Dimensionality | ☐ Low (≤10) ☐ High (>10) |
| Type | ☐ Continuous ☐ Binary ☐ Mixed |

---

### **4. Confounders (X)**
| Question | Options |
|-----------|----------|
| Are there known confounders to adjust for (e.g., age, sex, batch)? | ☐ Yes ☐ No |

---

### **5. Temporal and causal assumptions**
| Question | Options / Notes |
|-----------|-----------------|
| Does exposure precede mediator and outcome (A → M → Y)? | ☐ Yes ☐ No |
| Are major confounders of the A–M, M–Y, and A–Y paths measured? | ☐ Yes ☐ No |
| Is an exposure–mediator interaction plausible? | ☐ Yes ☐ No (If yes, include interaction term in the model) |

---

### **6. Modeling goals**
| Question | Options |
|-----------|----------|
| Goal | ☐ Estimate direct/indirect effects ☐ Identify key mediating variables ☐ Predict outcome |
| Need FDR or multiple-testing control? | ☐ Yes ☐ No |
| Visualization required? | ☐ Yes ☐ No |



---

###  **Minimum information to provide for consultation**
1. Outcome type (binary, continuous, or survival)  
2. Exposure type and number  
3. Mediator type and number  
4. Presence of confounders  
5. Study design (observational or experimental)  
6. Expected modeling goal (effect estimation vs. selection)

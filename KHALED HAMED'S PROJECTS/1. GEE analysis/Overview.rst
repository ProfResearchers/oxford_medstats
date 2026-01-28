--






Generalized Estimating Equations (GEE)
======================================

* **What GEE is:** A method to estimate **GLM regression parameters** when observations are **correlated** (e.g., repeated measures over time).

* **Key Liang–Zeger result:** The **β estimates** from Liang–Zeger GEE are **consistent** and **asymptotically normal** even if the **working correlation** is wrong (under mild conditions).

* **Why useful vs plain GLM:** When there’s **autocorrelation** (serial correlation), GEE can be **more efficient** than a GLM that wrongly assumes independence.

* **Missing data note (as stated):** If the *true* working correlation is known, **consistency may not require MCAR** (i.e., can be less strict than “missing completely at random”).

* **Standard errors terminology:**

  * **Liang–Zeger SE** and **Huber–White (“robust/sandwich”) SE** are both used in GEE contexts.
  * Robust/sandwich SE are widely used; different historical formulations exist.

* **Interpretation focus:** GEE typically gives **population-averaged (marginal)** effects (average over the population rather than subject-specific effects).

* **Semiparametric idea:** GEE is called **semiparametric** because it relies mainly on specifying the **mean model** and (roughly) the **variance/correlation** through the first two moments, not a full likelihood.

* **Compared with GLMM:** GEEs are a popular alternative to **generalized linear mixed models (GLMMs)** because GLMMs can be more sensitive to **variance-structure misspecification**.

* **Trade-off:** If the correlation/variance structure is misspecified, β can remain consistent but you may lose **efficiency** → **larger SE**, potentially **less significant Wald tests** (bigger p-values).

* **Common use case:** Big epidemiologic / cohort / multi-site studies where there’s **unmeasured dependence** within clusters.

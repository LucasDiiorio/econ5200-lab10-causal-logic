Causal Logic and DAGs: Diagnosing Bad Controls

Objective

I examined how controlling for the wrong variables can introduce bias into causal estimates and used directed acyclic graphs (DAGs) to identify valid adjustment sets.

Methodology

Simulated data to demonstrate collider bias, M-bias, and mediation.

Compared OLS regression estimates with and without control variables.

Used DAGs to identify confounders, colliders, mediators, and backdoor paths.

Compared the LaLonde randomized job-training experiment with observational estimates using CPS controls.

Used a dag_utils.py module to identify valid adjustment sets and evaluate the backdoor criterion.

Tested an AI-generated adjustment set against a known DAG and revised my prompt to correct its causal assumptions.

Key Findings

Controlling for a collider moved the estimated effect from −0.012 to −0.593 and increased R-squared to 0.585, despite a true causal effect of zero.

Controlling for a pre-treatment collider introduced M-bias, producing an estimate of −0.201 against a true effect of zero.

I separated the estimated total effect of 3.978 (true effect 4.0) from the estimated direct effect of 0.988 (true effect 1.0).

I compared the LaLonde experimental benchmark of $1,794 with an observational estimate of −$8,498 before covariate adjustment and $699 after adjustment.

The AI's initial adjustment set produced an estimate of 3.622 against a true effect of 4.0. After revising my prompt to explain the collider structure, the estimate improved to 4.047.

I demonstrated that causal identification depends on the underlying causal structure rather than statistical significance, R-squared, or the number of controls included.

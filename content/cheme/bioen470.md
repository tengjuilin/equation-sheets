---
title: "BIOEN 470 System Immunology and Immunoengineering"
date: 2022-04-15T00:00:00-08:00
---

## Receptor-Ligand Kinetics

{{< admonition type=info title="Definition of Terms" open=true >}}

- Variables
  - $\ce{[R]}$ - Receptor concentration
  - $\ce{[RL]}$ - Receptor-ligand complex concentration
- Parameters
  - $\ce{[L]}$ - Ligand concentration
  - $\ce{[R_T] = [R] + [RL]}$ - Total receptor concentration
  - $k_1$ - Forward (binding) rate
  - $k_{-1}$ - Reverse (unbinding) rate
- Derived parameters
  - $K_1 = \dfrac{k_1}{k_{-1}}$ - Association constant
  - $K_{-1} = \dfrac{k_{-1}}{k_1}$ - Dissociation constant
- Relationships
  - $K_{-1} = K_1^{-1}$
{{< /admonition >}}

{{< admonition type=tip title="Derivation" open=true >}}

Suppose reversible ligand binding to receptor is given by

$$
\color{blue} \ce{R + L <=>[\mathit{k}\_1][\mathit{k}_{-1}] RL}
$$

The total number of receptors is constant $\ce{[R_T]}$

$$
\ce{[R_T] = [R] + [RL]}.
$$

By steady-state approximation,

$$
\begin{aligned}
\dfrac{d\ce{[RL]}}{dt} &= k_1 \ce{[R][L]} - k_{-1} \ce{[RL]} && \footnotesize\text{Principle of detailed balance} \\\ 0 &= k_1 \ce{[R][L]} - k_{-1} \ce{[RL]} && \footnotesize\text{Steady state approximation } \frac{d\ce{[RL]}}{dt} = 0 \\\ 0 &= k_1\ce{([R_T] - [RL])[L]} - k_{-1} \ce{[RL]} && \footnotesize\text{Total receptor constraint } \ce{[R_T] = [R] + [RL]} \\\ k_1\ce{[L][R_T]} &= k_1\ce{[L][RL]} + k_{-1}\ce{[RL]} \\\ \ce{[RL]} &= \dfrac{k_1\ce{[L][R_T]}}{k_1\ce{[L]} + k_{-1}} \\\ \ce{[RL]} &= \dfrac{(k_1\ce{[L][R_T]})/k_1}{(k_1\ce{[L]} + k_{-1})/k_1} && \footnotesize\text{Divide by } k_1 \\\ \ce{[RL]} &= \dfrac{\ce{[L][R_T]}}{\ce{[L]} + \frac{k_{-1}}{k_1}} \\\ \ce{[RL]} &= \dfrac{\ce{[L][R_T]}}{\ce{[L]} + K_{-1}} && \footnotesize\text{Dissociation coefficient } K_{-1} = \frac{k_{-1}}{k_1}
\end{aligned}
$$

{{< /admonition >}}

{{< admonition type=warning title="Results" open=true >}}

The concentration of the bound receptor-ligand complex depends on concentration of ligands, total concentration of receptors, forward rate, and backward rate:

$$
\boxed{\ce{[RL]} = \dfrac{\ce{[L][R_T]}}{\ce{[L]} + K_{-1}}}
$$

The $\ce{[RL]}$ vs $\ce{[L]}$ graph has the following features

$$
\begin{aligned}
\lim_{\ce{[L] \to \infty}} \ce{[RL]} &= \ce{[R_T]} \\\ \lim_{\ce{[L] \to K_{-1}}} \ce{[RL]} &= \frac{1}{2}\ce{[R_T]}
\end{aligned}
$$

{{< /admonition >}}

<!-- ★ -->
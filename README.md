# A Sharp Adaptation Frontier for Heavy-Tailed Bandits with Unknown Moments

## Abstract

Heavy-tailed bandit algorithms attain optimal regret when given a finite moment order and its bound. Without either parameter, optimal adaptation is impossible unless one restricts the reward distributions. What can be achieved under the moment condition alone has remained open. We give a sharp answer in the form of a Pareto frontier. Our algorithm takes only an exploration exponent $\rho\in(0,1)$. It combines deterministic forced exploration with a median-of-means empirical leader and uses neither the moment order, its bound, nor a tail-sign condition. If the unknown rewards have $(1+\epsilon)$th absolute moments bounded by $u$, its worst-case regret is, up to explicit arm factors and an arbitrarily slow factor, \[ u^{1/(1+\epsilon)} T^{1-\rho\epsilon/(1+\epsilon)}, \] while its regret on every fixed instance is $O(T^\rho)$. A matching lower bound shows that improving either polynomial exponent worsens the other. Most notably, every fixed $\rho\leq2/3$ attains this frontier simultaneously for all $\epsilon\in(0,1]$. Thus at any point on this common segment, unknown tail order has no further polynomial price beyond unknown scale. This answers the assumption-free rate question posed at COLT 2025 on the maximal common segment and gives the first matching algorithm for the unknown-scale lower tradeoff.

## Main results

**Theorem.** There is a universal constant $C$ such that \FM{}, for every $\rho\in(0,1)$, $p\in(1,2]$, $u>0$, and $T\geq1$, satisfies, with $\gamma_p=(p-1)/p$, \begin{align} \sup_{\nu\in\cH_{p,u}}R_T(\nu) \leq C u^{1/p}\big\{&K\log(eK) \nonumber\\ &+K^{1-\rho}T^\rho\nonumber\\ &+K^{\rho\gamma_p}T^{1-\rho\gamma_p} L_T^{\gamma_p}\big\}, \end{align} where $L_T=1+\log(2K)+\ell(T)$. The policy is independent of $p$ and $u$.

**Theorem.** For every fixed bandit instance with a finite $p$th absolute moment for some $p>1$, \FM{} satisfies \begin{equation} \sum_{t=1}^\infty \Pr\{t\text{ is exploit and }I_t\notin\arg\max_i\mu_i\}<\infty. \end{equation} Consequently, \begin{equation} \limsup_{T\to\infty}\frac{R_T(\nu)}{T^\rho} \leq K^{-\rho}\sum_{i=1}^K\Delta_i. \end{equation}

**Theorem.** Fix $p\in(1,2]$. Suppose a policy, without knowing $u$, has a moment-free distribution-free bound $\Phi_p(T)=o(T)$ as in \eqref{eq:free-def}. Then on every fixed instance $\nu$ with at least one suboptimal arm, \begin{equation} \liminf_{T\to\infty} \frac{R_T(\nu)}{(T/\Phi_p(T))^{p/(p-1)}} \geq c_p\sum_{i:\Delta_i>0}\Delta_i, \end{equation} where $c_p>0$ depends only on $p$. Hence polynomial exponents $a$ and $b$ in $ ...

**Corollary.** Fix any $\rho\in(0,2/3]$. One policy, independent of $p$ and $u$, attains for every $p\in(1,2]$ the polynomial exponents \[ (a_p,b)=\left(1-\rho\frac{p-1}{p},\rho\right). \] These exponents satisfy the lower tradeoff with equality for every $p$. The slowly varying gap in \eqref{eq:upper} can be made arbitrarily small by the choice of $\ell$.

## Keywords

heavy-tailed bandits, median-of-means, adaptive regret, Pareto frontier, unknown moments, forced exploration

## Files

- `aistats2027.sty`
- `fancyhdr.sty`
- `main.bbl`
- `main.pdf`
- `main.tex`
- `references.bib`
- `supplement.bbl`
- `supplement.pdf`
- `supplement.tex`

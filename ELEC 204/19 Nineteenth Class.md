# Nineteenth Class
* Poles of multiplicity $>1$
  * Partial fraction is $\frac{P(s)}{Q_1(s)(s+p_1)^r)}=\frac{K_{11}}{(s+p_1)}+\frac{K_{12}}{(s+p_1)^2}+\ldots+\frac{K_{1r}}{(2+p_1)^r}+\ldots$
  * To find roots multiply by denominators and take derivatives
* Finding partial fraction constants
  * Divide by pole in question, then set $s$ to be the negative of that pole
* Complex roots
  * Constants are conjugates of each other
* Initial and final value theorem
  * If both $f(t), \frac{df}{dt}$ have laplace transform, then $\lim_{t\to0^+}f(t)=\lim_{s\to\infty}sF(s)$
  * If both $f(t), \frac{df}{dt}$ have laplace transform and $\lim_{t\to\infty} f(t)$ exists, then $\lim_{t\to\infty}f(t)=\lim_{s\to0}sF(s)$
* Laplace transform in circuit analysis
  * Use $s$-domain equivalent of circuit
  * Find expression for desired signal in $s$ domain
  * Use inverse Laplace transform to find time-domain expression
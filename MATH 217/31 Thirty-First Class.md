# Thirty-First Class
* Internal loops
  * For Green's theorem to apply loops in $D$ should be oriented clockwise
  * In this case the $\partial D$ is the sum of all of the regions
  * Intuition is that if you split the region into two parts with no holes in them, and compute Green's theorem separately for each of them, the holes end up going counter clockwise
* Integral theorems
  * $\int_C(\vec\nabla f)\cdot d\vec r=f(p_2)-f(p_1)$ (FTLI)
  * $\iint_D(Q_x-P_y)dA=\oint_{\partial D}Pdx+Qdy$ (Green's theorem)
  * $\iiint_E(div\vec F)dVol=\iint_{\partial E}\vec F\cdot d\hat S$ (divergence theorem)
  * Each of these have the form $\int_R derivative(*)=\int_{\partial R}(*)$
* If in Green's theorem, consider $\vec F=<P(x, y), Q(x, y), 0>$, then $curl\vec F=<0, 0, Q_x-P_y>$
  * $D\sub\R^2\rightarrow$ consider it as a surface $R\sub\R^3$
  * $\iint_R curl\vec F\cdot\hat NdS=\iint_R(Q_x-P_y)dxdy=\oint_{\partial R}\vec F\cdot d\vec r$
* Stoke's Theorem
  * $\iint_S(curl\vec F)d\hat S=\oint_{\partial S}\vec F\cdot d\vec r$
  * Orient $\partial S$ so that we walk along $C=\partial S$ in the direction of orientation, upright as dictated by $\hat N$, then then $S$ is on the left
  * If $\hat T$ is unit tangent vector to $C$, then $\hat N\times\hat T$ should point in to $S$
* e.g. Compute $\oint_C\vec F\cdot d\vec r$ where $C$ has parameterization $\vec R(t)=<\sin t, \cos t, -s\in(2t)>, 0\leq t\leq 2\pi,\vec F=<\tan\sqrt{1+x^4}, zy+e^{y^3}, \frac{x^2}2+\sqrt[3]{\sin z^2}>$
  * Computing by hand is extremely hard
  * Is $\vec F$ conservative? 
    * $curl\vec F=<y, x, 0>$
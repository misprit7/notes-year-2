# Seventeenth Class
* Taking double integrals in polar coordinates
  * $x=r\cos\theta, r=\sqrt{x^2+y^2}$
  * $y=r\sin\theta, \theta = \arctan(\frac yx)$
  * Usually $r\geq 0$, $0\leq\theta\leq2\pi$
    * Can still make sense of other $\theta$, e.g. might use $\theta =-\frac\pi4$ instead of $\frac74\pi$
  * Polar coordinates are useful in situations with some rotational symmetry about the origin
* e.g. $D=\{(x, y): 1\leq x^2+y^2\leq 4, x\geq 0, y\geq 0\}$
  * Awkward to do in cartesian coordinates
  * We can integrate over a region $\{(r, \theta): a\leq r\leq b, \alpha\leq\theta\leq\beta\}$
    * Divide up $[a, b]$ in to $N$ intervals of size $\Delta r = \frac{b-a}N$
    * Divide up $[\alpha, \beta]$ into intervals of size $\Delta\theta = \frac{\beta - \alpha}M$
    * $\int\int_RfdA=\lim_{N\to\infty, M\to\infty}\sum_{i=1}^N\sum_{j=1}^Mf(r_i, \theta_j)\Delta A_{ij}$
    * $\int\int_RfdA=\int_{\theta=\alpha}^\beta\int_{r=a}^bf(r, \theta)rdrd\theta$
  * More generally, we call a region radially sliceable if it is of the form $R=\{(r, \theta): g_1(\theta)\leq r\leq g_2(\theta), \alpha\leq\theta\leq\beta\}$
  * $\int\int_RfdA=\int_{\theta=\alpha}^\beta\int_{r=g_1(\theta)}^{g_2(\theta)}f(r\theta)rdrd\theta$
* e.g. Find the volue of the region in $\mathbb R^3$ below the paraboloid $z=x^2+y^2$, above the $xy$ plane, and inside the cylinder $(x-1)^2+y^2=1$
  * Volume$=\int\int_R(x^2+y^2)dA$
  * $R=\{(x-1)^2+y^2\leq 1\}$
  * $(x-1)^2+y^2=1\Rightarrow x^2-2x+1+y^2=1\Rightarrow r^2=2r\cos\theta\Rightarrow r=2\cos\theta$
  * $\int\int_Rr^2dA=\int_{\theta=-\frac\pi2}^{\frac\pi2}\int_{r=0}^{2\cos\theta}r^3drd\theta$
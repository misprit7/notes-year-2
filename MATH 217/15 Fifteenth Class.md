# Fifteenth Class
* Want to define integral of $f(x, y)$ over $R=[a, b]\times[c, d]\sub\mathbb R^2$
  * $\Delta x = \frac{b-a}N$, $\Delta y=\frac{a-c}M$
  * define $\int\int_Rf(x, y)dxdy=\int\int_Rf(x, y)dA=\lim_{M\to\infty, N\to\infty} \sum_{i=1}^N\sum_{j=1}^Mf(x_i, y_j)\Delta x\Delta y$
  * Twodimensional integral counts signed volume under/over function and $xy$ plane
  * Average value of $f$ over $R$
    * $\frac1{Area(R)}\int\int_Rf(x, y)dA$
* Properties of integrals
  * Linearity
    * $\int\int_Raf(x, y)+bg(x, y)dxdy=a\int\int_RfdA+b\int\int_RgdA$
  * Additive on domain
    * if $R=R_1\cup R_2$, then $\int\int_RfdA=\int\int_{R_1}fdA+\int\int_{R_2}fdA$
    * Two areas can't intersect
* Fundamental theorem of calculus
  * If $F(x)$ is a function such that $F^\prime(x)=f(x)$ ($F$ is an "antiderivative" of $f$) then $\int_{x=a}^bF(x)dx=F(b)-F(a)$
* Partial integrals
  * $g(y)=\int_a^bf(x, y)dx$
* Theorem: if $R=[a, b]\times[c, d]$ then $\int\int_Rf(x, y)dA=\int_{y=c}^d(\int_{x=a}^bf(x,y)dx)dy$ and Fubini Theorems says this works in either order
* e.g. Find the average value of $f(x, y)=e^y\sqrt{x+e^y}$ over the region $R=[0, 4]\times[0, 1]$
  * $\bar f=\frac1{Area(R)}\int\int_RfdA=\frac14\int\int_RfdA=\frac14\int_{x=0}^4\int_{y=0}^1e^y\sqrt{x+e^y}dydx$
  * $u=x+e^y, du=e^ydy$
  * $\bar f=\frac14\int_0^4\int_{x+1}^{x+e}\sqrt ududx=\frac14\int_0^4\frac23u^{3/2}\big|_{x+1}^{x+e}dx=\frac16\int_0^4((x+e)^{3/2}=(x+1)^{3/2})dx$
  * $\bar f=\frac16(\frac25(x+e^{5/2}-\frac25(x+1)^{5/2}\big|_{x=0}^4=\frac1{15}((4+e)^{5/2}-5^{5/2}-e^{5/2}+1)$
* General domains
  * $D$ is vertically sliceable if $D=\{(x, y): g_1(x)\leq y \leq g_2(x), a\leq x\leq b\}$
  * $\int_{x=a}^b\int_{y=g_1(x)}^{g_2(x)}f(x, y)dydx$
* e.g. Find $\int\int_DfdA$ where $f(x, y)=(1-x^2)^{3/2}, D=\{(x, y): x^2+y^2\leq 1\}$
  * $\int_{x=-1}^1\int_{y=-\sqrt{1-x^2}}^{\sqrt{1-x^2}}(1-x^2)^{3/2}dydx$
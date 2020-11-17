# Eighteenth Class
* e.g. Bell curve: $y=e^{-x^2}$
  * Want to compute $I=\int_{x\to-\infty}^\infty e^{-x^2}dx$
  * Looks impossible
  * $I=\int_{y=-\infty}^\infty e^{-y^2}dy$
  * $I^2=\int_{x\to-\infty}^\infty e^{-x^2}dx\cdot \int_{y=-\infty}^\infty e^{-y^2}dy$
  * $I^2=\int_{y=-\infty}^\infty\int_{x=-\infty}^\infty e^{-x^2}\cdot e^{-y^2}dxdy=\int_{\theta = 0}^{2\pi}\int_{r=0}^\infty e^{-r^2}drd\theta=2\pi(-\frac12e^{-r^2}\big|_{r=0}^\infty=2\pi$
  * $I=\sqrt\pi$
  * Therefore $\frac1{\sqrt\pi}e^{-x^2}$ has total area $I$
* Applications of double integrals
  * Read about total mass from mass density, total population from population density, center of mass, moments of intertia
* e.g. $R$ could be on a map, $f$ being population density
* Surface area of a graph of a function $z=f(x, y)$
  * By dividing it up, surface area is $\sum_{i=1}^N\sum_{j=1}^M$Area of little parallelogram above the $ij$-th rectangle
  * Area of little parallelogram is $|\begin{pmatrix}\Delta x\\0\\f_x(x_i, y_j)\Delta x\end{pmatrix}\times\begin{pmatrix}0\\\Delta y\\f_y(x_i, y_j)\Delta x\end{pmatrix}|=\Delta x\Delta y|\begin{pmatrix}-f_x\\-f_y\\1\end{pmatrix}|=\Delta x\Delta y\sqrt{1+f_x^2+f_y^2}$
  * Surface area is $\sum_{i=1}^N\sum_{j=1}^M\Delta x\Delta y\sqrt{1+f_x^2(x_i, y_j)+f_y^2(x_i, y_j)}$
  * Surface area $=\int\int_R\sqrt{1+f_x^2+f_y^2}dA$
* e.g. Consider the following funnel like region $z=-\frac1{\sqrt{x^2+y^2}}$ below $z=-1$. Find volume and surface area. 
  * Volume is $(-\int\int_R-\frac1{\sqrt{x^2+y^2}}dA)-\pi=-\pi+\int_{\theta=0}^2\int_{r=0}^1\frac1rrdrd\theta=2\pi-\pi=\pi$
  * Surface area $=\int\int_R\sqrt{1+z_x^2+z_y^2}dA$
  * $z=-\frac1{\sqrt{x^2}+y^2}, z_x=\frac{x}{(x^2+y^2)^{3/2}}, z_x^2=\frac{x^2}{(x^2+y^2)^3}$
  * Area $=\int\int\sqrt{1\frac{x^2+y^2}{(x^2+y^2)^3}}dA=\int_{\theta=0}^{2\pi}\int_{r=0}^1\sqrt{1+\frac1{r^4}}rdrd\theta=2\pi\int_{r=0}^1\frac1r\sqrt{1+r^4}dr>2\pi\int_{r=0}^1\frac1rdr=\infty$, therefore infinite
* Triple integrals
  * Suppose $f(x, y, z)$ is a function of 3 variables in the domain of a solid region $B\subset\mathbb R^3$
  * We want do define and compute $\int\int\int_Df(x, y, z)dVol$
  * For example $f$ is density, parameters are space
  * For simple box region $B=\{(x, y, z): a\leq x\leq b, c\leq y\leq d, e\leq z\leq g\}$:$\int\int\int_Df(x, y, z)dVol=\lim_{L\to\infty, N\to\infty, M\to\infty}\sum_{i=1}^L\sum_{j=1}^N\sum_{k=1}^Mf(x_i, y_j, z_k)\Delta x\Delta y\Delta z$
  * $=\int_{x=a}^b\int_{y=c}^d\int_{z=e}^gf(x, y, z)dzdydx$
* Vertically sliceable
  * Vertically sliceable if $B=\{(x, y, z):g_1(x, y)\leq z\leq g_2(x, y), (x, y)\in\mathbb R\}$
  * $\int\int\int_BfdVol=\int\int_R\int_{z=g_1(x, y)}^{g_2(x, y)}f(x, y, z)dzdA$
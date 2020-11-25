# Thirteenth Class
* Integrating over surfaces
  * For curves
    * Parameterization $\vec r(t)=<x(t), y(t), z(t)>$
    * $\hat T=\frac{\vec r^\prime(t)}{|\vec r^\prime(t)|}=$ unit tangent vector
    * Arclength $\int_{t=a}^b |\vec r^\prime(t)|dt$
    * Line integral of a function $\int_C fds$
    * Work integral $\int_C\vec F\cdot\hat Tds$
    * FTLI: $\int_C(\vec\nabla f)\cdot \hat Tds=f(p_2)-f(p_1)$
  * For surfaces
    * Parameterization $\vec r(u, v)=<x(u, v), y(u, v), z(u, v)>, (u, v)\in D\sub \R^2$
    * $\hat N=$ unit normal vector
    * Surface area $\iint_S fds$
    * Flux integral $\iint_C \vec F\cdot \hat N ds$
    * Stoke's, Green's, Divergence Theorem
* e.g. Find two different parameterizations of the surface $S=\{(x, y, z): x^2+y^2+z^2=25, x, y, z\geq 0\}$
  * $\vec r(\theta, \phi)<5\sin\phi\cos\theta, 5\sin\phi\sin\theta, 5\cos\phi>, 0\leq\phi, \theta\leq \frac\pi2$
  * Equivalent to $\vec r(u, v)=<u, v, \sqrt{25-u^2-v^2}, u, v\in D=\{(u, v):u^2+v^2\leq 25, u, v\geq 0\}$
* e.g. Parameterize $\{y=4-x^2-z^2, y\geq 0\}$
  * $\vec r(u, v)=<u, 4-u^2-v^2, v>, (u, v)\in D=\{u^2+v^2\leq 4\}$
  * $\vec r(\theta, u)=<\sqrt{4-u}\cos\theta, u, \sqrt{4-u}, 0\leq\theta\leq 2\pi, 0\leq u\leq 4$
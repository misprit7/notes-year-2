# Twenty-Fifth Class
* Finding techniques for finding parameterization of surfase $S$
  * If $S$ is graph of function
  * Surfaces of revolution
* Standard parameterization of a sphere or more generally an ellipsoid: 
  * $S=\{(\frac xa)^2+(\frac yb)^2+(\frac zc)^2=1\}$
  * $\vec r(\theta, \phi)=<a\sin\phi\cos\theta, b\sin\phi\sin\theta, c\cos\phi>$
* Parameterization of a torus
  * parameterization of a circle on $x$ axis of radius $a$ and distance $A$: $r=a\cos\alpha+A, z=a\sin\alpha$
  * $x=r\cos\theta, y=r\sin\theta, z=a\sin\alpha$
  * $\vec r(\alpha, \theta)=<x(\alpha, \theta), y(\alpha, \theta), z(\alpha, \theta)>$ $=<(a\cos\alpha+A)\cos\theta, (a\cos\alpha+A)\sin\theta, a\sin\alpha>, 0\leq\alpha\leq2\pi, 0\leq\theta\leq 2\pi$
  * $\vec r_\alpha=<-a\sin\alpha\cos\theta, -a\sin\alpha\sin\theta, a\cos\alpha>$
  * $\vec r_\theta=<-(a\cos\alpha+A)\sin\theta, (a\cos\alpha+A)\cos\theta, 0>$
  * $|\vec r_\alpha\times\vec r_\theta|=a(a\cos\alpha+A) \begin{pmatrix}\hat i&\hat j&\hat k\\-\sin\alpha\cos\theta&-\sin\alpha\sin\theta&\cos\alpha\\-\sin\theta&\cos\theta&0\end{pmatrix}$
  * $=a(a\cos\alpha+A)|<-\cos\alpha\cos\theta, -\cos\alpha\sin\theta, -\sin\alpha(\cos^2\theta+\sin^2\theta)>|=$ $a(a\cos\alpha+A)\sqrt{\cos^2\alpha(\cos^2\theta+\sin^2\theta)+\sin^2\alpha}$
  * $=a^2\cos\alpha+aA$
  * Area = $\int_{\theta=0}^{2\pi}\int_{\alpha = 0}^{2\pi}|\vec r_\alpha\times\vec r_\theta|d\alpha d\theta=\int_{\theta=0}^{2\pi}\int_{\alpha = 0}^{2\pi}(a^2\cos\alpha+aA)d\alpha d\theta=(2\pi a)(2\pi A)$
* Integration
  * Divide $D$ into a bunch of little rectangles of size $\Delta u\Delta v$
  * One side is $\frac{\partial\vec r}{\partial v}(u_i, v_j)\Delta v$ and other side is $\frac{\partial\vec r}{\partial u}(u_i, v_j)\Delta u$
  * $\Delta S_{ij}\approx|\vec r_v(u_i, v_j)\times\vec r_u(u_i, v_j)|\Delta u\Delta v$
  * Area $=\lim_{\Delta u\to0, \Delta v\to0}\sum_{i, j}\Delta S_{ij}=\iint_D|\vec r_u\times\vec r_v|dudv$
* If $S$ is a surface in $\R^3$ and $f(x, y, z)$ in a function we want to define $\iint_S fdS$
  * For example $S$ cold be the surface of the earth, $f$ is the population density then $\iint_S fdS=$ total population
  * $\iint_S fdS=\lim_{\Delta u\to0, \Delta v\to0}\sum_{i, j} f(x(u_i, v_i), y(x_i, v_j), z(u_i, v_j))\cdot \Delta S_{ij}$ $=\iint f(x(u, v), y(u, v), z(u, v))|\vec r_u\times\vec r_v|du dv$
  * Compared to arc length, $|\vec r_u\times\vec r_v|dudv$ is $dS$ whereas in arc length $dS=|\vec r^\prime(t)|dt$
* e.g. Let $S=\{x^2+y^2+z^2=4, z\geq 0\}$, find $\iint_S z(x^2+y^2) dS$
  * $\vec r(\theta, \phi)=<2\sin\phi\cos\theta, 2\sin\phi\sin\theta, 2\cos\phi>, 0\leq \theta\leq 2\pi, 0\leq \phi\leq\frac\pi2$
  * $\vec r_\theta=2<-\sin\phi\sin\theta, \sin\phi\cos\theta, 0>$
  * $\vec r_\theta=2<\cos\phi\cos\theta, \cos\phi\sin\theta, -\sin\phi>$
  * $|vec r_\theta\times\vec r_\phi|=4<-\sin^2\phi\cos\theta, -\sin^2\phi\sin\theta, -\sin\phi\cos\phi(\sin^2\theta+\cos^2\theta)>$ $=4\sin\phi|<\sin\phi\cos\theta, \sin\phi\sin\theta, \cos\phi>|$ $=4\sin\phi$
  * In general for the standard parameterization of a sphere of radius $R$ $|\vec r_\theta\times\vec r_\phi|=R^2\sin\phi$
  * $\iint_S z(x^2+y^2)dS=\int_0^{2\pi}\int_{\phi=0}^{\pi/2}8\cos\phi\sin^2\phi 4\sin\phi d\phi d\theta=2\pi\cdot 32\int_{\phi=0}^{\pi/2}\cos\phi\sin^3\phi d\phi$$=2\pi\cdot 32[\frac{\sin^4\phi}4]_0^{\pi/2}$
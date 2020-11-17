# Twenty-Seventh Class
* Example from last time
  * Fireball with heat flow vector field $\vec F=\frac{1000}{(1+x^2+y^2+z^2)^2}<x, y, z>$, what is rate of heat loss if it is in a container of radius $A$ and height $2a$
  * Integral of $S_2$ (top): pick a parameterization of $S_2$
    * $\vec r(r, \theta)=<r\cos\theta, r\sin\theta, a>, 0\leq r\leq A, 0\leq \theta\leq 2\pi$
    * $\vec r_r=<\cos\theta, \sin\theta, 0>$
    * $\vec r_\theta=<-r\sin\theta, r\cos\theta, 0>$
    * $\vec r\times\vec r_\theta=<0, 0, r\cos^2\theta+r\sin^2\theta>=<0, 0, r>$, which is in same orientation as given orientation
    * $\vec F(\vec r(r, \theta))=\frac{1000}{(1+r^2+a^2)^2}<r\cos\theta, r\sin\theta, a>$
    * $\int_0^{2\pi}\int_0^A\vec F(\vec r(r, \theta))\cdot\vec r_r\times\vec r_\theta drd\theta=1000\int_0^{2\pi}\int_0^A \vec{ra}{(1+r^2+a^2)}drd\theta$
    * $=2000\pi a\int_0^A\frac{r}{(1+a^2+r^2)^2}dr=2000\pi a[-\frac12\frac1{(1+a^2+r^2)}]_0^A=1000\pi a[\frac1{a+a^2}-\frac1{1+a^2+A^2}]$
  * Integral of $S_1$ (side of cylinder): 
    * $\vec r(z, \theta)=<a\cos\theta, a\sin\theta, z>, -a\leq z\leq a, 0\leq \theta\leq 2\pi$
    * $\vec r_z=<0, 0, 1>$
    * $\vec r_\theta=<-A\sin\theta, A\cos\theta, 0>$
    * $\vec r_z\times\vec r_\theta=<-A\cos\theta, -A\sin\theta, 0>$
    * $\vec F=\frac{1000}{(1+A^2+z^2)^2}<x, y, z>=\frac{1000}{(1+x^2+y^2+z^2)^2}<A\cos\theta, A\sin\theta, z>$
    * $\iint_{S_1}\vec F\cdot \hat N_1 dS=\int_0^{2\pi}\int_{z=-a}^a\vec F(\vec r(z, \theta))\cdot \vec r_z\times\vec r_\theta dzd\theta$
    * $=-\int_0^{2\pi}\int_{-a}^a\frac{1000}{(1+A^2+z^2)^2}(-A^2) dzd\theta$
    * $=2000\pi A^2\int_{-a}^a\frac{dz}{1+A^2+z^2)^2}=2000\pi A^2\frac1{(1+A^2)^{3/2}}[\arctan(\frac a{\sqrt{1+A^2}})+\frac{a\sqrt{1+A^2}}{1+a^2+A^2}]$ (calc 2)
* Spherical coordinates
  * $\vec r(\theta, \phi)=<R\sin\phi\cos\theta, R\sin\phi\sin\theta, R\cos\phi>$
  * $\vec r_\theta\times\vec r_\phi=R^2\sin\phi<\sin\phi\cos\theta, \sin\phi\sin\theta, \cos\phi>$
* e.g. Let $S$ be the part of the surface $z=4-x^2-y^2$ lying above the $xy$-plane oriented upward. Let $\vec F=<x(x^2+y^2), y(x^2+y^2, z>$. Compute $\iint_S\vec F\cdot d\hat S$
  * In this case "upwards" means $z$ coordinate is positive
  * $\vec r(x, y)=<x, y, 4-x^2-y^2>, D=\{x^2+y^2\leq 4\}$
    * $\vec r_x=<1, 0, -2x>$
    * $\vec r_y=<0, 1, -2y>$
    * $\vec r_x\times\vec r_y=<2x, 2y, 1>$, $z$ is positive so in same direction
    * $\iint_S\vec F\cdot d\hat S=$ $\iint_{\{x^2+y^2\leq 4\}}\vec F(\vec r(x, y))\cdot\vec r_x\times\vec r_y dxdy=\iint_{\{x^2+y^2\leq 4\}}<x(x^2+y^2), y(x^2+y^2), 4-x^2-y^2><2x, 2y, 1>dxdy$ $=\iint_{\{x^2+y^2\leq 4\}}{(2x^2+2y^2)(x^2+y^2)+4-x^2-y^2)}dxdy$ $=\int_0^{2\pi}\int_0^2(2r^4+4-r^2)rdrd\theta=$$2\pi(\frac1364+8-4)=\frac{2\pi}{3}76$
  * $\vec r(z, \theta>=<\sqrt{4-z}\cos\theta, \sqrt{4-z}\sin\theta, z>$
    * $\vec r_z=<-\frac1{2\sqrt{4-z}}\cos\theta, -\frac{1}{2\sqrt{4-z}}\sin\theta, 1>$
    * $\vec r_\theta=<-\sqrt{4-z}\sin\theta, \sqrt{4-z}\cos\theta, 0>$
    * $\vec r_z\times\vec r_\theta=<-\sqrt{4-z}\cos\theta, -\sqrt{4-z}\sin\theta, -\frac12>$
    * $\iint_S\vec F\cdot d\hat S=-\int_0^{2\pi}\int_0^4<\sqrt{4-z}\cos\theta(4-z), \sqrt{4-z}\sin\theta(4-z), z>\cdot<-\sqrt{4-z}\cos\theta, -\sqrt{4-z}\sin\theta, -\frac12>dzd\theta$$=-\int_0^{2\pi}\int_0^4-(4-z)^2(\cos^2\theta+\sin^2\theta)-\frac z2 dzd\theta$$=2\pi\int_0^4((4-z)^2+\frac z2)dz=2\pi[-\frac13(3-z)^3+\frac{z^2}4]_0^4$$=2\pi[4+\frac{64}{3}]=\frac{2\pi}376$
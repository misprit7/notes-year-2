# Thirtieth Class
* Last time
  * Proved that for the very special vector field $\vec F=\frac{\vec r}{r^3}$, $\iint_S\vec F\cdot d\hat S= 0$ if origin is not in $S$, $4\pi$ if origin is inside $S$
* e.g. Buoyancy: liquid of density $\rho$, surface is the $xy$ plane. Pressure at depth $-z$ is given by $P=-\rho gz$. Find effect of pressure on solid $E$. 
  * $g\approx 9.8ms^{-2}=$ gravitational constant
  * Units work out to be force per square meter as expected for pressure
  * Fore of pressure on a small section $\partial E$ is in the direction $-\hat N$ ($\hat N$ oriented outward) and has magnitude $(-\rho gz)\cdot Area(\partial E)$
  * $Force=\iint_{\partial E}P(-\hat N)dS=\iint_{\partial E}\rho gz\hat NdS$ (not a flux integral)
  * To get $\hat i$ component of force: $Force\cdot\hat i=\iint_{\partial E}\rho gz\hat i\cdot\hat NdS$ which is a flux vector field
    * Analogous for other 2 dimensions
  * $div(<\rho gz, 0, 0>)=0=div(<0, \rho gz, 0>)$
  * $div(<0, 0, \rho gz>)=\rho g$ so $Force=\hat k\iiint_{E}\rho gdVol=\hat k\rho gVol(E)$
  * Force of buoyancy is straight up with magnitude $\rho g Vol(E)=$ weight of the liquid displaced
  * Called Archimedes' principle
    * Means that density greater than water means you float and you sink otherwise
* Remark: to apply divergence theorem to compute flux integral over a surface $S$, we need $S$ to be closed i.e. $S=\partial E$
  * Sometimes if $S$ is not closed, we can make it closed by adding another surface
  * If $S=S^\prime=\partial E$, then $\iiint_E(div\vec F)dVol=\iint_S\vec F\cdot d\hat S+\iint_{S^\prime}\vec F\cdot d\hat S$
* e.g. evaluate $\\int_S\vec F\cdot d\hat S$ where $\vec F=<z^2x, \frac13y^3+\tan\sqrt z, x^2z+y^2>$ and $S$ is the top half of the sphere $x^2+y^2+z^2=1$ oriented upwards
  * Doing this with a parameterization is nasty because of the $\tan\sqrt z$ term
  * If $S$ were closed we could use divergence theorem
  * $div\vec F=z^2+y^2+x^2$ which is very nice
  * Let $S^\prime$ be the disk of radius $1$ in the $xy$ plane oriented with $\hat N^\prime=-\hat k$. Then $\partial E=S+S^\prime$ where $E=\{x^2+y^2+z^2\leq 1, z\geq 0\}$
  * $\iiint_E(x^2+y^2+z^2)dVol=\iint_S\vec F\cdot d\hat S+\iint_{S^\prime}\vec F\cdot d\hat S$
  * $\iint_S\vec F\cdot d\hat S=\int_0^{2\pi}\int_{0}^{\pi/2}\int_0^1\rho^2\rho^2\sin\phi d\rho d\phi d\theta-\iint_{S^\prime}\vec F\cdot(-\hat k)dS^\prime$
  * $\iint_S\vec F\cdot d\hat S=2\pi[\frac{\rho^5}5]_0^1[-\cos\phi]_0^{\pi/2}+\iint_{x^2+y^2\leq 1}<-, -, y^2>\cdot \hat k dx dy=\frac{2\pi}5+\int_0^{2\pi}\int_0^1r^2\sin^2\theta r drd\theta=\frac{2\pi}5+\frac\pi4=\frac{13\pi}{20}$
* Green's Theorem
  * Suppose $C=\partial D$ (oriented counterclockwise) and $\vec F=<P, Q>$, then if $Q_x-P_y=0\Rightarrow\vec F$ conservative $\Rightarrow\oint_C\vec F\cdot d\vec r=0=\oint_C Pdx+Qdy$
  * Green's theorem states that in general, $\oint_CPdx+Qdy=\iint_D(Q_x-P_y)dx dy$
* e.g. $D=\{x^2+y^2\leq R^2\}$, $\vec F=<yx^2, x^3>$, verify Green's theorem
  * $\partial D=C_R$, $\vec r(t)=<R\cos t, R\sin t>, 0\leq t\leq 2\pi$
  * $\oint_C{R}\vec F\cdot d\vec r=\int_0^{2\pi}<R\sin t R^2\cos t, R^3\cos^3 t>\cdot <-R\sin t, R\cos t>dt=R^4\int_0^{2\pi}(-\sin^2 t\cos^2 t+\cos^4 t)dt=R^4\frac\pi2$
  * $\iint_{\{x^2+y^2\leq R^2\}}\frac\partial{\partial x}(x^3)-\frac\partial{\partial y}(yx^2)dx dy=\int_0^{2\pi}\int_0^R 2r^2\cos^2\theta rdr d\theta=2\pi\frac{R^4}4=\frac\pi 2R^4$
* Computing area with Green's theorem
  * Pick $P, Q$ s.t. $Q_x-P_y=1$ then RHS of Green's theorem is $Area(D)$
  * Let $Q=\frac12 x, P=-\frac12 y$, then $Area(D)=\frac12\oint_{\partial D}(xdy-ydx)$
* e.g. $D$ is the polygon with vertices $(x_1, y_1), \ldots, (x_n, y_1)$, find area
  * $\partial D=C_1+\ldots+C_n$, $C_i$ is segment from $(x_i, y_i)$ to $(x_{i+1}, y_{i+1})$
  * $Area(D)=\frac12\oint_C(xdy-ydx)=\frac12\sum_{i=1}^n\int_{C_i}xdy-ydx$
  * Parameterize $C_i$
    * $\vec r(t)=(1-t)<x_i, y_i>+t<x_{i+1}, y_{i+1}>, 0\leq t\leq 1$
    * $=<(1-t)x_i+tx_{i+1}, (1-t)y_i+ty_{i+1}>$
    * $x(t)=x_i+t(x_{i+1}-x_i), y(t)=y_i+t(y_{i+1}-y_i)$
  * $xdy-ydx=(x_i+t(x_{i+1}-x_i))(y_{i+1}-y_i)dt-(y_i+t(y_{i+1}-y_i))(x_{i+1}-x_i)dt=x_i(y_{i+1}+y_i)-y_i(x_{i+1}-x_i))dt=(x_iy_{i+1}-y_ix_{i+1})dt$
  * So $Area(D)=\frac12\sum_{i=1}^n(x_iy_{i+1}-y_ix_{i+1})$
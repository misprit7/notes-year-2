# Thirty-Fifth Class
* e.g. $x=r\cos\theta, y=r\sin\theta$, compute the two from $dx\wedge dy$ in terms of $dr\wedge d\theta$
  * $dx=\frac{\partial x}{dr}dr+\frac{\partial x}{\partial\theta}d\theta=\cos\theta dr-r\sin\theta d\theta$
  * $dy=\frac{\partial y}{\partial r}dr+\frac{\partial y}{\partial\theta}d\theta=\sin\theta dr+r\cos\theta d\theta$
  * $dx\wedge dx dy=(\cos\theta dr-r\sin\theta d\theta)\wedge (\sin\theta dr+r\cos\theta d\theta)=r\cos^2\theta dr\wedge d\theta-r\sin^2\theta d\theta\wedge dr=r dr\wedge d\theta$
* e.g. Suppose that $\vec r(u, v)=<x(u, v), y(u, v), z(u, v)>$ is a parameterization of a surface $S\sub\R^3$. Compute the $2$-form $\omega=Pdy\wedge dz+Qdz\wedge dx+Rdx\wedge dy$ in terms of $du\wedge dv$
  * $dx=\frac{\partial x}{\partial u}du+\frac{\partial x}{\partial v}dv$ and similarly with $y$
  * $dy\wedge dz=(y_udu+y_vdv)\wedge(z_udu+z_vdv)=y_u z_v-y_vz_u)du\wedge dv$
  * $dz\wedge dx=(z_ux_v-z_vx_u)du\wedge dv$
  * $dx\wedge dy=(d_uy_v-x_vy_u)du\wedge dv$
  * $\omega = (P(y_uz_v-y_vz_u)+Q(z_ux_v-z_vx_u)+R(x_uy_v-x_vy_u))du\wedge dv=<P, Q, R>\cdot(\vec r_u\times\vec r_v)du\wedge dv$
  * So we see that $\iint_S Pdy\wedge dz+Q dz\wedge dx+R dx\wedge dy=\iint_D <P, Q, R>\cdot(\vec r_u\times\vec r_v)du dv$ which is a flux integral
* Integration of differential forms
  * We can integrate a differential $k$-form over a $k$-dimensial manifold
  * In $\R^3$ an oriented $3$-form can be integrated over a solid $E$; $\iiint fdx\wedge dy\wedge dz$
  * A $2$ form $Pdy\wedge dz+Qdz\wedge dy+Rdx\wedge dy$ can be integrated over a surface $S$; $\iint_S Pdy\wedge dz+Qdz\wedge dx+Rdx\wedge dy=$ flux of $<P, Q, R>$ through $S$
  * A $1$-form $Pdx+Qdy+Rdz$ can be integrated over a $1$-dimensional manifold/curve $C$; $\int_C Pdx+Qdy+Rdz=\int_C<P, Q, R>\cdot d\vec r=$ work integral
  * The integral of a $0$-form $f$ over a zero dimensional manifold $\{p_1, \ldots, p_n\}$ is a signed sum $\sum_{i=1}^n\pm f(p_1)$ where sign depends on orientation
  * If $M$ is a $k$ dimensional oriented manifold and $\omega$ is a $k$-form$ then $\int_M\omega$ makes sense
* Generalized Stokes Theorem
  * If $\omega$ is a $(k-1)$-form and $M$ is a $M$ is a $k$-dimensional manifold then $\int_M d\omega=\int_{\partial M}\omega$
* Integral Primer
  * Two main categories: integrals of curves, integrals over surfaces
  * Integral over curves
    * Integrals of functions: $\int_C fds$ (includes arc length)
      * Use parameterization, compute directly $\int_C fds=\int_{t=a}^b f(\vec r(t))|\vec r^\prime(t)|dt$
    * Integrate vector fields, a.k.a work integrals or circulation integrals
      * $\int_C\vec F\cdot\vec TdS=\int_C\vec F\cdot d\vec r=\int_CPdx+Qdy+Rdz, \vec F=<P, Q, R>$ need orientation on $C$
      * If $\vec F$ is conservative, find $f$ such that $\vec\nabla f=\vec F$ and use FTLI $\int_C\vec F\cdot d\vec r=f(p_2)-f(p_1)$
        * Sometimes if we determine $\vec F$ is conservative, we can solve problem without finding $f$, for example using path independence
      * If $C$ is a loop in the place ane $\vec F$ only involves $(x, y)$, then apply Green's theorem (make sure $\vec F$ is well defined over $D$ where $C=\partial D$)
      * If $C$ bounds a surface $S$ in $\R^3$, then Stoke's can help (if for example $curl \vec F$ is simple)
      * Otherwise compute directly $\int\vec F\cdot d\vec r=\int_{r=a}^b\vec F(\vec r(t))\cdot\vec r^\prime(t)dt$
      * Advanced tricks for work integrals
        * $C$ is not closed, but we can add a curve to make and apply methods above
        * $\vec F$ is not conservative, but it is "close", then write $\vec F=\vec F_1+\vec F_2$ where $\vec F_1$ is conservative and $\vec F_2$ is simple
  * Surface integrals
    * Integrals of functions over a surface: $\iint_S fdS$ (includes surface area)
      * Forced to use a parameterization $\vec r(u, v)=<x(u, v), y(u, v), z(u, v)>$, $(u, v)\in D\sub\R^2$
      * $\iint_S fdS=\iint_Df(\vec r(u, v))|\vec r_u\times\vec r_v|du dv$
    * Integrals of vector fields over surfaces (a.k.a. flux integrals), requires orientation: $\iint_S(\vec F\cdot\hat N)dS=\iint_S\vec F\cdot d\hat S$
      * If $\vec F=curl\vec G$, we can apply Stoke's theorem
      * If $S$ is closed (i.e. $S=\partial E$, $E$ solid region) then apply divergence theorem
        * Makes sure $\vec F$ is defined on all of $E$
      * Compute directly with a parameterization $\iint_S\vec F\cdot d\hat S=\pm\iint_D\vec F(\vec r(u, v))\cdot(\vec r_u\times\vec r_v)du 0dv$
        * $\pm$ depends on whether $\vec r_u\times\vec r_v$ is in the same or opposite direction from $\hat N$
      * Advanced tricks:
        * Add a surface $S^\prime$ to make the surface closed and apply divergence theorem to $S+S^\prime=\partial E$
          * $\iiint_E(div\vec F)dVol=\iint_S\vec F\cdot d\hat S+\iint_{S^\prime}\vec F\cdot d\hat S$
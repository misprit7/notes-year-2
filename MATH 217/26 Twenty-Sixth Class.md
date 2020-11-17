# Twenty-Sixth Class
* Surface integration of vector field
  * Called flux
  * Think of vector field $\vec F$ as velocity of fluid flow
  * The component of $\vec F$ in the direction of $\hat N$ is the contribution to the flow
  * Flux = $\iint_S\vec F\cdot \hat N dS=\iint_S\vec F\cdot d\hat s$
* An orientation of $S$ is a choice of a unit vector field $\hat N$
  * $\iint_S\vec F\cdot d\hat s=-\iint_{-S}\vec F\cdot d\hat s$
  * Unlike the situation for curves can have non-orientable surfaces
    * For example mobius strip
* Orientation in $\R^3$
  * In $\R^3$ is right hand rule
  * Is our universe orientable? 
  * Non orientable would mean we could travel far and come back with our hearts on the right side
  * There are also non-oreientable surfaces with no boundary (closed srufaces) such as the klein bottle
    * Cannot be embedded into $\R^3$, i.e. must pass through itself
* Application to heat flow
  * If a substance has heat conductivity constant $K$ is at temperature $(x, y, z)$ then the heat flow is given by $\vec F(x, y, z)=-k\vec\nabla T$
* e.g. The wizard Toby of house vectorfell in the kingdom of Fluxdor casts a fireball with temperature $T(x, y, z)=\frac{500}{1+x^2+y^2+z^2}$. At what rate does heat escape from a magic containing sphere of radius $R$? (assume $K=1$)
  * $\vec F=-\vec \nabla T$
  * $\frac{\partial T}{\partial x}=\frac{-1000x}{(1+x^2+y^2+z^2)^2}$
  * $\vec F=\frac{1000}{(1+x^2+y^2+z^2)^2}<x, y, z>$
  * Heat flow $=\iint_{S_R}\vec F\cdot\hat NdS$
  * Here we can "eyeball" the $\hat N$ to be $\hat N=\frac1R<x, y, z>$ for all points on $S_R$
  * $\vec F=\frac{1000}{(1+R^2)^2}<x, y, z>$
  * $\iint_{S_R}\vec F\cdot \hat NdS=\iint_{S_R}\frac{1000}{(1+R^2)^2}<x, y, z\cdot \frac1R<x, y, z>dS$
  * Since $<x, y, z>\cdot<x, y, z>=R^2$, becomes $\frac{1000R}{(1+R^2)^2}\iint_{S_R}dS=\frac{4000\pi R^3}{(1+R^2)^2}$
* General unit normal vector
  * Recall given a parameterization $\vec r(u, v)$, the vectors $\frac{\partial\vec r}{\partial u}(u_0, v_0)$ and $\frac{\partial\vec r}{\partial v}(u_0, v_0)$ are tangent to surface
  * $\hat N=\frac{\vec r_u\times \vec r_v}{|\vec r_u\times\vec r_v|}$
  * Flux $=\iint_S\vec F\cdot\hat NdS=\pm\iint_D \vec F(\vec r(u, v))\cdot \frac{\vec r_u\times \vec r_v}{|\vec r_u\times\vec r_v|}|\vec r_u\times\vec r_v|dudv$ $=\pm\iint_D\vec F(\vec r(u, v))\cdot \vec r_u\times\vec r_v dudv$
    * Sign is plus if $\vec r_u\times\vec r_v$ is in the direction of $\hat N$, minus otherwise
  * Work: $\int_C\vec F\cdot\hat T ds=\int_{t=a}^b\vec F(\vec r(t))\cdot \vec r^\prime(t)dt$
* e.g. Toby's assistant Toruk makes a cylindrical container for the fireball. It has height $2a$ and radius $A$ with fireball centered in it, at what rate does heat escape the container?
  * Trying to find $\iint_S\vec F\cdot\hat NdS$ for each surface (top, side and bottom)
  * $S_1$ is side, $S_2$ is top and $S_3$ is bottom
  * Need to parameterize $S_1$ and $S_2$
  * $S2$: plane $z=a$, $\vec r(u, v)=<u, v, a>$
  * $\vec r_u=<1, 0, 0>, r_v=<0, 1, 0>, \vec r_u\times\vec r_v=<0, 0, 1>$ in direction of $\hat N_2$
  * $\iint_S{2}\vec F\cdot \hat N_2 dS=\iint_{u^2+v^2\leq A}\frac{1000}{(1+_u^2+v^2+a^2)^2}<u, v, a>\cdot<0, 0, 1>dudv$
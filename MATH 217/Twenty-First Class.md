# Twenty-First Class
* Vector field
  * Vector field in $\R^2$ is a function $\vec F(x, y)=<P(x, y), Q(x, y)>$ at each point in the domain of $\vec F$ we get a vector
  * We draw tail at the point
  * $F$ could be wind velocity, magnetic field, etc.
  * $\vec\nabla f=<f_x, f_y>$
* A vector field $\vec F$ is called conservative if $\exists$ an $f$ such that $\vec F=\vec \nabla f$. $f(x, y)$ is called a potential function. 
  * Is every vector field conservative? 
    * No
  * Is there an easy way to tell if a vector field is conservative? 
    * It depends
* Will of ten use the vector field $\vec r(x, y)=<x, y>$ or $\vec r(x, y, z)=<x, y, z>$
  * Also $\hat r(x, y, z)=\frac{\vec r(x, y, z)}{|\vec r(x, y, z)|}=<\frac x{\sqrt{x^2+y^2+z^2}}, \frac y{\sqrt{x^2+y^2+z^2}}, \frac z{\sqrt{x^2+y^2+z^2}}>$
  * $r=|\vec r(x, y, z)|=\sqrt{x^2+y^2+z^2}$
  * $\hat r$ is not defined at the origin
* e.g. Gravitational force
  * $\vec F(x, y, z)=\frac{-\hat r(x, y, z)}{r(x, y, z)^2}=-mMG\frac{vec r}{r^3}$
    * $m$ is mass of planut, $M$ is mass of sun, $G$ is gravitational constant
  * Note that from this persepective we regard gravity as existing everywhere
  * $\vec F$ is conservative:
    * $f(x, y, z)=\frac{mMG}{r}=\frac{mMG}{\sqrt{x^2+y^2+z^2}}$
    * $f_x=mMG\frac{-x}{(x^2+y^2+z^2)^{3/2}}=-mMG\frac{x}{r^3}$
    * $\vec\nabla f=\vec F$
    * $-f(x, y, z)$ is the potential energy
  * Suppose a planet of mass $m$ moves along a path $\vec r(t)=<x(t), y(t), z(t)>$
  * $\vec r^\prime(t)=\vec v(t)=<x^\prime(t), y^\prime(t), z^\prime(t)>$
  * Newton's law: $m\frac{d\vec v}{dt}=\vec F=\vec\nabla f$
    * Dot both sides by $\vec v(t)$ to get $m\vec v\cdot\frac{d\vec v}{dt}=\vec v(t)\cdot <f_x, f_y, f_z>=m\frac12\frac d{dt}(\vec v\cdot\vec v)=\frac{dx}{dt}\frac{\partial f}{\partial x}+\frac{dy}{dx}\frac{\partial f}{\partial y}+\frac{dz}{dt}\frac{\partial f}{\partial z}$
    * $\frac{d}{dt}(\frac12m|\vec v|^2-f)=f$
    * Left is kinetic energy, $-f$ is potential energy
* Not all vector fields are conservative: $\vec F=<3x^2+2xy, 15y+11xy>$
  * Is there some $f$ with $\vec F=\vec\nabla f$
  * $\vec F=<P, Z>$ we need $P=f_x, Q=f_y$
  * $f_{xy}=7x, f_{yx}=11y$
  * A necessary condition for $\vec F=<P, Q>$ to be conservative is $P_y-Q_x=0$
    * If $\vec F(x, y)$$ is defined everywhere, this condition is also sufficient
    * In general, sufficiency of this condition depends on the topology of the domain
  * For $\vec F=<P, Q, R>$ to be conservative, a necessary condition is that $R_y-Q_z=0, P_z-R_x=0, Q_x-P_y=0$
* Definition: the curl of $\vec F$ is $\vec{curl} \vec F=(R_y-Q_z)\vec i+(P_z-R_x)\vec j+(Q_x-P_y)\vec k$
  * Restate necessary condition for $\vec F$ to be conservative is $curl \vec F=\vec 0$
  * Notation: $\vec\nabla=\frac{\partial}{\partial x}\vec i+\frac{\partial}{\partial y}\vec j+\frac\partial{\partial z}\vec k$
  * $\vec{curl} \vec F=\vec\nabla \times \vec F=$ definition above
  * $\vec{grad}=\vec\nabla f=(\frac{\partial}{\partial x}\vec i+\frac{\partial}{\partial y}\vec j+\frac\partial{\partial z}\vec k)f$
* Line integrals
  * Integrals along a curve, not just a line
  * $f(x, y)$ is a function, want to define $\int_C fds$
  * We parametrize the curve $\vec r(t)=<x(t), y(t)>$, $a\leq t\leq b$
  * Divide up $[a, b]$ into $N$ segments of size $\Delta t=\frac{b-a}{N}$
  * $\int_C fds=\lim_{N\to\infty}\sum_{i=0}^{N-1}f(x(t_i), y(t_i))\Delta s_i=\lim_{N\to\infty}\sum_{i=0}^{N-1}f(x(t_i), y(t_i))|\vec r^\prime(t_i)\Delta t$
  * $=\int_{t=a}^bf(x(t), y(t))\sqrt{(x^\prime)^2+(y^\prime)^2}dt=\int_{t=a}^bf(\vec r(t))|\vec r^\prime(t)|dt$
  * If $f=1$ then is arclength
  * $f{abg}=\frac{\int_Cfds}{\int_Cds}$
  * $ds=|\frac{d\vec r}{dt}|dt$
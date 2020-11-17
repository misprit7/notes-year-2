# Twenty-Eighth Class
* $div, grad, curl$
  * $grad$: Functions $\rightarrow$ vector fields
    * $f\rightarrow\vec\nabla f=<f_x, f_y, f_z>$
  * $curl$: Vector fields $\rightarrow$ Vector fields
    * $\vec F=<P, Q, R>\rightarrow \vec \nabla\times\vec F=<R_y-Q_z, P_z-R_x, Q_x-P_y>$
  * $div$: Vector fields $\rightarrow$ functions
    * $\vec F=<P, Q, R>\rightarrow\vec\nabla\cdot\vec F=P_x+Q_y+R_z$
  * Relationships
    * $curl(grad(f))=\vec0$
      * Analogous to cross product between parallel vectors is $\vec 0$
      * $\vec A\times(\vec Ac)=\vec 0$
    * $div(curl(\vec F))=\vec0$
      * Analogous to how dot product between a vector and a cross product involving the vector is always $0$
      * $\vec A\cdot(\vec A\times\vec B)=0$
  * Functions $\underbrace{\rightarrow}_{grad=\vec \nabla}$ Vector fields $\underbrace{\rightarrow}_{curl=\vec \nabla\times}$ Vector fields $\underbrace{\rightarrow}_{div=\vec \nabla\cdot}$Functions
    * Sequence of linear maps, composition of two successive maps is $0$
    * Called a complex sequence of linear maps
    * Image of gradient is the conservative vector field
    * Image of curl are vector fields having a vector potential ($\vec F=curl(\vec G)$)
    * $curl \vec F=\vec -0$ is a necessary condition for $\vec F$ to have a potential function
    * $div\vec F=0$ necessary condition for $\vec F$ to have a vector potential
      * For sufficient also need domain to be simply connected
* Product rules
  * $(f(t)g(t))^\prime=f^\prime(t)g(t)+f(t)g^\prime(t)$
  * Many product rules, basically all have the form $D(A*B)=(DA)*B\pm A*(DB)$
    * $D$ is $div, curl, grad$
    * $*$ is dot product, cross product or scalar product
    * $A$ and $B$ are vector fields or functions
  * For example, $div$ rule
    * Trying to compute $div(f\vec F)$, $\vec F=<P, Q, R>$
    * $\vec\nabla\cdot(fF)=\vec \nabla\cdot<fP, fQ, fR>=f_xP+f_yQ+f_zR+f =(\vec\nabla f)\cdot\vec F+f(\vec\nabla\cdot\vec F)$ as expected
  * Another example, $div(\vec F_1\times\vec F_2)=(curl\vec F_1)\cdot\vec F_2-\vec F_1\cdot(curl\vec F_2)$
* e.g. $\vec r=<x, y, z>$, $r=|\vec r|$, $r=\sqrt{x^2+y^2+z^2}$. Compue $div(r^k\vec r)$. For which $k$ is $r^k\vec r$ divergence free? 
  * $\vec\nabla(r^k\vec r)=\vec\nabla(r^k)\cdot\vec r+r^k\vec\nabla\cdot\vec r$
  * $\vec\nabla\cdot\vec r=\vec\nabla\cdot<x, y, z>=3$
  * $\vec\nabla r=<\frac x{\sqrt{x^2+y^2+z^2}}, \frac y{\sqrt{x^2+y^2+z^2}}, \frac z{\sqrt{x^2+y^2+z^2}}>=\frac1r\vec r$
  * $\vec\nabla(r^k)=kr^{k-1}\vec\nabla r=kr^{k-1}\frac1r\vec r=kr^{k-2}\vec r$
  * $div(r^k\vec r)=(kr^{k-2}\vec r)\cdot\vec r+r^k3=kr^k+3r^k=(3+k)r^k$
  * Divergence free for $k=-3$, so $\frac{\vec r}{r^3}$ is divergence free (e.g. gravitation)
* Interpretation of $div, grad, curl$
  * $(\vec\nabla)(x_0, y_0, z_0)$ points in the direction of greatest change in $f$, magnitude is the rate of change
  * $\vec F$ vector field (e.g. velocity vector field of a fluid flow)
  * $(div\vec F)(x_0, y_0, z_0)$ is rate fluid is being created (or destroyed if it's negative) at $x_0, y_0, z_0$
    * A vector field with $div\vec F=0$ is called divergence free or incompressible
    * $(div\vec F)(x_0, y_0, z_0)=\lim_{\epsilon\to0}\frac1{\frac43\pi\epsilon^3}\iint_{S_\epsilon}\vec F\cdot d\hat S$
  * $(curl\vec F)(x_0, y_0, z_0)$ points in direction in which an infinitesimally small "rotor" turns the fasts given by the right hand rule, magnitude is how fast it's turning
    * $C_\epsilon$ is a circle centered at $(x_0, y_0, z_0)$ oriented perpendicular to $curl\vec F$
    * $|(curl\vec F)(x_0, y_0, z_0)|=\lim_{\epsilon\to0}\frac1{\pi\epsilon^2}\oint_{C_\epsilon}\vec F\cdot d\vec r$
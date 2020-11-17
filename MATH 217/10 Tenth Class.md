# Tenth Class
* Last time
  * $(D_{\vec u}f)(x_0, y_0)=$ rate of change of $f$ at $(x_0, y_0)$ if we move at unit speed in direction of $\vec u$
  * To compute this we parameterized the line through $(x_0, y_0)$ going in the direction of $\vec u$
  * If $\vec u=<a, b>$, then $\vec r(t)=<x_0, y_0>+t<a, b>$
  * $(D_{\vec u}f)(x_0, y_0)=<f_x(x_0, y_0), f_y(x_0, y_0)>\cdot \vec u$
* Gradient
  * $\vec \nabla f=<f_x, f_y>$
  * Is a vector field, i.e. for each $(x_0, y_0)$ the gradient is a vector
  * $D_{\vec u}f=\vec\nabla f\cdot \vec u$
  * Points in direction of greatest rate of change
  * Magnitude is rate of change
  * Is $\perp$ to contour lines
  * Also works in more than 2 variables, gradient is perpendicular to contour surface
  * In general, vector normal to $f$ is $\vec N=(\vec\nabla f)(x_0, y_0, z_0)$
  * If we have surface given by $f(x, y, z)=k$ and a point $(x_0, y_0, z_0)$ on the surface, equation of plane tangent to surface is $f_x(x_0, y_0, z_0)(x-x_0)+f_y(x_0, y_0, z_0)(y-y_0)+f_z(x_0, y_0, z_0)(z-z_0)=0$
* e.g. Consider the two sheeted hyperboloid $z^2=1+x^2+y^2$. There are two planes which are tangent to this surface and contain the points $(1, 0, 0)$ and $(0, \frac12, 0)$. Find the planes of tangency. 
  * Surface is $1=z^2-x^2-y^2=f(x, y, z)$
  * $\vec \nabla f = <-2x, -2y, 2z>$
  * $\vec N=(\vec\nabla f)(x_0, y_0, z_0)=<-2x_0, -2y_0, 2z_0>$
  * $-2x_0(x-x_0)-2y_0(y-y_0)+2z_0(z-z_0)=0$
  * $1=z_0^2-x_0^2-y_0^2$
  * $-x_0x+x_0^2-y_0y+y_0^2+z_0z-z_0^2=0$
  * $-x_0x-y_0y+z_0z=1=$ equation of tangent plane
  * Plane contains $(1, 0, 0)\Rightarrow x_0=-1$
  * Plane contains $(0, \frac12, 0)\Rightarrow y_0=-2$
  * $z_0^2=1+x_0^2+y_0^2=6\Rightarrow z_0=\pm\sqrt6$
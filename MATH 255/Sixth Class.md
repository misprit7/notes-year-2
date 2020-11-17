# Sixth Class
* e.g. Logistic equation
  * $\frac{dx}{dt}=Kx(M-x), k>0$
  * $\frac{dx}{dt}=0$ if $x=M$
  * Critical points $x=0$ and $x=M$
  * If $x>0$, $\frac{dx}{dt}<0$
  * If $0<x<M, \frac{dx}{dt}>0$
  * If $x<0, \frac{dx}{dt}<0$
  * Conclusion: if $x(0)>0$ or $0<x(0)<M$ then $x(t)\to M$
  * If $x(0)<0$ then $x(t)\to-\infty$
* Phase diagram
  * Phase diagram looks like arrows going towards each other for stable points and unstable otherwise
* e.g.
  * $x^\prime=\sin x$
  * Multiples of $\pi$ are critical points
  * Multiples of$2\pi$ are unstable, stable otherwise
* Euler's method
  * Intuition from slope field, following lines
  * $y^\prime(t)=f(y(t), t)$
  * Define time step $h$ and set times $t_n=t_0+nh$
  * $y_{n+1}\approx y(t_{n+1})=y_n+h\cdot f(t_n, y_n)$
  * The method derives from 1st order Taylor expansion of $y$, as $y(x_0+\epsilon=y(x_0)+y^\prime(x_0)\epsilon+o(\epsilon))$
  * As $h\to 0$, this numerical approximation converges to real solution
  * Most simple estimate
* e.g. $y^\prime=\frac{y^2}3, y(0)=1$
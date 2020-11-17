# Fourteenth Class
* e.g. The plane $x+y+2z=2$ intersects the paraboloid $z=x^2+y^2$ in an ellipse. Find the points on the ellipse closest and furthest from the origin. 
  * Want to find min/max of $f(x, y, z) = \sqrt{x^2+y^2+z^2}$ subject to two constraints $z=x^2+y^2$ and $x+y+2z=2$
  * Equivalent to $f(x, y)=\sqrt{x^2+y^2+(x^2+y^2)^2}$ constrained to $x+y+2(x^2+y^2-2=0$
  * Trick: When optimizing distance, find min/max of distance squared
  * $D_x=\lambda g_x\Rightarrow 2x+4x(x^2+y^2)=\lambda(1+4x)$
  * $D_y=\lambda g_y\Rightarrow 2y+4y(x^2+y^2)=\lambda(1+4y)$
  * $g=0\Rightarrow x+y+2(x^2+y^2)=2$
  * $\lambda = 0$ or $x=y$
    * $\lambda = 0\Rightarrow x=y=0$, so not a solution since' it doesn't satisfy constraints
    * $x=y\Rightarrow 2x+2(x^2+x^2)=2\Rightarrow x=-1$ or $x=\frac12$
* Integration
  * Recall one variable:
    * $y=f(x)$
    * $\Delta x=\frac{b-a}N$
    * $x+k=a+k\Delta x$
    * $\int_{x=a}^bf(x)dx=\lim_{N\to\infty}\sum_{i=0}^Nf(x_i)\Delta x$
    * Averave value of $f(x)$ over $[a, b]$ is $\frac1{b-a}\int_{x=a}^bf(x)dx$
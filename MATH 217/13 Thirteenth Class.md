# Thirteenth Class
* First midterm
  * Oct 15, 9:30-11 a.m.
  * Webwork will be regular homework assignment
    * Limited amount of time
    * Limited number of tries (~5)
  * 3 or 4 written problems
  * Traditional midterm download
  * Single pdf
  * Uploads allowed to 11:15 a.m.
  * May consult CPL book and course notes but nothing else
* Trying to max/min of $f(x, y)$ on a closed and bounded domain $D$
  * Find critical points on interior
  * Analyze boundary
    * Last time learned how to parameterize the boundary and find max, min of it
  * Often boundary is given in form $g(x, y)=0$
    * e.g. $D-\{(x, y):x^2+y^2\leq1\}$, then boundary is $x^2+y^2-1=0=g(x, y)$
    * Want to find maximum/minimum of $f$ subject to the constraint $g(x, y)=0z$
  * Key idea behind method of Lagrange multipliers: the maximum of $f(x, y)$ subject to the constraint $g(x, y)=0$ occurs at points on $g(x, y)$ where $\vec \nabla g$ is parrallel to $\vec\nabla f$, i.e. $\vec\nabla f=\lambda\vec\nabla g, \lambda\in\mathbb R$
  * Three equations, 3 unknowns
    * $g(x, y)=0$
    * $f_x=\lambda g_x$
    * $f_y=\lambda g_y$
* e.g. find maximum of $f(x, y)=xy$ on the domain $D=\{(x, y): x^2+\frac{y^2}4\leq1\}$
  * Critical poitns of $f$ on interior of $D$
    * $f_x=y=0$
    * $f_y=x=0$
    * $(0, 0)$ critical
    * $f_{xx}f_{xy}-f_{xy}^2=-1$, therefore saddle
  * Maximum of $f(x, y)=xy$ subject to constraint $g(x, y)=x^12+\frac{y^2}4-1=0$
    * $x^2+\frac{y^2}2-1=0$
    * $f_x=\lambda g_x\Rightarrow y=\lambda 2x$
    * $f_y=\lambda g_y\Leftarrow x=\lambda \frac y2$
    * After solving, possibilities are $(\frac1{\sqrt{2}}, \sqrt2), (-\frac1{\sqrt2}, \sqrt2), (\frac1{\sqrt{2}}, -\sqrt2), -(\frac1{\sqrt2}, -\sqrt2)$
    * Correspond to $f$ values of $1, -1, -1, 1$ respectively
  * Max occurs at $(\frac1{\sqrt{2}}, \sqrt2), (-\frac1{\sqrt{2}}, -\sqrt2)$ with value $1$
* Lagrange multipliers also work in three variable problems
* e.g. Find the equation of the plane which passes through $(1, 2, 3)$ and encloses the smallest volume in the positive octant
  * Forms triangle, with volume $\frac13\times base\times height$
  * Lable $x, y, z$ intercepts $a, b, c$ respecitvely
  * $V=\frac13(\frac12ab)c=\frac16abc$
  * Equation of the plane is $\frac xa+\frac yb+\frac zc=1$
  * Subject to constraint $\frac1a+\frac2b+\frac3c=1$
    * $g(a, b, c)=\frac1a+\frac2b+\frac3c-1$
  * $V(a, b, c)=\frac16abc$
  * Solving system of equations, we get 
    * $\frac16bc=-\frac\lambda{a^2}$
    * $\frac16ac=-\frac{2\lambda}{b^2}$
    * $\frac16ab=-\frac{3\lambda}{c^2}$
    * Solving gives $a=3, b=6, c=9$
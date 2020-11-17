# Sixth Class
* Quadratic equations
	* Linear equation determines a plane, now interested in equations involving $x^2,  y^2, z^2, xy, \ldots, x, y, z$
	* Curves in $\mathbb R^2$ given by quadratic equations: parabolas, circles, ellipses, hyperbolas, etc.
	* Ellipses: $\frac {x^2}a+\frac{y^2}b=1$
	* Circles: $(x-a)^2+(y-b)^2=c^2$
	* Hyperbola: $\frac{y^2}{a^2}-\frac{x^2}{b^2}=1$
		* e.g. $xy=1$
* In fact these are all the same up to a projective change of coordinates
	* In projective geometry we think about the set of rays through the origin, projected onto a plane
* Quadratic surfaces
	* To analyze quadratic surfaces in $\mathbb R^3$, we will study the curves we get by setting $x$ or $y$ to a constant (trace curves) or setting $z$ to a constant (contour curves)
	* e.g. $z=y^2-x^2$
	* When $x=0$ surface is parabola
	* When $y=0$ parabola facing downward
	* When $z=1$ we get hyperbola
	* When $z=-1$ another hyperbola facing different direction
	* Makes saddle shape
* Functions of 2 or 3 variables
	* A function $f$ with domain $D\sub\mathbb R^2$ is a rule $f$ which assigns to each point in the domain a real number $f(x, y)\in\mathbb R$
	* e.g. $f(x, y)=$ the tenth digit in the decimal expansion of $x$ if $y\in\mathbb Q$ and 0 if $y\notin\mathbb Q$
	* If $f$ is given by a formula there is usually an implicit domain
	* e.g. $f(x, y)=\sqrt{1-x^2-y^2}, D=\{(x, y): x^2+y^2\leq1\}$
	* e.g. $g(x, y)=\log(x+y), D=\{(x, y):y>-x\}$
	* e.g. $h(x, y)=\frac1{(x-1)^2+(y-1)^2}, D=\mathbb R^2-\{(1, 1)\}$
	* e.g. $k(x, y)=e^{x^2+y}+\sin(y^4+\sqrt[3]{x}), D=\mathbb R^2$
	* Just as in the one variable case we study/understand functions using their graphs
	* e.g. $f(x, y)=\sqrt{1-x^2-y^2}, D=\{(x, y): x^2+y^2\leq 1\}$, is a hemisphere
* Contour plots
	* We draw the curves $f(x, y)=K$ for various values of $K$ (usually even spaces)$
	* e.g. $\sqrt{1-x^2-y^2}=K$ for $K=0, \frac14, \frac12, \frac34, 1$
	* Contour plot is circles of radius $1-K^2$
	* Can be visualized as elevation maps
* Functions of 3 variables
	* Graph lives in 4-space, $w=f(x, y, z)$
	* We do have contour surfaces (level surfaces), but are hard to work with since they are nested
	* e.g. $f(x, y, z)=x^2+y^2+z^2$
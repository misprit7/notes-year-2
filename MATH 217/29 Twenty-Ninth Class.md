# Twenty-Ninth Class
* Divergence Theorem: If $E$ is a solid region in $\R^3$ and $S=\partial E$ (boundary of $E$), i.e. $S$ is the boundary of $E$ oriented with the outward vector, then $\iint_S\vec F\cdot d\hat S=\iiint_E(div\vec F)dVol$
  * Note that to use this to compute a flux integral  $S$ must be the boundary of a closed solid (i.e. $S$ has no boundary)
  * If $S=\partial E$, then $\partial S=\emptyset$
    * $\partial(\partial E)=\emptyset$
* e.g. Verify the divergence theorem for $E=\{(x, y, z): -1\leq x, y, z\leq 1\}$, the cube of side length $2$ centered at origin with vector field $\vec F=<x^3, y^3, z^3>$
  * $div\vec F=3x^2+3y^2+3z^2$
  * $\partial E=S=S_1+S_2+\ldots+S_6$
  * Flux method
    * By symmetry all faces are the same, so $\iint_S\vec F\cdot d\hat S=\iint_{S_1}\vec F\cdot\hat N_1d\hat S+\ldots+\iint_{S_6}\vec F\cdot\hat N_6d\hat S=6\iint_{S_1}\vec F\cdot\hat N_1 d\hat S$
    * $\vec r(x, y)=<x, y, 1>, -1\leq x\leq y\leq 1$
    * $\vec r_x=<1, 0, 0>, \vec r_y=<0, 1, 0>, \vec r_x\times\vec r_y=<0, 0, 1>$ which is correct orientation
    * Total flux is then $6\int_{x=1-1}^1\int_{y=-1}^1<x^3, y^3, 1>\cdot <0, 0, 1>dy dx=6\cdot 4=24$
  * Divergence theorem
    * $\iiint_E(div \vec F)dVol = \int_{-1}^1\int_{-1}^1\int_{-1}^1(3x^2+3y^2+3z^2)dz dy dx=3\int_{-1}^1\int_{-1}^1\int_{-1}^13z^2 dz dy dx=3\cdot 2\cdot 4=24$
* Note: solid body $E$ for divergence theorem can have cavities, e.g. $E=\{(x, y, z): 1\leq x^2+y^2+z^1\leq 4\}$
  * $\partial E=S_1+S_2$
  * Outside vectors are pointing outward, inside vectors are pointing towards the origin
* e.g. Let $\vec F=\frac{\vec r}{r^3}$, $\vec F=<\frac x{(x^2+y^2+z^2)^{3/2}}, \frac y{(x^2+y^2+z^2)^{3/2}}, \frac z{(x^2+y^2+z^2)^{3/2}}>$. Let $S$ be any closed surface, oriented outwards enclosing $(0, 0, 0)$. Compute $\iint_S\vec F\cdot d\hat S$
  * From last class this is divergence free, $div\vec F=0$
  * Let $E$ be the interior of $S$ so that $S=\partial E$
  * $\iint_S\vec F\cdot d\hat S=\iiint_F(div \vec F)dVol=0$, but **this is wrong**
  * In order to apply the divergence theorem, we need $\vec F$ to be defined on all of $E$, but $\vec F$ is not defined at $(0, 0, 0)$
  * Let $E^\prime$ be $E$ with a small ball of radius $\epsilon$ removed
  * Now $\partial E^\prime=S+S_\epsilon$
  * Divergence theorem applies to $E^\prime$ since the vector field $\vec F$ is defined everywhere in the volume
  * $0=\iiint_{E^\prime}(div\vec F)dVol = \iint_S\vec F\cdot\hat Nd S+\iint_{S_\epsilon}\vec F\cdot d\hat S\Rightarrow \iint_S\vec F\cdot d\hat S=-\iint_{S_\epsilon}\frac{\vec r}{r^3}\cdot (\frac{-\vec r}{r})d S=\iint_{S_\epsilon}\frac{r^2}{r^4} dS=\frac1{\epsilon^2}\iint_{S_\epsilon} dS=\frac{4\pi\epsilon^2}{\epsilon^2}=4\pi$
  * Therefore $\iint_S\vec F\cdot d\hat S=4\pi$

```diff
+ this text is highlighted in green
- $a+b=c$ this text is highlighted in red
```
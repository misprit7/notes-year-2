# Eleventh Class
* Max|min-imizing functions of two or three variables
  * Review of one variable
    * Want to find max/min of $f(x)$ on closed and bounded domain, i.e. $[a, b]$
    * Critical points when $f^\prime=0$
    * The max and the min will occur at either the critical points on interior or on the boundary
    * $F^{\prime\prime}<0$ implies local max, $f^{\prime\prime}$ implies local min, and $^{\prime\prime}=0$ could be either or neither 
  * For max|min-imizing $f(x, y)$ on a closed and bounded domain $R\sub\mathbb R^2$ we use same strategy
  * Max/min will lie on critical points on interior or on the boundary (which is now a curve)
  * We are also interested in classifying these critical points
  * $(x_0, y_0$ critical $\Leftrightarrow$ $(\vec\nabla f)(x_0, y_0)=\vec 0$, i.e. tangent plane is horizontal
  * Ordinary critical points
    * Local max
      * $z=-x^2-y^2$
    * Local min
      * $z=x^2+y^2$
    * Saddle / pass
      * $z=y^2-x^2$
      * Contour plot looks like a cross
  * Second derivative test
    * $D=\begin{vmatrix}f_{xx} & f_{xy}\\f_{yx} & f_{yy}\end{vmatrix}=f_{xx}f_{yy}-f_{xy}^2$
    * If $(x_0, y_0)$ is a critical point then: 
      * $D(x_0, y_0)<0\Rightarrow(x_0, y_0)$ is a saddle
      * $D(x_0, y_0)>0\Rightarrow(x_0, y_0)$ is a local min max, $f_{xx}>0\Rightarrow$ local min and $f_{xx}<0\Rightarrow$ local max
      * $D(x_0, y_0)=0\Rightarrow$ not ordinary critical point
* e.g. $f(x, y)=(2x-x^2)(2y-y^2)$, find and classify critical points
  * $(2-2x)(2y-y^2)=0$, $(2x-x^2)(2-2y)=0$
  * $2y(1-x)(2-y)=0$, $2x(1-y)(2-x)=0$
  * $(y=0$ or $x=1$ or $y=2)$ and $(x=0$ or $y=1$ or $x=2)$
  * If $y=0, (0, 0)$ or $(2, 0)$
  * If $x=1, (1, 1)$
  * If $y=2$, $(0, 2)$ or $(2, 2)$
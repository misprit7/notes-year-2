# Fifteenth Class
* Complex eigenvalues
  * $\vec X^\prime=P\vec X$, $P$ is a $2\times2$ real matrix
  * $(0, 0)$ is a critical points which is classifiable from $P$'s egenvalues
  * $\lambda_1, \lambda_2$ are complex, so in this case they are complex conjugates
    * i.e. $\lambda_1=a+ib, \lambda_2=a-ib, b\neq0$
  * From past lectures, we know that solutions are linear combinations of $Re(e^{\lambda_1t}\vec v_1)$ and $Im(e^{\lambda_1t}\vec v_1)$, where $\vec v_1$ is an eigenvector associated with $\lambda_1$
  * $a=0$
    * $\Rightarrow Re(e^{ibt}\vec v_1)$ and $Im(e^{ibt}\vec v_1)$ are solutions
    * Means that solutions are periodic (of period $\frac{2\pi}b$)
    * Obtain a parameterization of an ellipse 
      * Generic parameterization: $x(t)=\alpha \cos t, y(t)=\beta \sin(t)$
    * Phase portrait looks like ellipse centered around origin
    * $(0, 0)$ is called a center
  * $a<0$
    * $Re(e^{\lambda _1 t}\vec v_1)=e^{at}Re(e^{ibt}\vec v_1)$
    * Since $e^{at}$ goes to zero, trajectories will converge to the origin
    * Phase portrait looks like spiral going towards origin
    * $(0, 0)$ called a spiral sink (stable)
  * $a>0$
    * Same as $a<0$ except in reverse
    * Phase portrait looks like spiral going outward
    * $(0, 0)$ called spiral source (unstable)
* Nullclines
  * To complete the phase portrait, one can also include (besides critical points, vector field and trajectories) $x$ and $y$ nullclines
  * Defined as the set of points such that the vector field is horizontal ($y$ nullcline) or vertical ($x$ nullcline)
  * Remark: this also helps to guess the direction of the field in the whole $x-y$ plane
* e.g. $\begin{pmatrix}x^\prime\\y^\prime\end{pmatrix}=\begin{pmatrix}1&0\\1&2\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix}=P\vec x$
  * Eigenvalues of $P$  
    * Characteristic polynomial is $(1-\lambda)(2-\lambda)$
    * Eigenvalues are $\lambda_1=1, \lambda_2=2$
  * Eigenvectors
    * Solving gives $\vec v_1=<1, -1>, \vec v_2=<0, 1>$
  * Critical point
    * $<0, 0>$, since it is linear
    * Stability: unstable source, since both eigenvalues are positive
  * $x$ and $y$ nullclines
    * $x$ nullclines: solve $P\vec x=0\Leftrightarrow x=0$
    * Therefore $x$ nullcline is vertical line
    * $y$ nullcline: solve $P\vec x=0\Leftrightarrow x=-2y$
    * Therefore $y$ nullcline is line along vector $<-2, 1>$
  * Nullclines define 4 quadrants where we can qualitively tell the direction of the field
    * Can tell sign of field by looking which nullclines the regions is between by taking test points
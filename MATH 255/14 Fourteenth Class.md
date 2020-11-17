# Fourteenth Class
* Remarks on linear ODEs from last time
  * If $P$ of size $n$ has $n$ distinct eigenvalues, then using the solutions above allows to completely solve the system (the set of solutions is a vector space of size $n$)
  * If not, there are multiple eigenvalues ($\dim(\ker(P-\lambda I))>1$) and we cannot get all solutions by just extractng eigenvectors
    * In this case one can build additional independent solutions (refer to textbook 3.7, won't be tested on)
* 2 dimensional systems and their vector fields
  * $<x^\prime, y^\prime>=P<x, y>$, $P$ is $2\times2$ matrix
  * Solutions of this autonomous system can be represented inn the $x-y$ plane and define trajectories, or solutions curves, consistent with the vector field associated with the equation
  * To get vector field at each point $\vec x$ associated $\vec x^\prime=\vec g(\vec x)$, we can associate a phase velocity $\vec g(\vec x)$
* e.g. $y^{\prime\prime}+y=0\Leftrightarrow\begin{pmatrix}x_1\\x_2\end{pmatrix}^\prime=\begin{pmatrix}0&1\\-1&0\end{pmatrix}\begin{pmatrix}x_1\\x_2\end{pmatrix}$ with $x_1=y$ an $x_2=y^\prime$. What is the vector field?
  * $\vec g=\begin{pmatrix}0&1\\-1&0\end{pmatrix}$, so $\vec g(<x_1, x_2>)=<x_2, -x_1>$
  * Exercise: one can show solution curves are circles centered at $0$ (solve the system with the eigenvalue method)
  * We call the diagram of these trajectories the phase portrait of the system
* 1D case
  * In 1D, we can study the asymptotic behaviour of an autonomous ODE by studying critical points and their stability
* 2D analysis
  * $<x^\prime, y^\prime>=P<x, y>$, we have that $<0, 0>$ is a critical point since $P<0, 0>=\vec 0$
  * We now assume that this is the only one (otherwise, the null space of $P$ would be of dimension $\geq 1$, and so the system would reduce to an ODE in 1D)
  * Means that $P$ has 2 non-null eigenvalues, $\lambda_1, \lambda_2$ with eigenvectors $\vec v_1, \vec v_2$
  * Well now classify the behaviour and stability of solutions according to $\lambda_1, \lambda_2$
  * Case 1: $\lambda_1, \lambda_2\in\R$
    * Along the lines of direction $\vec v_i, i=1, 2$, each point $\vec x=C\vec v_1$, so the phase velocity is $P(C\vec v_i)=\lambda_iC\vec v_i=\lambda_i\vec x$
    * Along the line $R\vec v_i$ the field is tangent to $R\vec v_i$ and the direction depends on the sign of $\lambda_i$
    * If $0<\lambda_1<\lambda_2$, field is going away from origin
      * $(0, 0)$ is a nodal source and is unstable
      * Outside $\vec v_1$ and $\vec v_2$, we know that solutions are linear combinations of $e^{\lambda_1t}\vec v_1$ and $e^{\lambda_1t}\vec v_2$
      * As $0<\lambda_1<\lambda_2$, when $t\to\infty$, $e^{\lambda_1t}<<e^{\lambda_2t}$ so dominates solution
      * $\lambda_1$ is weak eigenvalue whiel $\lambda_2$ is strong
    * If $0>\lambda_1>\lambda_2$, $\lambda_1$ is weak and $\lambda_2$ is strong
      * Trajectories converge faster along $R\vec v_1$
      * $(0, 0)$ is a nodal sink and is a stable node
    * If $\lambda_1<0<\lambda_2$, $(0, 0)$ is a saddle point and is unstable
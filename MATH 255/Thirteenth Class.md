# Thirteenth Class
* System of ODEs
  * So far, have been studying scalar DEs (1D)
    * Means only one dimension
  * More complex systems and phenomena require higher dimensionality
    * Systems of several coupled ODEs
  * An example is epidemiology, where SIR model (1927) is used to model measles and COVID 19
  * To study the spread of a disease among a population, we divide it into different variables
    * Susceptible population $S(t)$
    * Infected $I(t)$
    * Recovered $R(t)$
  * $S(\beta)\Rightarrow I (\gamma)\Rightarrow R$
  * System of equations
    * $\frac{dS}{dt}=\beta SI$
    * $\frac{dI}{dt}=\beta SI-\gamma I$
    * $\frac{dR}{dt}=\gamma I$
  * This kind of system can get more and more complex with more variables as we add more variables
  * More generally, we define a 1st order system of ODEs as a system of type
    * $x_1^\prime=g_1(x_1, \ldots, x_n, t)$
    * $x_2^\prime=g_2(x_1, \ldots, x_n, t)$
    * $\ldots$
    * $x_n^\prime=g_n(x_1, \ldots, x_n, t)$
  * In vector notation $\vec x=\vec g(\vec x, t)$ where $\vec x=(x_1, \ldots, x_n)\in\R^n$
  * A solution $\vec x(t)=(x_1, \ldots, x_n)$ is obtained when it satisfies this system of equations when substituded in
* Linear systems
  * Linear systems are written $\vec x^\prime = P(t)\vec x + \vec f(t)$
    * $\vec x$ and $\vec f$ are of size $n$
    * $P(x)$ is a matrix of size $n\times m$
  * This system is homogenous if $\vec f=0$
* Theorem: The solutions of a homogenous 1st order system of size $n$ form a vector space of dimension $n$, so solutions are of the form $\vec x=C_1\vec x_1+C_2\vec x_2+\ldots+ C_n\vec x_n$ where $C_1, \ldots, C_n$ and $\vec x_1, \ldots, \vec x_n$ are linearly independent solutions
  * Remark: Any linear combination of solutions is also a solution of the system. 
  * $\vec x_1(t), \ldots, \vec x_n(t)$ are linearly independent on an interval $I$ if $\lambda_1\vec x_1+\ldots\lambda_n\vec x_n=\vec 0$ for all $t\in I$, $\lambda_1=\lambda_2=\ldots=\lambda_n=0$
  * For example, if $n=2$, $\vec x_1$ and $\vec x_2$ are independent if one is a multiple of the other
* Eigenvalue method
  * To solve linear systems, we will take advantage of tools from matrix algebra, and more precisely decomposition of a matrix into eigenvalues and eigenvectors
  * Definition: for a matrix $M$, $\vec v$ is a eigenvector with associated eigenvalue $\lambda$ if $M\vec v=\lambda \vec v$
  * For linear systems, $\vec x^\prime=M\vec x$ with $M$ constant
  * Suppose that $M$ has an eigenvector $\vec v$ with eigenvector $\lambda$ and consider $\vec x(t)=e^{\lambda t}\vec v$
  * $\vec x^\prime(t)=\lambda e^{\lambda t}\vec v$
  * $M\vec x(t)=M(e^{\lambda t}\vec v)=e^{\lambda t}\cdot M\vec v=\lambda e^{\lambda t}\vec v$ using the fact that $\vec v$ is an eigenvector
  * Therefore $\vec x^\prime(t)=M\vec x$
  * Therefore $e^{\lambda t}\vec v$ is a solution
* $\lambda$ is an eigenvalue of $M$ if $\exists \vec x\neq \vec 0, M\vec x=\lambda \vec x$
  * Equivalent to $(M-\lambda I)\vec x=\vec 0$ and $\ker(M-\lambda I)\neq\{\vec 0\}=$ "null space"
  * Means that $\det(M-\lambda I)=0$ from linear algebra, which is a polynomial equation in $\lambda$
  * We call $\chi_M(\lambda)=\det(M-\lambda I)$ the characteristic polynomial associated with $M$, with $\lambda$ being the roots
* e.g. $M=\begin{pmatrix}2&1&1\\1&2&0\\0&0&2\end{pmatrix}$
  * Characteristic polynomial are $1, 2, 3$ (exercise)
  * To solve subtract eigenvalues from diagonal and take determinant
  * One we have eigenvalues, still need to find eigenvectors, in this case e.g. eigenvector for $\lambda=1$
  * $Mx=\lambda x\Leftrightarrow\begin{pmatrix}2&1&1\\1&2&0\\0&0&2\end{pmatrix}\begin{pmatrix}x_1\\x_2\\x_3\end{pmatrix}=\lambda\begin{pmatrix}x_1\\x_2\\x_3\end{pmatrix}$, need to solve to find $x_i$ (exercise for live session)
  * Solutions of $\vec x^\prime=M\vec x=C_1<1, -1, 0>e^t+C_2<0, 1, -1)e^{2t}+C_3<1, 1, 0>e^{3t}$, with $C_1, C_2, C_3$
* Theorem: If $P$ has $n$ distinct real eigenvalues, $(\lambda_i)_{1\leq i\leq n}$, then the general solution of $\vec x^\prime=P\vec x$ is $C_1\vec v_1e^{\lambda_1t}+\ldots+C_n\vec v_ne^{\lambda_n t}$ where $C_i$s are constant
  * Remark: Real polynomials do not necessarily have all distinct real roots, for example $x^1+1$ has $2$ imaginary roots $i$ and $-i$
  * Remark: If $P$ is a real valued constant square matrix with a complex eigenvalue $\lambda = a+ib$ and complex eigenvector $\vec v$, then $P$ also has for eigenvalue the complex conjugate of $\lambda =a-ib$, with complex conjugate eigenvectors $\bar{\vec v}$
    * Proof: $P\vec v=\lambda\vec v\Rightarrow\bar{P\vec v}=\bar{\lambda \vec v}\Rightarrow \bar P\cdot\bar{\vec v}=\bar \lambda\bar{\vec v}\Rightarrow P\bar{\vec v}=\bar \lambda\bar{\vec v}$
* Theorem: 2 linearly independent real solutions of $\vec x^\prime(t)=P\vec x$ are $\vec x_1(t)=Re(\vec ve^{\lambda t}), \vec x_2(t)=Im(\vec v e^{\lambda t})$ when $P$ has complex eigenvalue $\lambda$ with eigenvector $\vec v$
  * This comes from the fact that $Re(z)=\frac{z+\bar z}2, Im(z)=\frac{z-\bar z}{2i}$
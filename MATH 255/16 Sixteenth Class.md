# Sixteenth Class
* Nonhomogeneous systems
  * We now study $\vec X^\prime=A(t)\vec x+\vec f(t)$
  * Similarly to 1D, solutions are in form $\vec X=\vec X_c+\vec X_p$
    * $\vec X_c$ is complementary solution
    * $\vec X_p$ is particular solution
* Variation of parameters (dimension $n$)
  * In dimension $n$, we know that complementary solutions are linear combinations of $n$ independent solutions
    * $\vec X_c=C_1\vec X_1+\ldots+C_n\vec X_n$
  * Given these independent functions, we look for $\vec X_p$ of the form $\vec X_p=X\vec u(t)$
    * $\vec X_p$ and $\vec u(t)$ are both vectors of size $n$
    * $X=(\vec X_1, \ldots, \vec X_n)=$ fundamental matrix of the system
  * If $\vec X_p=X\vec u$, then $\vec X_p^\prime=X^\prime\vec u+X\vec u^\prime$ and $\vec X^\prime=(A\vec X_1, \ldots, A\vec X_n)$, i.e. $\vec X=AX$
    * $\vec X_p^\prime=AX\vec u+X\vec u^\prime$
    * Since $\vec X_p$ is a solution of $\vec X^\prime=A\vec X+\vec f$ we also have $\vec X_p^\prime=A\vec X_p+\vec f=AX\vec u+\vec f$
    * $AX\vec u+X\vec u^\prime=AX\vec u+\vec f\Rightarrow X\vec u^\prime=\vec f$
  * Remark: $X^{-1}$ exists (because $\vec X_i$s are independent)
    * Means $\vec u^\prime=X^{-1}\vec f$
    * $\vec X_p=X\int^t(X^{-1}(s))\vec f(s)ds$
  * In practice, follow following steps to solve nonhomogeneous system
    * Find solutions of the homogenous solution
    * Compute $X^{-1}$ to find $\vec X_p$ using $\vec X_p=X\int^t(X^{-1}(s))\vec f(s)ds$
      * Will only actually do this with systems of size $2$ where inverse follows formula if $X=\begin{pmatrix}a&b\\c&d\end{pmatrix}$ then $X^{-1}=\frac1{\det X}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$
        * $\det X=ad-bc$
* e.g. Solve $x^\prime=-5y+2, y^\prime=5x+1, x(0)=0, y(0)=0$
  * $\vec X^\prime=\begin{pmatrix}0&-5\\5&0\end{pmatrix}\vec X+\begin{pmatrix}2\\1\end{pmatrix}$
  * Solve homogenous system
    * $\lambda_{1, 2}=\pm 5i$
    * Eigenvector $\vec v=<1, -i>$
    * Therefore $\vec ve^{5it}=<\cos 5t, \sin 5t>+i<\sin 5t, -\cos 5t>$
    * $\vec X_c(t)=C_1<\cos 5t, \sin 5t>+C_2<\sin 5t, -\cos 5t>$
  * Variation of parameters
    * $\vec X_p=(\vec X_1\ \vec X_2)\int^t(\vec X_1\ \vec X_2)^{-1}<2, 1>ds$
    * $X^{-1}=\frac1{-\cos^2 t-\sin^2 t}\begin{pmatrix}-\cos 5t&-\sin 5t\\-\sin 5t&\cos 5t\end{pmatrix}=\begin{pmatrix}\cos 5t&\sin 5t\\\sin 5t&-\cos 5t\end{pmatrix}$
    * $X^{-1}<2, 1>=\begin{pmatrix}2\cos 5t+\sin 5t\\2\sin 5t-\cos 5t \end{pmatrix}$
    * So $\vec X_p=\begin{pmatrix}\cos 5t&\sin 5t\\\sin 5t&-\cos 5t\end{pmatrix}\begin{pmatrix}\int^t2\cos 5t+\sin 5t dt\\\int^t 2\sin 5t-\cos 5t dt \end{pmatrix}=\frac15<-1, 2>$ (exercise)
  * So $\vec X=\frac15<-1, 2>+<\cos 5t, \sin 5t>+ 2<\sin 5t, -\cos 5t>$ (initial conditions left as exercise)
* Nonlinear systems
  * We will see how the information gained in the study of linear systems can be useful to study non linear ones
* Lineralization, critical points and equilibrium
  * Focus on autonomous system $\vec X^\prime=f(\vec X)$ where $\vec f$ does not depend explicitely on time and $\vec f$ is not necessarily linear
  * Definition: a critical point is a solution $\vec X=\vec X_0$ of $\vec f(\vec X_0)=\vec 0$
    * Critical points correspond to equilibrium solutions $\vec X(t)=\vec X_0$
    * $\vec X_0$ constant function
* e.g. $x^\prime=y, y^\prime=-y+x+x^2$
  * Critical points: $(0, 0)$ and $(-1, 0)$
  * Will use these to find out about stability of critical points
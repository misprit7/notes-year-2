# Seventeenth Class
* Classification of critical points
  * $\vec x^\prime=\vec f(x)$
  * Critical points $\vec x_0$ if $\vec f(\vec x_0)=\vec 0$
  * We know from generalized Taylor series theorem that $F(x-x_0, y-y_0)=F(x_0, y_0)+DF(x_0, y_0)<x-x_0, y-y_0>+o(||(x-x_0, y-y_0)||)$
    * $DF$ is differential form of $F$ at $(x_0, y_0)$ (matrix of size 2)
    * $o(\ldots)$ is a term that vanishes
    * $DF(x_0, y_0)=\begin{pmatrix}\frac{\partial f}{\partial x}&\frac{\partial f}{\partial y}\\\frac{\partial g}{\partial x}&\frac{\partial g}{\partial y}\end{pmatrix}_{(x_0, y_0)}$
    * $DF$ is called the Jacobian matrix associated with $\vec F=<f(x, y), g(x, y)>$ evaluated at $(x_0, y_0)$
* e.g. $F(x, y)=<y, -y+x+x^2>$
  * $DF(x_0, y_0)=\begin{pmatrix}\frac{\partial f}{\partial x}&\frac{\partial f}{\partial y}\\\frac{\partial g}{\partial x}&\frac{\partial g}{\partial y}\end{pmatrix}_{(x_0, y_0)}=\begin{pmatrix}0&1\\1+2x^0&-1\end{pmatrix}$
  * Previously, we found $2$ critical points at $(0, 0)$ and $(-1, 0)$
  * $DF(0, 0)=\begin{pmatrix}0&1\\1&-1\end{pmatrix}$
  * $DF(-1, 0)=\begin{pmatrix}0&1\\-1&-1\end{pmatrix}$
  * In terms of notation, we commonly denote the Jacobian matrix of $F$ at $(x_0, y_0)$ as $Jac(F(x_0, y_0)$
* Definition: We call the linearization of $\vec x^\prime=\vec F(x, y)$ at $(x_0, y_0)$ the linear system $<u, v>^\prime=Jac(F(x_0, y_0))<u, v>$
  * St critical points, the linearized system can be seen as an approximation of the original one, which will help to study stability
* Definition: A critical point is isolated if it is the only critical point in some sufficiently small rectangle (dim 2) that contains the critical point
* Definition: A system of critical points is almost linear if the critical point is isolated, and the jacobian matrix at the critical point is invertible
  * In this case, we can approximate $\vec x^\prime=f(\vec x)$ near $\vec x=\vec x_0$ by the linearization $\vec u^\prime=D\vec f(\vec x_0)\cdot\vec u$
  * This will allow to assess the stability of the critical point
* Definition: A critical point $\vec x_0$ is stable if every solution that starts $\vec x(t)$ that starts at $t=0$ with $\vec x(0)$ sufficiently close to $\vec x_0$ remains arbitrarily close to $\vec x_0$ for all $t\geq0$
  * Unstable if it is not stable
  * Asymptotically stable if it is stable, and every solution $\vec x(t)$ that starts with $\vec x(0)$ sufficiently close to $\vec x_0$ converges to $\vec x_0$, i.e. $\lim_{t\to\infty}\vec x(t)=\vec x_0$
* In most cases, the local behavior and stability of critical points can be determined from the Jacobian matrix and its eigenvalues
  * $\lambda_1\neq\lambda_2, \lambda_1, \lambda_2>0$: nodal source (unstable node), unstable
  * $\lambda_1\neq\lambda_2, \lambda_1, \lambda_2<0$: nodal sink (stable node), asymptotically stable
  * $\lambda_1<0<\lambda_2$: saddle, unstable
  * $\lambda_1=a+ib, a>0, b\neq 0$, spiral source, unstable
  * $\lambda_1=a+ib, a<0, b\neq0$, spiral sink, asymptotically stable
  * Remark: Like for the linear case, we won't cover double eigenvalues
  * When the eigenvalues are purely imaginary ($\lambda_1=ib$, center in the linear case), we cannot tell the stability and the critical point can be a spiral source, sink or center
    * Behavior depends on higher order terms in the Taylor expansion
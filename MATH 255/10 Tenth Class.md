# Tenth Class
* Second order linear equations
  * $y^{\prime\prime}+p(x)y^{\prime}+q(x)y=0 (E)$
  * Left hand of side of $(E)$ is the result of an "operator" $L$ on $y$
  * An operator $L$ is linear if $\forall a, b\in\mathbb R, \forall y, y_2$ then $L(ay_1+by_2)=aL(y_1)+bL(y_2)$
  * The operator above is linear
    * Can prove easily since derivative is linear and expand out terms
  * Also cant hink of $L$ as $\begin{pmatrix}y\\y^\prime\end{pmatrix}^\prime=\underbrace{\begin{pmatrix}0 &1\\-q &-p\end{pmatrix}}_M\begin{pmatrix}y\\y^\prime\end{pmatrix}=\begin{pmatrix}y^\prime\\-qy-py^\prime\end{pmatrix}$
  * $\begin{pmatrix}y\\y^\prime\end{pmatrix}^\prime=M\begin{pmatrix}y\\y^\prime\end{pmatrix}\Leftrightarrow\begin{pmatrix}y\\y^\prime\end{pmatrix}^\prime-M\begin{pmatrix}y\\y^\prime\end{pmatrix}=\begin{pmatrix}0\\0\end{pmatrix}$
  * Having $L(y)=\begin{pmatrix}0\\0\end{pmatrix}$, solutions $(E)$ can now be seen as the kernel (or null-space) of the linear operator
    * We know that this null-space forms a vector space
* Superposition and linearity of solutions theorem
  * If $y_1$ and $y_2$ are solutions to $(E)$, then $ay_1+by_2$ is also a solution
  * The solutions of $(E)$ form a vector space of dimension $2$. 
  * The general solutions of $(E)$ are $\begin{cases}ay_1+by_2, a, b\in\mathbb R\end{cases}$ where $y_1$ and $y_2$ are indepenent solutions of $(E)$. 
  * 2 functions $y_1$ and $y_2$ if $ay_2+by_2\equiv0\Rightarrow a=b=0$
* Existense and uniquenss of IVP
  * If $p$ and $q$ are continuous on an interval $I$ then there exists a unique solution of $(E)$ that satisfies the IC $\begin{cases}y(a)=b_0\\y^\prime(a)=b_1\end{cases}$ where $a\in I$ and $b_0, b_1\in\mathbb R$
* Linear second order ODE with constant coefficients
  * We now consider $ay^{\prime\prime}+by^\prime+cy=0(E)$, where $a, b, c\in\mathbb R$
  * Want to show that for constant coefficient, solutions can be written as $y(x)=e^{rx}$ where $r$ has to be determined
  * $(x)\Rightarrow a(e^{rx})^{\prime\prime}+b(e^{rx})^\prime+ce^{rx}=0$
  * $ar^2e^{rx}+bre^{rx}+ce^{rx}=0$
  * $ar^2+br+c=0(*)$
  * If $r$ is solution of $(*)$ then $y(x)=e^{rx}$ is a soludion of the ODE. 
  * If we solve $ax^2+bx+c=0$, and we get two roots $x_1, x_2$, then we can derive the set of solutions of the ODE
  * $ax^2+bx+c$ is called the characteristic equation associated with $(E)$
* Theorem: The solutions of $(E)$ depend on $\Delta=b^2-4ac$
  * If $\Delta>0$ two real roots $r_1, r_2$
    * $y=C_1e^{r_1x}+C_2e^{r_2x}$
  * If $\Delta = 0$, 1 root $r$
    * $y=C_1e^{rx}+C_2xe^{rx}$
  * If $\Delta <0$, 2 conjugate roots, $r_{\pm}=\alpha\pm i\beta$
    * $y=C_1e^{\alpha x}\cos(\beta x)+C_2e^{\alpha x}\sin(\beta x)$
# Seventh Class
* Exact solutions
  * Derive from energy, or potential function $F(x, y(x))$
  * Suppose that we're given such a function we can define the orbits, or trajectories of constant energy
  * $F(x, y(x))=C$
  * These trajectories can be seen as solutions of differential equations
  * To see this, differentiate $F$
  * Taylor expansion: $F(x+dx, y+dy)=F(x, y)+<(\frac{\partial F}{\partial x}, \frac{\partial F}{\partial y})\cdot (dx, dy)>+o(||(dx, dy)||)$
  * $F(x, y)=C\Leftrightarrow dF=0$
  * $dF=\frac{\partial F}{\partial x}dx+\frac{\partial F}{\partial y}dy\Leftrightarrow M+N\frac{dy}{dx}=0, M=\frac{\partial F}{\partial x}, N=\frac{\partial F}{\partial y}$
  * Def: an ODE is called exact if it can be written as $dF=0$, for some potential function $F(x, y)$ and in this case, solutions satisfy $F(x, y(x))=C$
  * Remark: If we have $M+N\frac{dy}{dx}=0$, this is an exact equation if $M=\frac{\partial F}{\partial x}$, $N=\frac{\partial F}{\partial y}$ for some function $F$
* e.g. $2x=2y\frac{dy}{dx}=0$ (E)
  * $F(x, y)=x^2+y^2$
  * (E) is exact and (E) $\Leftrightarrow dF=0\Leftrightarrow F(x, y)=C$
  * $x^2+y^2=C\geq0\Leftrightarrow y=\pm\sqrt{C-x^2}$
* General method to solve exact equation
  * $M+N\frac{dy}{dx}=0 (E)$, goal is to find $F$
  * If $(E)$ is an exact equation, $\frac{\partial F}{\partial x}=M$ by integrating in x to find $F(x, y)=g(x, y)+A(y) (*)$, $A$ is constant of integrationg that depends on $y$
  * Differentiate $(*)$ with respect to $y$
    * $\frac{\partial F}{\partial y}=N=\frac{\partial g}{\partial y}+A^\prime(y)$, so we can find $A$ such that $A^\prime=N-\frac{\partial g}{\partial y}$
* e.g. $\frac{dy}{dx}=\frac{-2x-y}{x-1} (*), y(0)=1$
  * $(*)\Leftrightarrow 2x+y+(x-1)\frac{dy}{dx}=0$
  * $M=2x+y, N=x-1$
  * Integrate M in x: $\int M=\int(2x+y)dx=x^2+xy+A(y)$
  * Differentiate $F$ in $y$ and identify with $N$: $\frac{\partial F}{\partial y}=0+x+A^\prime(y)=x-1\Rightarrow A^\prime(y)=-y$ works
  * Therefore the solutions of $(*)$ satisfy $F(x, y)=C\Leftrightarrow x^2+xy-y=C$
  * $y(0)=1\Rightarrow C=-1$, so solution is $y=\frac{-x^2-1}{x-1}$
  * This doesn't always work
* e.g. $2x+y+xy\frac{dx}{dy}=0(E)$
  * $M=2x+y, N=xy$
  * If $(E)$ is an exact equation, applying the method gives $M=2x+y\Rightarrow\frac{\partial F}{\partial x}=2x+y$
  * $F(x, y)=x^2+xy+A(y)$
  * $\frac{\partial F}{\partial y}=x+A^\prime(y)=xy\Rightarrow A^\prime(y)=xy-x$, which is impossible since $A$ should only depend on $y$
  * Not an exact equation
* Theorem (Poincare): If $M$ and $N$ are continuously differentiable functions of $x, y$ such that $\frac{\partial M}{\partial y}=\frac{\partial N}{\partial x}$, then we can locally write $M=\frac{\partial F}{\partial x}$ and $N=\frac{\partial F}{\partial y}$
  * Remark: if $M$ and $N$ satisfy the hypothesis of the theorem, we can then solve $M+N\frac{dy}{dx}=0$ as an exact equation
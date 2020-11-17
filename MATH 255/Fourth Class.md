# Fourth Class
* e.g. A water tank initially contains $10kg$ of salt dissolved in $100L$ of water; we add brine of concntration $50g/L$ at a rate of $5L/min$, and well stirred mix is removed at same rate. Find how much salt at time $t$
  * $x(t)$=mass of salt in tank
  * $\frac{dx}{dt}=0.05\frac{kg}{L}\cdot5L\frac{L}{min}-\frac{5x}{V}$, $V=100L$
  * $\frac{dx}{dt}=0.25-0.05x, x(0)=10$
* e.g. Consider $\frac{dx}{dt}=-k(x-A), k>0$ where $A=A_0\cos(\omega t), A_0, \omega\in\mathbb R$. Find general solutions and asymptotic behaviour
  * 1st order linear ODE
  * $\frac{dx}{dt}+kx=kA_0\cos(\omega t)$
  * $r(t)=e^{kt}$
  * $(e^{kt}x)^\prime=kA_0(\cos(\omega t)e^{kt}$
  * To evaluate integral, use Euler's formula $\cos x=\frac{e^{ix}+e^{-ix}}{2}$
  * $e^{kt}x=kA_0\int^t(\frac{e^{i\omega u}+e^{-i\omega u}}2)e^{ku}du+C$
  * $\frac{kA_0}{2}(\frac{e^{(k+i\omega)t}}{k+i\omega}+\frac{e^{(-k-i\omega)t}}{k+i\omega})$
  * $\frac{kA_0}2\cdot e^{kt}\cdot \frac{k(e^{i\omega t}+e^{-i\omega t})-i\omega (e^{i\omega t}-e^{-i\omega t})}{k^2+\omega^2}$
  * $x(t)=kA_0\cdot \frac{k\cos \omega t+\omega \sin\omega t}{k^2+\omega^2}+Ce^{-kt}$
  * When $t\to\infty$ $Ce^{-kt}$ vanishes
    * $x(t)\approx kA_0\cdot \frac{k\cos \omega t+\omega \sin\omega t}{k^2+\omega^2}$
* Autonomous equations
  * Consider problems of the following form: $\frac{dx}{dt}=f(x)$
  * We call these equations autonomous equations (independent of $t$)
  * Remark: We saw how to treat these equations using seperation of variables $\Rightarrow t+C=\int\frac1f$
  * Here we are not interested in fully solving the equation, only finding asymptotic behavior of solutions ($t\to\infty$)
  * Remark: Suppose we find a root of $x$, i.e. $x_0$ s.t. $f(x_0)=0$ then the constant function $x=x_0$ is a solution of $\frac{dx}{dt}=0=f(x)$
  * e.g. $\frac{dx}{dt}=k(A-x), A\in\mathbb R$, $x=A$ is a solution
  * The constant solutions of autonomous equations are called equilbirium solutions
  * The solutions of $f(x)=0$ are called critical points
  * We say that a critical point is stable if any solution that gets close enough to the critical pointconverges asymptotically to this point
  * Remark: If we want to write this mathematically, stability $\Rightarrow\exists \epsilon>0 | \forall x_0\in]x_c-\epsilon, x_c+\epsilon[$ the solution of $x^\prime=f(x), x(t_0)=x_0$ converges to $x_c$ as $t\to\infty$
* e.g. $\frac{dx}{dt}=k(A-x)$, we know how to solve this (IF)
  * $x(t)=A(1+C\exp(-kt))\Rightarrow x=A$ is a solution
  * A is a critical point
  * When $t\to\infty x\to A$
  * A is stable
# Eighth Class
* Integrating factors
  * $M(x, y)+N(x, y)\frac{dy}{dx}=0 (E)$
  * Recall: criterion for $(E)$ being exact: $M_y=N_x$
  * When this criteria is not satisfies, we can still try to make it exact by multiplying by a factor $u(x, y)$
  * $u(x, y)M+u(x, y)N\frac{dy}{dx}=0$
  * $\bar M+\bar N\frac{dy}{dx}=0$
  * $\bar M_y=u_y M+uM_y, \bar N_x=u_xN+uN_x$
  * To be exact, $\bar M_y=\bar N_x\Leftrightarrow (M_y-N_x)u=u_x N-u_yM$
  * If $u=u(x)$ or $u=u(y)$, this last equation simplifies
  * e.g. if we set $u=u(x)$, then we obtain $(M_y-N_x)u=u^\prime$
    * $u^\prime-\frac{M_y-N_x}Nu=0$
    * If $\frac{M_y-N_x}N$ only depends on $x$, then we obtain a linear equation which we know how to solve using integrated factor
    * $u(x)=e^{\int\frac{M_y-N_x}Ndx}$ ($u$ is a function of $x$) or $u(y)=e^{-\int\frac{M_y-N_x}{M}dy}$ ($u$ is a function of $y$)
* e.g.$\frac{x^2+y^2}{x+1}+2y\frac{dy}{dx}=0(E)$
  * $M_y=\frac{2y}{x+1}, N_x=0$, so not exact
  * $\frac{M_y-N_x}N=\frac1{x+1}$ which only depends on $x$
  * $\therefore$ by solving $u^\prime-\frac u{x+1}=0$ can solve for $u$
    * Integrating factor: $e^{\int^x\frac1{t+1}dt}=x+1+C$, so $u(x)=x+1$ works
  * Multiplying $(E)$ by $x+1$, we find $x^2+y^2+2y(x+1)\frac{dy}{dx}=0\Rightarrow M^*_y=2y, N^*_x=2y$
  * $y=\pm\sqrt{\frac{C-(\frac13)x^3}{x+1}}$
* Chapter 1 Conclusion
  * Covered 1st order ODEs
  * It is important to be able to identify proper method
* Types of ODEs we've seen
  * Linear
    * $y^\prime+ay=0$ homogenous
      * $y=Ce^{-ax}$
    * $y^\prime+p(x)=q(x)$ heterogenous
      * Integrating factor method
      * Explicit solutions
  * Seperable
    * $f(x)dx=g(y)dy$
      * Integrate
      * Implicit solutions
  * Exact
    * $Mdx+Ndy=0$
      * Criterion: $M_y=N_x$ (IF method if needed)
      * Implicit solutions
  * Autonomous
    * $y^\prime=f(y)$
      * We can seek equilibrium solutions (constant)
      * Can study their stability
* In general, one should now how to use initial conditions provided to solve the IVP, and also model some simple problems with ODEs
* Aside from analytical methods, also studied some important other tools and properties that necessitate the use of computational resources, e.g. MATLAB
  * Slope fields
    * Allows to study stability, asymptotic behaviour and visualize solutions
  * Numerical schemes
    * Euler's scheme
    * Allows to approximate solutions
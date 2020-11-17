# Eleventh Class
* IVP for 2nd order linear ODE
* e.g. $\begin{cases}y^{\prime\prime}-6y\prime+8y=0\\y(0)=-2\\y^\prime(0)=6\end{cases}$
  * We solve characteristic polynomial to get $\Delta = 4>0, y=Ce^{2x}+De^{4x}$
  * Solve IVP using IC to get
  * $C+d=-2, C+2D=3\Rightarrow C=-7, D=5$
  * $y(x)=-7e^{2x}+5e^{4x}$
  * Same applies when $\Delta=0, \Delta <0$\
  * When $\Delta<0$ the solution $Ce^{\alpha x}\cos(bx)+De^{\alpha x}\sin(bx)$ can also be written as $Ae^{\alpha x}\cos(\omega(t-t_0))$
    * Works because $\cos(\alpha-\beta)=\cos\alpha\cos\beta+\sin\alpha\sin\beta$
* Physical systems
  * Electrical circuits
  * Pendulum (small oscillations)
  * Mass attached to a spring
    * Spring constant $K$, spring constant $C$, external for $\vec F(t)$
    * Want to study position $x(t)$ of mass $m$
    * $mx^{\prime\prime}=F-cx^\prime-kx\Rightarrow mx^{\prime\prime}+cx^\prime+kx=F(t)$
    * To solve ODE apply what we saw previously
    * Case of free damped motion (homogenous case, $F=0$)
    * $x^{\prime\prime}+2px^\prime+\omega_0^2x=0$, $\omega_0=\sqrt{\frac km}, p=\frac{c}{2m}$
    * Characteristic equation $x^2+2px+\omega_0^2=0$
    * $\Delta = 4(\frac{c^2}{4m^2}-\frac km)$
    * If $\Delta>0 (c^2\>4km)$, overdamping
      * $r_\pm=-p\pm\sqrt{p^2-\omega_0^2}<0$
      * $x(t)=C_1e^{r_1t}+C_2e^{r_2t}$
      * No oscillations, only exponential
    * If $\Delta=0(c^2=4km)$, critical damping
      * $x(t)=C_1e^{-pt}+C_2te^{-pt}$
    * $\Delta <0(c^2<4km)$, underdamping
      * $r=-p\pm\omega_1, \omega_1=\sqrt{\omega_0^2-p^2}$
      * $x(t)=Ce^{-pt}\cos(\omega_1(t-t_0))$
* Non-homogenous 2nd order linear ODE
  * $y^{\prime\prime}+p(x)y^\prime+q(x)y=L(y)=f(x)$
* Theorem: general solution of $L(y)=f(x)$ is $y(x)=y_c(x)+y_p(x)$, where $y_c$ is the general solution to $L(y)=0$, called the complementary solution and $y_p$ is any particular solution of $L_y=f$. 
  * This tells that if find a particular solution, we can just solve the homogenous equation (which know how to do) to fully solve the ODE
* e.g. Solve $y^{\prime\prime}-y^\prime+y=e^{2x}$
  * $Ae^{2x}$ is a particular solution with $A=\frac13$
  * Then solve homogenous equation, $y_c=C_1e^{x/2}\cos(\frac{\sqrt3}2x)+C_2e^{x/2}\sin(\frac{\sqrt{3}}2x)$
  * Therefore general solution is $y_c=C_1e^{x/2}\cos(\frac{\sqrt3}2x)+C_2e^{x/2}\sin(\frac{\sqrt{3}}2x)+\frac13e^{2x}$
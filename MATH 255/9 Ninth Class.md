# Ninth Class
* Linear 2nd order ODE
  * DE in form $x^{\prime\prime}+p(t)x^\prime+q(t)=0$
* Damped harmonic motion
  * e.g. block connected to wall by string
  * $x^{\prime\prime}=-kx-cx^\prime\Rightarrow x^{\prime\prime}+cx^\prime+kx=0$
    * $k$ is spring constant, $c$ is friction constant
  * Characteristic equation
    * $r^2+cr+k=0$
    * $\Delta = c^2-4k$
  * Case 1: $\Delta>0$ overdamped motion
    * Two real solutions
    * $r_{\pm}=\frac{-c\pm\sqrt{c^2-4k}}2$
    * Note that $r_-<r_+<0$
    * Two independent solutions
    * $x=e^{r_+t}, x=e^{r_-t}$
    * Form of general solution: $x(t)=Ae^{r_+t}+Be^{r_-t}, A, B\in\mathbb R$
  * Case 2: $\Delta <0$ underdamped motion
    * Two complex solutions: $r_\pm=\frac{-c\pm i\sqrt{4k-c^2}}2=\alpha\pm i\omega$
      * $\alpha=-\frac c2, \omega=\frac12\sqrt{4k-c^2}$
    * Two independent solutions
    * $x=e^{r_\pm t}=e^{\alpha t}\cdot e^{\pm i\omega t}$
    * $x=e^{\alpha t}\cos(\omega t), x=e^{\alpha t}\sin(\omega t)$
    * Form of general solution: $x(t)=Ae^{\alpha t}\cos(\omega t)+Be^{\alpha t}\sin(\omega t), A, B\in\mathbb R$
    * Also equivalent to $Ce^{\alpha t}\cos(\omega t+\phi), C\geq 0, \phi\in\mathbb R$ (can convert between the two with trig identities)
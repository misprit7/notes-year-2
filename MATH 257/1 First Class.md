# First Class
* 1st order ODE
  * Separable: $y^\prime=\frac{dy}{dx}=p(x)Q(y)$
    * $\int\frac{dy}{Q(y)}=\int P(x)dx+C$
    * e.g. $\frac{dy}{dx}=y\cos x\rightarrow \frac{dy}y=\cos xdx$
      * $\log|y|=\sin x+C$
      * $y=c_1e^{\sin x}$
  * Linear: $Ly=y^\prime+p(x)y=Q(x)$ where $L=\frac{d}{dx}+p(x)$
    * e.g. $y^\prime+\frac{2x}{1+x^2}y=\frac{\cot(x)}{1+x^2}$
      * $\mu(x)y^\prime+\mu(x)\frac{2x}{1+x^2}y=\frac{\cot(x)}{1+x^2}\mu(x)$
      * Choose $\mu(x)=e^{\int p(x)dx}=(1+x^2)$
      * $\frac{d}{dx}((1+x^2)y)=\cot(x)$
      * $(1+x^2)y=\int\cot(x)+C$
      * $y=\frac{log|sin(x)}{1+x^2}+\frac{C}{1+x^2}$
* 2nd order ODE
  * Constant coefficient: $Ly=y^{\prime\prime}+ay^\prime+by=0$
    * Guess $e^{rx}$
      * $(ar^2+br+c)e^{rx}=0$
      * $ar^2+br+c=0$ is characteristic equation
      * $r_{1, 2}=\frac{-b\pm\sqrt{b^2-4ac}}{2a}, \Delta=b^2-4ac$
        * $\Delta>0\Rightarrow$ 2 real distinct roots
        * $\Delta<0\Rightarrow$ 2 complex roots
        * $\Delta=0\Rightarrow$ repeated roots
    * e.g. $2y^{\prime\prime}+2y^\prime+y=0$
      * $r_1, 2=\frac{-2\pm\sqrt{4-8}}{2(2)}=-\frac12\pm\frac i2, \Delta=-4<0$
      * $y(x)=c_1e^{(-\frac12+\frac i2)x}+c_2e^{(-\frac12-\frac i2)x}=e^{-x/2}(c_1e^{ix/2}+c_2e^{-ix/2})$
      * Applying Euler's formula and rearranging, we get $e^{-x/2}((c_1+c_2)\cos\frac x2+i(c_1-c_2)\sin\frac x2)=e^{-x/2}(A_1\cos\frac x2+A_2\sin x2)$
  * Cauchy Euler/Equidimentional: $Ly=x^2y^{\prime\prime}+\alpha xy+\beta y=0$
    * Guess: $y=x^r$
    * e.g. $2x^2y^{\prime\prime}-xy^\prime+y=0$
      * Substituting guess, we get $2r(r-1)x^r-rx^r+x^r=0\Rightarrow 2r^2-3r+1=0$
      * $r_{1, 2}=1, \frac12$
      * $y(x)=c_1x+c_2 x^{1/2}$
    * e.g. x^2y^{\prime\prime}-xy^\prime+y=0$
      * Guess $y=x^r$, solving gives $r=1$
      * $y_1=x, y_2=\log x\cdot x$
        * Second answer comes from derivative of the first answer
      * $y(x)=c_1x+c_2x\log x$
    * e.g. $x^2y^{\prime\prime}-xy^\prime+5y=0$
      * y(x)=x^r$
      * $(r(r-1)-r+5)x^r=0$
      * $r_{1, 2}=1\pm2i$
      * $y(x)=c_1x^{1+2i}+c_2x^{1-2i}$
      * $=x(c_1(\cos(2\log x)+i\sin(2\log x))+c_1(\cos(2\log x)-i\sin(2\log x)))$ (applying Euler's formula)
      * $=x(A_1\cos(2\log x)+A_2\sin(2\log x)$, $A_1, A_2$ are real
    * e.g. solve the IVP $x^2y^{\prime\prime}-3xy^\prime+4y=0, y(1)=1, y^{\prime}(1)=1$
      * $y=x^r$
      * $r=2$, repeated root
      * $y(x)=c_1x^2+c_2x^2\log x$
      * $y(1)=1\Rightarrow c_1=1$
      * $y^\prime(x)=2x+2c_2 x\log x+c_2 x\Rightarrow c_2=-1$
      * $y(x)=x^2-x^2\log x$
* Series solutions of ODEs: 
  * Use power series expansions to solve variable coefficient ODEs
  * $f(x)$ can be represented as $f(x)=\sum_{m=0}^\infty a_mx^mn$
  * General case around point $x_0$ is $f(x)=\sum_{n=0}^\infty a_n(x-x_0)^n$
  * Taylor series: $a_n=\frac{f^{(n)}(x_0)}{n!}$
  * $f(x)=\sum_{n=0}^\infty \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n$
* e.g. $y^\prime+(1-2x)y=0$
  * $\mu(x)=e^{\int(1-2x)dx}=e^{x-x^2}$
  * $y=Ce^{-x+x^2}$
# Twelfth Class
* e.g. $f(x, y)=(2x-x^2)(2y-y^2)$, find and classify critical points
  * $f_x=(2-2x)(2y-y^2)=0$, $(2x-x^2)(2-2y)=0$
  * $f_y=2y(1-x)(2-y)=0$, $2x(1-y)(2-x)=0$
  * $(y=0$ or $x=1$ or $y=2)$ and $(x=0$ or $y=1$ or $x=2)$
  * If $y=0, (0, 0)$ or $(2, 0)$
  * If $x=1, (1, 1)$
  * If $y=2$, $(0, 2)$ or $(2, 2)$
  * Find Critical points: 
    * $f_{xx}=-2(2y-y^2), f_{yy}=-2(2x-x^2), f_{xy}=(2-2x)(2-2y)$
    * $D=f_{xx}f_{yy}-f_{xy}=4(2y-y^2)(2x-x^2)-(2-2x)^2(2-2y)^2$
    * $D(0, 0)=-16, D(2, 0)=D(2, 2)=D(0, 2)=-16$, so saddle points
    * $D(1, 1)=4, f_{xx}=-2<0$, so local max
  * Find global max/min of $f(x, y)$ on the domains $R_1=\{(x, y): 0\leq x\leq3, 0\leq y\leq2\}$ and $R_2=$ disk of radius 1 centered at $(1, 1)=\{(x-1)^2+(y-1)^2\leq1\}$
  * Max/min of $f$ on $R_1$ occurs at either $(1, 1)$ or on boundary $f(1, 1)=1$
    * $f(x, y)=0$ along top bottom and left edges of boundary
    * Parameterization of right boundary: $\vec r(t)=<3, t>, 0\leq t\leq 2$
    * $g(t)=f(x(t), y(t))=-3(2t-t^2)=-6t+3t^2, 0\leq t\leq 2$
    * $g^\prime(t)=-6+6t=0\Rightarrow t=1\Rightarrow x=3, y=1, f(3, 1)=-3$
  * Max/min of $f$ occurs on $R_2$ is $(1, 1)$ or on the boundary $(x-1)^2+(y-1)^2=1$
    * $\vec r(t)=<\cos t+1, \sin t+1, 0\leq t\leq2\pi$
    * $f(x(t), y(t))=(2(\cos t+1)-(cos t+1)^2)(2(\sin t+1)-(\sin t+1)^2)=(1-\cos^2 t)(1-\sin^2t)=\sin^2t\cos^2t$
    * $f(x, y)=0=2\sin t\cos^3t-2\cos t\sin^3t$
    * $\sin t=0$ or $\cos t=0$ or $\cos^2t=\sin^2t=1-\cos^2t$
    * $t=\pi\Rightarrow f=0, t=\frac\pi2\Rightarrow f=0, t=\frac{3\pi}2$ or $t=\frac\pi4, \frac{3\pi}4, \frac{5\pi}4, \frac{7\pi}4\Rightarrow f=\frac14$
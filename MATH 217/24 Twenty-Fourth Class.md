# Twenty-Fourth Class
* FTLI gives us a good reason to know when a vector field is conservative
* All statements following are equivalent
  * $\vec F$ conservative
  * $\vec F$ is path independent, i.e. $\int_C\vec F \cdot d\vec r$
  * $\oint_C\vec F\cdot d\vec r$
  * $\vec\nabla \times \vec F=\vec 0$, must be simply connected to go from this to the others
* e.g. $\vec F=<2x, z, y+2z>$, is $\vec F$ conservative? If so, find the potential function. 
  * $\vec{curl}\vec F=\vec\nabla\times\vec F=\vec 0$
  * Domain of $\vec F$ is $\R^3$ which is simply connected, so $\vec F$ is conservative
  * $f_x=2x, f_y=z, f_z=y+2z$
  * $f(x, y, z)=x^2+c(y, z)$
  * $f_y=0+\frac{\partial c}{\partial y}=z\Rightarrow f(x, y, z)=x^2+yz+h(z)$
  * $f_z(x, y, z)=y+h^\prime(z)=y+2z\Rightarrow h(z)=z^2+C$
  * $f(x, y, z)=x^2+yz+z^2+C$
* e.g. $\vec F=\frac{-y}{x^2+y^2}\vec i+\frac{x}{x^2+y^2}\vec j$
  * $P=\frac{-y}{x^2+y^2}, Q=\frac{x}{x^2+y^2}$
  * $\vec{curl}\vec F=<0, 0, Q_x-P_y>$
  * $P_y=\frac{y^2-x^2}{(x^2+y^2)^2}$
  * $Q_x=\frac{y^2-x^2}{(x^2+y^2)^2}$
  * Domain is $\vec \R^2-\{(0, 0)\}$ which isn't simply connected (there are loops in the domain which are not the boundary of a closed region)
  * $C_R$ circle of radius $R$ centered at $(0, 0)$, oriented counter clockwise
  * Compute $\int_{C_R}\vec F\cdot d\vec r$
  * Parameterize $C_R: \vec r(t)=<R\cos t, R\sin t>, 0\leq t\leq 2\pi$
  * $=\int_{t=0}^{2\pi}\vec F(\vec r(t))\cdot \frac{d\vec r}{dt}dt$
  * $\vec F(\vec r(t))=<\frac{-R\sin t}{r^2}, \frac{R\cos t}{R^2}>$
  * $\int_{C_R}\vec F\cdot d\vec r=\int_{t=0}^{2\pi}(\frac{R}{R^2})(R)((-\sin t)^2+\cos^2 t)dt=2\pi$
  * Clearly not conservative
  * Consider $\vec F$ on $\R^2-\{$ positive $x$ axis $\}\Rightarrow \exist f(x, y)$ such that $\vec F=\vec\nabla f$, where $f$ is conservative
  * Also can think about same thing except for negative $x$ axis and actually get potential function for both
  * Question: why does this not tell us what the potential function is everywhere but the origin? 
  * $f_y(x, y)=\frac{1/x}{1+(\frac yx)^2}\Rightarrow f(x, y)=\tan^{-1}(\frac yx)+C(x)$
  * $f_x(x, y)=\frac{-y/x^2}{1+(\frac yx)^2}+C^\prime(x)=\frac{-y}{x^2+y^2}+C^\prime(x)=\frac{-y}{x^2+y^2}\Rightarrow C^\prime(x)=0, C(x)=0$
  * $f(x, y)=\tan^{-1}(\frac yx)=\theta$, not defined on $x$ axis
  * Notice $f(x, y)=\theta+\pi$ is defined everywhere but negative $x$ axis
  * Notice that the above argument can be used to show $\oint_C\frac{-ydx+xdy}{x^2+y^2}=2\pi\cdot$ winding number of $C$ about the origin
    * Winding number is how many times path goes around origin, counting direction
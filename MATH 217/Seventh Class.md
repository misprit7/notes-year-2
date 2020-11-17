# Seventh Class
* Partial derivatives'
  * Can treat one variable as constant and take a deriviatvie with respect to the other
  * $\frac{\partial f}{\partial x}(x, y)=f_x(x, y)=$ derivative with respect to $x$, treating $y$ as constant
  * In terms of limits, $f_x(x_0, y_0)=\lim_{h\to0}\frac{f(x_0+h, y_0)-f(x_0, y_0)}{h}$
* Interpretation of trace curves
* Iterating partial derivatives
  * $\frac{\partial}{\partial y}(\frac{\partial z}{\partial x})=\frac{\partial^2z}{\partial y\partial x}=f_{xy}$
* Theorem: $f_{xy}=f_{yx}$, i.e. partial derivatives commute
  * Follows that this also works for higher order derivatives
* e.g. $f(x, y)=ye^{xy}$
  * $f_x=y^2e^{xy}, f_y=e^{xy}+yxe^{xy}, f_{xy}=2ye^{xy}+y^2(xe^{xy})$
* Aside: partial differential equations
  * Equatiosn involving on or more partial derivatives of some function $u$
  * "Solving" such a PDE means finding a function $u$ satisfying the equation
  * Top three PDEs
    * $u_{xx}+u_{yy}=0$, Laplace's equation
      * Solutions are called harmonic functions
      * Their graphs are area minimizing surfaces(soap bubble films)
    * $u_{xx}-u_{tt}=0$, Wave equation
      * Solutions describe waves
      * $x$ is position, $t$ is time, $u(x, t)$ is displacement
    * $u_{xx}-u_t=0$, Heat equation
      * Solutions describe how heat disperses
      * $x$ is position, $t$ is time and $u(x, t)$ is temperature
  * Schrodinger's equation
    * $u_{xx}-iu_t=0, i=\sqrt{-1}$
    * Solution describes evolution of the wave function in quantum mechanics
* Implicit differentiation
  * e.g. $\frac{\partial z}{\partial x}=\sqrt{1-x^2-y^2}\Rightarrow\frac{\partial z}{\partial x}=\frac{-x}{\sqrt{1-x^2-y^2}}$
  * Sometimes $z$ not given explicitely
* e.g. law of cosines: $c^2=a^2+b^2-2ab\cos\theta(*)$
  * $\frac{\partial}{\partial c}(*)\Rightarrow 2c=0+0+2ab\sin\theta\frac{\partial \theta}{\partial c}\Rightarrow\frac{\partial\theta}{\partial c}=\frac c{ab\sin\theta}$
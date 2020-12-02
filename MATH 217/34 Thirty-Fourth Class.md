# Thirty-Fourth Class
* Maxwell's equations
  * $\vec\nabla\cdot\vec B=0$
  * $\vec\nabla\cdot\vec E=\frac{\rho}{\epsilon_0}$
  * $\vec\nabla\times\vec E+\frac{\partial\vec B}{\partial t}=\vec 0$
  * $\vec\nabla\times\vec B-\frac1{c^2}\frac{\partial\vec E}{\partial t}=\mu_0\vec J$
  * $\vec B=<B_1, B_2, B_3>$ magnetic field
  * $\vec E=<E_1, E_2, E_3>$ electric field
  * $\vec J=<j_1, j_2, j_3>$ current density, $\rho=$ charge density
  * $\epsilon_0$ electric constant, $\mu_0$ magnetic constant, $c$ speed of light
    * Take system of units so these are $1$
* Maxwell's equations in $\R^4$
  * Coordinates $x, y, z, t$
  * The electro-magnetic $2$-form $F=B_1dy\wedge dz+B_2 dz\wedge dx+B_3 dx\wedge dy+(E_1dx+E_2dy+E_3dz)\wedge dt\in\Omega^2(\R^4)$
  * Current $3$-form $J=\rho dx\wedge dy\wedge dz-(j_1 dy\wedge dz+j_2 dz\wedge dx+j_3 dx\wedge dy)\wedge dt\in\Omega^3(\R^4)$
* Hodge start operator
  * $\Omega^2(\R^4)\underbrace{\rightarrow}_{*}\Omega^2(\R^4)$
  * $*(dx\wedge dy)=dt\wedge dz$
  * $*(dy\wedge dz)=dt\wedge dx$
  * $*(dz\wedge dx)=dt\wedge dy$
  * $*(dx\wedge dt)=dy\wedge dz$
  * $*(dy\wedge dt)=dz\wedge dx$
  * $*(dz\wedge dt)=dx\wedge dy$
  * $\omega$ is a coordinate $2$-form $\omega\wedge*\omega=dt\wedge dx\wedge dy\wedge dz$
* Maxwell's equations
  * $dF=0$, $d(*F)=J$
  * We know that in general $d^2=0\Rightarrow dJ=0$ (so called continuity equation for current)
  * On $\R^4$ $dF=0\Rightarrow$ there exists $A\in\Omega^1(\R^4)$ s.t. $dA=F$
    * $A$ is called the gauge potential and it is unique up to $A\rightarrow A+df, f\in\Omega^0(\R^4)$
    * When such a transformation occurs it is called a gauge transfer
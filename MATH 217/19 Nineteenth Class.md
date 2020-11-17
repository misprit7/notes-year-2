# Nineteenth Class
* Last time
  * Talked about vertically drillable functions and triple integrals
  * There are analogous statements that are drillable in othe directions
* e.g. Let $E$ be the solid region between $x=4$ and $x=y^2+z^2$. Set up limits for $\int\int\int_E fdVol$
  * $\int\int\int_E fdVol=\int\int_R\int_{x=y^2+z^2}^4 fdVol=\int_{y=-2}^2\int_{z=-\sqrt{4-y^2}}^{\sqrt{4-y^2}}\int_{x=y^2+z^2}^4 fdxdzdy$
  * Could also set up as vertically drillable
  * $\int\int_R(\int_{z=-\sqrt{x-y^2}}^{\sqrt{x-y^2}} fdz)dA=\int_{x=0}^4\int_{y=-\sqrt x}^{\sqrt x}\int_{z=-\sqrt{x-y^2}}^{\sqrt{x-y^2}}fdzdydx$
* e.g. Consider the iterated integral $\int_{x=0}^1\int_{y=\sqrt x}^1\int_{z=0}^{1-y} fdzdydx$, set up integral in the other 5 orders
  * $x$ integral first: $\int_{y=0}^{1}\int_{z=0}^{1-y}\int_{x=0}^{y^2} fdxdzdy$
  * $y$ integral first $\int_{z=0}^1\int_{x=0}^{(1-z)^2}\int_{y=\sqrt x}^{1-z}fdydxdz$
# Sixteenth Class
* e.g. compute $\int\int_RfdA$ where $f(x, y)=(1-x)^{3/2}$ and $R=\{(x, y): x^2+y^2\leq 1\}$
  * $\int\int_RfdA=\int_{x=-1}^1\int_{y=-\sqrt{1-x^2}}^{\sqrt{1-x^2}}(1-x^2)^{3/2}dydx=\int_{x=-1}^12(1-x^2)^2dx=2x-\frac43x^3+\frac25x^5\big|_{-1}^1$
  * $=\frac{32}{15}$
* Region $R$ is horizontally sliceable if $R=\{(x, y): g_1(y)\leq x\leq g_2(y), a\leq y\leq b\}$
* e.g. Let $D$ be the region between the line $x=y$ and the parabola $x=2-y^2$
  * $\int\int_DydA=\int_{y=-2}^1\int_{x-y}^{2-y^2}ydxdy=\int_{y=-2}^1y{}_y^{2-y^2}dy=\int_{y=-2}^1y(2-y^2-y)dy=y^2-\frac14y^4-\frac13y^3\big|_{-2}^1=-\frac{-9}{4}$
* e.g. same as above except vertically sliceable
  * On bottom is $y=-\sqrt{2-x}$, top is $y=\sqrt{2-x}$
  * Split into $R_1$ and $R_2$, with $R_1$ being on left and $R_2$ on right
  * $\int\int_RydA=\int_{x=-2}^1\int_{y=-\sqrt{2-x}}^{x}ydydx+\int_{x=1}^2\int_{y=-\sqrt{2-x}}^{\sqrt{2-x}}ydydx=\int_{x=-2}^1\frac{y^2}2\big|_{-\sqrt{2-x}}^xdx=\int_{x=-2}^1\frac{x^2}2-\frac12(2-x)dx$
  * $=\frac{x^3}3-x+\frac{x^2}4\big|_{-2}^1=\frac5{12}-1+\frac43-3=\frac{-9}4$
* e.g. computer $\int_{x=0}^1\int_{y=3x}^3e^{-y^2}dydx$
  * Reverse order of integration
  * =$\int_{y=0}^3\int_{x=0}^{\frac13y}e^{-y^2}dxdy=\int_{y=0}^3\frac13ye^{-y^2}=-\frac16(e^{-9}-1)=\frac16-\frac16e^{-9}$
* Odd functions
  * $f(-t)=f(t)\Rightarrow$ $f$ odd
  * $\int_{t=-a}^af(t)dt=0$
  * If a function is odd in $x$ and $R$ is symmetric under $x\Leftrightarrow-x$ then $\int\int_RfdA=0$
* e.g. $R=\{(x, y): x^2+y^2\leq 4\}$, find $\int\int_R(e^yx^2\tan x+(1+x)^{10}\sin(y^3)+5)dA$
  * $=5Area(R)=20\pi$
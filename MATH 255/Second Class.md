# Second Class
* Separable equations
	* $y^\prime=F(x, y)$ is seperable if it can be written as $y^\prime = f(x)\cdot g(y)$
	* In this case we solve the ODE by seperating $y$ and x and integrating
	* $y^\prime=f(x)\cdot g(y)\Leftrightarrow=\frac{dy}{dx}=f(x)\cdot g(y)$
	* By integrating we get 
	* $\int\frac1{g(y)}dy=\int f(x)dx)+C$
	* More rigorously we show that if $y^\prime(x)=f(x)g(y(x))$ then assuming $g(y)\neq 0$, we can write $\frac{y^\prime(x)}{g(y(x))}=f(x)$
	* Since this is true for all $x$, we can also write $\int^x\frac1{g(y(x))}y^\prime(u)du=\int^x f(u)du+C$ where $C$ is a constant
	* With change of variables $t=y(u)$, we get $\int^{y(x)}\frac{dt}{g(t)}=\int^x f(u)du+C$
	* If we know a primitive of $\frac1g$ ($G$) and a primitive of $f$ (F) then we obtain $G(y)=F(x)+C$
	* This is called implicit solution
* e.g. $y^\prime=xy$
	* This is seperable, assume $y\neq 0$
	* $\int\frac{dy}{y}=\int xdx$
	* $\log|y|=\frac{x^2}2+C\Leftrightarrow |y|=Ke^{x^2/2}=\Leftrightarrow y=Ke^{x^2/2}$
		* Can remove absolute value since $e^x$ is always same sign
* Integrating factor
	* Def: A first order ODE is linear if it can be written as $y^\prime+p(x)y=f(x)$
	* To solve, multiply by a factor $r(x)\neq0\Rightarrow(x)y^\prime+r(x)p(x)y=r(x)f(x)$
	* We want to make left hand side appear as a derivative of a product 
	* $\Rightarrow\frac d{dx}(v(x)y)=r(x)dx\Leftrightarrow y=\int^x\frac{r(u)du}{v(x)}$
	* To make work, this works if $r^\prime=r\cdot p\Leftarrow \int\frac{r^\prime}{r}dx=\int p(x)dx+C\Rightarrow \log|r(x)|=\int^x p(t)dt+C\Rightarrow |r(x)|=e^{\int^x p(t)dt}$
# Third Class
* Trig functions
	* $\sin^\prime(x)=\cos(x)$
	* $\cos^\prime(x)=-\sin(x)$
	* $\sin^2(x)+\cos^2(x)=1$
	* $\tan^\prime(x)=\frac1{\cos^2(x)}$
* e.g. $x^\prime=x\cdot \sin(t), x(0)=1$
	* $\frac{dx}{dt}=x\sin(t)\Leftrightarrow\frac{dx}{x}=\sin(t)dt$
	* $\log(x)=-\cos(t)+C$
	* $|x|=e^{-\cos(t)+C}=Ke^{-\cos(t)}$
	* $x=\bar Ke^{-\cos(t)}, K\in\mathbb R$
	* $x(0)=1\Rightarrow\bar K=e$
* Linear equations
	* LE: $y^\prime + p(x)y=f(x)$
	* Method: Integrating factor of $r(x)=e^{\int^xp}$
	* $(y\cdot r(x))^\prime=f(x)r(x)$
	* $yr(x)=\int f(x)r(x)$
	* $y=\frac1{r(x)}\int f(x)r(x)dx$
	* Two types of linear equations
		* Homogenous: $f(x)=0$
		* Heterogenous: otherwise
* e.g. same example as above with using integrating factor, $x^\prime=x\sin(t)$
	* $y^\prime=y\sin(x)$
	* $p(x)=-\sin(x)$, $f(x)=0$
	* Homogenous
	* $r(x)=e^{-\int\sin(x)}=e^{\cos(x)}$
	* $y^\prime e^{\cos x}-\sin(x)e^{\cos(x)}y=0$
	* $(ye^{\cos(x)})^\prime=0$
	* $ye^{\cos(x)}=C$
	* $y=Ce^{-\cos(x)}$
* e.g. $y^\prime+\cos(x)y=\cos(x)$
	* $r(x)=e^{\int\cos(x)}=e^{\sin(x)}$
	* $(y\cdot e^{\sin(x)})^\prime=\cos(x)\cdot e^{\sin(x)}$
	* $ye^{\sin(x)}=\int\cos(x)e^{\sin(x)}dx=e^{\sin(x)}+C$
	* $y=1+C\cdot e^{-\sin(x)}$
* e.g. $\frac{y^\prime}{x^2+1}+xy=3$
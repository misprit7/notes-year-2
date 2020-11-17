# Fifth Class
* Derviatives of vector valued functions
	* $\frac{d\vec r}{dt}=\vec r^\prime(t)=\lim_{h\to0}\frac{\vec r(t+h)-\vec r(t)}{h}$
	* Since vector subtraction is done componentwise it follows that if $\vec r(t)=<f(t), g(t), h(t)>$ then $\vec r(t)=<f^\prime(t), g^\prime(t), h^\prime(t)>$
	* We think of $\vec r(t)$ as a position of an object at time $t$ and $\vec r^\prime(t)$ is the velocity
* Product rules
	* $\frac d{dt}(f(t)\vec r(t))=f^\prime(t)\vec r(t)+f(t)\vec r^\prime(t)$
	* $\frac d{dt}(\vec u(t)\cdot\vec v(t)) = \vec u^\prime\cdot \vec v+\vec u\cdot \vec v^\prime$
	* $\frac d{dt}(\vec u\times \vec v)=\vec u^\prime\times\vec v + \vec u\times \vec v^\prime$
* Important example
	* What can be said about a vector-valued function $\vec r(t)$ who's magnitude is contant
	* $|\vec r(t)| = C\Leftrightarrow \vec r\cdot\vec r=c^2=\Leftrightarrow \frac d{dt}(\vec r\cdot \vec r)=0\Leftrightarrow0=\vec r^\prime\cdot \vec r+\vec r\cdot \vec r^\prime=2\vec r\cdot\vec r^\prime\Leftrightarrow \vec r\cdot\vec r^\prime=0\Leftrightarrow\vec r^\prime\perp\vec r$
* Arc lengh of a curve
	* Divide the time interval in to $N$ small segments of size $\Delta t = \frac{t_{end}-t_0}N$
	* In limit arclength $=\lim_{N\to\infty}\sum_{i=01}^N|\vec r^\prime(t_i)|\Delta t=\int_{t=t_0}^{t_{end}}|\vec r^\prime(t)|dt$
	* Only assuming parameterization traverses the cruve once
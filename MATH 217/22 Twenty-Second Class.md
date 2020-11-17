# Twenty-Second Class
* e.g. Integrate $f(x, y)=xy^4$ along the right half of the circle $x^2+y^2=16$
  * $\vec r(t)=<4\cos t, 4\sin t>$, $-\pi/2\leq t\leq \pi/2$, $r^\prime(t)=<-4\sin t, 4\cos t>$
  * $|r^\prime(t)|=4$
  * $\int_C xy^4 ds=\int_{t=-\pi/2}^{\pi/2}(4\cos t)(4\sin t)^44dt$
  * $4^6[\frac{\sin^5t}5]_{t=-\pi/2}^{\pi/2}=\frac{2^{13}}5$
  * Try a different parameterization: $x=\sqrt{16-y^2}$, $\vec r(t)=<\sqrt{16-t^2}, t>, -4\leq t\leq 4$
  * $r^\prime(t)=<\frac{-t}{\sqrt{16-t^2}}, 1>, |vec r^\prime(t)=\sqrt{\frac{t^2}{16-t^2}+1}=\frac4{\sqrt{16-t^2}}$
  * $\int_C xy^4ds=\int_{t=-4}^4\sqrt{16-t^2}\cdot t^4\cdot \frac4{\sqrt{16-t^2}}dt=4[\frac{t^5}5]_{t=-4}^4=\frac{2^13}{5}$
* e.g. Same $f=xy^4$ over top half of same circle
  * $0$ by symmetry, since $f$ is odd in $x$
* $f(x)=1$
  * $\int_Cds=$ arclength of $C$
* Average
  * $\bar f=\frac{\int_C fds}{\int_C ds}$
* Line integrals of vector fields
  * To define the integral of $\vec F$ over $C$ we use the concept of work
  * In 2 dimensions, the force is $W=FD$
  * More generally, only force in direction of displacement contributes to work
  * $W=\vec F\cdot \vec D$
  * Work = $\int_{t=a}^b\vec F(x(t), y(t))\cdot \vec r^\prime(t)dt=\int_C\vec F\cdot d\vec r=\int_C(\vec F\cdot\vec T)ds$
  * If $\vec F=P(x, y)\vec i, Q(x, y)\vec j$, then $W=\int_CPdx+Qdy$
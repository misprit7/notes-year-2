# Twentieth Class
* Cylindrical coordinates
  * Good for symmetry about the $z$ axis
  * Essentially polar coordinates in $(x, y)$
  * $(r, \theta, z), x=r\cos\theta, y=r\sin\theta, z=z$
  * $dVol=rdzdrd\theta$
  * Generally integrate $z$ first
* e.g. A drill of diameter $a$ is used to make hole through center of ball of radius $a$. What is the volume of the remaining object? 
  * $x^2+y^2+z^2=a^2\Rightarrow z^2=a^2-r^2$
  * $Vol=\int_{\theta = 0}^{2\pi}\int_{r=a/2}^a\int_{z=-\sqrt{a^2-r^2}}^{\sqrt{a^2-r^2}} rdzdrd\theta$
  * $=2\pi\int_{r=a/2}^a 2r\sqrt{a^2-r^2}dr=\frac{4\pi}3(a^2-(\frac a2)^2)^{3/2}=\frac{4\pi}3(\frac{3a^2}4)^{3/2}=\frac{\sqrt 3}2\pi a^3$
* Spherical coordinates
  * $(x, y, z)\Rightarrow(\rho, \theta, \phi)$
  * $x=\rho\sin\phi\cos\theta, y=\rho\sin\phi\sin\theta, z=\rho\cos\phi$
  * $\theta$ is angle to $x$ axis from projection onto the $xy$ plane, $\phi$ is angle from $z$ axis
  * $0\leq \theta\leq 2\pi$
  * $\theta$ is longitude, $\phi$ is latitude
    * $\phi=0$ is north pole, $\phi=\frac\pi2$ is equator, $\phi=\pi$ is south pole
  * To do a triple integral, we do as usual and divide up $\rho, \theta, \phi$ into little intervals of size $\Delta\rho, \Delta\theta, \Delta\phi$
  * Little box has $dVol=\sin\phi\rho^2d\rho d\phi d\theta$
  * $\int\int\int_E fdVol=\int_{\theta=\alpha}^\beta\int_{\phi=g_1(\theta)}^{g_2(\theta}\int_{\rho=h_1(\theta, \phi)}^{h_2(\theta, \phi)}f \sin\phi\rho^2d\rho d\phi d\theta$
* e.g. Compute $\int\int\int fdVol$ where $(x, y, z)=z$ and $E=\{(x, y, z) x^2+y^2+z^2\leq9, x, y, z\geq 0\}$
  * Rays from origin enter $E$ at $\rho=0$, exit at $\rho=3$
  * $\int\int\int_E zdVol=\int\int\int\rho\cos\phi\rho^2\sin\phi d\rho d\phi d\theta$
  * $=\int_{\theta=0}^{\pi/2}\int_{\phi=0}^{\pi/2}\int_{\rho=0}^3\rho^3\sin\phi\cos\phi d\rho d\phi d\theta$
* e.g. Compute $\int\int\int_E fdVol, f=\sqrt{x^2+y^2+z^2}$, $E$ is ball of radius $1$ centered at $(0, 0, 1)$
  * Equation for sphere is $x^2+y^2+(z-1)^2=1\Rightarrow x^2+y^2+z^2-2z+1=1$ means $\rho^2-2\rho\cos\phi=0\Rightarrow \rho=2\cos\phi$
  * $\int_{\theta=0}^\pi\int_{\phi=0}^{\pi/2}\int_{\rho = 0}^{2\cos\phi}\rho^2\sin\phi d\rho d\phi d\theta$
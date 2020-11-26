# Eighteenth Class
* Shockley
  * Along with coworkers invented the transistor
  * Commercialization of transistor started Silicon Valley
* Actual $VI$ curve of diode
  * $i_D=I_0e^{v_D/V_T}$
  * $V_T=\frac{kT}{q_e}$
    * $k$ is boltzmann constant
    * $q_e$ is charge of electron
    * $T$ is temperature
    * Normally around $25$ to $26mV$
  * More general equation is $i_D=I_0(e^{v_D/(nV_T)}-1)$
    * $n$ is ideality factor
* Zener diodes
  * Designed to operate backwards
  * Can be designed to have a specific voltage breakdown
  * Behaves almost like an ideal voltage source assuming it's in the zener region
  * Specifications
    * Maximum power
    * Zener voltage
    * Current at Zener voltage/current
    * Minimum Zener current
    * Dynamic $R_k$
    * Dynamic $R_{ZT}$
* Usages of Zener diodes
  * Can clamp a voltage output
* Diode applications
  * Commonly used for rectification
  * Half wave rectifier is an AC source, a diode and a resistor in a loop
    * Removes negative part of the AC source
  * Can also have a full-wave rectifier that takes absolute value of AC source
    * Can also add a capacitor to this to add a smoothing filter
* Other types of diodes
  * Light emitting, i.e. LEDs
    * Emits light when forward biased
    * Forward bias voltage across LEDs is typically around $2V$, so usually need resistor to limit current
  * Photodiodes
    * Converts light into electrical current
    * How digital cameras work
  * Silicon controlled rectifier
    * Has a third pin called gate that controls device
    * Doesn't turn on until gate is high while forward biased
    * Once on, stays one even if gate is turned off until it is reverse biased
* Laplace Transform
  * $\mathcal{L}(f(t))=F(s)=\int_{0^-}^\infty f(t)e^{-st}dt$
  * Sufficient condition for existence of Laplace transform: $\int_{0^-}^\infty e^{-\sigma t}|f(t)|dt<\infty, Re(s)+\sigma >0$
    * $s=\sigma+j\omega$
  * Inverse transform is $\mathcal{L}^{-1}=f(t)=\frac1{2\pi j}\int_{\sigma_1-j\infty}^{\sigma_1+j\infty}F(s)e^{st}ds$
* Important functions
  * Unit step function
    * $u(t)=0$ for $t<0, 1$ for $t>0$
  * Impulse function
    * $\delta(t-t_0)=0$ if $t\neq t_0, \int_{t_0-epsilon}^{t_0+\epsilon}\delta(t-t_0)dt=1$ for $\epsilon>0$
    * Undefined for $t=t_0$
    * $f(t)\delta(t-t_0)=f(t_0)\delta(t-t_0)$
* Laplace transform pairs
  * $\mathcal{L}(\delta t)=1$
  * $\mathcal{L}(u(t))=\frac1s$
  * $\mathcal{L}(t)=\frac1{s^2}$
  * $\mathcal{L}(e^{-at})=\frac1{s+a}$
  * Full list in their notes, too lazy to write them all out
* Laplace transform operations
  * $kf(t)\rightarrow kF(s)$
  * Addition is conserved
  * $\frac{df(t)}{dt}\rightarrow sF(s)-f(0^-)$
  * $\int_0^tf(x)\rightarrow \frac{F(s)}s$
  * $f(at), a>0\rightarrow \frac1a F(\frac sa)$
  * Many others given in the notes
* Inverse transforms
  * Often a rational function of $s$
    * $F(s)=\frac{N(s)}{D(s)}$
    * If the order of numerator is less than that of denominator, then $F(s)$ is called proper rational function
  * For proper rational functions, we use partial fraction expansion to find inverse laplace transform for time-domain response of the system
    * Zeros are the roots of numerator, poles are roots of denominator
    * $\frac{P_1(s)}{Q_1(s)(s+\alpha-j\beta)(s+\alpha+j\beta)}=\frac{C_1(s+\alpha)}{(s+\alpha)^2+\beta^2}+\frac{C_2\beta}{(s+\alpha)^2+\beta^2}$
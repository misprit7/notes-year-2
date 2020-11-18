# Fifteenth Class
* Sinusoidal steady state power
  * For any component, $p(t)=v(t)i(t)$
  * For AC power we assume $v=V_m\cos(\omega t+\theta_v), i=I_m\cos(\omega t+\theta_i)$
  * For convenience shift time such that $i=I_m\cos\omega t)$
  * Using $\cos\alpha\cos\beta=\frac12\cos(\alpha-\beta)+\frac12\cos(\alpha+\beta)$, we get the following: 
    * $p=V_m\cos(\omega t+\theta_v-\theta_i)I_m\cos(\omega t)=\frac{V_mI_m}2\cos(\theta_v-\theta_i)+\frac{V_mI_m}2\cos(\theta_v-\theta_i)\cos(2\omega t)-\frac{V_mI_m}2\sin(\theta_v-\theta_i)\sin(2\omega t)$
    * Note that leftmost term is time independent, so minimum power loss occurs when $\theta_v-\theta_i=\pm\frac{\pi}2$, i.e. pure capacitor or inductor
  * Real power or active power is part of power that isn't a time sinusoid
    * Real power $=P=\frac{V_mI_m}2\cos(\theta_v-\theta_i)$
    * $P=\frac1T\int_{t_0}^{t_0+T}pd\tau$, hence name of average power
  * $Q=\frac{V_mI_m}2\sin(\theta_v-\theta_i)$ is reactive power and is measured in volt-ampere reactive or VAR
  * For general circuit, $p=P+P\cos(2\omega t)-Q\sin(2\omega t)$
  * Purely resistive circuits
    * $Q=0$
    * $p=P+P\cos(2\omega t)$
  * Purely inductive circuits
    * $P=0$
    * $p=-Q\sin2\omega t$
  * Purely capactive circuits
    * $P=0$
    * $p=Q\sin2\omega t$
  * Power factor
    * The angle $\theta_v-\theta_i$ is power factor
    * Cosine of this angle is the power factor ($pf$), sine is reactive factor ($rf$)
    * $pf=\cos(\theta_v-\theta_i), rf=\sin(\theta_v-\theta_i)$
    * Lagging power factor means that current is lagging voltage and thus load is inductive, leading power factor means that the current is leading the voltage and thus the load is capacitive
* rms power calculations
  * For a purely resistive circuit, $P=\frac{V_{rms}^2}R$, and $P=I_{rms}^2R$
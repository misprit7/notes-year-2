# Twenty-Sixth Class
* Resistors
  * $V=IR$
  * $i(t)=I_m\cos(\omega t+\theta_i), v(t)=RI_m\cos(\omega t+\theta_i)$
  * $v(t)=V_m\cos(\omega+\theta_v)$
  * Means that $\theta_v=\theta_i$
  * $I=I_me^{j\theta}$
  * $V=RI_m\angle\theta=RI$
* Inductor
  * $V=j\omega LI$
  * $V(t)=L\frac{di}{dt}$
  * $i(t)=I_m\cos(\omega t+\theta_i)\Rightarrow I_me^{j\omega_i}$
  * $v(t)=L\frac{di}{dt}=L\frac{d}{dt}(I_m\cos(\omega t+\theta_i))=-LI_m\omega\sin(\omega t+\theta_i)=\omega LI_m\cos(\omega t+\theta_i+\frac\pi2)$
  * $V=\omega LI_me^{j(\theta_i+\frac\pi2)}=\omega Le^{j\frac\pi2}I_me^{j\theta_i}$
  * $V=j\omega LI$
  * i.e. voltage is $90\degree$ ahead
* Capacitor
  * $I=j\omega CV$
  * $i=C\frac{dv}{dt}$
  * $v(t)=V_m\cos(\omega t+\theta_V), i(t)=-C\omega V_m\sin(\omega t+\theta_v)$
  * $=C\omega V_m\cos(\omega t+\theta_v+\frac\pi2)$
  * $I=j\omega CV$
  * $V=\frac1{j\omega C}I$
* Impedance and reactance
  * $Z=R+jX$
  * Real part of impedance is resistance and imaginary part is called reactance
  * Resister: $Z=R$
  * Inductor: $Z=j\omega L$
  * Capacitor: $Z=\frac{-j}{\omega C}$
  * $V=ZI$
  * $Z_m\angle\theta_Z$
  * If reactance is positive voltage leads current, if negative current leads voltage
* Admittance and susceptance
  * $Y=\frac1Z=G+jB$
  * $G$ is conductance, $B$ is susceptance
* KVL and KCL in frequency domain
  * Also work with phasor voltages and currents
* Impedance and admittance
  * $Z=\frac{V}{I}=\frac{V_m}{I_m}\angle \theta_v-\theta_i$
* Series and parallel combinations of impedances
  * Combine the same as resistances
# Tenth Class
* Second order circuit
  * If inductor, capacitor and resistor are in series differential equation is $\frac{d^2i_L(t)}{dt^2}+\frac RL\frac{di_L(t)}{dt}+\frac1 {LC}i_L(t)=0$ and $\frac{d^2v_C(t)}{dt^2}+\frac RL\frac{dv_C(t)}{dt}+\frac1{LC}v_C(t)=0$
  * If they are in parrallel it is $\frac{d^2i_L(t)}{dt^2}+\frac 1{RC}\frac{di_L(t)}{dt}+\frac1 {LC}i_L(t)=0$ and $\frac{d^2v_C(t)}{dt^2}+\frac1{RC}\frac{dv_C(t)}{dt}+\frac1{LC}v_C(t)=0$
  * General form is $x^{\prime\prime}+bx^\prime+cx=F$, for no sources $F=0$
  * General solution is $x(t)=x_n(t)+X_F$, $x_n$ is homogenous response, $X_F$ is particular solution
  * If $F$ is constant, $x(t)=\frac Fc$
  * Characterisitic polynomial is $s^2+bs+c=0$
  * If $b^2-4c=0$ then solution is $x(t)=K_1e^{s_1t}+K_2e^{s_2t}+X_F$
    * $X_F=\frac Fc$
    * $x(0^+)=K_1+K_2+X_F$
    * $\frac{dx(0^+)}{dt}=s_1K_1+s_2K_2$
    * $s1, s_2$ are roots of characteristic polynomial
  * If $b^2-4c=0$ then solution is $x(t)=(K_1+K_2t)e^{s_1t}+X_F$
    * $X_F=\frac Fc$
    * $x(0^+)=K_1+X_F$
    * $\frac{dx(0^+)}{dt}=s_1K_1+K_2$
  * If $b^2-4c<0$, solution is $x(t)=e^{-\alpha t}(K_1\cos(\omega_dt)+K_2\sin(\omega_d t))+X_F$
    * $s_1, s_2=-\alpha\pm j\omega_d$
    * $X_F=\frac Fc$
    * $x(0^+)=K_1+X_F$
    * $\frac{dx(0^+)}{dt}=-\alpha K_1+\omega_dK_2$
* Complex roots
  * $K_1\cos\omega t+K_2\sin\omega t=\sqrt{k_1^2+K_2^2}(\frac{K_1}{\sqrt{K_1^2+K_2^2}}\cos\omega t+\frac{K_2}{\sqrt{K_2^2+K_2^2}}\sin\omega t)=A\cos(\omega t+\theta)$
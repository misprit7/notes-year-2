# Eighth Class
* Inductors
  * $L=\frac{N^2\mu A}{l}$
    * $l=$ Length
    * $N=$ Number of turns
    * $A=$ Cross sectional area
  * Is resistance and capacitance in reality
  * Unit in Henry
  * Instantaneous power is $p_L(t)=v_L(t)i_L(t)=L\frac{di_L(t)}{dt}i_L(t)$
  * Total stored energy is $W_L(t)=\int_{-\infty}^tp_L(\tau)\cdot d\tau=\int_{-\infty}^tLi_L(\tau)di_L(\tau)=\frac12Li_L^2(t)$
* Series/parrallel inductors
  * Series
    * $L_{eq}=L_1+L_2+\ldots+L_n$
  * Parrallel
    * $\frac1{L_{eq}}=\frac1{L_1}+\frac1{L_2}+\ldots+\frac1{L_n}$
* First order circuit
  * Applying KVL or KCL to purely resistive circuits results in algebraic equations
  * Applying to RC or RL circuits results in differential equations
  * If only one $C$ or $L$ in circuit the resulting differential equation is of the first order
  * Circuit is characterized by first order DE is called first order circuit
    * If can combine to equivalent, still first order
* Source free first order RC circuit
  * $v_C(0)=V_0$
  * $i_C(t)+i_R(t)=0$
  * $C\frac{dv_C(t)}{dt}+\frac{v_C(t)}R=0$
  * $\frac{dv_C(t)}{v_C(t)}=-\frac1{RC}dt$
  * $v_C(t)=V_0e^{-\frac1{RC}t}$
* Source free first order RL circuit
  * $\frac{di_L(t)}{dt}=-\frac RLi_L(t)\Rightarrow i_L(t)=I_0e^{-\frac RLt}$
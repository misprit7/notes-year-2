# Twelfth Class
* Method of undetermined coefficients
  * Consists of guessing a particular solution, when $f$ has a specific form
  * This method applies for linear ODEs with constant coefficients ($ay^{\prime\prime}+by^\prime+cy=f$)
  * First, if necessary, write $f=f_1(x)+f_2(x)+\ldots f_m(x)$, where each $f_i$ has an appropriate form (see below)
  * Then $y_p=y_{p_1}+\ldots+y_{p_m}$, where each $y_{p_i}$ solves for $ay^{\prime\prime}+by^\prime+cy=f_i$
  * To find $y_{p_i}$ use following: 
    * If $f_i$ is $P_n(x)+a_0+a_1x+\ldots+a_nx^n$, then $y_{p_i}$ is $x^s(A_0+A_1x+\ldots A_nx^n)$
    * If $f_i$ is $Q_n(x)=P_n(x)\cdot e^{\alpha x}$, then $y_{p_i}=x^s(A_0+A_1x_\ldots+A_nx^n)e^{\alpha x}$
    * If $f_i$ is $P_n(x)\cdot e^{\alpha x}\cos\beta x$ (or with $\sin$) then $y_{p_i}=x^s((A_0+A_1x+\ldots A_nx^n)\cos\beta x+(B_0+\ldots+B_nx^n)\sin\beta x)e^{\alpha x}$
    * Where $s$ is the smallest value ensuring that no term in $Y_{p_i}$ that is solution of the homogenous equation ($L(y)=0$)
  * Upon guessing the appropriate form, one can then determine the coefficients $A_i$ or $B_i$
  * About $s$: In practice, start with $s=0$ and if it doesn't work go with $s=1, 2, \ldots$
* e.g. $y^{\prime\prime}-9y=-2e^{3x}$
  * $y_c\Rightarrow y^{\prime\prime}-9y=0\Rightarrow y_c=C_1e^{3x}+C_2e^{-3x}$
  * $y_p$: we use method of undetermined coefficients with $f(x)=-2e^{3x}$
    * 1st guess: $y_p=Ae^{3x}$
    * This is a solution of $L(y)=0$
    * Next try $Axe^{3x}$ which works
    * $y_p^\prime=Ae^{3x}+3Axe^{3x}$
    * $y_p^{\prime\prime}=3Ae^{3x}+3Ae^{3x}+9Axe^{3x}=3A(2+3xe^{3x})$
    * $A=-\frac13$
  * General solution is $y(x)=C_1e^{3x}+C_2e^{-3x}-\frac13xe^{3x}$
* Variation of parameters
  * More general method that works for constant or variable coefficients in $L(y)=f(x)$, where $L$ is $y^{\prime\prime}+p(x)y^\prime+q(x)y=f(x)$
  * From earlier lecture, we know that solutions of $L(y)=y$ are $C_1y_1(x)+C_2y_2(x)$, where $y_1$ and $y_2$ are independent solutions
  * Idea to solve heterogenous case is to treat $C_1$, $C_2$ as functions in or der to find a paraticular solution
  * We assume $y_P=v_1(x)y_1(x)+v_2(x)y_2(x)$
  * $y_P^\prime=u_1^\prime y_1+u_1y_1^\prime+u_2^\prime y_2+u_2y_2^\prime$
  * Let's assume $u_1^\prime y_1+u_2^\prime y_2=0$
  * $y_P^\prime=u_1y_1^\prime+u_2y_2^\prime$
  * $y_P^{\prime\prime}=u_1^\prime y_1\prime+u_1 y_1^{\prime\prime}+u_2^\prime y_2^\prime+u_2y_2^{\prime\prime}$
  * $L(y_P)=L(u_1y_1+u_2y_2)=u_1y_1^{\prime\prime}+u_1^\prime y_1^\prime+u_2 y_2^{\prime\prime}+u_2^\prime y_2^\prime+p(x)(u_1y_1^\prime+u_2y_2^\prime)+q(x)(u_1y_1+u_2y_2)$
  * $L(y_P)=u_1(y_1^{\prime\prime}+py_1^\prime+qy_1)+u_2(y_2^{\prime\prime}+py_2^\prime+qy_2)+u_1^\prime y_1^\prime+u_2^\prime y_2^\prime$
  * $L(y_P)=u_1^\prime y_1^\prime+u_2^\prime y_2^\prime$
  * Since $y_P$ is a particular solution, $L(y_P)=f$
  * In the end, two conditions
    * $u_1^\prime y_1^\prime+u_2^\prime y_2^\prime=f$
    * $u_1^\prime y_1+u_2^\prime y_2=0$
  * In practice, to use this method to solve $L(y)=f(x)$:
    * Solve the homogenous equation to get $y_1, y_2$
    * Assume $y_P=u_1y_1 + u_2y_2$ and solve conditions above
* e.g. $y^{\prime\prime}-2y^\prime+y=\frac{e^t}{1+t^2}$
  * Must use variation of parameters since $f$ does not fall in requisite form
  * First, solve $y^{\prime\prime}-2y^\prime+y=0$
    * Double root $r=1$
    * $y=C_1e^t+C_2te^t$
    * $y_1=e^t, y_2=C_2te^t$
  * Particular solution, $y_P=u_1e^t+v_2te^t$, where:
    * $u_1^\prime e^t+u_2^\prime te^t=0$
    * $u_1^\prime e^t+u_2^\prime e^t(1+t)=\frac{e^t}{1+t^2}$
  * Equivalent to:
    * $u_1^\prime + u_2^\prime t=0$
    * $u_1^\prime + u_2^\prime (1+t)=\frac1{t+t^2}$
  * Equivalent to:
    * $u_1^\prime = \frac{-t}{t+t^2}$
    * $u_2^\prime = \frac1{t+t^2}$
  * Equivalent to:
    * $u_1=-\frac12\log(1+t^2)$
    * $u_2=\arctan(t)$
    * No need for constants, since we want a particular solution
  * Conclusion: 
    * $y=C_1e^t+C_2te^t-\frac12\log(1+t^2)e^t+\arctan(t)te^t$
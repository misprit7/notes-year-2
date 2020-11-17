# First Class
* Definitions
	* Differential equation is an equation for an unkown function that contains derivatives of the function
		* In this course only have to worry about ODE where unknown function depends only on a single variable
			* e.g. $y(t,), y^\prime(t), y^{\prime\prime}(t), \ldots$
		* e.g. Newton's law for a falling body
			* $F=mg$
			* $y(t)=$ pos of object over time
			* $my^{\prime\prime}(t)=mg\Rightarrow y{\prime\prime}=g$
		* e.g. RC-circuit
        	* $C\frac{dV}{dt}+\frac VR = 0$
	* The order of a DE is the highest derivative that appears in the DE
* Solving DEs
	* e.g. $y^{\prime\prime}=9.8\Rightarrow y(t)=4.9t^2$ as one possible solution
	* e.g. $CV^\prime + \frac VR=0$ with $C=R=1$, so $V^\prime+V=0\Rightarrow V(t)=e^{-t}$ as one possible solutions
* Rank
	* $y^\prime+y=0$ has a solution of $e^{-t}$, but $2e^{-t}$ is also a solution
		* More generally functions of the form $y(t)=K\cdot e^{-t}$ are solutions where $K\in\mathbb R$
    * In complement to the DE, one can specify initial conditions (IC) that functions at some given value must satisfy
    	* e.g. At time $t$...
    * An initial value problem (IVP) is gen by a DE+IC
    * e.g. $y^\prime+y=0$ and $y(0)=0$
    	* So y(0)=Ke^{-t}=K=0
    	* If $y(0)=1$ then $y=e^{-t}$ solution instead
	* The solutions of $y^\prime+ay=0$ are of the form $y(t)=Ke^{-at}, K\in\mathbb R$
		* Can use any time
		* $K$ determined by IC
* In rest of chapter will work with equations of form $y^\prime=F(x, y)$
* Slope fields
	* Textbook 1.2.1
	* $y^\prime=F(x, y)$ gives the slop (direction of the tangent in the graph of solutions) of solutions at each point of the $(x, y)$ plane
	* If we do this for many points, we get a pictture of the slope field of the DE (such that graph of solutions are tangent to the field)
	* e.g. $y^\prime=x\cdot y$
		* Remark: one can check $y=Ke^{\frac{x^2}2}$
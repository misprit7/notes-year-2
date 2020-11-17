# Third Class
* Dot product
	* Geometric
		* $\vec A\cdot \vec B =|\vec A||\vec B|\cos\theta$
		* $\theta$ is angle between them
    * Algebraic
    	* $\vec A = <a_1, a_2, a_3>$
    	* $\vec B = <b_1, b_2, b_3>$
    	* $\vec A \cdot \vec B = a_1b_1+a_2b_2+a_3b_3$
    * Note
    	* $\vec A\cdot \vec A = |\vec A|^2$
    	* $\vec A\cdot \vec B = 0\Leftrightarrow\theta=\frac\pi2\Leftrightarrow \vec A\perp \vec B$
* e.g. A pyramid is built from 3 $45\degree-45\degree-90\degree$ triangles as sides and an equilateral triangle as a base. What  is the angle between the base & side? 
	* Pyramid with vertices $(1, 0, 0, (0, 1, 0), (0, 0, 1)$ and $(0, 0, 0)$ is the kind we want
	* $\theta = \cos^{-1}\frac1{\sqrt3}$
* e.g. A pyramid is built from 4 equilateral triangles as sides and a square base. What is the angle between base and side?
	* Square base around with one leg on each axis
	* Use dot product formulas with vectors bisecting base and going to top
	* $\theta = \cos^{-1}\frac1{\sqrt3}$
* Cross product
	* Geometric
		* $\vec A\times\vec B$ is perpendicular to both $\vec A$ and $\vec B$
		* $|\vec A\times\vec B| = |\vec A||\vec B|\sin\theta$
		* Direction determined by right hand rule
    * Algebraic
    	* $\vec A=<a_1, a_2, a_3>$
    	* $\vec B=<b_1, b_2, b_3>$
    	* $\vec A\times\vec B = <a_2b_3-a_3b_2, a_3b_1-a_1b_3, a_1b_2-a_2b_1>$
    * Notes
    	* $\vec A || \vec B \Leftrightarrow \vec A\times\vec B=\vec 0$
    	* $\vec A\times\vec B = -\vec B\times\vec A$
    	* Not commutive, is distributive
    	* Not associative
    		* $(\vec A\times\vec B)\times\vec C\neq \vec A\times(\vec B\times\vec C)$
    		* Why not? Look at case $(\vec A\times\vec B)\times\vec B ?= \vec A\times(\vec B\times\vec B)$
    		* $\vec B\times\vec V$ is zero by definition and left hand side is nonzero, so can't be the case
* Scalar triple product
	* $\vec A\cdot(\vec B\times \vec C) = \det<\vec A, \vec B, \vec C>$ is (up to sign) the volume of parallelepiped
	* spanned by $\vec A, \vec B, \vec C$
	* Notes: $\vec A\cdot (\vec B\times\vec C) = (\vec A\times\vec B)\cdot \vec C=\vec C\cdot (\vec A\times\vec B)$
		* Cannot do $\vec A\cdot (\vec B\times\vec C) = (\vec A\cdot \vec B)\times\vec C$
* One way to think about dot product in terms of project
	* $comp_{\vec B} = |\vec A|\cos\theta = \frac{\vec A\cdot \vec B}{|\vec B|}$
		* $comp$ is component operation
    * $proj_{\vec B}\vec A = (comp_{\vec B}\vec A)\frac{\vec B}{|\vec B|} = (\frac{\vec A\cdot \vec B}{\vec B\cdot \vec B})\vec B$
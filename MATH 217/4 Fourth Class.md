# Fourth Class
* Lines
	* Determined by a point on the line and a vector parallel to the line
* Planes
	* Uniquely determined by point and two vectors
	* If given 3 points in a plane that are all on three axises, can write as $\frac x{a_1}+\frac y{a_2}+\frac z{a_3}=1$ where $a_1, a_2, a_3$ are the $x, y, z$ intercepts respectively
* Circles
	* In $xy$ plane unit circle is $x^2+y^2=1$
		* $\vec r(t)=<\cos t, \sin t, 0>$
		* Could also have $<\cos t^3, \sin t^3, 0>, 0\leq t\leq(2\pi)^{1/3}$
	* Helix can be made by $<\cos t, \sin t, t>$
* e.g. Find a parameterization of the curve given by $\{z=\sqrt{x^2+y^2}\}\cap \{z=1+y\}$
	* Can't use $z=t$ or $y=t$ since if a point on the curve is not uniquely specified by it's $z$ or $y$ coordinate it not be a parameterization
	* Set $x(t)=t\Rightarrow z=\sqrt{t^2+y^2}=1+y\Rightarrow y(t)=\frac12(t^2-1)\Rightarrow z(t)=\frac12(t^2+1)$
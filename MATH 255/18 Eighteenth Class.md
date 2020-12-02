# Eighteenth Class
* Eighteenth Class
  * Previously only studied linear constant systems with distinct eigenvalues
  * For $\vec X=PX$ ($P$ matrix of size $n$), eigenvalues $\lambda_i$ are roots of $x_p$, so $x_p(\lambda)=\prod_{i=1}^k(\lambda-\lambda_i)^{\alpha i}, i\neq j, \lambda_i\neq\lambda_j$
  * By definition, $\exists\vec v_i$ s.t. $P(\vec v_i)=\lambda_i\vec v_i$, i.;e. $\ker(P-\lambda_i I)\neq \{\vec 0\}$
  * We call $\alpha_i$ the algebraic multiplicity of $\lambda_i$ (multiplicity as root of $x_p$) and we call the dimension of $\ker(P-\lambda_i I)$ the geometric multiplicity of $\lambda_i$ (in the context of this class, this multiplicity characterizes the number of linear independent solutions)
* Theorem (from linear algebra): The geometric multiplicity $\leq$ algebraic multiplicity
  * When the multiplicities are all equal (which is the case when all eigenvalues are distinct since $\alpha_i=1$), we have "enough" linearly independent vectors to build solutions: $C_1\vec v_1e^{\lambda_1 t}+\ldots$
* e.g. $P=\begin{pmatrix}1&0\\0&1\end{pmatrix}$
  * $x_p(\lambda)=(1-\lambda)^2, \lambda_1=1, \alpha_1=2$
  * $\ker(\lambda-I)=\R^2$ so $\dim\ker(\lambda-I)=2$
  * Solutions are for example $C_1<1, 0>e^t+C_2<0, 1>e^t$ so solutions are $\vec v e^t$, where $\vec v\in\R^2$
  * When the geometric multiplicity $<$ we have a defective eigenvalue, and we will need to complete the eigenvectors to build the whole set of solutions
* No more notes since I just realized this is optional, so there's not point recording things down
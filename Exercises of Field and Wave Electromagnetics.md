# Exercises of Field and Wave Electromagnetics

## Static Electric Fields

### Example 4-7
- Problem:

	![Figure for Example 4-7](https://github.com/AlbertYoung0112/Notes/blob/master/FWE-Img/FWE_E47.png?raw=true)
	Consider the region enclosed on three sides by the grounded conducting planes shown, in figure. The end plate on the left has a constant potential $V_0$. All planes are assumed to be infinite in extent in the z-direction. Determine the potential distribution within this region.
- Solution:
	$\because V$ is irrelevant to the *Z* axes.
	$\therefore V(x,y,z)=V(x,y)$ 
	The boundary conditions:
	$$
		\begin{cases}
			V(0,y)=&V_0 \\
			V(a,y)=&0 \\
			V(x,0)=&0 \\
			V(x,b)=&0
		\end{cases}
	$$
	$$
		\because 
		\begin{cases}
			\nabla\times\vec{E}=0 \\
			\vec{E}=-\nabla V
		\end{cases}
		\implies
		\nabla^2V=0
	$$
	Suppose the equation $\nabla^2V=0$ has the solution $V$ with formation of:
	$$
		V(x,y)=X(x)\cdot Y(y)
	$$
	Then,
	$$
		\nabla^2V=0 \implies 
			\frac{1}{X(x)}\frac{\partial X(x)}{\partial x} + 
			\frac{1}{Y(x)}\frac{\partial Y(y)}{\partial y}=0
	$$

	$$
		\iff -\frac{1}{X(x)}\frac{\partial X(x)}{\partial x}=\frac{1}{Y(y)}\frac{\partial Y(y)}{\partial y}
	$$
	Because the equation holds for all the $x$ and $y$, thus:
	$$
		\exist k_x, k_y, s.t:
		\begin{cases}
			\frac{1}{X(x)}\frac{\partial X(x)}{\partial x}=-k_x^2 \\
			\frac{1}{Y(y)}\frac{\partial Y(y)}{\partial y}=-k_y^2 \\
			k_y^2=-k_x^2=k^2
		\end{cases}
	$$
	$$
		\iff 
		\begin{cases}
			\frac{\partial X(x)}{\partial x} - k^2 X(x) = 0\\
			\frac{\partial Y(y)}{\partial y} + k^2 Y(y) = 0
		\end{cases}
	$$


	We suppose $k\in R$ first. Therefore solution to the equation set is :
	$$
		\begin{cases}
		X(x) = C_{x1}e^{kx}+C_{x2}e^{-kx} \\
		Y(y) = C_{y1}\cos(ky)+C_{y2}\sin(ky)
	\end{cases}
	$$
	$\because V(x, 0) = 0, Y(0) = 0 \implies C_{y1} = 0$
	$\because V(x, b) = 0, Y(b) = 0 \implies C_{y2}\sin(kb)=0$
	$\implies kb=n\pi \implies Y(y)=C_y\sin(\frac{n\pi}{b}y)$
	$$\therefore V_n(x, y) = 
		( C_{x1} e^{ \frac{n\pi}{b} x } + C_{x2} e^{ -\frac{n\pi}{b}x} )
		C_y \sin( \frac{n\pi}{b} y )$$
	It can be proved that every $V_n$ does **not** satisfies all the constrains listed above, but $V_n(x,y)$ satisfying the boundary constrains on $y=0$ and $y=b$ means that its linear combination should also satisfies the constrains. We try to find a solution $V$ which is the linear combination of $V_n$.
	$$\begin{aligned}
		V(x, y)	&= \sum V_n(x,y)\\
					&= \sum ( C_{x1} e^{ \frac{n\pi}{b} x } + C_{x2} e^{ -\frac{n\pi}{b}x} )
								C_y \sin( \frac{n\pi}{b} y )
		\end{aligned}
	$$
	$$
		\begin{aligned} 
			&V(0, y) = V_0\\ 
			\implies& \sum (C_{x1n}+C_{x2n}) C_{yn}\sin(\frac{n\pi}{b}y) = V_0\\
			\implies& 
				\int_0^b \sum (C_{x1n}+C_{x2n}) C_{yn} \sin( \frac{n\pi}{b} y) \sin( \frac{m\pi}{b} y )
				 = \int_0^b V_0 \sin(\frac{m\pi}{b}y) \\
			\implies&
				\begin{cases}
					\frac{b}{2}  (C_{x1n}+C_{x2n}) C_{yn} &, m=n \\
					0 &, m =\not n
				\end{cases}
				= 
				\begin{cases}
					\frac{2bV_0}{m\pi} &, m \in \{Odd \} \\
					0 &, m \in \{Even\}
				\end{cases} \\
			\implies& (C_{x1n}+C_{x2n}) C_{yn} = 
				\begin{cases}
					\frac{4V_0}{n\pi} &, n \in \{Odd\} \\
				0 &, n \in \{Even\}
				\end{cases}
		\end{aligned}
	$$
	$$
		\begin{aligned}
			&V(a, y) = 0 \\
			\implies& \sum ( C_{x1n} e^{ \frac{n\pi}{b} a } + C_{x2n} e^{ -\frac{n\pi}{b} a} )
								C_{yn} \sin( \frac{n\pi}{b} y ) = 0 \\
			\implies&  C_{x1n} e^{ \frac{n\pi}{b} a } + C_{x2n} e^{ -\frac{n\pi}{b} a}  = 0 \\
			\implies& C_{x2n} = -C_{x1n} (1 - e^{2\frac{n\pi}{b} a})
		\end{aligned}
	$$
	$$
		\begin{aligned}
			V(x, y)	&= \sum ( C_{x1} e^{ \frac{n\pi}{b} x } + C_{x2} e^{ -\frac{n\pi}{b}x} )
								C_y \sin( \frac{n\pi}{b} y ) \\
						&= \sum_{n\in \{Odd\}} 
							\frac{ e^{ \frac{n\pi}{b} \cdot x} -e^{ \frac{n\pi}{b} \cdot(2a-x) }} {1-e^{2n\pi\frac{a}{b} }}
							\cdot \frac{2V_0}{n\pi} \cdot \sin(\frac{n\pi}{b} \cdot y)
		\end{aligned}
	$$
	The solution with parameter $a=b=1[m], V_0=1[V]$ is plotted below:
		![Figure for Example 4-7](https://github.com/AlbertYoung0112/Notes/blob/master/FWE-Img/FWE_E47_funcGrid.png?raw=true)
	The $V(x,y)$ on the boundary:
		![Figure for Example 4-7](https://github.com/AlbertYoung0112/Notes/blob/master/FWE-Img/FWE_E47_boundaryGrid.png?raw=true)
		It's obvious the boundary constrains are satisfied.
		The ***uniqueness of the electrostatic solutions*** tells us that the solution above is the only solution.

## Static Magnetic Fields

### Example 6-8

- Problem:

	![Figure for Example 6-8](https://github.com/AlbertYoung0112/Notes/blob/master/FWE-Img/FWE_E68.png?raw=true)

	Determine the magnetic flux density on the axis of a uniformly magnetized circular cylinder of a magnetic material. The cylinder has a radius $b$, length $L$, and axial magnetization $\vec{M} = \vec{a_x}M_0$.
- Solution:

	Determine the current density:
	$$
		\begin{aligned}
			\vec{J}_m 		&= \nabla^{'} \times \vec{M} = 0 \\
			\vec{J}_{ms} 	&= \vec{M} \times \vec{a_n}^{'} \\
									&= (\vec{a_z}M_0) \times \vec{a_r}  \\
									&= \vec{a_{\phi}} M_0
		\end{aligned}
	$$
	From the $Biot-Savart's Law$:
	$$ \vec{B} = \oint_{c^{'}} d\vec{B}$$
	$$ d\vec{B} = \frac{\mu_0I}{4\pi}$$
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTc4Nzk1NDczLDU4ODg5MDI0NCw0Njc1MT
UwNTUsMTY1MTE3NjMwMywtMTY5MTgyNDk2MywtNzQzMjU5ODc1
LDEyNDg1MjY1NDZdfQ==
-->
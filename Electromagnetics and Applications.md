# Notes on ***Electromagnetics and Applications***

## Basics

- Lorentz Force Law
	
	$$\vec{f} = q(\vec{E}\times\mu_0 \vec{H})$$

- Electric Field

$$\vec{E}=\frac{\vec{f}}{q}$$

- Electric Displacement Vector

	***Electric displacement vector***, denoted by $\vec{D}$, is a vector field that appears in *Maxwell's equations*. It accounts for the effects for the effects of *free and bounded charge* with in the materials.

	- Free charge
		
		Free charges are the excess charges which can move into electrostatic equilibrium
		
	- Bounded charge

		Bound charges set up electric dipoles in response to an applied electric field $\vec{E}$, and polarize other nearby dipoles tending to line them up, the net accumulation of charge from the orientation of the dipoles is the bound charge.

	- Polarization density
	
		***Polarization density*** (or electric polarization, or simply polarization) is the vector field that expresses the density of permanent or induced electric dipole moments in a dielectric material.
	
		For a infinitesimal volume $dV$ with an infinitesimal dipole moment $d\vec{p}$, polarization density is:
	
		$$\vec{P}=\frac{d\vec{p}}{dV}$$

	- Defination of ***electric displacement vector***

		$$\vec{D}=\varepsilon_0 \vec{E} + \vec{P}$$

- ***Gauss's Law for Charge***
	$$\oiint_A(\vec{D}\cdot\hat{n})da = \iiint_V \rho dv=Q$$

- ***Ampere's Law***
	
	$$\oint_c\vec{H}\cdot d\vec{s}=\iint_A\vec{J}\cdot d\vec{a}$$


## Introduction to Electrodynamics

### ***Differential form of Maxwell's equations***

  

$$\nabla\times\vec{E}=-\frac{\partial\vec{B}}{\partial t} \tag{Faraday's Law}$$

$$\nabla\times\vec{H}=\vec{J}+\frac{\partial\vec{D}}{\partial t} \tag{Ampere's Law}$$

$$\nabla\cdot\vec{D}=\rho \tag{Gauss's Law}$$

$$\nabla\cdot\vec{B}=0 \tag{Gauss's Law}$$

  

- Field variables:

	- $\vec{E}$, *electric field*, $V/m$;

	- $\vec{H}$, *magnetic field*, $A/m$;

	- $\vec{B}$, *magnetic flux density*, $T$;

	- $\vec{D}$, *electric displacement*, $C/m^2$;

	- $\vec{J}$, *electric current density*, $A/m^2$;

	- $\rho$, *electric charge density*, $C/m^3$;

  

- Constitutive Relations in **VACUUM**

	- $\vec{D}=\varepsilon_0\vec{E}$, where the *permittivity of vacuum* $\varepsilon_0\approx 8.8532\times10^{-12} farads/m$

	- $\vec{B}=\mu_0\vec{H}$, where *permeability of vacuum* $\mu_0=4\pi\times10^{-7} henries/m$

	- $\vec{J}=\rho\vec{v}=\sigma\vec{E}$, where $v$ is the velocity of the local net charge density $\rho$, and $\sigma$ is the *conductivity* of the medium (*Siemems/m*).

- Requirement: Conservation of charge

	$$\because \nabla\cdot(\nabla\times\vec{A})=0$$

	$$\therefore \nabla\cdot(\nabla\times\vec{H})=0=\nabla\cdot\frac{\partial\vec{D}}{\partial t} + \nabla\cdot\vec{J}$$

	$$\therefore \nabla\cdot\vec{J}=-\nabla\cdot\frac{\partial\vec{D}}{\partial t} \xlongequal{Gauss's law}-\frac{\partial \rho}{\partial t}$$

  

### Electromagnetic waves in the *time domain*

  

- ***Differential form of Maxwell's equations in VACUUM***

	$$\nabla\times\vec{E}=-\mu_0\frac{\partial\vec{H}}{\partial t} \tag{Faraday's Law in vacuum}$$

	$$\nabla\times\vec{H}=\varepsilon_0\frac{\partial\vec{E}}{\partial t} \tag{Ampere's Law in vacuum}$$

	$$\nabla\cdot\vec{E}=0 \tag{Gauss's Law in vacuum}$$

	$$\nabla\cdot\vec{H}=0 \tag{Gauss's Law in vacuum}$$

- ***Helmholtz Wave Equation***
		
	Computing the curl of the *Faraday's law in vacuum*, and replacing the $\nabla\times\vec{H}$ with *Amperes's law*, we got:
		
	$$\nabla\times(\nabla\times\vec{E})=-\mu_0\frac{\partial(\nabla\times\vec{H})}{\partial t}\xlongequal{Ampere's Law}-\varepsilon_0\mu_0\frac{\partial^2\vec{E}}{\partial t^2}$$

	$$\because \nabla\times(\nabla\times\vec{A})=\nabla(\nabla\cdot\vec{A})-\nabla^2\vec{A}$$

	$$\therefore\nabla\times(\nabla\times\vec{E})=\nabla(\nabla\cdot\vec{E})-\nabla^2\vec{E}\xlongequal{Gauss's law}-\nabla^2\vec{E}$$

	$$\therefore\nabla^2\vec{E}-\mu_0\varepsilon_0\frac{\partial^2\vec{E}}{\partial t^2}=0 \tag{Helmholtz Wave Equation}$$
- The velocity of light
	
	Take the wave $\vec{E}(\vec{r}, t)=\hat{x}E_x(z-ct)$ as an example. Substitute it into the *Helmholtz Wave Equation*, yielding:

	$$\vec{E}''=\mu_0\varepsilon_0(-c)^2\vec{E}''$$

	$$\Longrightarrow c=\frac{1}{\sqrt{\mu_0\varepsilon_0}}\approx2.998\times10^8 [m/s]$$
- ***Polarization***
	***Polarization*** of a wave by convention refers to the direction of its electric vector. In the example above, the wave $\vec{E}(\vec{r}, t)=\hat{x}E_x(z-ct)$ is called *x-polarized*.

	If the fields are uniform with respect to two of the coordinates (x, y) so that $\frac{\partial\vec{E}}{\partial x}=\frac{\partial\vec{E}}{\partial y}=0$, we have a ***uniform plane wave***.
- The magnetic field in uniform plane wave
	Still, we take the wave $\vec{E}(\vec{r}, t)=\hat{x}E_x(z - ct)$ as an example. $Using *Faraday's law*:
	$$\frac{\partial \vec{H}}{\partial t}=-\frac{\nabla\times\vec{E}}{\mu_0}=-\hat{y}\frac{1}{\mu_0}\frac{\partial E_x}{\partial z}=-\hat{y}\frac{1}{\mu_0}E_x'$$

	Integrate over time:

	$$\vec{H}(z, t)=-\int_{-\infty}^{t} \frac{\nabla\times\vec{E}}{\mu_0}dt = \hat{y}\frac{1}{\mu_0}\int_{-\infty}^{t}\frac{\partial E_x}{\partial z}dt=\hat{y}\frac{1}{c\mu_0}E_z(z-ct)=\hat{y}\sqrt{\frac{\varepsilon_0}{\mu_0}}E_y(z-ct)$$

	$$\vec{H}(z,t)=\sqrt{\frac{\varepsilon_0}{\mu_0}}\hat{z}\times\vec{E}(z, t)=\hat{z}\times\frac{\vec{E}(z, t)}{\eta_0}$$

- ***Characteristic Impedance of Free Space***
		
	For a single uniform place wave in free space, 

	$$\frac{|\vec{E}|}{|\vec{H}|}=\eta_0=\sqrt{\frac{\mu_0}{\varepsilon_0}}\approx377[Ohms]$$

### Maxwell's equations, waves, and polarization in the *frequency domain*

- The basic elements: *Sinusoidal waves*
	
	Free space is a LTI system so that it's fully characterized by its response to sinusoidal plane waves. For example, a z-propagating x-polarized uniform sinusoidal plane wave can be expressed by:
	$$\vec{E}(\vec{r}, t)=\hat{x}E_0\cos(k(z-ct))$$

	$$\vec{H}(\vec{r}, t)=\hat{y}\sqrt{\frac{\varepsilon_0}{\mu_0}}E_0\cos(k(z-ct))$$

	To make the frequency and spatial dependence more evident, rewrite the $(k(z-ct))$ into $(\omega t-kz)$. $\omega$ is called *angular frequency* and $k$ is called *spatial frequency*, or *wavenumber*. The relationship between wavenumber. wavelength, propagation velocity is:

	$$k=\frac{2\pi}{\lambda}=\frac{\omega}{c}$$
- Maxwell's equations in the complex-frequency domain
	- Express the sinusoidal wave with complex notation
		
		Generally, the $\hat{x}$ component of a general sinusoidal $\vec{E}$ might be:

		$$\vec{E}_x(\vec{r}, t)=\hat{x}E_x(\vec{r})cos(\omega t + \phi(\vec{r}))$$

		Convert to the complex notation, it becomes:

		$$\vec{E}_x(\vec{r},t)=\hat{x}Re[E_x(\vec{r})e^{j(\omega t + \phi_x(\vec{r}))}]=\hat{x}Re[\underline{E}_x(\vec{r})e^{j\omega t}]$$
		
		Here, $\underline{E}_x(\vec{r})$ is called a ***phasor***. The under bar of a phasor indicated the phasor is independent of time.

- ***Time-harmonic Maxwell Equations***
	Substitute the $\vec{E}(\vec{r}, t)$ with its complex notations and omit the $Re[(\cdot) e^{j\omega t}]$, we got:

	$$\nabla\times\vec{\underline{E}}=-j\omega\vec{\underline{B}} \tag{Faraday's Law}$$

	$$\nabla\times\vec{\underline{H}}=\vec{\underline{J}}+j\omega\vec{\underline{D}}\tag{Ampere's Law}$$

	$$\nabla\cdot\vec{\underline{V}}=\underline{\rho}\tag{Gauss's Law}$$

	$$\nabla\cdot\vec{\underline{B}}=0\tag{Gauss's Law}$$

	- Similarly, by computing the curl of the *Faraday's Law* in frequency domain, Helmholtz equation becomes:

	$$\nabla\times(\nabla\times\vec{\underline{E}})=-j\omega\nabla\vec{\underline{B}}$$ 

	$$\nabla(\nabla\cdot\vec{\underline{E}})-\nabla^2\vec{\underline{E}}=-j\omega\mu_0\varepsilon_0\vec{\underline{E}}$$

	$$(\nabla^2+\omega^2\mu_0\varepsilon_0)\vec{\underline{E}}=0 \tag{Wave Equation}$$

	- Example: One possible form of solution to the *wave equation* above is $\vec{\underline{E}}(\vec{r})=\hat{y}E_0e^{-jkz}$. Substituting it in to the wave equation yields:

	$$(\frac{\partial^2}{\partial z^2}+\omega^2\mu_0\varepsilon_0)\vec{\underline{E}}=((-jk)^2+\omega^2\mu_0\varepsilon_0)E_0=0 $$
	$$\Longrightarrow k=\omega\sqrt{\mu_0\varepsilon_0}=\frac{\omega}{c}=\frac{2\pi f}{c}=\frac{2\pi}{\lambda}$$
	$$\vec{\underline{H}}(\vec{r})\xlongequal{Faraday's Law}-\frac{\nabla\times{\vec{\underline{E}}}}{j\omega \mu_0}=-\hat{x}\sqrt{\frac{\varepsilon_0}{\mu_0}}E_0e^{-jkz}=-\hat{x}\frac{1}{\eta_0}E_0e^{-jkz}$$


## Relations between *Integral and Differential* forms of Maxwell's equations

### Recall: The Mathematical Basis
- *Gauss's divergence theorem*
	
	$$\iiint_V(\nabla\cdot\vec{A})dv=\oiint_S(\vec{A}\cdot\hat{n})da \tag{Gauss's Divergence Theorem}$$
	
	Proof:
	
	$$
		\begin{aligned}
			\nabla\cdot\vec{A} & =\frac{\partial\vec{A}}{\partial x}+\frac{\partial\vec{A}}
				{\partial y}+\frac{\partial\vec{A}}{\partial z} \\
		& \begin{aligned} =\lim_{\Delta i\rightarrow0}(
						\frac{
							\Delta y\Delta z(A_x(x_0 + \frac{\Delta x}{2}) ) - A_x(x_0 - \frac{\Delta x}{2}))}
						{\Delta x\Delta y\Delta z} + \\
						\frac{
							\Delta z\Delta x(A_y(y_0 + \frac{\Delta y}{2}) ) - A_y(y_0 - \frac{\Delta y}{2}))}
						{\Delta x\Delta y\Delta z} + \\
						\frac{i
							\Delta x\Delta y(A_z(z_0 + \frac{\Delta z}{2}) ) - A_z(z_0 - \frac{\Delta z}{2}))}
						{\Delta x\Delta y\Delta z}
					)
				\end{aligned}\\
			& = \lim_{\Delta i \rightarrow0}(\frac{\oiint_{S_i}\vec{A}\cdot\hat{n}da}{\Delta v_i})
		\end{aligned}
	$$

	$$
		\lim_{\Delta v \rightarrow0}\sum_i\nabla\cdot\vec{A}\Delta v_i = 
			\lim_{\Delta v \rightarrow0}\sum_i(\oiint_{S_i}\vec{A}\cdot\hat{n}da)
	$$

	$$
		\Longrightarrow \iiint_V(\nabla\cdot\vec{A})dv=\oiint_S(\vec{A}\cdot\hat{n})da
	$$

- *Stokes theorem*

	$$
		\iint_A(\nabla\times\vec{A})\cdot \hat{n} da=\oint_C\vec{A}\cdot d\vec{s} \tag{Stokes Theorem}
	$$

### *Integral Form of Maxwell's Equations*

$$
	\oint_C\vec{E}\cdot d\vec{s}=-\frac{\partial}{\partial t}\iint_A\vec{B}\cdot\hat{n}da \tag{Faraday's Law}
$$

$$
	\oint_C\vec{H}\cdot d\vec{s}=\iint_A(\vec{J}+\frac{\partial\vec{D}}{\partial t})\cdot\hat{n}da \tag{Ampere's Law}
$$

$$
	\oiint_A(\vec{D}\cdot\hat{n})da=\iiint_V\rho dv \tag{Gauss's Law for Charge}
$$

$$k
	\oiint_A(\vec{B}\cdot\hat{n})da=0 \tag{Gauss's Law for Magnetics}
$$

## Electric and Magnetic in *Media*

### Conductivity $\sigma$

$$\vec{J}=\sigma \vec{E}$$

### Permittivity $\varepsilon$
	
- Polarization

	- *Electric Dipoles* $\vec{p}$
	![Polarized Atom](https://github.com/AlbertYoung0112/Notes/blob/master/EA-Img/PolarizedAtom.png?raw=true)

		- $\vec{p}=q\vec{d}$
		- The nucleus deviates from the center with displacement $\vec{d}$.
		- Induced from the applied electric fields or the asymmetric structure of the molecules, such as $H_2O$
	- *Polarized charges*
	![enter image description here](https://github.com/AlbertYoung0112/Notes/blob/master/EA-Img/PolarizedMedia.png?raw=true)

		- Density: $\rho_{p}$
		- The polarized charges are generally canceled within the media, so that the $\rho_{p}=0$ insides.
		- The immobile atomic dipoles on the outside surfaces of the medium are not fully canceled, contributing to the ***surface polarization charges***, $\rho_{sp}$.

- Electric Displacement Vector $\vec{D}$ 

	$$\vec{D}=\varepsilon\vec{E}=\varepsilon_0\vec{E}+\vec{P}=\varepsilon_0\vec{E}(1+\chi)$$


	
	- Origin

		- ***Polarization Vector*** $\vec{P}=nq\vec{d}$, *n* is the density of atoms.
		
		Suppose the electric field is parallel to the z axes. Take a volume *V* that encloses a unit area *A* of the left-hand face of the polarized dielectric, yielding:
		$$-\int_V\rho_pdv=nq\vec{d}=\int_A\vec{P}\cdot\hat{n}da=\int_v\nabla\cdot\vec{P}dv$$
	
		$$\therefore \nabla\cdot\vec{P}=-\rho_p$$

		 From the Gauss's Law for charge:

		$$\varepsilon_0\nabla\cdot\vec{E}\xlongequal{Gauss's Law}\rho=\rho_{f}+\rho_{p}$$

		$$\varepsilon_0\nabla\cdot\vec{E}+\nabla\cdot\vec{P}=\rho_f$$

		$$\nabla\cdot(\varepsilon_0\vec{E}+\vec{P})=\rho_f$$

		Define: 

		$$\vec{D}\equiv\varepsilon_0\vec{E}+\vec{P} \tag{Electric Displacement Vector}$$

		And:
		
		$$\varepsilon=\frac{||\vec{D}||}{||\vec{E}||} \tag{Permittivity in Media}$$

		$$\chi=\frac{||\vec{P}||}{\varepsilon_0||\vec{E}||} \tag{Susceptibility}$$

		Then:
		
		$$\vec{D}=\varepsilon_0\vec{E}+\vec{P}=\varepsilon\vec{E}=\varepsilon_0(1+\chi)\vec{E}$$

	- $\chi$ is generally less than 3, because the nuclei are bound tightly to their electron clouds.

### Permeability $\mu$

$$
	\vec{B}=\mu\vec{H}=\mu_0(\vec{H}+\vec{M})=\mu_0(1+\chi_m)
$$

-	$\vec{M}$, ***Magnetization***
-	$\chi_m$, ***Magnetic Susceptibility***
	-	$\chi_m < 0, \mu<\mu_0$ in *diamagnetic materials*
	-	$\chi_m > 0, \mu>\mu_0$ in *paramagnetic materials*
	-	$\mu\approxeq\mu_0$ in both diamagnetic and prarmagnetic materials
	-	$\chi_m\gg0, \mu\gg\mu_0$, in *ferromagnetic materials*
- *Ferromagnetic materials*
	- The atomic magnetic dipoles spontaneously align over ***magnetic domains***
	- The size of those domains oriented in the general direction of the applied magnetic field grow ad that field increases.
	- If the domain wall moves easily, the magnetic susceptibility $\chi_m$ is large.
	- ***Magnetic Saturation*** Sufficiently high magnetic fields forces all domains expand to their maximum and rotate in the direction $\vec{H}$, leading to the maximum value of $\vec{M}$
	- ***Hysteresis Curve***
	





<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwODM1Nzk4OTQsLTc0Mjg0NDcwNCwtMT
gyMzg5NjI4MCwyMDIwODYxOTg5LC0xMTYzMzU1MTQ4LDE3MTIx
NzYwODcsNTI5NzUyNzY4LC05NDU4NDg5MzgsLTE0NjE4Njk4MD
IsLTQwODM1NjIzMywyMDE2MDY0NTEwLDE4MTQ3MTkzMywxMDMw
MDk1NjQwLDIwOTE2Mjk2NTMsOTI1NzY3MDY0LC0xODUyNDY4ND
I2LDIwNTUxODA2MDUsLTMwMTE4NDk4LDQ1ODk3MjI4NSwxMDYz
NTY0NjY4XX0=
-->
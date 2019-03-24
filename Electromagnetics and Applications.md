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

		$$\vec{E}_x(\vec{r},t)=\hat{x}Re[E_x(\vec{r})e^{j(\omega t + \phi_x(\vec{r}))}]=\hat{x}Re[]$$
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjE0NTIzNjcwMiwxMDYzNTY0NjY4LDE4ND
Y0NzM2NTcsNDk4NDkxNjU0LC0xNjg4NjA5MTUzLC0yODgxODMw
MjZdfQ==
-->
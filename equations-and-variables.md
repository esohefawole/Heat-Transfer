# Heat Transfer Equations and Units

## Unit Symbol Definitions  
$m$: meters  
$g$: grams  
$K$: Kelvin  
$W$: watts  
$J$: joules  
$\theta$: theta (angle in radians or dimensionless temperature)  
$\phi$: phi (angle in radians)
$s$: seconds  

## Variables with Units  
length(l), height (h), or width (w) [=] $m$  
diameter (D) or radius (r) [=] $m$  
area (A) [=] ${m^2}$  
volume (V) [=] $m^3$   
temperature ($T$) [=] $K$  
temperature of surroundings ($T_{surr}$) [=] $K$  
temperature of surface ($T_s$) [=] $K$  
temperature of bulk fluid ($T_\infty$)  
time (t) [=] $s$  
velocity (v) [=] $\frac{m}{s}$  
mass (m) [=] $kg$    
density ($\rho$) [=] $kg/m$  
heat capacity ($C_p$) [=] $\frac{kJ}{kg \cdot K}$   
heat rate ($q$) [=] $W$  
heat flux ($\underline{q}''$) [=] $\frac{W}{m^2}$  
volumetric energy rate ($\dot{q}$ or $q'''$) [=] $\frac{W}{m^3}$  
heat transfer coefficient (h) [=] $\frac{W}{m^2 \cdot K}$   
thermal conductivity (k) [=] $\frac{W}{m \cdot K}$    
Stefan-Boltzmann constant ($\sigma$) [=] $\frac{W}{m^2 \cdot K^4}$  
thermal diffusivity ($\alpha$) [=] $\frac{m^2}{s}$  
irradiation (G) [=] $\frac{W}{m^2}$    
emissivity ($\epsilon$) [=] dimensionless  
emissive power ($E$) [=] $\frac{W}{m^2}$  
ideal emissive power of black body ($E_b$) [=] $\frac{W}{m^2}$  
thermal energy rate ($\dot{E}$) [=] $W$  
thermal energy rate in ($\dot{E_{in}}$) [=] $W$  
thermal energy rate out ($\dot{E_{out}}$) [=] $W$  
thermal energy stored rate ($\dot{E_{st}}$) [=] $W$  
thermal energy generation rate ($\dot{E_{gen}}$) [=] $W$    

## Equations

### Dimensionless Numbers

Biot Number (Bi) $\equiv \frac{hL}{k}$  
Grashof Number (Gr) $\equiv \frac{g L^3 \beta (T_s - T_\infty)}{\nu^2}$  
Nusselt Number (Nu) $\equiv \frac{hL}{k}$  
Peclet Number (Pe) $\equiv \frac{\nu L}{\alpha}$  
Prandtl Number (Pr) $\equiv \frac{\nu}{\alpha} = \frac{\mu C_p}{k}$  
Rayleigh Number (Ra) $\equiv Gr \cdot Pr$  
Reynolds Number (Re) $\equiv \frac{\rho v L}{\mu}$


### Energy Rate Balance

$\dot{E_{st}} = \dot{E_{in}} - \dot{E_{out}} + \dot{E_{gen}}$  

where  
- $\dot{E}_{st} = \rho C_p \frac{\partial T}{\partial t} \partial x \partial y \partial z$  
- $\dot{E}_{in} = q''_s A_s$ where $q''_s$ is the heat flux from a source (conduction or convection) and $A_s$ is the surface area of the heat flux source   
- $\dot{E}_{out} = q''_s A_s$ where $q''_s$ is the heat flux from a source (conduction, convection or radiation) and $A_s$ is the surface area of the heat flux source  
- $\dot{E}_{gen} = q'''V$ (for a resistor)

-----------------------------
### Laws


Fourier's Law (Conduction) 

heat flux:   
$\underline{q}'' = -k \underline{\nabla} T$ (differential)  
$q'' = k \frac{\triangle T}{L}$ 
 
heat rate:  
$q = -k A\triangle T /L$ (for circuit analogy)  

$\cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot$

Newton's Law of Cooling (Convection) 

$q'' = h(T_s - T_\infty)$  

$\cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot$

Stefan-Boltzmann Law (Radiation)  

$E = \epsilon \sigma T_s^4$ or $q_r'' = \epsilon \sigma (T_s^4 - T_{surr}^4)$

-----------------

### Heat Diffusion Equation  

Cartesian Coordinates:  

$\frac{\partial}{\partial x} (k \frac{\partial T}{\partial x}) + \frac{\partial}{\partial y} (k \frac{\partial T}{\partial y}) + \frac{\partial}{\partial z} (k \frac{\partial T}{\partial z}) + q''' = \rho C_p \frac{\partial T}{\partial t}$  

dividing the equation by $k$ gives  

$\frac{\partial^2 T}{\partial x^2} + \frac{\partial^2 T}{\partial y^2} + \frac{\partial^2 T}{\partial z^2} + \frac{q'''}{k} = \frac{1}{\alpha} \frac{\partial T}{\partial t}$  

where $\alpha = \frac{k}{\rho C_p}$  

$\cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot$

Cylindrical Coordinates:  

$\frac{1}{r} \frac{\partial}{\partial r} (kr \frac{\partial T}{\partial r}) + \frac{1}{r^2} \frac{\partial}{\partial \phi} (k \frac{\partial T}{\partial \phi}) + \frac{\partial}{\partial z} (k \frac{\partial T}{\partial z}) + q''' = \rho C_p \frac{\partial T}{\partial t}$  

$\cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot \cdot$

Spherical Coordinates:

$\frac{1}{r^2} \frac{\partial}{\partial r} (k r^2 \frac{\partial T}{\partial r}) + \frac{1}{r^2 sin^2 \theta} \frac{\partial}{\partial \phi} (k \frac{\partial T}{\partial \phi}) + \frac{1}{r^2 sin \theta} \frac{\partial}{\partial \theta} (k \frac{\partial T}{\partial \theta}) + q''' = \rho C_p \frac{\partial T}{\partial t}$  

-----------------

### Boundary Conditions  

1. Constant Surface Temperature: $T(\underline{r},t) = T_s(\underline{r_s},t)$  

2. Constant surface heat flux: 
    - finite: $-k \frac{dT}{dx} = q_s''$ at $x=0$
    - insulation or adiabatic: $-k \frac{dT}{dx} = 0$  

3. Convection surface condition: $-k \frac{dT}{dx} = h(T_\infty - T(x))$ at $x=0$  

4. Boundary between two adjoining bodies (interface):
    - $T_1 = T_2$ at $x=x_{boundary}$
    - $-k_1 \frac{dT_1}{dx} = -k_2 \frac{dT_2}{dx}$ at $x=x_{boundary}$ (conservation of energy)
    - $q_1'' = q_2''$ at $x=x_{boundary}$  

------------------------



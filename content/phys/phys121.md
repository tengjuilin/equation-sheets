---
title: "PHYS 121 Mechanics"
date: 2021-08-17T00:00:00+08:00
---

## Kinematics

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Displacement|$\mathrm{m}$|$\Delta \vec{r} = \vec{r}\_{f} - \vec{r}_{i}$|
|Instantaneous velocity|$\mathrm{m/s}$|$\vec{v} = \dfrac{d\vec{r}}{dt}$|
|Instantaneous acceleration|$\mathrm{m/s^{2}}$|$\vec{a} = \dfrac{d\vec{v}}{dt} = \dfrac{d^{2}\vec{x}}{dt^{2}}$|

|Description|Equations|
|-:|:-|
|Kinematics equations at constant acceleration|$x = x_{0} + v_{0}t + \dfrac{1}{2}at^{2}$ <br/> $v = v_{0} + at$ <br/> $v_{f}^{2} = v_{i}^{2} + 2a\Delta x$|
|Relative velocity|$\vec{v}\_{P/A} = \vec{v}\_{P/B} + \vec{v}\_{B/A}$|
|Centripetal acceleration|$a_{\mathrm{rad}} = \dfrac{v^{2}}{R} = \dfrac{4\pi^{2}R}{T^{2}}$|

## Dynamics

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Spring force (Hooke's law)|$\mathrm{N}$|$F_{s} = -k\Delta x$|
|Static friction|$\mathrm{N}$|$f_{s} \leq (f_{s})_{\mathrm{max}} = \mu_{s} F_{N}$ <br/> $\mu_{s} = \tan(\theta)$|
|Kinetic friction|$\mathrm{N}$|$f_{k} = \mu_{k} F_{N}$|
|Gravitational force near Earth surface|$\mathrm{N}$|$\vec{F}\_{g} = m\vec{g}$ <br/> $g = 9.81 \mathrm{m/s^{2}}$|

|Description|Equations|
|-:|:-|
|Newton's first law moving at constant velocity|$\sum \vec{F}\_{\mathrm{ext}} = \vec{0}$|
|Newton's second law|$\sum \vec{F}\_{\mathrm{ext}} = m\vec{a}$|
|Newton's third law|$\vec{F}\_{AB} = - \vec{F}\_{BA}$|
|Acceleration on an inclined plane|$a = g\sin\theta$|

## Energy

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Work|$\mathrm{J}$|$W = \vec{F} \cdot \vec{x} = Fx\cos\theta$ <br/> $W = \displaystyle\int_{x_{1}}^{x_{2}} F \ dx$|
|Kinetic energy|$\mathrm{J}$|$K = \dfrac{1}{2}mv^{2}$|
|Power|$\mathrm{W}$|$P = \dfrac{dW}{dt} = \dfrac{dE}{dt}$ <br/> $P = \vec{F} \cdot \vec{v}$|
|Gravitational potential energy|$\mathrm{J}$|$U = mgh$ <br/> $W_{\mathrm{grav}} = - \Delta U_{\mathrm{grav}}$|
|Elastic potential energy|$\mathrm{J}$|$U = \dfrac{1}{2}kx^{2}$ <br/> $W_{\mathrm{el}} = - \Delta U_{\mathrm{el}}$|
|Reduced mass|$\mathrm{kg}$|$\mu = \dfrac{m_{1}m_{2}}{m_{1} + m_{2}}$|
|Coefficient of restitution|-|$e = -\dfrac{v_{12, f}}{v_{12, i}}$|

|Description|Equations|
|-:|:-|
|Work-energy theorem|$W_{\mathrm{total}} = \Delta K$|
|Conservation of mechanical energy|$K_{i} + U_{i} = K_{f} + U_{f}$|
|Energy of system with external force (non-isolated system)|$K_{i} + U_{i} + W = K_{f} + U_{f}$|
|Conservation of energy|$\Delta K + \Delta U + \Delta U_{int} = 0$|
|Force as a function of potential energy|$\vec{F} = -\vec{\nabla} U$ <br/> $F = -\dfrac{dU}{dx}$|

## Momentum

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Momentum|$\mathrm{kg\cdot m/s}$|$\vec{p} = m\vec{v}$ <br/> $\sum \vec{F}\_{\mathrm{ext}} = \dfrac{d\vec{p}}{dt}$|
|Impulse|$\mathrm{kg\cdot m/s}$|$\vec{J} = \sum \vec{F} \Delta t$ <br/> $\vec{J} = \displaystyle\int_{t_{1}}^{t_{2}} \sum \vec{F} \ dt$|
|Center of mass|$\mathrm{m}$|$\vec{r}\_{\mathrm{cm}} = \dfrac{\sum\limits_{i} m_{i}\vec{r}\_{i}}{\sum\limits_{i} m_{i}}$|

|Description|Equations|
|-:|:-|
|Impulse-momentum theorem|$\vec{J} = \Delta \vec{p}$|
|Conservation of momentum (closed system)|$\vec{p}\_{i} = \vec{p}\_{f}$ <br/> $\sum \vec{F}\_{\mathrm{ext}} = \dfrac{d\vec{p}}{dt}$|
|Force on extended body|$\sum \vec{F}_{\mathrm{ext}} = m\vec{a}\_{\mathrm{cm}}$|

## Rotational Kinematics

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Angular displacement|$\mathrm{rad}$|$\Delta \theta = \theta_{f} - \theta_{i}$|
|Angular velocity|$\mathrm{rad/s}$|$\omega_{z} = \dfrac{d\theta}{dt}$|
|Angular acceleration|$\mathrm{rad/s^{2}}$|$\alpha_{z} = \dfrac{d\omega_{z}}{dt} = \dfrac{d^{2}\theta}{dt^{2}}$|
Rotational Inertia of particle|$\mathrm{kg\cdot m^{2}}$|$I = \sum\limits_{i} m_{i}r_{i}^{2}$|
Rotational kinetic energy|$\mathrm{J}$|$K = \dfrac{1}{2}I\omega^{2}$|

|Description|Equations|
|-:|:-|
Rotational kinematics equation with constant angular acceleration|$\theta = \theta_{0} + \omega_{0z}t + \dfrac{1}{2}\alpha_{z} t^{2}$ <br/> $\omega_{z} = \omega_{0z} + \alpha_{z}t$ <br/> $\omega_{fz}^{2} = \omega_{iz}^{2} + 2\alpha_{z}\Delta\theta$|
Relationship between linear kinematics and rotational kinematics|$s = r\theta$ <br/> $v = r\omega$ <br/> $a_{\mathrm{tan}} = r\alpha$ <br/> $a_{\mathrm{rad}} = \dfrac{v^{2}}{r} = \omega^{2}r$|
Parallel-axis theorem|$I_{\mathrm{parallel}} = I_{\mathrm{cm}} +md^2$|

## Rotational Dynamics

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Torque|$\mathrm{N\cdot m}$|$\vec{\tau} = \vec{r} \times \vec{F} = Fr\sin\theta$ <br/> $\sum \vec{\tau} = \dfrac{d\vec{L}}{dt}$|
Angular momentum of a particle|$\mathrm{kg\cdot m^{2}/s}$|$\vec{L} = \vec{r} \times \vec{p} = mvr\sin\theta$|
Angular momentum of rotating body|$\mathrm{kg\cdot m^{2}/s}$|$\vec{L} = I \vec{\omega}$|

|Description|Equations|
|-:|:-|
Rotational Newton's second law|$\sum \tau = I\alpha_{z}$|
Condition of mechanical equilibrium|$\sum \vec{F}\_{\mathrm{ext}} = m\vec{a}$ <br/> $\sum \tau = I\alpha_{z}$|
Total kinetic energy of rotating and translating object|$K = \dfrac{1}{2}mv^{2}_{\mathrm{cm}} + \dfrac{1}{2} I\_{\mathrm{cm}} \omega^{2}$|
Rolling without slipping|$v_{\mathrm{cm}} = R\omega$|
Slipping (only rolling)|$v_{\mathrm{cm}} < R\omega$|
Skidding (only translating)|$v_{\mathrm{cm}} > R\omega$|
Rotational Work|$W = \tau_{z}\Delta\theta$ <br/> $W = \displaystyle\int_{\theta_{1}}^{\theta_{2}} \tau_{z} \ d\theta$ <br/> $W = \Delta K_{\mathrm{rot}}$|
Power|$P = \dfrac{dW}{dt}$ <br/> $P = \tau_{z}\omega_{z}$|
Conservation of angular momentum (closed system)|$\vec{L}\_{i} = \vec{L}\_{f}$ <br/> $\sum \vec{\tau} = \dfrac{d\vec{L}}{dt}$|

## Universal Gravitation

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Gravitational force|$\mathrm{N}$|$F_{g} = G\dfrac{m_{1}m_{2}}{r^{2}}$|
|Gravitational acceleration|$\mathrm{m/s^{2}}$|$g = G\dfrac{m_{E}}{r^{2}}$|
|Gravitational potential energy|$\mathrm{J}$|$U = - G\dfrac{m_{E}m}{r}$|

|Description|Equations|
|-:|:-|
|Escape velocity|$v_{\mathrm{escape}} = \sqrt{\dfrac{2Gm_{E}}{R}}$|
|Velocity in circular orbit|$v_{\mathrm{circ}} = \sqrt{\dfrac{Gm_{E}}{R}} = \dfrac{2\pi R}{T}$|
|Period in circular orbit|$T = \dfrac{2\pi R}{v} = 2\pi R\sqrt{\dfrac{R}{Gm_{E}}} = \dfrac{2\pi r^{3/2}}{\sqrt{Gm_{E}}}$|

---
title: "(1+1)-dimensional KPZ equation simulation"
excerpt: "Estimation of critical exponents of the KPZ universality class.<br/><img src='/images/500x300.png'>"
collection: portfolio
---

## Introduction
For this project, the KPZ equation in one spatial dimension is simulated, i.e., the non-linear stochastic partial differential equation (SPDE) describing the height of a surface that grows over time:
$$\frac{\partial h(x,t)}{\partial t}=\nu\frac{\partial^2 h(x,t)}{\partial x^2}+\frac{\lambda}{2}\left(\frac{\partial h(x,t)}{\partial x}\right)^2+\xi(x,t),$$
where $\nu, \lambda$ are parameters of the model and $\xi(x,t)$ represents a Gaussian white noise with zero mean and delta-like correlation in both $x,t$. The growing surface is characterized by its **width** $w(L,t)$, where $L$ is the size of the system, defined via
$$w^2(L,t)=\left\langle \overline{h^2(t)}-\overline{h(t)}^2\right\rangle.$$

This width can be expressed through dynamic scaling relations which introduce the **roughness exponent** $\alpha$, the **growth exponent** $\beta$ and the **dynamic exponent** $z$:
$$w^2(L,t)=t^{2\beta}F\left(\frac{t}{L^z}\right)=L^{2\alpha}\tilde{F}\left(\frac{t}{L^z}\right)$$.
For one-dimensional systems, the KPZ universality class is characterized by the following values of the critical exponents: $\alpha=1/2,\ \beta=1/3,\ z=3/2$.

The aim of the project is to evaluate the impact of the lattice size $L$ and the parameter $\lambda$ on the estimation of the critical exponents $\alpha$ and $\beta$. To do this, the integration time step $\Delta t$ will be fixed, as well as the noise strength $D$ and the parameter $\nu$. The former will be fixed to $\Delta t=0.1$ and $2D=\nu=1$ and to ensure numerical integration stability the Courant criterion will be used to extract the minimum stable spatial step:
$$\frac{2\nu\Delta t}{(\Delta x)^2}\leq 1.$$

The parameter $\lambda$ will take values $0.5,\ 1,\ 2,\ 3$ and the lattice size $L$ will range from $L=50$ to $L=200$ in steps of $50$. For each value of $\lambda$, 4 curves will be extracted for each corresponding $L$. Numerically, the stochastic Heun method has been implemented in Python with a forward-time, centered-space (FTCS) scheme.

## Results
In what follows, the graphs containing the simulated $w^2(L,t)$ for each corresponding value of $\lambda$ will be presented, along with tables for the fitted $\beta$ and the average $\alpha$ in each case.
[!](/images/kpz/lambda05.png)
[!](/images/kpz/lambda1.png)
[!](/images/kpz/lambda2.png)
[!](/images/kpz/lambda3.png)

As one can observe, the value of $\alpha$ was correctly estimated, with all obtained values including the theoretical result $\alpha=1/2$ in their uncertainty interval. The opposite happens for $\beta$, where one can see that it is underestimated in all cases. This is due mostly to a small lattice size and low values for the parameters.

---
title: "Convergence of Deffuant model with opinions absolutely continuous with respect to Lebesgue measure (ID: **CDM230517**)"
excerpt: "We lift the analysis of the **Deffuant model** with $$k$$ agents exhibiting opinions absolutely continuous with respect to Lebesgue measure to the **manifold of the densities** implied by the model. We conjecture that there is an **embedding into 3-dim. space** based on the two model parameters and a fixed initial density for i.i.d. opinions with a unique singularity. This **singularity gives the limit law of the model** and is probably given by a Dirac delta over the projection of the support of the $$k$$ product of the initial density to the digonal of the $$k$$ cube. "
collection: portfolio
---

The Deffuant model is a well known model in opinion dynamics which models opinion evolution based on labeled vertices, representing agents and their opinions, and their conflictious relationships by a convex combination of the labels of two interacting agents based on some relationship network.
 
Consider a graph $G=(\mathcal{V},\mathcal{E})$ with $|\mathcal{V}|=n$ and $|\mathcal{E}|=m$ as well as two parameters $\theta\in(0,1)$ and $\mu\in\left[0,\frac{1}{2}\right)$. Each vertex $x\in\mathcal{V}$ exhibits a label $X_v\sim\mathcal{L}([0,1])$ i.i.d. with $\mathcal{L}$ absolutely continuous with respect to the Lebesgue measure. 
The Deffuant model model evolves as follows in time $t\in\mathbb{N}$.

If $|X^t_A-X^t_B|<\theta$, then
- set, firstly, $X_A^{t+1}= X_A^{t} +\mu(X_B^{t}-X_A^{t})$ and,
- secondly, $X_B^{t+1}= X_B^{t} +\mu(X_A^{t}-X_B^{t+1})$ for the new opinions. 

Denote the joint initial distribution of the labels $X$ by $\mathcal{D}^0$ and assume that it exhibits a density $\pi^0$. At any time $t\in\mathbb{N}$ an edge $\langle I,J\rangle$ is drawn uniformly from all edges $\mathcal{E}$ and we can rewrite the algorithmic step described hereinabove as a recurrence relation. To this end, let $A^{\theta}=  \lbrace x\in\mathbb{R}^2\big\| \, \|x_1-x_2\| > \theta \rbrace $ as well as $A_{ij}^{\theta}= \lbrace x\in\mathbb{R}^n\big\|\, (x_i,x_j)\in A^{\theta} \rbrace $ and define for $i,j\in\lbrace 1,...,n\rbrace $ the function

$$\Phi_{ij}^{\mu}(x_1,...,x_d) = (x_1,..., x_i+\mu(x_j-x_i),...,x_j+\mu(x_i-x_j),...,x_n).$$

Then, the labels at time $t+1$ are constructed as

$$X^{t+1} = X^t\,\delta_{A_{IJ}^{\theta}}(X^t) + \Phi_{IJ}^{\mu}(X^t)\,\delta_{\left(A_{IJ}^{\theta}\right)^c}(X^t).$$

Due to the dynamics, the density $\pi^0$ evolves over time as follows. Denote by $E^t$ the edge drawn during the $t$-th step and by $\pi^t$ the density of the joint distribution of the labels at time $t$. Then, for $t\in\mathbb{N}$, at time $t+1$ the process of labels $X^{t+1}=(X_1^{t+1},...,X_d^{t+1})$ follows the following law. Let $B\in\mathcal{B}([0,1]^n)$, 

$$\mathbb{P}\left[X^{t+1}\in B\right] = \dfrac{1}{m}\sum_{<i,j>\in E} \mathbb{P}\left[X^{t+1}\in B, X^t\in A_{ij}^{\theta}| E^t = <i,j>\right]\\  
		\qquad\qquad + \mathbb{P}\left[X^{t+1}\in B, X^t\in \left(A_{ij}^{\theta}\right)^c| E^t = <i,j>\right]\\
		\qquad = \dfrac{1}{m}\sum_{<i,j>\in E} \mathbb{P}\left[X^t\in B\cap A_{ij}^{\theta}\right]+ \mathbb{P}\left[X^t\in \left(\Phi_{ij}^{\mu}\right)^{-1}(B)\cap \left(A_{ij}^{\theta}\right)^c\right]\\
		\qquad =\dfrac{1}{m}\sum_{<i,j>\in E}\int_B \pi^t(x)\delta_{A_{ij}^{\theta}}(x) + {\scriptstyle{\tfrac{\pi^t\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)}{1-2\mu}}}\delta_{\left(A_{ij}^{\theta}\right)^c}\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right) dx\\
		\qquad =\int_B \dfrac{1}{m}\sum_{<i,j>\in E}\left(\pi^t(x)\delta_{A_{ij}^{\theta}}(x) + {\scriptstyle{\tfrac{\pi^t\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)}{1-2\mu}}}\delta_{\left(A_{ij}^{\theta}\right)^c}\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)\right) dx.$$
		
Thus, the following identity can be deduced.

$$\pi^{t+1}(x)=\dfrac{1}{m}\sum_{<i,j>\in E}\left(\pi^t(x)\delta_{A_{ij}^{\theta}}(x) + {\scriptstyle{\tfrac{\pi^t\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)}{1-2\mu}}}\delta_{\left(A_{ij}^{\theta}\right)^c}\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)\right).$$

One approach, to showing convergence of the model, would be to use the obtained equation to show convergence of the sequence $(\pi^t)_{t\in\mathbb{N}}$ as a sequence in $L^1\left(\[0,1\]^n\right)$. We define the operator $\mathcal{T}_{\theta}$ for $f\in L^1\left([0,1]^n\right)$ as

$$\left(\mathcal{T}_{\theta}f\right)(x):=\dfrac{1}{m}\sum_{<i,j>\in E}\left(f(x)\delta_{A_{ij}^{\theta}}(x) + {\scriptstyle{\tfrac{f\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)}{1-2\mu}}}\delta_{\left(A_{ij}^{\theta}\right)^c}\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)\right)$$
	
skipping the dependence on the underlying graph $G$ in the notation of $\mathcal{T}_{\theta}$. Then, for any initial density $\pi^0\in L^1\left(\[0,1\]^n\right)$ the density $\pi^t$ is given by $(\mathcal{T}_{\theta})^t \pi^0$ and 

$$\|\mathcal{T}_{\theta}f\|_1 = \dfrac{1}{m}\sum_{<i,j>\in E}\int_{[0,1]^n}\left| f(x)\delta_{A_{ij}^{\theta}}(x)dx + {\scriptstyle{\tfrac{f\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)}{1-2\mu}}}\delta_{\left(A_{ij}^{\theta}\right)^c}\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)\right|dx\\
	\qquad \leq  \dfrac{1}{m}\sum_{<i,j>\in E}\int_{[0,1]^n} |f(x)|\delta_{A_{ij}^{\theta}}(x) + \int_{[0,1]^n}{\scriptstyle{\tfrac{\left|f\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)\right|}{1-2\mu}}}\delta_{\left(A_{ij}^{\theta}\right)^c}\left(\left(\Phi_{ij}^{\mu}\right)^{-1}(x)\right)dx\\
	\qquad = \dfrac{1}{m}\sum_{<i,j>\in E}\int_{[0,1]^n} |f(x)|\delta_{A_{ij}^{\theta}}(x) + |f(x)|\delta_{\left(A_{ij}^{\theta}\right)^c}\left(x\right)dx\\
	\qquad = \int_{[0,1]^n} |f(x)|dx=\|f\|_1.$$

Considering the constant function $1(x)=1$ we obtain that $$\|\mathcal{T}_{\theta}\|=1$$. Consequently, the operator $$\mathcal{T}_{\theta}$$ is linear and continuous but not a contraction in the sense of the Banach fixed point theorem since the distance $$\|\|\mathcal{T}_{\theta} \delta - \mathcal{T}_{\theta} 0\|\|_1=1=\|\|\delta-0\|\|_1$$ is not decreasing. Additionally, this would imply that, independently of the initially chosen density, $$\left(\mathcal{T}_{\theta}\right)^n\pi^0$$ would converge to the same limit which is the constant $0$ and, therefore, not a probability density. We, consequently, focus subsequently on the more detailed structure of the densities of probability distributions and not only their role as a subset of $L^1\left([0,1]^n\right)$.  

**The manifold of probability densities and opinion paths**

We start this subsection by the observation that by equation \eqref{eq:Deffuant_density_recurrsion} the set of densities is invariant under $$\mathcal{T}_{\theta}$$, i.e., using

$$\partial B_1^+(0):=\{f\in L^1([0,1]^n)|\,||f||_1 = 1,\; f\geq 0\}$$

we have $$\mathcal{T}_{\theta}(\partial B_1^+(0))\subseteq \partial B_1^+(0)$$. Consequently, we can consider only the restriction of $$\mathcal{T}_{\theta}$$ to $$\partial B_1^+(0)$$ which we also call $$\mathcal{T}_{\theta}$$. This opens the doors to Information Geometry for our analysis. We aim at showing that by varying the parameters $$\theta,\mu$$ and applying iteratively the operator $$\mathcal{T}_{\theta}$$ we obtain a manifold structure $$\mathcal{M}$$ which can be seen as a statistical manifold. We, then, can define for any $$\pi\in \mathcal{M}$$ a sequence of paths $\left(\gamma_{\pi}^{(i)}\right)_{i=1}^{\infty}$ where $$\gamma_{\pi}^{(i)}:[0,1]\to \mathcal{M}$$ as

$$\gamma_{\pi}^{(1)}(t) = \mathcal{T}_{t\theta}\pi,\qquad \gamma_{\pi}^{(i)}(t)=\mathcal{T}_{t\theta}\left(\mathcal{T}_{\theta}^{i-1}\pi\right),\; i\geq 2.$$

We call the associated paths \textit{opinion paths} due to their representation of the process of changing opinions within the Deffuant model. Using an appropriate metric $$g$$ we go on to defining the length of a path $$\gamma:[0,1]\to\mathcal{M}$$ in $$(\mathcal{M}, g)$$ as it is done on any Riemannian manifold with metric $$g$$, see for example \cite{jost2017riemannian} by

$$	l_{\mathcal{M}}(\gamma):=\int_0^1 ||\gamma'(t)|| \mathrm{d}t := \int_0^1\sqrt{g_{\gamma(t)}\left(\frac{d\gamma}{dt},\frac{d\gamma}{dt}\right)}\mathrm{d}t.$$

Intuitively, if the length $$l_{\mathcal{M}}\left(\gamma_{\pi}^{(i)}\right)$$ of each $$\gamma_{\pi}^{(i)}$$ is decreasing sufficiently rapidly in $$i$$, such that $$\sum_{i=1}^{\infty} l_{\mathcal{M}}\left(\gamma_{\pi}^{(i)}\right)<\infty$$, then the sequence $$\left(\pi^{i}\right)_{i\in\mathbb{N}}$$ defined above converges to some limit, which is attained after a final distance in the manifold $\mathcal{M}$. 


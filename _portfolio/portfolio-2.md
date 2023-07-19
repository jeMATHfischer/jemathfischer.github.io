---
title: "The log grid and its measurements (ID: **LGM230517**)"
excerpt: "We consider the positive cone of the $d$-dimensional grid and apply to any vertex a logarithm, where the basis is at first irrelevant. We observe in the $2$-dimensional case that along the diagonal the cab driver distance of grid points converges to $0$ but the distance between points of the form $(a,x)$ and $(x,x)$ grow infinitely far appart as $x$ goes to infinity. The project is designed to investigate the implied geometry of the log grid."
collection: portfolio
---

What we call the **log grid** is simply the image of the grid $$\mathbb{Z}_+^d$$ under a logarithm, with the only assumption that its basis is a positive integer. So the definition is simply
$$l\mathbb{Z}_+^d := \lbrace \log(z) | \mathbb{Z}_+^d \rbrace$$
and a simple consequence from the construction is that $(0,...,0)\in l\mathbb{Z}_+^d$. To start, we consider its relation the underlying grid $$\mathbb{Z}_+^d$$. Note to this end, that two neighbors in $$\mathbb{Z}_+^d $$ always have distance $1$ in the $$L^1$$ norm. This pertains even for grid points with arbitrary large entries since they differ in at most one coordinate $x$ and the difference is $1$. For $$l\mathbb{Z}_+^d$$ this difference becomes $$\log(x+1)-\log(x) = \log(1+x^{-1})\to 0$$ as $x\to\infty$. Note that this limit always implies going along the same "horizontal" or "vertical" line to employ the illustrative terms from $2$ dimensions for which we present the following figure showin $$l\mathbb{Z}_+^d$$.    
<div style="text-align:center" ><img style="max-height:150%" src="/images/log_grid-1.png" /></div>
<br/>
Questions which could be of interest are the same as in differential geometry in terms of as embedded geometry in $$\mathbb{R}_+^d$$ or intrinsic geometry and discrete interpretations of curvature relativ to the "flat" $$\mathbb{Z}_+^d$$. We will focus on first step questions which concern the embedded geometry and the comparison with scalings and translations of $$\mathbb{Z}_+^d $$ of the form $$\alpha\cdot\mathbb{Z}_+^d +\beta$$ for $$\alpha > 0$$, $$\beta \in\mathbb{R}_*^d$$ with $$\exists i,j$$ such that $$\beta_i\neq \beta_j$$ or $$\beta=(0,...,0)$$. In this regard we want to answer the following questions:
- Characterize the values $$\alpha$$ such that $$\mathcal{Z}_d = l\mathbb{Z}_+^d \cap (\alpha\cdot\mathbb{Z}_+^d+\beta)$$ has size $n=2,3,4,...$.
- Find the symmetries of $$\mathcal{Z}_d$$ as structure embedded in $$\mathbb{R}_+^d$$.

In $$2$$ dimensions, we see by the picture and $$\beta=0$$, that the choices $$\alpha=\log(k)$$ and $$\alpha=\log(1+k^{-1})$$ for $$k\in\mathbb{N}$$ give always 
$$| \mathcal{Z}_d |=4$$ 
and $$\mathcal{Z}_d$$ is symmetric around the main axis 
$$\lbrace (l,l) | l\in\mathbb{N}\rbrace.$$ 
Other solutions with $$\beta \neq (0,...,0)$$ only have size $2$ and do not bear any particular symmetry aside from the fact that they lie on the same horizontal or vertical line.

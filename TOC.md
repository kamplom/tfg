# Abstract

Quantum Field Theory (QFT) is the naive approach to a Quantum Gravity (QG) theory, providing us with important results that guide us into the path to a proper Quantum Gravity theory.

One of such results is the ambiguity on the definition of a vacuum state when not in a flat space-time, giving famous results like the Casimir effect, Hawking radiation or particle creation with moving mirror.

In this work we will expose the key differences between doing QFT in flat versus curves space-times, showing why the vacuum definition is not universal in curved space-times, and describing the mathematical framework to quantificate it.

And in the spirit of showing and understanding the close relation of the above mentioned phenomena we will find a proper mirror trajectory to mimic Hawking thermal radiation from a black hole.

We will do so in a unidimensional, (1+1), Minkowski space-time with a massless scalar field and a moving mirror. Later we will consider the collapse of a null shell, also in (1+1), compute the particle creation and show the equivalence to the selected trajectory.

# Introduction
# Theoretical framework

## Klein-Gordon field
We simply grab some relativistic equation and shove in there some quantum operators, and the resulting equation may represent something.

We go for the equation
$$
\mathbf{p}^{2}c^{2}+m^{2}c^{4}=E^{2}
$$

because we already know it will work :) and quantizie it by swaping the momentum and energy by the momentum and energy operators
$$
\hat{\mathbf{p}}=-\hbar \nabla \ \text{ and } \ \hat{E}=i\hbar \frac{ \partial  }{ \partial t } 
$$
getting in natural units ($\hbar=c=1$)
$$
-\nabla^{2}\psi + m^{2}\psi = -\frac{ \partial^{2} }{ \partial t^{2} } \psi
$$
that is
$$
\frac{ \partial^{2} }{ \partial t^{2} } \psi -\Delta \psi+m^{2}\psi=0 = \Box\psi + m^{2}\psi
$$
### Klein-Gordon field Lagrangian density

Now we want to know the associated Lagrangian density of the KG field.
Compare the Klein-Gordon equation to the Euler-Lagrange equations:
$$
\begin{split}
&\partial_{\mu}\partial^{\mu}\phi+m^{2}\phi=0 \\
&\partial_{\mu}\left( \frac{ \partial \mathcal{L} }{ \partial (\partial_{\mu}\phi) }  \right)-\frac{ \partial \mathcal{L} }{ \partial \phi } =0
\end{split}

$$
so
$$
\pi=\partial^{\mu}\phi
$$
and thus
$$
\frac{ \partial \mathcal{L} }{ \partial \phi } =-m^{2}\phi
$$
with the Lagrangian density taking the form
$$
\mathcal{L}=-\frac{1}{2}m^{2}\phi^{2} + \mathcal{K}(\partial_{\mu}\phi,x^{\mu})
$$
Doing the same with the conjugated momentum
$$
\frac{ \partial \mathcal{L} }{ \partial (\partial_{\mu }\phi) } = \partial^{\mu}\phi
$$
note that although $\mu$ is a dummy index, we set it to be the same on both summatories and then we can remove one of the operators, that means is has to be the same on the equation above, whatever but the same. So the Lagrangian density will take the form
$$
\mathcal{L}=k\partial_{\mu}\phi\partial^{\mu}\phi + \mathcal{K}(\phi,x^{\mu}) = k\eta^{\mu \alpha}\partial_{\mu}\phi \partial_{\alpha}\phi + \mathcal{K}(\phi,x^{\mu})
$$
we note that the index $\mu$ is a dummy one, and to be able to differenciate we write it in the second form. Now we determine the value of the constant $k$
$$
\frac{ \partial \mathcal{L} }{ \partial (\partial_{\mu}\phi) } =k\frac{ \partial  }{ \partial (\partial_{\mu}\phi) } (\eta^{\nu \alpha}\partial_{\nu}\phi \partial_{\alpha}\phi) = k (\eta^{\nu \alpha}\delta^{\mu}_{\nu} \partial_{\alpha}+\eta^{\nu \alpha}\delta^{\mu}_{\alpha}\partial_{\nu})\phi=k(\eta^{\mu \alpha}\partial_{\alpha}+\eta^{\nu \mu}\partial_{\nu})\phi
$$
lastly note that $\alpha$ and $\nu$ are dummies so we can change them getting
$$\frac{ \partial \mathcal{L} }{ \partial (\partial_{\mu}\phi) }= k(\eta^{\mu \alpha}\partial_{\alpha}+\eta^{\mu\alpha}\partial_{\alpha})\phi=2k \eta^{\mu \alpha}\partial_{\alpha}\phi=2k\partial^{\mu}\phi$$
and by simply comparing we got that $k=\frac{1}{2}$. Therefore, with the two forms of the Lagrangian density and assuming it does not depend explicitly on the $x^{\mu}$, it is determined to be
$$
\mathcal{L}=\frac{1}{2}(\partial_{\mu}\phi \partial^{\mu}\phi-m^{2}\phi^{2})
$$
and indeed we obtain the Klein-Gordon equation if we apply the Euler-Lagrange to this Lagrangian density.

## QFT in flat space-time

The way to quantize our field and get a Hilbert and Fock spaces is to expand our field in positive and negative frequency modes. In general we will expand our field as
$$
\phi(x)=\sum_{i}\left[a_{i}\phi_{i}(x)+a^{\dagger}_{i}\phi^{*}_{i}(x)\right] 
$$
^51d1d4
where $a_{w}$ and $a^{\dagger}_{w}$ represent the creation and annihilation operators and $\phi_{w}$ and $\phi_{w}^{*}$ the different field modes.
We make such a split in a way that we get positive and negative frequency modes, that means, in the case of a flat space-time where $t$ represents the inertial time, that the partial derivatives with respect to our time for positive frequency modes are
$$
\partial_{t}\phi_{i}=-iw_{i}\phi_{i}
$$
and we define the value of $w_{i}$ to be the frequency for the *i*-th mode.
### Ladder operators and Canonical Commutation Relationships
The canonical quantisation process is simply treating the field as a quantum operator. Since we the modes can be seen as operators, it verifies the following commutators
$$
[\phi(t,\vec{x}),\pi(t,\vec{x}')]=i\delta(\vec{x}-\vec{x}')
$$
$$
[\phi(t,\vec{x}),\phi(t,\vec{x}')]=[\pi(t,\vec{x}),\pi(t,\vec{x})]=0
$$
where $\pi$ is simply the conjugated momentum of $\phi$
$$
\pi(t,\vec{x})=\frac{ \partial  }{ \partial t } \phi(t,\vec{x})
$$
This relations hold since we have an inertial time $t$ that defines the splitting into positive and negative frequencies and they imply that the operators $a_{w}$ and $a_{w}^{\dagger}$ verify the commutation relationships
$$
[a_{i},a_{j}^{\dagger}]=\delta_{ij}
$$
$$
[a_{i},a_{j}]=[a_{i}^{\dagger},a_{j}^{\dagger}]=0
$$
This means that we can expand our field in an assembly of harmonic oscillators, each one labelled by $i$ and with its own operators $a_{i}$ and $a_{i}^{\dagger}$.
### Klein-Gordon scalar product

The idea of constructing a Hilbert space may seem rather obvious at this point, looking that we are dealing with harmonic oscillators, so we shall define an internal product in the space of the 1-particle space, in a flat spacetime,
$$
\langle{\phi_{1}^{+}}, {\phi_{2}^{+}}\rangle:=\frac{i}{\hbar}\int_{\sum} \, d^{3}\mathbf{x}(\bar{\phi_{1}^{+}}\partial_{t}\phi^{+}_{2}-{\phi_{2}^{+}}\partial_{t}\bar{\phi^{+}_{1}})n^{t}   
$$
where $\sum$ is any space-like hypersurface and $n^{t}$ denotes a time-like vector normal to $\sum$. This is only a constant $t$ surface.This ensures that the result of the integral has the information for the whole  space-time, so $\sum$ is often referred as "initial data" surface.

The idea of the particular inner product is, first that the positive frequency modes form a complete orthonormal basis with respect it and, secondly, to be able torecover the function in momentum space with the inner product, in our case
$$
a(k)=\langle \phi^{+},e^{-ikx} \rangle 
$$

Then the positive or negative modes are an orthonormal basis for our Hilbert space, since they verify
$$
(\phi_{i},\phi_{j})=\delta_{ij}
$$
### Hilbert and Fock spaces

We can construct the one-particle Hilbert space based on the action of the creation operators onto the vacuum state $\ket{0}$. We may define the vacuum state as the one that verifies
$$
a_{i}\ket{0} =0
$$
and construct the rest of states as linear combinations of vectors
$$
\ket{n_{i}} =(n!)^{-1/2}(a_{i}^{\dagger})^{n}\ket{0} 
$$
resulting in a Hilbert space $\mathcal{H}$ for one particle.

We can construct the $m$ particle state by the action of $k$ independent creation operators upon the vacuum state
$$
\ket{n_{i_{1}}^{(1)},n_{i_{2}}^{(2)},\dots,n_{i_{m}}^{(m)}}=(n^{(1)!}n^{(2)}!\dots n^{(m)}!)^{-1/2}(a^{\dagger}_{i_{1}})^{n^{(1)}}(a^{\dagger}_{i_{2}})^{n^{(2)}}\dots (a^{\dagger}_{i_{m}})^{n^{(m)}}\ket{0} 
$$
which is the product of $m$ $\mathcal{H}$ spaces, $\mathcal{H}\otimes\dots \otimes \mathcal{H}$.

Then we define the Fock space as the direct sum of all the $m$ particle spaces,
$$
\mathcal{F}:=\mathbb{C}\oplus \mathcal{H} \oplus(\mathcal{H}\otimes \mathcal{H})\oplus(\mathcal{H}\otimes \mathcal{H}\otimes \mathcal{H})\oplus\dots \oplus(\mathcal{H}\otimes \mathcal{H}\otimes \dots \otimes \mathcal{H})\oplus\dots
$$

The above mentioned process holds for any inertial time we may choose, that is any time coordinate that preserves the Poincaré symmetry group. Furthermore, any of such times is related by a Poincaré transformation, leaving the vacuum state invariant and by extension the Fock space.

## QFT in curved space-time

In a curved space-time, we do not have a Poicaré symmetry group, so we do not have the notion of an inertial time. We need to generalise the notion of the time coordinate, by the introduction of the Killing time, and see the implications on the canonical quantisation procedure.

In the case of the absence of an inertial and Kiling time, we do not have a way to split our field in positive and frequency modes, since there is no variable that verifies the condition (). Then the relations () and () do not hold and therefore the annihilation and creation operators do not verify the CCR. Which this ultimately means is that we cannot define the notion of particle or vacuum the way we have done, with a Hilbert space.

### Fourier transform and Killing time

Consider a four dimensional pseudo-Riemannian manifold ($M$, $g$) and there is a $T\subset M$ such that it is a time-like Killing vector field. For our purposes we also need $T$ to be isomorphic to $\mathbb{R}$, since we want the metric $g$ to be the same function of it's argument on the whole space-time direction of $T$. If one is familiar with Lie algebra, this simply means that the Lie derivative of the metric tensor along a vector $\xi \in T$ is null:
$$
\mathcal{L}_{T}g=0
$$
We may write any point $x \in M$ as $x=(t,q)\in\mathbb{R} \times Q$ where $Q$ is simply the quocient manifold $Q=M / T$. Now since the Killing vector field is isomorphic to $\mathbb{R}$ and we parametrizate $M$ in terms of $t$, the action of the operator $\mathcal{L}_{T}$ is equivalent to $\partial_{t}$, hence $\partial_{t}g=0$. We refer now to $t$ as *Killing time* instead of inertial time.

So in general the volumetric differential element $\sqrt{|g(t,q)| }dtdq$ will be independent of $t$ provided that $T$ is a Killing vector field: $\sqrt{ |g(q)| }dtdq$.

Knowing this we may attempt to perform a Fourier transform or our Klein-Gordon field:
$$
\partial_{\mu}\partial^{\mu}\phi+m^{2}\phi=0
$$
as
$$
	\phi(x)=\int d^{4}k\sqrt{ |g(k)| }e^{i(k^{\nu}x_{\nu})}\tilde{\phi}(k) 
$$

If we apply the Klein-Gordon equation to the field decomposition we shall extract the form of the function $\tilde{\phi}(k)$, noting that the operator $\Box$ acts upon the variable $x$ and not $k$.
$$
(\partial_{\mu}\partial^{\mu}+m^{2})\phi(x)=(\partial_{\mu}\partial^{\mu}+m^{2})\int d^{4}k\sqrt{ |g(k)| }e^{ik^{\nu}x_{\nu}}\tilde{\phi}(k)= \int d^{4}k\sqrt{ |g(k)| }(m^{2}-k^{2})e^{ik^{\nu}x_{\nu}}\tilde{\phi}(k)=0 
$$
so we have that $(m^{2}-k^{2})\tilde{\phi}(k)=0, \ \forall k \in M$. Since $(m^{2}-k^{2})\delta(m^{2}-k^{2})=0$ we may write for some arbitrary function $h(x)$, $(m^{2}-k^{2})\tilde{\phi}(k)=0=(m^{2}-k^{2})\delta(m^{2}-k^{2})h(k)$, hence
$$
\tilde{\phi}(k)=\delta(m^{2}-k^{2})h(k)
$$
Now we shall find the roots for $m^{2}-k^{2}$ at $k^{0}=\pm w$ with $w=\sqrt{ m^{2}+\vec{k}^{2} }$ so we can expand the above Dirac delta
$$
\tilde{\phi}(k)=\frac{1}{2w}[\delta(k^{0}-w)+\delta(k^{0}+w)]h(k)
$$
so looking back at the transform for $\phi(x)$
$$
\phi(x)=\int d\vec{k}dk^{0}\sqrt{ |g(\vec{k})| }e^{ik^{\nu}x_{\nu}} \frac{1}{2w} [\delta(k^{0}-w)+\delta(k^{0}+w)]h(k) = \int \frac{d\vec{k}}{2w} \left[e^{iwt}e^{-i\vec{k}\vec{x}}h(w,\vec{k})\sqrt{ |g(\vec{k})| }+e^{-iwt}e^{-i\vec{k}\vec{x}}h(-w,\vec{k})\sqrt{ |g(\vec{k})| } \right] 
$$
because we integrate all over $Q$ we can swap $\vec{k}\to-\vec{k}$ on the second term and defining $a_{w}(k)= h(w,\vec{k})\sqrt{ |g(\vec{k})| }$ we finally get
$$
\phi(x)=\int \frac{d\vec{k}}{2w}\left[e^{iwt}e^{-i\vec{k}\vec{x}}a_{w}(k)+e^{-iwt}e^{-i\vec{k}\vec{x}}a_{w}^{\dagger}(k)\right] 
$$
so we can identify the positive frequency modes as $\phi_{w}(k)=e^{iwt}e^{-i\vec{k}\vec{x}}$ and the negative ones as $\phi_{w}^{-}=\phi_{w}^{+*}$ so
$$
\phi(x)=\int \frac{d\vec{k}}{2w}\left[\phi^{+}_{w}(k)a_{w}(k)+\phi^{-}_{w}(k)a_{w}^{\dagger}(k)\right] 
$$
And indeed if we do the Lie derivative, on on our case the equivalent partial with respect to $t$ we get
$$
\mathcal{L}_{T}\phi^{+}=\partial_{t}\phi^{+}=-iw\phi^{+}
$$
so the splitting defines well-behaved positive and negative frequency modes, because the independence of the metric determinant from $t$ allows us to perform the integral.

We have thus extended the concept of positive and negative frequency splitting to curved space-times provided they are stationary, that is, a time-like Killing vector field isomorphic to $\mathbb{R}$ exists. If such Killing vector field does not exist we cannot do the splitting [] in a way that gives positive and negative frequencies, hence the notion of particle does not exists in a natural way, since we cannot construct the Hilbert space using the ladder operators as we will see.

We can however define such mode expansions in a non-stationary space-time provided this are asymptotically stationary in the past (future), that is, in the limit $t\to-\infty$ ($t\to \infty$) the space-time can be regarded as stationary. We denote this region as the "in" ("out") region, and provides us with a natural sense of particle.

We denote as $\ket{in}$ ($\ket{out}$) with no particle, the vacuum state, in the "in" ("out") region. Looking at the $\ket{in}$ state through the operators of the "out" region allows us to quantify what we denote as "particle creation" in a process of a dynamical non-stationary space-time, such as the one with a moving mirror or a collapsing null-shell.
### Quantisation procedure

Otherwise, the procedure explained for the flat space-time is largely valid for the case of a curved space-time with a Killing vector field, but we have to addres a couple of formal details.

The Klein-Gordon equation has to be written in terms of covariant derivatives operators so
$$
\nabla_{\mu}\nabla^{\mu}\phi=\Box \phi=0
$$
where we define $\Box:=\nabla _\mu \nabla^{\mu}$ as the d'Alambert operator

We shall define the integration hypersurface of the inner product () as a Cauchy hypersurface
$$
\langle{\phi_{1}^{+}}, {\phi_{2}^{+}}\rangle:=\frac{i}{\hbar}\int_{\Sigma} \, d\Sigma^{\mu}(\bar{\phi_{1}^{+}}\nabla_{\mu}\phi^{+}_{2}-{\phi_{2}^{+}}\nabla_{\mu}\bar{\phi^{+}_{1}})   
$$
where $\Sigma$ is now a Cauchy hypersurface and $d\Sigma^{\mu}=d\Sigma n^{\mu}$, with $d\Sigma$ being the volume element and $n^{\mu}$ the future directed unit vector normal to $\Sigma$. 

Cauchy hypersurface: what it is, generalisation of constant t, initial data surface + figure


### Bogolubov transformations

As mentioned at the end of section () the mode expansion may not be unique in a curved space-time, so we need to relate two physically meaningful expansions by the means of what is known as a Bogolubov transformation. We will proceed by relating the expansions in "in" and "out" modes, but this will work for any other pair.

Since the both expansions are a complete orthonormal basis of the Fock space one can expand some $\phi_{i}^{out}$ mode as a combination of $\phi_{i}^{in}$ and $\phi_{i}^{in*}$ modes,
$$
\phi_{j}^{out}=\sum_{i}(\alpha_{ji}\phi_{i}^{in}+\beta_{ji}\phi_{i}^{in*})
$$
Note that an "out" mode may not be a combination of "in" positive frequency modes, but also possibly negative frequency ones.



The matrices $\alpha_{ji}$ and $\beta_{ji}$ are known as Bogolubov coefficients, and can be computed as
$$
\alpha_{ij}=(\phi_{i}^{out},\phi_{j}^{in}),\ \ \beta_{ij}=-(\phi_{i}^{out},\phi_{j}^{in*})
$$
since the modes are orthonormal,
$$
(u_{i}^{in},u_{j}^{in})=\delta_{ij}, \ (u_{i}^{in*},u_{j}^{in*})=-\delta_{ij}, \ (u_{i}^{in},u_{i}^{in*})=0
$$
As mentioned earlier (), $a_{i}^{in}=(\phi,\phi_{i}^{in})$, and analogly for "out", so the operators are related by the Bogolubov coefficients as,
$$
a_{i}^{in}=\sum_{j}(\alpha_{ji}a_{j}^{out}+\beta^{*}_{ji}a_{j}^{out\dagger})
$$
So the action of the "in" annihilation operator upon the "out" vacuum state
$$
a^{in}_{i}\ket{out}=\sum_{j}(\alpha_{ji}a_{j}^{out}+\beta^{*}_{ji}a_{j}^{out\dagger})\ket{out}= \sum_{j}\beta^{*}_{ji}a_{j}^{out\dagger}\ket{out}
$$
which is in general not equal to zero if the Bogolubov beta coefficients are different from zero.
We can define the "out" particle number operator as
$$
N_{i}^{out}=a_{i}^{out\dagger}a_{i}^{out}
$$
and apply it to the "in" vacuum state to get
$$
\bra{in} N_{i}^{out}\ket{in} =\sum_{j}|\beta_{ij}|^{2} 
$$
We can see that the $\alpha_{ji}$ Bogolubov coefficients do not appear on the above expression () nor on the (), which means that the $\alpha$ matrix relates the "in" and "out" states by a transformation that preserves the inner product. Indeed
$$
\sum_{k}\alpha_{ik}\alpha_{kj}^{*}=\delta_{ij}
$$
if $\beta_{ij}=0, \forall i,j$, and therefore $\ket{in}=\ket{out}$.

This leaves us with an ambiguous definition of vacuum state since it depends on our choice of Killing time $t$, where the vacuum state in one expansion can contain particles in another one.

When the "out" vacuum state,$\ket{out}$, is not equivalent to the "in" vacuum state, $\ket{in}$, we say that there has been "particle creation" since the quantity () will not be zero. In general any phenomena that makes this two differ is said to create particles or radiation.

# Particle creation with accelerated mirrors

## Mode expansion and null coordinates

Consider once more the expansion
$$
\phi(x)=\int \frac{dw}{w}\left[a_{w}\phi_{w}(x)+a^{\dagger}_{w}\phi^{*}_{w}(x)\right] 
$$
in the case of a flat empty space-time the solutions will simply be field modes that propagate along null geodesics, that is $t+x$ and $t-x$,
$$
\phi_{w}=\frac{1}{\sqrt{ 4\pi w }}e^{-iw(t+x)}, \phi_{w}^{*}=\frac{1}{\sqrt{ 4\pi w }}e^{iw(t+x)}
$$
for left moving modes with positive and negative frequency respectively, and
$$
\phi_{w}=\frac{1}{\sqrt{ 4\pi w }}e^{-iw(t-x)}, \phi_{w}^{*}=\frac{1}{\sqrt{ 4\pi w }}e^{iw(t-x)}
$$
for left moving modes with positive and negative frequency respectively.

It is natural to work in null coordinates, $u=t-x$ and $v=t+x$. The Klein-Gordon for a massless scalar equation becomes
$$
\frac{ \partial  }{ \partial u } \left(\frac{ \partial \phi(u,v) }{ \partial v }\right) =\partial_{u}\partial_{v}\phi(u,v)=0
$$
and the modes take the form
$$
\phi_{w}=\frac{1}{\sqrt{ 4\pi w }}e^{-iwv}, \phi_{w}^{*}=\frac{1}{\sqrt{ 4\pi w }}e^{iwv}
$$
for left moving modes with positive and negative frequency respectively, and
$$
\phi_{w}=\frac{1}{\sqrt{ 4\pi w }}e^{-iwu}, \phi_{w}^{*}=\frac{1}{\sqrt{ 4\pi w }}e^{iwu}
$$
for left moving modes with positive and negative frequency respectively.

For the computation of the scalar product it is useful to consider the Cauchy surfaces conformed by the null infinites, $\mathcal{I}^{-}=\mathcal{I}^{-}_{L}\cup \mathcal{I}^{-}_{R}$ and $\mathcal{I}^{+}=\mathcal{I}^{+}_{L}\cup \mathcal{I}^{+}_{R}$. This surfaces can be parametrizated by setting one of $u$ or $v$ to $\infty$ or $-\infty$, for example, $\mathcal{I}^{-}_{L}$ is characterised by $v=-\infty$.
So for $\mathcal{I}^{-}=\mathcal{I}^{-}_{L}\cup \mathcal{I}^{-}_{R}$ we have the form
$$
(\phi_{w},\phi_{w'})=i \int_{-\infty}^{\infty}  \, du \phi^{*}_{w'}(u,v=-\infty)\overleftrightarrow{\partial_{u}}\phi_{w}(u,v=-\infty)+i\int_{-\infty}^{\infty}  \, dv \phi^{*}_{w'}(u=-\infty,v)\overleftrightarrow{\partial_{u}}\phi_{w}(u=-\infty,v) 
$$
So the first integral vanishes for left moving modes and the second vanishes for right moving ones.

## The mirror problem

We are now in a position to describe the moving mirror problem. Consider a mirror moving in a two dimensional Minkowsky space-time with a given trajectory
$$
x=z(t),\ \ |\dot{z}(t)|<1
$$
Then, on the region on the right of the mirror $(x>z(t))$, we consider a Klein-Gordon field, that is a massless scalar field.
In two dimensions the Klein-Gordon equation
$$
\frac{ \partial^{2}\phi }{ \partial t^{2} } - \frac{ \partial^{2}\phi }{ \partial x^{2} } =0
$$
is verified on the above mentioned region, and we have the Dirichlet boundary condition
$$
\phi(t,z(t))=0
$$
since the mirror is a reflective surface.
## Klein-Gordon field and positive frequency modes

Consider a conformal transformation to the null coordinates,
$$

\partial_{u}\partial_{v}\phi(u,v)=0
$$
and
$$
\phi(t-z(t),t+z(t))=0
$$
where $\phi$ is expressed as a function of $(u,v)$ and not as $(x,t)$, that is is not the same function of its argument.

We expand our field in both the "in" and "out" regions
$$
\phi(u,v)=\frac{1}{4\pi}\int  \, \frac{dw}{w} [a_{w}^{out}\phi_{w}^{out}(u,v)+a^{out\dagger}_{w}\phi^{out*}_{w}(u,v)] =\frac{1}{4\pi}\int  \, \frac{dw}{w} [a_{w}^{in}\phi_{w}^{in}(u,v)+a^{in\dagger}_{w}\phi^{in*}_{w}(u,v)]
$$

The imposed boundary condition will modify the form of the solutions shown for the case of an empty Minkowski space-time. The solution will still be left-moving plane waves for the "in" region,
$$
\phi_{w}^{in}(u,v)=e^{-iwv}-e^{-iwp(u)}
$$
or right-moving plane waves for the "out" region, where the radiation has "bounced" from the mirror
$$
\phi_{w}^{out}(u,v)=e^{-iwf(v)}-e^{-wu}
$$
$f(v)$ and $p(u)$ are each other inverse function, but $f(v)$ is singular on the event horizon $v=v_{0}$, while $p(u)$ is real for for all values of $u$, so it is preferred.

$f(v)$ and $p(u)$ are known as ray-tracing functions, because $p(u)$ describes the world-line of the radiation coming from $\mathcal{I}^{-}_{R}$ and bouncing off the mirror into to head into $\mathcal{I}^{+}_{R}$. And $f(v)$ traces backwards in time the radiation that has arrived to $\mathcal{I}^{+}_{R}$ back to $\mathcal{I}^{-}_{R}$.

The approach taken does not work if some radiation *never* reaches the mirror, that is, the mirror has an asymptotically null trajectory forming an event horizon at $v=v_{0}$. Then some of the radiation coming from $\mathcal{I}^{-}_{R}$ never reaches $\mathcal{I}^{+}_{R}$ and goes to $\mathcal{I}_{L}^{+}$, which means that the $\phi_{w}^{out}$ solution is incomplete.

As we will see, the radiation that never reaches the mirror is equivalent to the one trapped by the black-hole, that goes trough the event horizon, so we are not specially interested since we want to get a thermal bath equivalent to the Hawking radiation, which will be described by the mode solution exposed

We will then proceed with the exposed methodology because of the simplicity of calculus. It is not new to consider such radiation, on [] the method is well described and by considering two out modes, one for each part of $\mathcal{I}^{+}$, $\phi_{w}^{outL}$ and $\phi_{w}^{outR}$ it reaches an integration over an actual Cauchy surface and a complete basis for the algebra. That is outside the scope of this work, and our approach will allow us to get the relevant Bogolubov coefficient to obtain the desired result.
## Bogolubov coefficients

The beta Bogolubov coefficients
$$
\beta_{w'w}=i \int _{-\infty}^{\infty} \, du\phi_{w'}^{in*}(u,v=\infty)\overleftrightarrow{\partial_{u}}\phi_{w}^{out*}(u,v=\infty)=(4\pi \sqrt{ ww' })^{-1}\int _{-\infty}^{\infty} \, due^{iwu}e^{iw'p(u)}(w'p'(u)-w) 
$$

and the number of particle created
$$
\langle N_{w}\rangle = \bra{in} N^{out}_{w}\ket{in} =  \int _{0}^{\infty} \, |\beta_{ww'}|^{2}dw' 
$$
This integral however diverges for a mirror that accelerates indefinitely, so some sort of localisation process has to be introduced by the means of wave packets.
## Wave packets and temperature calculation

To get partial frequency and time resolution, we modulate the amplitude of our plane wave so it has a sharp peak around a time instant, as
$$
\phi_{jn}(u,v)=\frac{1}{\sqrt{ \epsilon  }}\int _{j\epsilon}^{(j+1)\epsilon} \, dwe^{2\pi iwn/\epsilon}\phi_{w}(u,v)
$$
Graph of a packet.

The physical meaning of this quantity is clear, it represents what a detector would see if turned on during a period of time of $2\pi/\epsilon$, at the time $2\pi n/\epsilon$ sensible to frequencies between $\pm\epsilon/2$. If $\epsilon$ is sufficiently small the frequency may be approximated as constant by $w\approx w_{j}=(j+1/2)\epsilon$.

We may define this process as *packetization* and assign it an operator
$$
\widehat{P_{jn}}^{\pm}:=\frac{1}{\sqrt{ \epsilon }}\int _{j\epsilon}^{(j+1)\epsilon} \, dwe^{\pm2\pi iwn/\epsilon} 
$$
so that [] is simply $\phi_{jn}=\widehat{P_{jn}}^{+}\phi_{w}$.

The Bogolubov coefficients will change with the same operator but with oposite sign as shown in [] that is $\widehat{P_{jn}}^{\pm}\phi _{w}\iff \widehat{P_{jn}}^{\mp}\beta_{ww'}$. So the packetizated Bogolubov coefficient
$$
\beta_{jn,w'}=\widehat{P_{jn}}^{+}\beta_{ww'}=\frac{1}{\sqrt{ \epsilon }}\int _{j\epsilon}^{(j+1)\epsilon} \, dwe^{2\pi iwn/\epsilon}\beta_{ww'}
$$
We can lastly compute the expected number of particles as
$$
\langle N_{jn} \rangle =\int _{0}^{\infty} \, |\beta_{jn,w'}|^{2}dw' 
$$
explain what this number is.

## Inertial trajectory
$\beta_{ww'}=0$
## Carlitz-Wiley trajectory

In their paper CW looked for a trajectory that has a thermal spectre for all times. This is a rather courius trajectory and their approach was to get a function $p(u)$ that gave the appropiated Bogolubov coefficient for an always thermal radiation.

In the paper the explicit form of the trajectory is not mentioned, and they only give the corresponding $p(u)$
$$
p(u)=-\frac{1}{\kappa}e^{-\kappa u}
$$
by inverting it one find the explicit form of the trajectory to be
$$
z(t)=-t-\frac{1}{\kappa}W(e^{-2\kappa t})
$$
where $W$ is the Lambert W function.

We will describe some properties of the trajectory since it is very closely related to the Hawking radiation from a black hole. As mentioned the trajectory has a future horizon at $v=v_{0}=0$, so the particles that never reach the mirror will reach the accessible part of $\mathcal{I}^{+}_{L}$, that goes from $v=0$ to $v=\infty$. In the analogy with a black hole this are the particles that fall into it, and we are not interested in them as of now, so our solution $\phi_{w}^{out}$ will only consist of the particles that are actually reflected by the mirror. It does not preset a past horizon and since it radiates thermally for all time we expect a constant energy flux.

By using eq () we obtain $\beta_{ww'}$
$$
\beta_{ww'}=\frac{1}{4\pi \sqrt{ ww'}}\left[ -\frac{2w}{\kappa}e^{-\pi w/2\kappa} \left( \frac{w'}{\kappa} \right)^{iw/\kappa}\Gamma\left( -\frac{iw}{\kappa} \right)\right]
$$

which is indeed the $\beta_{ww'}^{R}$ from the CW construction, and by packetazing it
$$
\beta_{jn,w'}=\widehat{P_{jn}}^{+}\beta_{ww'}=\frac{1}{\sqrt{ \epsilon }}\int _{j\epsilon}^{(j+1)\epsilon} \, dwe^{\pm2\pi iwn/\epsilon}\beta_{ww'}
$$
giving
$$
\langle N_{jn} \rangle = \int _{0}^{\infty} \, |\beta_{jn,w'}|^{2}dw'=\frac{\kappa}{2\pi\epsilon}\ln{\left(\frac{{e^{2\pi(j+1)\epsilon/\kappa}}-1}{{e^{2\pi(j)\epsilon/\kappa}}-1}\right)}-1
$$
Note that $\langle N_{jn} \rangle$ is independent of $n$, thus independent of time. This is because for the CW trajectory the mirror radiates thermally at a constat temperature for all times, so no matter when we turn on our detector, the expected number of particles is always the same.

In the limit where $\epsilon$ is small, the expression can be approximated by
$$
\langle N_{jn} \rangle =\frac{1}{e^{2\pi w_{j}/\kappa}-1}
$$
where $w_{j}=(j+\frac{1}{2})\epsilon$ is the value where the wavepackets peak.

This is a Planck spectrum with a temperature of $T=\kappa/2\pi$.

Graph comparing aproximation with different values for $\epsilon$.

# Hawking radiation

We shall see that the quantitative description of Hawking black hole radiation may be desribed in the same mathematical formalism developed for the moving mirror problem. It will not be shown to a quantitative extend but rather in a qualitative way, to grasp the idea and comprenhend the result. For more details see ().
## Two dimensional collapsing null-shell

Consider a two dimensional (1+1) space time, parametrizated by the null coordinates $u=t-x$ and $v=t+x$. 

We are not interested in the collapse itslef but the "in" and "out" regions, so we consider an ingoing radiation flux at $v=v_{0}$ that generates a black hole of mass $M$ in an instantaneous fashion. We refer this as a "shock wave". This means that the mass is null before the shock wave and $M$ after, so
$$
M(v)=M\theta(v-v_{0})
$$
Before the collapse we have an space with a Minkoswki metric, and after it we have a region with a Schwarchild metric. This means that the mode solutions for a field $\phi$ will be different in the two regions.

As before this means we have a non-trivial Bogolubov transformation. The corresponding ray tracing function $f(v)$ from (), as shown in (), is
$$
f(v)=-\kappa^{-1}\ln(\kappa(v-v_{0}))
$$
valid in the region $v<v_{0}$.
## Bogoluvob coefficients

As with the mirror model we will disregard the solution in the region $v<v_{0}$, since we are not going to compute correlation functions between trapped and escaping radiation, so we will compute the Bogolubov coefficient at $\mathcal{I}^{-}$ with our function $f(v)$. Otherwise we should analytically extend the function $f(v)$ into the region $v>v_{0}$.

Using equation ()
$$
\beta_{ww'}=-\frac{2M\sqrt{ ww' }}{\pi(w+w')}e^{-i(w+w')v_{0}}\left[-4Mi(w+w')\right]^{-4Mwi}\Gamma(4Mwi)
$$

## Particle creation. Wave packets and temperature calculation

In the same way that with the mirror we packetize our coefficient and integrate to get a plack spectrum approximated for late times
$$
\langle N_{jn} \rangle 
$$
with a temperature
$$
T
$$
# Conclusion

First part: no universlity of vacuum. same physical character of diverse phenomena

Mirror trajectory as a the way to go to explore the quantum gravity solutions for black hole.
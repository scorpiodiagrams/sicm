!!Polyglot
## Canonical Perturbation Theory
### Chapter 7
#page(457)
#Quote(Having treated the motion of the moon about the earth, and having obtained an elliptical orbit, [Newton] considered the effect of the sun on the moon's orbit by taking into account the variations of the latter. However, the calculations caused him great difficulties ... Indeed, the problems he encountered were such that [Newton] was prompted to remark to the astronomer John Machin that “... his head never ached but with his studies on the moon.” )

#Caption June Barrow-Green, /Poincaré and the Three Body Problem/ [7](bibliography!bib_7), [p.15](chapter001!p15)

Closed-form solutions of dynamical systems can be found only rarely. However, some systems differ from a solvable system by the addition of a small effect. The goal of perturbation theory is to relate aspects of the motion of the given system to those of the nearby solvable system. We can try to find a way to transform the exact solution of this approximate problem into an approximate solution to the original problem. We can also use perturbation theory to try to predict qualitative features of the solutions by describing the characteristic ways in which solutions of the solvable system are distorted by the additional effects. For instance, we might want to predict where the largest resonance regions are located or the locations and sizes of the largest chaotic zones. Being able to predict such features can give insight into the behavior of the particular system of interest. 

Suppose, for example, we have a system characterized by a Hamiltonian that breaks up into two parts as follows:

$$\begin{matrix} {H = H_{0} + \mathit{\epsilon}H_{1},} \tag{7.1} \\ \end{matrix}$$

where /H/_{0} is solvable and /ϵ/ is a small parameter. The difference between our system and a solvable system is then a small additive complication.

#page(458)

There are a number of strategies for doing this. One strategy is to seek a canonical transformation that eliminates from the Hamiltonian the terms of order /ϵ/ that impede solution---this typically introduces new terms of order /ϵ/^{2}. Then one seeks another canonical transformation that eliminates the terms of order /ϵ/^{2} impeding solution, leaving terms of order /ϵ/^{3}. We can imagine repeating this process until the part that impedes solution is of such high order in /ϵ/ that it can be neglected. Having reduced the problem to a solvable problem, we can reverse the sequence of transformations to find an approximate solution of the original problem. Does this process converge? How do we know we can ever neglect the remaining terms? Let's follow this path and see where it goes.

### 7.1 Perturbation Theory with Lie Series
Given a system, we look for a decomposition of the Hamiltonian in the form

$$\begin{matrix} {H\left( {t,q,p} \right) = H_{0}\left( {t,q,p} \right) + \mathit{\epsilon}H_{1}\left( {t,q,p} \right),} \tag{7.2} \\ \end{matrix}$$

where /H/_{0} is solvable. We assume that the Hamiltonian has no explicit time dependence; this can be ensured by going to the extended phase space if necessary. We also assume that a canonical transformation has been made so that /H/_{0} depends solely on the momenta: 

$$\begin{matrix} {\partial_{1}H_{0} = 0.} \tag{7.3} \\ \end{matrix}$$

We carry out a Lie transformation and find the conditions that the Lie generator /W/ must satisfy to eliminate the order /ϵ/ terms from the Hamiltonian.

The Lie transform and associated Lie series specify a canonical transformation:

$$\begin{array}{rll} {H\prime} & {= E_{\mathit{\epsilon},W}^{\prime}H = e^{\mathit{\epsilon}L_{W}}H} & \\ q & {= {({E_{\mathit{\epsilon},W}^{\prime}Q})}{({t,q\prime,p\prime})} = {({e^{\mathit{\epsilon}L_{W}}Q})}{({t,q\prime,p\prime})}} & \\ p & {= {({E_{\mathit{\epsilon},W}^{\prime}P})}{({t,q\prime,p\prime})} = {({e^{\mathit{\epsilon}L_{W}}P})}{({t,q\prime,p\prime})}} & \\ {({t,q,p})} & {= {({E_{\mathit{\epsilon},W}^{\prime}I})}{({t,q\prime,p\prime})} = {({e^{\mathit{\epsilon}L_{W}}I})}{({t,q\prime,p\prime})},} \tag{7.4} \\ \end{array}$$

#page(459)

where /Q/ = /I/_{1} and /P/ = /I/_{2} are the coordinate and momentum selectors and /I/ is the identity function. Recall the definitions

$$\begin{array}{lll} {e^{\mathit{\epsilon}L_{W}}F} & {= F + \mathit{\epsilon}L_{W}F + \frac{1}{2}\mathit{\epsilon}^{2}L_{W}^{2}F + \cdots} & \\ & {= F + \mathit{\epsilon}\left\{ {F,W} \right\} + \frac{1}{2}\mathit{\epsilon}^{2}\left\{ {\left\{ {F,W} \right\},W} \right\} + \cdots,} \tag{7.5} \\ \end{array}$$

with /L_{W}F/ = {F, /W/ }.

Applying the Lie transformation to /H/ gives us

$$\begin{array}{lll} {H\prime} & {= e^{\mathit{\epsilon}L_{W}}H} & \\ & {= H_{0} + \mathit{\epsilon}L_{W}H_{0} + \frac{1}{2}\mathit{\epsilon}^{2}L_{W}^{2}H_{0} + \cdots} & \\ & {\text{           } + \mathit{\epsilon}H_{1} + \mathit{\epsilon}^{2}L_{W}H_{1} + \cdots} & \\ & {= H_{0} + \mathit{\epsilon}\left( {L_{W}H_{0} + H_{1}} \right) + \mathit{\epsilon}^{2}\left( {\frac{1}{2}L_{W}^{2}H_{0} + L_{W}H_{1}} \right) + \cdots.} \tag{7.6} \\ \end{array}$$

The first-order term in /ϵ/ is zero if /W/ satisfies the condition

$$\begin{matrix} {L_{W}H_{0} + H_{1} = 0,} \tag{7.7} \\ \end{matrix}$$

which is a linear partial differential equation for /W/. The transformed Hamiltonian is

$$\begin{array}{lll} {H\prime} & {= H_{0} + \mathit{\epsilon}^{2}\left( {\frac{1}{2}L_{W}^{2}H_{0} + L_{W}H1} \right) + \cdots} & \\ & {= H_{0} + \frac{1}{2}\mathit{\epsilon}^{2}L_{W}H_{1} + \cdots,} \tag{7.8} \\ \end{array}$$

where we have used condition (#Eqn(chapter007,7.7,7.7)) to simplify the /ϵ/^{2} contribution.

This basic step of perturbation theory has eliminated terms of a certain order (order /ϵ/) from the Hamiltonian, but in doing so has generated new terms of higher order (here /ϵ/^{2} and higher).

At this point we can find an approximate solution by truncating Hamiltonian (#Eqn(chapter007,7.8,7.8)) to /H/_{0}, which is solvable. The approximate solution for given initial conditions /s/_{0} = (/t/_{0}, /q/_{0}, /p/_{0}) is obtained by finding the corresponding $\left( {t_{0},q_{0}^{\prime},p_{0}^{\prime}} \right)$ using the inverse of transformation (#Eqn(chapter007,7.4,7.4)). Then the system is evolved to time /t/ using the solutions of the truncated Hamiltonian /H/_{0}, giving the state (/t/, /q/′, /p/′). The phase-space coordinates of the evolved point are transformed back to the original variables using the transformation (#Eqn(chapter007,7.4,7.4)) to
#page(460)
state /s/ = (/t/, /q/, /p/). The approximate solution is

$$\begin{array}{lll} s & {= \left( {\left( {E_{\mathit{\epsilon},W}^{\prime}I} \right) \circ \left( {E_{t - t_{0},H_{0}}I} \right) \circ \left( {E_{- \mathit{\epsilon},W}^{\prime}I} \right)} \right)\left( s_{0} \right)} & \\ & {= \left( {E_{- \mathit{\epsilon},W}^{\prime}E_{t - t_{0},H_{0}}E_{\mathit{\epsilon},W}^{\prime}I} \right)\left( s_{0} \right)} & \\ & {= \left( {e^{- \mathit{\epsilon}L_{W}}e^{{({t - t_{0}})}D_{H_{0}}}e^{\mathit{\epsilon}L_{W}}I} \right)\left( s_{0} \right),} \tag{7.9} \\ \end{array}$$

using the identity (#Eqn(chapter006,6.111,6.111)). Notice that the time evolution of /H/_{0} is expressed in terms of the evolution operator /E/ rather than the Lie-transform operator /E/′, because the time must also be advanced. The power-series expansion for $ E_{\Delta t,H_{0}}$ is expressed in terms of $ D_{H_{0}}$ rather than $ L_{H_{0}}$(see #Eqn(chapter006,6.136,6.136)). If the Lie transform $ E_{\mathit{\epsilon},W}^{\prime} = e^{\mathit{\epsilon}L_{W}}$ must be evaluated by summing the series, then we must specify the order to which the sum extends.

Assuming everything goes okay, we can imagine repeating this process to eliminate the order /ϵ/^{2} terms and so on, bringing the transformed Hamiltonian as close as we like to /H/_{0}. Unfortunately, there are complications. We can understand some of these complications and how to deal with them by considering some specific applications.

### 7.2 Pendulum as a Perturbed Rotor
The pendulum is a simple one-degree-of-freedom system, for which the solutions are known. If we consider the pendulum as a free rotor with the added complication of gravity, then we can carry out a perturbation step as just described to see how well it approximates the known motion of the pendulum.

The motion of a pendulum is described by the Hamiltonian

$$\begin{matrix} {H\left( {t,\theta,p} \right) = \frac{p^{2}}{2\alpha} - \mathit{\epsilon}\beta\cos\left( \theta \right),} \tag{7.10} \\ \end{matrix}$$

with coordinate /θ/ and conjugate angular momentum /p/, where /α/ = /ml/^{2} and /β/ = /mgl/. The parameter /ϵ/ allows us to scale the perturbation; it is 1 for the actual pendulum. We divide the Hamiltonian into the free-rotor Hamiltonian and the perturbation from gravity:

$$\begin{matrix} {H = H_{0} + \mathit{\epsilon}H_{1},} \tag{7.11} \\ \end{matrix}$$

#page(461)

where

$$\begin{array}{rll} {H_{0}\left( {t,\theta,p} \right)} & {= \frac{p^{2}}{2\alpha}} & \\ {\mathit{\epsilon}H_{1}\left( {t,\theta,p} \right)} & {= - \mathit{\epsilon}\beta\cos\theta.} \tag{7.12} \\ \end{array}$$

The Lie generator /W/ satisfies condition (#Eqn(chapter007,7.7,7.7)):

$$\begin{matrix} {\left\{ {H_{0},W} \right\} + H_{1} = 0,} \tag{7.13} \\ \end{matrix}$$

or

$$\begin{matrix} {- \frac{p}{\alpha}\partial_{1}W\left( {t,\theta,p} \right) - \beta\cos\theta = 0.} \tag{7.14} \\ \end{matrix}$$

So

$$\begin{matrix} {W\left( {t,\theta,p} \right) = - \frac{\alpha\beta\sin\theta}{p},} \tag{7.15} \\ \end{matrix}$$

where the arbitrary integration constant is ignored.

The transformed Hamiltonian is /H/′ = /H/_{0} + /o/(/ϵ/^{2}). If we can ignore the /ϵ/^{2} contributions, then the transformed Hamiltonian is simply

$$\begin{matrix} {H\prime\left( {t,\theta\prime,p\prime} \right) = \frac{\left( p\prime \right)^{2}}{2\alpha},} \tag{7.16} \\ \end{matrix}$$

with solutions

$$\begin{array}{lll} {\theta\prime} & {= \theta_{0}^{\prime} + \frac{p_{0}^{\prime}}{\alpha}\left( {t - t_{0}} \right)} & \\ {p\prime} & {= p_{0}^{\prime}.} \tag{7.17} \\ \end{array}$$

To connect these solutions to the solutions of the original problem, we use the Lie series

$$\begin{array}{lll} \theta & {= \left( {e^{\mathit{\epsilon}L_{W}}Q} \right)\left( {t,\theta\prime,p\prime} \right)} & \\ & {= \theta\prime + \mathit{\epsilon}\left\{ {Q,W} \right\}\left( {t,\theta\prime,p\prime} \right) + \cdots} & \\ & {= \theta\prime + \mathit{\epsilon}\partial_{2}W\left( {t,\theta\prime,p\prime} \right) + \cdots} & \\ & {= \theta\prime + \mathit{\epsilon}\frac{\alpha\beta\sin\theta\prime}{\left( p\prime \right)^{2}} + \cdots.} \tag{7.18} \\ \end{array}$$

#page(462)

Similarly,

$$\begin{matrix} {p = p\prime + \mathit{\epsilon}\frac{\alpha\beta\cos\theta\prime}{p\prime} + \cdots.} \tag{7.19} \\ \end{matrix}$$

Note that if the Lie series is truncated it is not exactly a canonical transformation; only the infinite series is canonical.

The initial values $\theta_{0}^{\prime}$ and $ p_{0}^{\prime}$ are determined from the initial values of /θ/ and /p/ by the inverse Lie transformation:

$$\begin{array}{lll} {\theta\prime} & {= \left( {e^{- \mathit{\epsilon}L_{W}}Q} \right)\left( {t,\theta,p} \right)} & \\ & {= \theta - \mathit{\epsilon}\frac{\alpha\beta\sin\theta}{\left( p \right)^{2}} + \cdots} \tag{7.20} \\ \end{array}$$

and

$$\begin{matrix} {p\prime = p - \mathit{\epsilon}\frac{\alpha\beta\cos\theta}{p} + \cdots.} \tag{7.21} \\ \end{matrix}$$

Note that if we truncate the coordinate transformations after the first-order terms in /ϵ/ (or any finite order), then the inverse transformation is not exactly the inverse of the transformation.

The approximate solution for given initial conditions (/t/_{0}, /θ/_{0}, /p/_{0}) is obtained by finding the corresponding $\left( {t_{0},\theta_{0}^{\prime},p_{0}^{\prime}} \right)$ using the transformation (#Eqn(chapter007,7.20,7.20)) and (#Eqn(chapter007,7.21,7.21)). Then the system is evolved using the solutions (#Eqn(chapter007,7.17,7.17)). The phase-space coordinates of the evolved point are transformed back to the original variables using the transformation (#Eqn(chapter007,7.18,7.18)) and (#Eqn(chapter007,7.19,7.19)).

We define the two parts of the pendulum Hamiltonian:
```Scheme
(define ((H0 alpha) state) (let ((p (momentum state))) (/ (square p) (* 2 alpha)))) (define ((H1 beta) state) (let ((theta (coordinate state))) (* -1 beta (cos theta)))) 
```
The Hamiltonian for the pendulum can be expressed as a series expansion in the parameter /ϵ/ by
```Scheme
(define (H-pendulum-series alpha beta epsilon) (series (H0 alpha) (* epsilon (H1 beta)))) 
```
where the series procedure is a constructor for a series whose first terms are given and all further terms are zero. The Lie generator that eliminates the order /ϵ/ terms is
```Scheme
(define ((W alpha beta) state) (let ((theta (coordinate state)) (p (momentum state))) (/ (* -1 alpha beta (sin theta)) p))) 
```
We check that W satisfies condition (#Eqn(chapter007,7.7,7.7)):
```Scheme
((+ ((Lie-derivative (W 'alpha 'beta)) (H0 'alpha)) (H1 'beta)) (up 't 'theta 'p)) 
```
```Scheme
0 
```
and that it has the desired effect on the Hamiltonian:
```Scheme
(show-expression (series:sum (((exp (* 'epsilon (Lie-derivative (W 'alpha 'beta)))) (H-pendulum-series 'alpha 'beta 'epsilon)) (up 't 'theta 'p)) 2)) 
```

$$\frac{\frac{1}{2}p^{2}}{\alpha} + \frac{\frac{1}{2}\alpha\beta^{2}\mathit{\epsilon}^{2}\left( {\sin\left( \theta \right)} \right)^{2}}{p^{2}}$$

Indeed, the order /ϵ/ term has been removed and an order /ϵ/^{2} term has been introduced.

Ignoring the /ϵ/^{2} terms in the new Hamiltonian, the solution is
```Scheme
(define (((solution0 alpha beta) t) state0) (let ((t0 (time state0)) (theta0 (coordinate state0)) (p0 (momentum state0))) (up t (+ theta0 (/ (* (- t t0) p0) alpha)) p0))) 
```
The transformation from primed to unprimed phase-space coordinates is, including terms up to order,
```Scheme
(define ((C alpha beta epsilon order) state) (series:sum (((Lie-transform (W alpha beta) epsilon) identity) state) order)) 
```
#page(464)

To second order in /ϵ/ the transformation generated by W is
```Scheme
(show-expression ((C 'alpha 'beta 'epsilon 2) (up 't 'theta 'p))) 
```

$$\begin{pmatrix} t \\ {- \frac{\frac{1}{2}\alpha^{2}\beta^{2}\mathit{\epsilon}^{2}\cos\left( \theta \right)\,\sin\left( \theta \right)}{p^{4}} + \frac{\alpha\beta\mathit{\epsilon}\sin\left( \theta \right)}{p^{2}} + \theta} \\ {- \frac{\frac{1}{2}\alpha^{2}\beta^{2}\mathit{\epsilon}^{2}}{p^{3}} + \frac{\alpha\beta\mathit{\epsilon}\cos\left( \theta \right)}{p} + p} \\ \end{pmatrix}$$

The inverse transformation is
```Scheme
(define (C-inv alpha beta epsilon order) (C alpha beta (- epsilon) order)) 
```
With these components, the perturbative solution (equation #Eqn(chapter007,7.9,7.9)) is
```Scheme
(define (((solution epsilon order) alpha beta) delta-t) (compose (C alpha beta epsilon order) ((solution0 alpha beta) delta-t) (C-inv alpha beta epsilon order))) 
```
The resulting procedure maps an initial state to the solution state advanced by delta-t.

We can examine the behavior of the perturbative solution and compare it to the true behavior of the pendulum. There are several considerations. We have truncated the Lie series for the phase-space transformation. Does the missing part matter? If the missing part does not matter, how well does this perturbation step work?

[Figure 7.1](#figure_7.1) shows that as we increase the number of terms in the Lie series for the phase-space coordinate transformation the result appears to converge. The lone trajectory includes only terms of first order. The others, including terms of second, third, and fourth order, are closely clustered. On the left edge of the graph (at /θ/ = −/π/), the order of the solution increases from the top to the bottom of the graph. In the middle (at /θ/ = 0), the fourth-order curve is between the second-order curve and the third-order curve. In addition to the error in phase-space path, there is also an error in the period---the higher-order orbits have longer periods
#page(465)
than the first-order orbit. The parameters are /α/ = 1.0 and /β/ = 0.1. We have set /ϵ/ = 1. Each trajectory was started at /θ/ = 0 with /p/ = 0.7. Notice that the initial point on the solution varies between trajectories. This is because the transformation is not perfectly inverted by the truncated Lie series.

#Image(Art_P1187.jpg,figure_7.1)
#Caption *Figure 7.1* The perturbative solution in the phase plane, including terms of first, second, third, and fourth order in the phase-space coordinate transformation. The solutions appear to converge. #CaptionEnd

[Figure 7.2](#figure_7.2) compares the perturbative solution (with terms up to fourth order) with the actual trajectory of the pendulum. The initial points coincide, to the precision of the graph, because the terms to fourth order are sufficient. The trajectories deviate both in the phase plane and in the period, but they are still quite close.

The trajectories of [figures 7.1](#figure_7.1) and [7.2](#figure_7.2) are all for the same initial state. As we vary the initial state we find that for trajectories in the circulation region, far from the separatrix, the perturbative solution does quite well. However, if we get close to the separatrix or if we enter the oscillation region, the perturbative solution is nothing like the real solution, and it does not even seem to converge. [Figure 7.3](#figure_7.3) shows what happens when we try to use the perturbative solution inside the oscillation region. Each trajectory was started at /θ/ = 0 with /p/ = 0.55. The parameters are /α/ = 1.0 and /β/ = 0.1, as before.

#page(466)

#Image(Art_P1188.jpg,figure_7.2)
#Caption *Figure 7.2* The perturbative solution in the phase plane, including terms of fourth order in the phase-space coordinate transformation, is compared with the actual trajectory. The actual trajectory is the lower of the two curves. The parameters are the same as in [figure 7.1](#figure_7.1). #CaptionEnd

This failure of the perturbation solution should not be surprising. We assumed that the real motion was a distorted version of the motion of the free rotor. But in the oscillation region the assumption is not true---the pendulum is not rotating at all. The perturbative solutions can be valid (if they work at all!) only in a region where the topology of the real orbits is the same as the topology of the perturbative solutions.

We can make a crude estimate of the range of validity of the perturbative solution by looking at the first correction term in the phase-space transformation (#Eqn(chapter007,7.18,7.18)). The correction in /θ/ is proportional to /ϵαβ//(/p/′)^{2}. This is not a small perturbation if

$$\begin{matrix} {\left| p\prime \right| < \sqrt{\mathit{\epsilon}\alpha\beta}.} \tag{7.22} \\ \end{matrix}$$

This sets the scale for the validity of the perturbative solution.

We can compare this scale to the size of the oscillation region (see [figure 7.4](#figure_7.4)). We can obtain the width of the region of oscillation of the pendulum#Footnote(1) by considering the separatrix. The value
#page(467)
of the Hamiltonian on the separatrix is the same as the value at the unstable equilibrium: /H/(/t/, /θ/ = /π/, /p/ = 0) = /βϵ/. The separatrix has maximum momentum /p/^{sep} at /θ/ = 0:

#Image(Art_P1189.jpg,figure_7.3)
#Caption *Figure 7.3* The perturbative solution does not converge in the oscillation region. As we include more terms in the Lie series for the phase-space transformation, the resulting trajectory develops loops near the hyperbolic fixed point that increase in size with the order. #CaptionEnd

$$\begin{matrix} {H\left( {t,0,p^{\text{sep}}} \right) = H\left( {t,\pi,0} \right).} \tag{7.23} \\ \end{matrix}$$

Solving for /p/^{sep}, the half-width of the region of oscillation, we find

$$\begin{matrix} {p^{\text{sep}} = 2\sqrt{\alpha\beta\mathit{\epsilon}}.} \tag{7.24} \\ \end{matrix}$$

Comparing equations (#Eqn(chapter007,7.22,7.22)) and (#Eqn(chapter007,7.24,7.24)), we see that the requirement that the terms in the perturbation solution be small excludes a region of the phase space with the same scale as the region of oscillation of the pendulum.

What the perturbation theory is doing is deforming the phase-space coordinate system so that the problem looks like the free-rotor problem. This deformation is sensible only in the circulating case. So, it is not surprising that the perturbation theory fails in the oscillation region. What may be surprising is how well the perturbation theory works just outside the oscillation region. The
#page(468)
range of /p/ in which the perturbation theory is not valid scales in the same way as the width of the oscillation region. This need not have been the case---the perturbation theory could have failed over a wider range.

#Image(Art_P1190.jpg,figure_7.4)
#Caption *Figure 7.4* The oscillation region of the pendulum is delimited by the separatrix. The maximum momentum occurs at the zero-crossing of the angle. Energy is conserved, so the energy is the same at the point of maximum momentum and at the unstable fixed point. At the unstable fixed point the energy is entirely potential energy, because the momentum is zero. We use this to compute the maximum momentum (where the potential energy is zero and all of the energy is kinetic). #CaptionEnd

### Exercise 7.1: Symplectic residual

For the transformation (C alpha beta epsilon order), compute the residuals in the symplectic test for various orders of truncation of the Lie series.

##### 7.2.1 Higher Order
We can improve the perturbative solution by carrying out additional perturbation steps. The overall plan is the same as before. We perform a Lie transformation with a new generator that eliminates the desired terms from the Hamiltonian.

After the first step the Hamiltonian is, to second order in /ϵ/,

#page(469)

$$\begin{array}{lll} {H\prime\left( {t,\theta\prime,p\prime} \right)} & {= \frac{\left( p\prime \right)^{2}}{2\alpha} + \mathit{\epsilon}^{2}\frac{\alpha\beta^{2}}{2\left( p\prime \right)^{2}}\left( {\sin\theta\prime} \right)^{2} + \cdots} & \\ & {= \frac{\left( p\prime \right)^{2}}{2\alpha} + \mathit{\epsilon}^{2}\frac{\alpha\beta^{2}}{4\left( p\prime \right)^{2}}\left( {1 - \cos\left( {2\theta\prime} \right)} \right) + \cdots} & \\ & {= H_{0}\left( p\prime \right) + \mathit{\epsilon}^{2}H_{2}\left( {t,\theta\prime,p\prime} \right) + \cdots.} \tag{7.25} \\ \end{array}$$

Performing a Lie transformation with generator /W/′ yields the Hamiltonian

$$\begin{array}{lll} {H''} & {= e^{\mathit{\epsilon}^{2}L_{W\prime}}H\prime} & \\ & {= H_{0} + \mathit{\epsilon}^{2}\left( {L_{W\prime}H_{0} + H_{2}} \right) + \cdots.} \tag{7.26} \\ \end{array}$$

So the condition on /W/′ that the second-order terms are eliminated is

$$\begin{matrix} {L_{W\prime}H_{0} + H_{2} = 0.} \tag{7.27} \\ \end{matrix}$$

This is

$$\begin{matrix} {- \frac{p\prime}{\alpha}\partial_{1}W\prime\left( {t,\theta\prime,p\prime} \right) + \frac{\alpha\beta^{2}}{4\left( p\prime \right)^{2}}\left( {1 - \cos\left( {2\theta\prime} \right)} \right) = 0.} \tag{7.28} \\ \end{matrix}$$

A generator that satisfies this condition is

$$\begin{matrix} {W\prime\left( {t,\theta\prime,p\prime} \right) = \frac{\alpha^{2}\beta^{2}}{4\left( p\prime \right)^{3}}{\theta\prime} + \frac{\alpha^{2}\beta^{2}}{8\left( p\prime \right)^{3}}\sin\left( {2\theta\prime} \right).} \tag{7.29} \\ \end{matrix}$$

There are two contributions to this generator, one proportional to /θ/′ and the other involving a trigonometric function of /θ/′.

The phase-space coordinate transformation resulting from this Lie transform is found as before. For given initial conditions, we first carry out the inverse transformation corresponding to /W/, then that for /W/′, solve for the evolution of the system using /H/_{0}, then transform back using /W/′ and then /W/. For initial state /s/_{0} = (/t/_{0}, /θ/_{0}, /p/_{0}) and advanced state /s/ = (/t, θ/, /p/), the approximate solution is

$$\begin{matrix} \begin{array}{lll} s & {= \left( {E_{- \mathit{\epsilon},W}^{\prime}E_{- \mathit{\epsilon}^{2},W\prime}^{\prime}E_{{({t - t_{0}})},H_{0}}E_{\mathit{\epsilon}^{2},W\prime}^{\prime}E_{\mathit{\epsilon},W}^{\prime}I} \right)\left( s_{0} \right)} & \\ & {= \left( {e^{- \mathit{\epsilon}L_{W}}e^{- \mathit{\epsilon}^{2}L_{W\prime}}e^{{({t - t_{0}})}D_{H_{0}}}e^{\mathit{\epsilon}^{2}L_{W\prime}}e^{\mathit{\epsilon}L_{W}}I} \right)\left( s_{0} \right).} \tag{7.30} \\ \end{array} & \\ \end{matrix}$$

#page(470)

#Image(Art_P1191.jpg,figure_7.5)
#Caption *Figure 7.5* The solution using a second perturbation step, eliminating /ϵ/^{2} terms from the Hamiltonian, is compared to the actual solution. The initial agreement is especially good, but the error increases with time. #CaptionEnd

The solution obtained in this way is compared to the actual evolution of the pendulum in [figure 7.5](#figure_7.5). Terms in all Lie series up to /ϵ/^{4} are included. The perturbative solution, including this second perturbative step, is much closer to the actual solution in the initial segment than the first-order perturbative solution ([figure 7.2](#figure_7.2)). The time interval spanned is 10. Over longer times the second-order perturbative solution diverges dramatically from the actual solution, as shown in [figure 7.6](#figure_7.6). These solutions begin at /θ/ = 0 with /p/ = 0.7. The parameters are /α/ = 1.0 and /β/ = 0.1. The time interval spanned is 100.

A problem with the perturbative solution is that there are terms in /W/′ and in the corresponding phase-space coordinate transformation that are proportional to /θ/′, and /θ/′ grows linearly with time. So the solution can be valid only for small times; the interval of validity depends on the frequency of the particular trajectory under investigation and the size of the coefficients multiplying the various terms. Such terms in a perturbative representation of the solution that are proportional to time are called /secular terms/. They limit the validity of the perturbation theory to small times.

#page(471)

#Image(Art_P1192.jpg,figure_7.6)
#Caption *Figure 7.6* The two-step perturbative solution is shown over a longer time. The actual solution is a closed curve in the phase plane; this perturbative solution wanders all over the place and gets worse with time. #CaptionEnd

##### 7.2.2 Eliminating Secular Terms
A solution to the problem of secular terms was developed by Lindstedt and Poincaré. The goal of each perturbation step is to eliminate terms in the Hamiltonian that prevent solution. However, the term in /H/′ that led to the secular term in the generator /W/′ does not actually impede solution. So a better procedure is to leave that term in the Hamiltonian and find the generator /W/″ that eliminates only the term that is periodic in /θ/′. So /W/″ must satisfy

$$\begin{matrix} {- \frac{p\prime}{\alpha}\partial_{1}W''\left( {t,\theta\prime,p\prime} \right) - \frac{\alpha\beta^{2}}{4\left( p\prime \right)^{2}}\cos\left( {2\theta\prime} \right) = 0.} \tag{7.31} \\ \end{matrix}$$

The generator is

$$\begin{matrix} {W''\left( {t,\theta\prime,p\prime} \right) = \frac{\alpha^{2}\beta^{2}}{8\left( p\prime \right)^{3}}\sin\left( {2\theta\prime} \right).} \tag{7.32} \\ \end{matrix}$$

#page(472)

After we perform a Lie transformation with this generator, the new Hamiltonian is

$$\begin{matrix} {H''\left( {t,\theta'',p''} \right) = \frac{\left( p'' \right)^{2}}{2\alpha} + \mathit{\epsilon}^{2}\frac{\alpha\beta^{2}}{4\left( p'' \right)^{2}} + \cdots.} \tag{7.33} \\ \end{matrix}$$

Including terms up to the /ϵ/^{2} term, the solution is

$$\begin{array}{lll} {\theta''} & {= \theta_{0}^{''} + \left( {\frac{p_{0}^{''}}{\alpha} - \mathit{\epsilon}^{2}\frac{\alpha\beta^{2}}{2\left( p_{0}^{''} \right)^{3}}} \right)\left( {t - t_{0}} \right)} & \\ {p''} & {= p_{0}^{''}.} \tag{7.34} \\ \end{array}$$

We construct the solution for a given initial condition as before by composing the transformations, the solution of the modified Hamiltonian, and the inverse transformations. The approximate solution is

$$\begin{array}{lll} \left( {t,\theta,p} \right) & {= \left( {E_{- \mathit{\epsilon},W}^{\prime}E_{- \mathit{\epsilon}^{2},W''}^{''}E_{{({t - t_{0}})},H''}E_{\mathit{\epsilon}^{2},W''}^{\prime}E_{\mathit{\epsilon},W}^{\prime}I} \right)\left( {t_{0},\theta_{0},p_{0}} \right)} & \\ & {= \left( {e^{- \mathit{\epsilon}L_{W}}e^{- \mathit{\epsilon}^{2}L_{W''}}e^{{({t - t_{0}})}D_{H''}}e^{\mathit{\epsilon}^{2}L_{W''}}e^{\mathit{\epsilon}L_{W}}I} \right)\left( {t_{0},\theta_{0},p_{0}} \right).} \tag{7.35} \\ \end{array}$$

The resulting phase-space evolution is shown in [figure 7.7](#figure_7.7). Now the perturbative solution is a closed curve in the phase plane and is in pretty good agreement with the actual solution.

By modifying the solvable part of the Hamiltonian we are modifying the frequency of the solution. The secular terms appeared because we were trying to approximate a solution with one frequency as a Fourier series with the wrong frequency. As an analogy, consider

$$\begin{array}{lll} {\sin\left( {\omega + \Delta\omega} \right)t} & {= \sin\omega t\cos\Delta\omega t + \cos\omega t\sin\Delta\omega t} & \\ & {= \sin\omega t\left( {1 - \frac{\left( {\Delta\omega t} \right)^{2}}{2} + \cdots} \right)} & \\ & {\,\,\,\,\, + \cos\omega t\,\left( {\Delta\omega t + \cdots} \right).} \tag{7.36} \\ \end{array}$$

The periodic terms are multiplied by terms that are polynomials in the time. These polynomials are the initial segment of the power series for periodic functions. The infinite series are convergent, but if the series are truncated the error is large at large times.

Continuing the perturbative solution to higher orders is now a straightforward repetition of the steps carried out so far. At each step in the perturbation solution there will be new contributions to
#page(473)
the solvable part of the Hamiltonian that absorb potential secular terms. The contribution is just the angle-independent part of the Hamiltonian after the Hamiltonian is written as a Fourier series. The constant part of the Fourier series is the same as the average of the Hamiltonian over the angle. So at each step in the perturbation theory, the average of the perturbation is included with the solvable part of the Hamiltonian and the periodic part is eliminated by a Lie transformation.

#Image(Art_P1193.jpg,figure_7.7)
#Caption *Figure 7.7* The two-step perturbative solution without secular terms is compared to the actual solution. The perturbative solution is now a closed curve and is very close to the actual solution. #CaptionEnd

### 7.3 Many Degrees of Freedom
Other problems are encountered in applying perturbation theory to systems with more than a single degree of freedom. Consider an /n/ degrees-of-freedom Hamiltonian of the form

$$\begin{matrix} {H = H_{0} + \mathit{\epsilon}H_{1},} \tag{7.37} \\ \end{matrix}$$

where /H/_{0} depends only on the momenta and therefore is solvable. We assume that the Hamiltonian has no explicit time dependence.
#page(474)
We further assume that the coordinates are all angles and that /H/_{1} is a multiply periodic function of the coordinates.

Carrying out a Lie transformation with generator /W/ produces the Hamiltonian

$$\begin{array}{lll} {H\prime} & {= e^{\mathit{\epsilon}L_{W}}H} & \\ & {= H_{0} + \mathit{\epsilon}\left( {L_{W}H_{0} + H_{1}} \right) + \cdots,} \tag{7.38} \\ \end{array}$$

as before. The condition that the order /ϵ/ terms are eliminated is

$$\begin{matrix} {\left\{ {H_{0},W} \right\} + H_{1} = 0,} \tag{7.39} \\ \end{matrix}$$

a linear partial differential equation. By assumption, the Hamiltonian /H/_{0} depends only on the momenta. We define

$$\begin{matrix} {\omega_{0}\left( p \right) = \partial_{2}H_{0}\left( {t,\theta,p} \right),} \tag{7.40} \\ \end{matrix}$$

where /θ/ = (/θ/^{0}, ..., /θ/^{n−1}), and /p/ = [/p/_{0}, ..., /p/_{n−1}]. So /ω/_{0}(/p/) is the up tuple of frequencies of the unperturbed system. The condition on /W/ is

$$\begin{matrix} {w_{0}\left( p \right)\partial_{1}W\left( {t,\theta,p} \right) = H_{1}\left( {t,\theta,p} \right).} \tag{7.41} \\ \end{matrix}$$

As /H/_{1} is a multiply periodic function of the coordinates, we can write it as a Poisson series:#Footnote(2)

$$\begin{matrix} {H_{1}\left( {t,\theta,p} \right) = {\sum\limits_{k}{A_{k}\left( p \right)\,\cos\left( {k \cdot \theta} \right),}}} \tag{7.42} \\ \end{matrix}$$

where /k/ = [/k/_{0}, ..., /k/_{n−1}] ranges over all /n/-tuples of integers. Similarly, we assume /W/ can be written as a Poisson series:

$$\begin{matrix} {W\left( {t,\theta,p} \right) = {\sum\limits_{k}{B_{k}\left( p \right)\,\sin\left( {k \cdot \theta} \right).}}} \tag{7.43} \\ \end{matrix}$$

Substituting these into the condition that order /ϵ/ terms are eliminated, we find

$$\begin{matrix} {\sum\limits_{k}{B_{k}\left( p \right)\left( {k \cdot \omega_{0}\left( p \right)} \right)\,\cos\left( {k \cdot \theta} \right) = {\sum\limits_{k}{A_{k}\left( p \right)\,\cos\left( {k \cdot \theta} \right).}}}} \tag{7.44} \\ \end{matrix}$$

#page(475)

The cosines are orthogonal so the coefficients of corresponding cosine terms must be equal:

$$\begin{matrix} {B_{k}\left( p \right) = \frac{A_{k}\left( p \right)}{k \cdot \omega_{0}\left( p \right)}} \tag{7.45} \\ \end{matrix}$$

and that the required Lie generator is

$$\begin{matrix} {W\left( {t,\theta,p} \right) = {\sum\limits_{k}{\frac{A_{k}\left( p \right)}{k \cdot \omega_{0}\left( p \right)}\sin\left( {k \cdot \theta} \right).}}} \tag{7.46} \\ \end{matrix}$$

There are a couple of problems. First, if /A/_{0,...,0} is nonzero then the expression for /B/_{0,...,0} involves a division by zero. So the expression for /B/_{0,...,0} is not correct. The problem is that the corresponding term in /H/_{1} does not involve /θ/. So the integration for /B/_{0,...,0} should introduce linear terms in /θ/. But this is the same situation that led to the secular terms in the perturbation approximation to the pendulum. Having learned our lesson there, we avoid the secular terms by adjoining this term to the solvable Hamiltonian and excluding /k/ = [0, ..., 0] from the sum for /W/. We have

$$\begin{matrix} {H\prime = H_{0} + \mathit{\epsilon}A_{0,\ldots,0} + \cdots,} \tag{7.47} \\ \end{matrix}$$

and

$$\begin{matrix} {W\left( {t,\theta,p} \right) = {\sum\limits_{k \neq {\lbrack{0,\ldots,0}\rbrack}}{\frac{A_{k}\left( p \right)}{k \cdot \omega_{0}\left( p \right)}\sin\left( {k \cdot \theta} \right).}}} \tag{7.48} \\ \end{matrix}$$

Another problem is that there are many opportunities for small denominators that would make the perturbation large and therefore not a perturbation. As we saw in the perturbation approximation for the pendulum in terms of the rotor, we must exclude certain regions from the domain of applicability of the perturbation approximation. These excluded regions are associated with commensurabilities among the frequencies /ω/_{0}(/p/). Consider the phase-space transformation of the coordinates

$$\begin{array}{lll} \theta & {= \left( {e^{\mathit{\epsilon}L_{W}}Q} \right)\left( {t,\theta\prime,p\prime} \right)} & \\ & {= \theta\prime + \mathit{\epsilon}\partial_{2}W\left( {t,\theta\prime,p\prime} \right) + \cdots} & \\ & {= \theta\prime + \mathit{\epsilon}{\sum\limits_{k \neq {\lbrack{0,\ldots,0}\rbrack}}\left( {\frac{DA_{k}\left( p\prime \right)}{k \cdot \omega_{0}\left( p\prime \right)} - \frac{A_{k}\left( p\prime \right)\left( {k \cdot D\omega\left( p\prime \right)} \right)}{\left( {k \cdot \omega_{0}\left( p\prime \right)} \right)^{2}}} \right)}\sin\left( {k \cdot \theta} \right).} \tag{7.49} \\ \end{array}$$

#page(476)

We must exclude from the domain of applicability all regions for which the coefficients are large. If the second term in the coefficient of sin dominates, the excluded regions satisfy

$$\begin{matrix} {\left| {{({k \cdot D\omega{(p\prime)}})}A_{k}{(p)}} \right| > {({k \cdot \omega_{0}{(p)}})}^{2}.} \tag{7.50} \\ \end{matrix}$$

Considering the fact that for any tuple of frequencies /ω/_{0}(/p/′) we can find a tuple of integers /k/ such that /k/·/ω/(/p/′) is arbitrarily small, this problem of small divisors looks very serious.

However, the problem, though serious, is not as bad as it may appear, for a couple of reasons. First, it may be that /A_{k}/ ≠ 0 only for certain /k/. In this case, only the regions for these terms are excluded from the domain of applicability. Second, for analytic functions the magnitude of /A_{k}/ decreases strongly with the size of /k/ (see [4](bibliography!bib_4)):

$$\begin{matrix} {\left| {A_{k}\left( p\prime \right)} \right| \leq Ce^{- \beta{|k|}_{+}},} \tag{7.51} \\ \end{matrix}$$

for some positive /β/ and /C/, and where |/k/|_{+} = |/k/_{0}| + |/k/_{1}| + ⋯. At any stage of a perturbation approximation we can limit consideration to just those terms that are larger than a specified magnitude. The size of the excluded region corresponding to a term is of order square root of |/A_{k}/(/p/′)| and the inequality (#Eqn(chapter007,7.51,7.51)) shows that |/A_{k}/(/p/′)| decreases exponentially with the order of the term.

##### 7.3.1 Driven Pendulum as a Perturbed Rotor
More concretely, consider the periodically driven pendulum. We will develop approximate solutions for the driven pendulum as a perturbed rotor.

We use the Hamiltonian

$$\begin{matrix} {H\left( {t,\theta,p} \right) = \frac{p^{2}}{2ml^{2}} - \mathit{\epsilon}ml{({g - A\omega^{2}\cos{({\omega t})}})}\,\cos\theta.} \tag{7.52} \\ \end{matrix}$$

For a real driven pendulum /ϵ/ = 1; here it is used to help organize the computation. We will see that it need not be small and can be set to 1 at the end. We can remove the explicit time dependence by going to the extended phase space. The Hamiltonian is

#page(477)

$$\begin{array}{ll} {H{({\tau;\theta,t;p,p_{t}})}} & \\ {\,\,\,\,\,\,\,\,\,\, = p_{t} + \frac{p^{2}}{2ml^{2}} - \mathit{\epsilon}ml{({g - A\omega^{2}\cos{({\omega t})}})}\,\cos\theta} & \\ {\,\,\,\,\,\,\,\,\,\, = p_{t} + \frac{p^{2}}{2\alpha} - \mathit{\epsilon}\beta\cos{(\theta)} + \mathit{\epsilon}\gamma\cos{({\theta + \omega t})} + \mathit{\epsilon}\gamma\cos{({\theta - \omega t})},} \tag{7.53} \\ \end{array}$$

with the constants /α/ = /ml/^{2}, /β/ = /mlg/, and $\gamma = \frac{1}{2}mlA\omega^{2}$.

With the intent to approximate the driven pendulum as a perturbed rotor, we choose

$$\begin{array}{lll} {H_{0}\left( {\tau;\theta,t;p,p_{t}} \right)} & {= p_{t} + \frac{p^{2}}{2\alpha}} & \\ {H_{1}\left( {\tau;\theta,t;p,p_{t}} \right)} & {= - \beta\cos\theta + \gamma\cos\left( {\theta + \omega t} \right) + \gamma\cos\left( {\theta - \omega t} \right).} \tag{7.54} \\ \end{array}$$

The perturbation /H/_{1} is particularly simple: it has only three terms, and the coefficients are constants. Because /H/_{1} has only three terms in its Poisson series, only three regions will be excluded from the domain of applicability in the first perturbation step.

The Lie series generator that eliminates the terms in /H/_{1} to first order in /ϵ/, satisfying

$$\begin{matrix} {\left\{ {H_{0},W} \right\} + H_{1} = 0,} \tag{7.55} \\ \end{matrix}$$

is

$$\begin{array}{lll} {W\left( {\tau;\theta,t;p,p_{t}} \right)} & {= - \frac{\beta}{\omega_{r}\left( p \right)}\sin\theta} & \\ & {+ \frac{\gamma}{\omega_{r}\left( p \right) + \omega}\sin\left( {\theta + \omega t} \right)} & \\ & {+ \frac{\gamma}{\omega_{r}\left( p \right) - \omega}\sin\left( {\theta - \omega t} \right),} \tag{7.56} \\ \end{array}$$

where /ω_{r}/(/p/) = ∂_{2,0}/H/_{0}(/τ/; /θ/, /t/; /p/, /p_{t}/) = /p///α/ is the unperturbed rotor frequency.

The resulting approximate solution has three regions in which there are small denominators, and so three regions that are excluded from applicability of the perturbative solution. Regions of phase space for which /ω_{r}/(/p/) is near 0, /ω/, and −/ω/ are excluded. Away from these regions the perturbative solution works well,
#page(478)
just as in the rotor approximation for the pendulum. Unfortunately, some of the more interesting regions of the phase space of the driven pendulum are excluded: the region in which we find the remnant of the undriven pendulum is excluded, as are the two resonance regions in which the rotation of the pendulum is synchronous with the drive. We need to develop methods for approximating these regions.

### 7.4 Nonlinear Resonance
We can develop an approximation for an isolated resonance region as follows. We again consider Hamiltonians of the form

$$\begin{matrix} {H = H_{0} + \mathit{\epsilon}H_{1},} \tag{7.57} \\ \end{matrix}$$

where /H/_{0}(/t/, /q/, /p/) = /Ĥ/_{0}(/p/) depends only on the momenta and so is solvable. We assume that the Hamiltonian has no explicit time dependence. We further assume that the coordinates are all angles, and that /H/_{1} is a multiply periodic function of the coordinates that can be written

$$\begin{matrix} {H_{1}\left( {t,\theta,p} \right) = {\sum\limits_{k}{A_{k}\left( p \right)\,\cos\left( {k \cdot \theta} \right).}}} \tag{7.58} \\ \end{matrix}$$

Suppose we are interested in a region of phase space for which /n/ · /ω/_{0}(/p/) is near zero, where /n/ is a tuple of integers, one for each degree of freedom. If we develop the perturbation theory as before with the generator /W/ that eliminates all terms of order /ϵ/, then the transformed Hamiltonian is /H/_{0}, which is analytically solvable, but there would be terms with /n/ · /ω/_{0}(/p/) in the denominator. The resulting solution is not applicable near this resonance.

Just as the problem of secular terms was solved by grouping more terms with the solvable part of the Hamiltonian, we can develop approximations that are valid in the resonance region by eliminating fewer terms and grouping more terms in the solvable part.

To develop a perturbative approximation in the resonance region for which /n/ · /ω/_{0}(/p/) is near zero, we take the generator /W/ to be

$$\begin{matrix} {W_{n}\left( {t,\theta,p} \right) = {\sum\limits_{k \neq 0,k \neq n}{\frac{A_{k}\left( p \right)}{k \cdot \omega_{0}\left( p \right)}\sin\left( {k \cdot \theta} \right),}}} \tag{7.59} \\ \end{matrix}$$

#page(479)

excluding terms in /W/ that lead to small denominators in this region. The transformed Hamiltonian is

$$\begin{matrix} {H_{n}^{\prime}\left( {t,\theta,p} \right) = {\widehat{H}}_{0}\left( p \right) + \mathit{\epsilon}A_{0}\left( p \right) + \mathit{\epsilon}A_{n}\left( p \right)\,\cos\left( {n \cdot \theta} \right) + \cdots,} \tag{7.60} \\ \end{matrix}$$

where the additional terms are higher-order in /ϵ/. Because the term /k/ = /n/ is excluded from the sum in the generating function, that term is left after the transformation.

The transformed Hamiltonian depends only on a single combination of angles, so a change of variables can be made so that the new transformed Hamiltonian is cyclic in all but one coordinate, which is this combination of angles. This transformed Hamiltonian is solvable (reducible to quadratures).

For example, suppose there are two degrees of freedom /θ/ = (/θ/_{1}, /θ/_{2}) and we are interested in a region of phase space in which /n/ · /ω/_{0} is near zero, with /n/ = [/n/_{1}, /n/_{2}]. The combination of angles /n/ · /θ/ is slowly varying in the resonance region. The transformed Hamiltonian (#Eqn(chapter007,7.60,7.60)) is of the form

$$\begin{array}{lll} {H_{n}^{\prime}\left( {t;\theta_{1},\theta_{2};p_{1},p_{2}} \right)} & {= {\widehat{H}}_{0}\left( {p_{1},p_{2}} \right) + \mathit{\epsilon}A_{0}\left( {p_{1},p_{2}} \right)} & \\ & {\,\,\,\,\,\,\, + \mathit{\epsilon}A_{n}\left( {p_{1},p_{2}} \right)\,\cos\left( {n_{1}\theta_{1} + n_{2}\theta_{2}} \right).} \tag{7.61} \\ \end{array}$$

We can transform variables to /σ/ = /n/_{1}/θ/_{1} + /n/_{2}/θ/_{2}, with second coordinate, say, /θ/′ = /θ/_{2}.#Footnote(3) Using the /F/_{2}-type generating function

$$\begin{matrix} {F_{2}\left( {t;\theta_{1},\theta_{2};\Sigma,\Theta\prime} \right) = \left( {n_{1}\theta_{1} + n_{2}\theta_{2}} \right)\Sigma + \theta_{2}\Theta\prime,} \tag{7.62} \\ \end{matrix}$$

we find that the transformation is

$$\begin{array}{rll} p_{1} & {= n_{1}\Sigma} & \\ p_{2} & {= n_{2}\Sigma + \Theta\prime} & \\ \sigma & {= n_{1}\theta_{1} + n_{2}\theta_{2}} & \\ {\theta\prime} & {= \theta_{2}.} \tag{7.63} \\ \end{array}$$

In these variables the transformed resonance Hamiltonian $ H_{n}^{\prime}$ becomes

$$\begin{array}{lll} {H_{n}^{''}\left( {t;\sigma,\theta\prime;\Sigma,\Theta\prime} \right)} & {= {\widehat{H}}_{0}\left( {n_{1}\Sigma,n_{2}\Sigma + \Theta\prime} \right) + \mathit{\epsilon}A_{0}\left( {n_{1}\Sigma,n_{2}\Sigma + \Theta\prime} \right)} & \\ & {\,\,\,\,\,\, + \mathit{\epsilon}A_{n}\left( {n_{1}\Sigma,n_{2}\Sigma + \Theta\prime} \right)\,\cos\left( \sigma \right).} \tag{7.64} \\ \end{array}$$

#page(480)

This Hamiltonian is cyclic in /θ/′, so Θ′ is constant. With this constant momentum, the Hamiltonian for the conjugate pair (/σ/, Σ) has one degree of freedom. The solutions are level curves of the Hamiltonian. These solutions, reexpressed in terms of the original phase-space coordinates, give the evolution of $ H_{n}^{\prime}$. An approximate solution in the resonance region is therefore

$$\begin{matrix} {{({t,\theta,p})} = {({E_{- \mathit{\epsilon},W_{n}^{\prime}}^{\prime}E_{t - t_{0},H_{n}^{\prime}}E_{\mathit{\epsilon},W_{n}^{\prime}}^{\prime}I})}{({t_{0},\theta_{0},p_{0}})}.} \tag{7.65} \\ \end{matrix}$$

If the resonance regions are sufficiently separated, then a global solution can be constructed by splicing together such solutions for each resonance region.

##### 7.4.1 Pendulum Approximation
The resonance Hamiltonian (#Eqn(chapter007,7.64,7.64)) has a single degree of freedom and is therefore solvable (reducible to quadratures). We can develop an approximate analytic solution in the vicinity of the resonance by making use of the fact that the solution is valid there. The resonance Hamiltonian can be approximated by a generalized pendulum Hamiltonian.

Let

$$\begin{array}{ll} {H_{n,0}^{''}\left( {t;\sigma,\theta\prime;\Sigma,\Theta\prime} \right)} & \\ {\,\,\,\,\,\,\,\,\, = {\widehat{H}}_{0}\left( {n_{1}\Sigma,n_{2}\Sigma + \Theta\prime} \right) + \mathit{\epsilon}A_{0}\left( {n_{1}\Sigma,n_{2}\Sigma + \Theta\prime} \right)} \tag{7.66} \\ \end{array}$$

and

$$\begin{matrix} {H_{n,1}^{''}\left( {t;\sigma,\theta\prime;\Sigma,\Theta\prime} \right) = A_{n}\left( {n_{1}\Sigma,n_{2}\Sigma + \Theta\prime} \right)\,\cos\left( \sigma \right);} \tag{7.67} \\ \end{matrix}$$

then the resonance Hamiltonian is

$$\begin{matrix} {H_{n}^{''} = H_{n,0}^{''} + \mathit{\epsilon}H_{n,1}^{''}.} \tag{7.68} \\ \end{matrix}$$

Define the resonance center Σ/_{n}/ by the requirement that the resonance frequency be zero there:

$$\begin{matrix} {\partial_{2,0}H_{n,0}^{''}\left( {t;\sigma,\theta\prime;\Sigma_{n},\Theta\prime} \right) = 0.} \tag{7.69} \\ \end{matrix}$$

Now expand both parts of the resonance Hamiltonian about the resonance center:

#page(481)

$$\begin{array}{lll} {H_{n,0}^{''}\left( {t;\sigma,\theta\prime;\Sigma,\Theta\prime} \right)} & {= H_{n,0}^{''}\left( {t;\sigma,\theta\prime;\Sigma_{n},\Theta\prime} \right)} & \\ & {\,\,\,\,\,\,\,\,{+ \partial_{2,0}H_{n,0}^{''}\left( {t;\sigma,\theta\prime;\Sigma_{n},\Theta\prime} \right)\left( {\Sigma - \Sigma_{n}} \right)}} & \\ & {\,\,\,\,\,\,\,\,{+ \frac{1}{2}\partial_{2,0}^{2}H_{n,0}^{''}\left( {t;\sigma,\theta\prime;\Sigma_{n},\Theta\prime} \right)\left( {\Sigma - \Sigma_{n}} \right)^{2}}} & \\ & {\,\,\,\,\,\,\,\,{+ \cdots,}} \tag{7.70} \\ \end{array}$$

and

$$\begin{matrix} {H_{n,1}^{''}\left( {t;\sigma,\theta\prime;\Sigma,\Theta\prime} \right) = H_{n,1}^{''}\left( {t;\sigma,\theta\prime;\Sigma_{n},\Theta\prime} \right) + \cdots.} \tag{7.71} \\ \end{matrix}$$

The first term in the expansion of $ H_{n,0}^{''}$ is a constant and can be ignored. The coefficient of the second term is zero, from the definition of Σ/_{n}/. The third term is the first significant term. We presume here that the first term of $ H_{n,1}^{''}$ is a nonzero constant. Now the scale of the separatrix in Σ at resonance is typically proportional to $\sqrt{\mathit{\epsilon}}$. So the third term of $ H_{n,0}^{''}$ and the first term of $ H_{n,1}^{''}$ are both proportional to /ϵ/. Subsequent terms are higher-order in /ϵ/. Keeping only the order /ϵ/ terms, the approximate resonance Hamiltonian is of the form

$$\begin{matrix} {\frac{\left( {\Sigma - \Sigma_{n}} \right)^{2}}{2\alpha\prime} - \mathit{\epsilon}\beta\prime\cos\sigma,} \tag{7.72} \\ \end{matrix}$$

which is the Hamiltonian for a pendulum with a shifted center in momentum. This is analytically solvable. The constants are:

$$\begin{array}{lll} {\alpha\prime =} & {= {1/\left( {\partial_{2,0}^{2}H_{n,0}^{''}\left( {t;\sigma,\theta\prime;\Sigma_{n},\Theta\prime} \right)} \right)}} & \\ {\beta\prime =} & {= H_{n,1}^{''}\left( {t;\sigma,\theta\prime;\Sigma_{n},\Theta\prime} \right).} \tag{7.73} \\ \end{array}$$

#### Driven pendulum resonances
Consider the behavior of the periodically driven pendulum in the vicinity of the resonance /ω_{r}/(/p/) = /ω/.

The Hamiltonian (#Eqn(chapter007,7.54,7.54)) for the driven pendulum has three resonance terms in /H/_{1}. The full generator (#Eqn(chapter007,7.56,7.56)) has three terms that are designed to eliminate the corresponding resonance terms in the Hamiltonian. The resulting approximate solution has small denominators close to each of the three resonances, /ω_{r}/(/p/) = 0, /ω_{r}/(/p/) = /ω/, and /ω_{r}/(/p/) = −/ω/.

To develop a resonance approximation near /ω_{r}/(/p/) = /ω/, we do not include the corresponding term in the generator, so that the
#page(482)
corresponding term is left in the Hamiltonian. It is helpful to give names to the various terms in the full generator (#Eqn(chapter007,7.56,7.56)):

$$\begin{array}{rll} {W^{0}\left( {\tau;\theta,t;p,p_{t}} \right)} & {= - \frac{\beta}{\omega_{r}\left( p \right)}\sin\theta} & \\ {W^{-}\left( {\tau;\theta,t;p,p_{t}} \right)} & {= \frac{\gamma}{\omega_{r}\left( p \right) + \omega}\sin\left( {\theta + \omega t} \right)} & \\ {W^{+}\left( {\tau;\theta,t;p,p_{t}} \right)} & {= \frac{\gamma}{\omega_{r}\left( p \right) - \omega}\sin\left( {\theta - \omega t} \right).} \tag{7.74} \\ \end{array}$$

The full generator is /W/^{0} + /W/^{−} + /W/^{+}.

To investigate the motion in the phase space near the resonance /ω_{r}/(/p/) = /ω/ (the “+” resonance), we use the generator that excludes the corresponding term

$$\begin{matrix} {W_{+} = W^{0} + W^{-}.} \tag{7.75} \\ \end{matrix}$$

With this generator the transformed Hamiltonian is

$$\begin{matrix} {H_{+}\left( {\tau;\theta,t;p,p_{t}} \right) = p_{t} + \frac{p^{2}}{2\alpha} + \mathit{\epsilon}\gamma\cos\left( {\theta - \omega t} \right) + \cdots.} \tag{7.76} \\ \end{matrix}$$

After we exclude the higher-order terms, this Hamiltonian has only a single combination of coordinates, and so can be transformed into a Hamiltonian that is cyclic in all but one degree of freedom. Define the transformation through the mixed-variable generating function

$$\begin{matrix} {F_{2}\left( {\tau;t,\theta;\Sigma,p_{t}^{\prime}} \right) = \left( {\theta - \omega t} \right)\Sigma + tp_{t}^{\prime},} \tag{7.77} \\ \end{matrix}$$

giving the transformation

$$\begin{array}{rll} \sigma & {= \theta - \omega t} & \\ t & {= t\prime} & \\ p & {= \Sigma} & \\ p_{t} & {= p_{t}^{\prime} - \omega\Sigma.} \tag{7.78} \\ \end{array}$$

Expressed in these new coordinates, the resonance Hamiltonian is

$$\begin{array}{lll} {H_{+}\prime\left( {\tau;\sigma,t\prime;\Sigma,p_{t}^{\prime}} \right)} & {= p_{t}^{\prime} - \omega\Sigma + \frac{\Sigma^{2}}{2\alpha} + \mathit{\epsilon}\gamma\cos\sigma} & \\ & {= \frac{\left( {\Sigma - \alpha\omega} \right)^{2}}{2\alpha} + \mathit{\epsilon}\gamma\cos\sigma + p_{t}^{\prime} - \frac{1}{2}\alpha\omega^{2}.} \tag{7.79} \\ \end{array}$$

#page(483)

#Image(Art_P1194.jpg,figure_7.8)
#Caption *Figure 7.8* Contours of the resonance Hamiltonian /H/_{+}′ give the motion in the (/σ/, Σ) plane. In this case the resonance Hamiltonian is a generalized pendulum shifted in momentum and phase. The half-width of the resonance oscillation zone is ¶ $ 2\sqrt{\alpha\gamma\mathit{\epsilon}}$ ¶ . #CaptionEnd

This Hamiltonian is cyclic in /t/′, so the solutions are level curves of /H/_{+}′ in (/σ/, Σ). Actually, more can be said here because /H/_{+}′ is already of the form of a pendulum shifted in the Σ direction by /αω/ and shifted by /π/ in phase. The shift by /π/ comes about because the sign of the cosine term is positive, rather than negative as in the usual pendulum. A sketch of the level curves is given in [figure 7.8](#figure_7.8).

### Exercise 7.2: Resonance width

Verify that the half-width of the resonance region is $ 2\sqrt{\alpha\gamma\mathit{\epsilon}}$.

### Exercise 7.3: With the computer

Verify, with the computer, that with the generator /W/_{+} the transformed Hamiltonian is given by equation (#Eqn(chapter007,7.76,7.76)).

An approximate solution of the driven pendulum near the /ω_{r}/(/p/) = /ω/ resonance is

$$\begin{matrix} {{({\tau;\theta,t;p,p_{t}})} = (E_{- \mathit{\epsilon},W_{+}}^{\prime}E_{\tau - \tau_{0},H + \prime}E_{\mathit{\epsilon},W_{+}}^{\prime}I){({\tau_{0};\theta_{0},t_{0};p_{0},{(p_{t})}_{0}})}.} \tag{7.80} \\ \end{matrix}$$

To find out to what extent the approximate solution models the actual driven pendulum, we make a surface of section using this approximate solution and compare it to a surface of section for the
#page(484)
actual driven pendulum. The surface of section for the approximate solution in the resonance region is shown in [figure 7.9](#figure_7.9). A surface of section for the actual driven pendulum is shown in the lower part of [figure 7.10](#figure_7.10). The correspondence is surprisingly good. Note how the resonance island is not symmetrical about a line of constant momentum. The resonance Hamiltonian is symmetrical about Σ = /αω/, and by itself would give a symmetric resonance island (see [figure 7.8](#figure_7.8)). The necessary distortion is introduced by the /W/_{+} transformation that eliminates the other resonances. Indeed, in the full section the distortion appears to be generated by the nearby /ω_{r}/(/p/) = 0 resonance “pushing away” nearby features so that it has room to fit. However, some features of the actual section are not represented in [figure 7.9](#figure_7.9): for instance, the small chaotic zone near the actual separatrix.

#Image(Art_P1195.jpg,figure_7.9)
#Caption *Figure 7.9* Surface of section of the first-order perturbative solution for the driven pendulum constructed for the region near the resonance /ω_{r}/(/p/) = /ω/. The parameters of the system are /α/ = 1, /β/ = 1, /γ/ = 1/4, and /ω/ = 5. Only order /ϵ/ terms were kept in the Lie series for the /W/ transformation. The perturbative solution captures the essential shape and position of the resonant island it is designed to approximate. #CaptionEnd

The distortion introduced by the transformation generated by /W/_{+} is small because the terms that it introduces are proportional to the inverse of a combination of frequencies.#Footnote(4) Since this combination is not small, dividing by it makes the correction small. Thus the “order parameter” /ϵ/ need not be small to make the correction terms small, and from now on we can set /ϵ/ = 1.

#page(485)
#page(486)

#Image(Art_P1196.jpg,figure_7.10)
#Caption *Figure 7.10* A composite surface of section (top) for the driven pendulum is constructed by combining the first-order perturbative solution for the region near the resonance /ω_{r}/(/p/) = 0 and the solutions for the regions near the resonances /ω_{r}/(/p/) = ±/ω/. A corresponding surface of section for the actual driven pendulum is shown below. The parameters of the system are: /α/ = 1, /β/ = 1, /γ/ = 1/4, and /ω/ = 5. #CaptionEnd

The perturbation solution near the /ω_{r}/(/p/) = 0 resonance merges smoothly with the perturbation solutions for the /ω_{r}/(/p/) = /ω/ and /ω_{r}/(/p/) = −/ω/ resonances. We can make a composite perturbative solution by using the appropriate resonance solution for each region of phase space. A surface of section for the composite pertur-bative solution is shown in the upper part of [figure 7.10](#figure_7.10), above the corresponding surface of section for the actual driven pendulum. The perturbative solution captures many features seen on the actual section. The shapes of the resonance regions are distorted by the transformations that eliminate the nearby resonances, so the resulting pieces fit together consistently. The predicted width of each resonance region agrees with the actual width: it is not substantially changed by the distortion of the region introduced by the elimination of the other resonance terms. But not all the features of the actual section are reproduced in this composite of first-order approximations. The first-order perturbative solution does not capture the resonant islands between the two primary resonances or the secondary island chains contained within a primary resonance region. Also, the first-order perturbative solution does not show the chaotic zone near the separatrix apparent in the surface of section for the actual driven pendulum.

For larger drives, the approximations derived by first-order perturbations are worse. In the lower part of [figure 7.11](#figure_7.11), with drive larger by a factor of five, we lose the invariant curves that separate the resonance regions. The main resonance islands persist, but the chaotic zones near the separatrices have merged into one large chaotic sea.

The composite first-order perturbative solution for the more strongly driven pendulum in the upper part of [figure 7.11](#figure_7.11) still approximates the centers of the main resonance islands reasonably well, but it fails as we move out and encounter the secondary islands that are visible in the resonance region for /ω_{r}/(/p/) = /ω/. Here the approximations for the two regions do not fit together so well. The chaotic sea is found in the region where the perturbative solutions do not match.

#page(487)

#Image(Art_P1197.jpg,figure_7.11)
#Caption *Figure 7.11* Composite surface of section (top) for the driven pendulum constructed by combining the first-order perturbative solution for the region near the resonance /ω_{r}/(/p/) = 0 and the regions near the resonances /ω_{r}/(/p/) = ±/ω/. A corresponding surface of section for the actual driven pendulum is shown below. The parameters of the system are the same as in [figure 7.10](#figure_7.10) except that /γ/ = 5/4. #CaptionEnd

#page(488)

##### 7.4.2 Reading the Hamiltonian
The locations and widths of the primary resonance islands can often be read straight off the Hamiltonian when expressed as a Poisson series. For each term in the series for the perturbation there is a corresponding resonance island. The width of the island can often be simply computed from the coefficients in the Hamiltonian. So just by looking at the Hamiltonian we can get a good idea of what sort of behavior we will see on the surface of section. For instance, in the driven pendulum, the Hamiltonian (#Eqn(chapter007,7.54,7.54)) has three terms. We could anticipate, just from looking at the Hamiltonian, that three main resonance islands are to be found on the surface of section. We know that these islands will be located where the resonant combination of angles is slow. So for the periodically driven pendulum the resonances occur near /ω_{r}/(/p/) = /ω/, /ω_{r}/(/p/) = 0, and /ω_{r}/(/p/) = −/ω/. The approximate widths of the resonance islands can be computed with a simple calculation.

##### 7.4.3 Resonance-Overlap Criterion
As the size of the drive increases, the chaotic zones near the separatrices get larger and then merge into a large chaotic sea. The resonance-overlap criterion gives an analytic estimate of when this occurs. The basic idea is to compare the sum of the widths of neighboring resonances with their separation. If the sum of the half-widths is greater than the separation, then the resonance-overlap criterion predicts there will be large-scale chaotic behavior near the overlapping resonances. In the case of the periodically driven pendulum, the half-width of the /ω_{r}/(/p/) = 0 resonance is $ 2\sqrt{\alpha\beta}$ and the half-width of the /ω_{r}/(/p/) = /ω/ resonance is $ 2\sqrt{\alpha\gamma}$(see [figure 7.12](#figure_7.12)). The separation of the resonances is /αω/. So resonance overlap occurs if

$$\begin{matrix} {2\sqrt{\alpha\beta} + 2\sqrt{\alpha\gamma} \geq \alpha\omega.} \tag{7.81} \\ \end{matrix}$$

The amplitude of the drive enters through /γ/. Solving, we find the value of /γ/ above which resonance overlap occurs. For the parameters /α/ = /β/ = 1, /ω/ = 5 used in [[#figure_7.9][figures 7.9]]--[7.11](#figure_7.11), the resonance overlap value of /γ/ is 9/4. We see that, in fact, the chaotic zones have already merged for /γ/ = 5/4. So in this case the resonance-overlap criterion overestimates the strength of the resonances required to get large-scale chaotic behavior. This is typical of the resonance-overlap criterion.

#page(489)

#Image(Art_P1198.jpg,figure_7.12)
#Caption *Figure 7.12* Resonance overlap occurs when the sum of the half-widths of adjacent resonances is larger than the spacing between them. #CaptionEnd

A way of thinking about why the resonance-overlap criterion usually overestimates the strength required to get large-scale chaos is that other effects must be taken into account. For instance, as the drive is increased second-order resonances appear between the primary resonances; these resonances take up space and so resonance overlap occurs for smaller drive than would be expected by considering the primary resonances alone. Also, the chaotic zones at each separatrix have area that must be accounted for.

##### 7.4.4 Higher-Order Perturbation Theory
As the drive is increased, a variety of new islands emerge, which are not evident in the original Hamiltonian. To find approximations for motion in these regions we can use higher-order perturbation theory. The basic plan is the same as before. At any stage the Hamiltonian (which is perhaps a result of earlier stages of perturbation theory) is expressed as a Poisson series (a multiple-angle Fourier series). The terms that are not resonant in a region of interest are eliminated by a Lie transformation. The remaining resonance terms involve only a single combination of angle and are thus solvable by making a canonical transformation to resonance coordinates. We complete the solution and transform back to the original coordinates.

#page(490)

Let's find a perturbative approximation for the second-order islands visible in [figure 7.10](#figure_7.10) between the /ω_{r}/(/p/) = 0 resonance and the /ω_{r}/(/p/) = −/ω/ resonance. The details are messy, so we will just give a few intermediate results.

This resonance is not near the three primary resonances, so we can use the full generator (#Eqn(chapter007,7.56,7.56)) to eliminate those three primary resonance terms from the Hamiltonian. After this perturbation step the Hamiltonian is too hairy to look at.

We expand the transformed Hamiltonian in Poisson form and divide the terms into those that are resonant and those that are not. The terms that are not resonant can be eliminated by a Lie transform. This Lie transform leaves the resonant terms in the Hamiltonian and introduces an additional distortion to the curves on the surface of section. In this case this additional distortion is small, but very messy to compute, so we will just not include this effect. The resonance Hamiltonian is then (after considerable algebra)

$$\begin{array}{ll} {H_{2:1}\left( {\tau;\theta,t;p,p_{t}} \right)} & \\ {\,\,\,\,\,\,\,\,\, = \frac{p^{2}}{2\alpha} + p_{t} + \frac{\alpha\beta\gamma}{4p^{2}}\frac{\alpha^{2}\omega^{2} + 2\alpha\omega p + 2p^{2}}{\left( {\alpha\omega + p} \right)^{2}}\cos\left( {2\theta + \omega t} \right).} \tag{7.82} \\ \end{array}$$

This is solvable because there is only a single combination of coordinates.

We can get an analytic solution by making the pendulum approximation. The Hamiltonian is already quadratic in the momentum /p/, so all we need to do is evaluate the coefficient of the potential terms at the resonance center /p/_{2:1} = /αω//2. The resonance Hamiltonian, in the pendulum approximation, is

$$\begin{matrix} {H_{2:1}^{\prime}\left( {\tau;\theta,t;p,p_{t}} \right) = \frac{p^{2}}{2\alpha} + \frac{2\beta\gamma}{\alpha\omega^{2}}\cos\left( {2\theta + \omega t} \right).} \tag{7.83} \\ \end{matrix}$$

Carrying out the transformation to the resonance variable /σ/ = 2/θ/ − /ωt/ reduces this to a pendulum Hamiltonian with a single degree of freedom. Combining the analytic solution of this pendulum Hamiltonian with the transformations generated by the full /W/, we get an approximate perturbative solution

$$\begin{matrix} {{({\tau;\theta,t;p,p_{t}})} = {({E_{- \mathit{\epsilon},W}^{\prime}E_{\tau - \tau_{0},H_{2:1}^{''}}E_{\mathit{\epsilon},W}^{\prime}I})}{({\tau_{0};\theta_{0},t_{0};p_{0},{(p_{t})}_{0}})}.} \tag{7.84} \\ \end{matrix}$$

#page(491)

#Image(Art_P1199.jpg,figure_7.13)
#Caption *Figure 7.13* Second-order perturbation theory gives an approximation to the second-order islands near the resonance 2/ω_{r}/(/p/) + /ω/ = 0. #CaptionEnd

A surface of section in the appropriate resonance region using this solution is shown in [figure 7.13](#figure_7.13). Comparing this to the actual surface of section ([figure 7.10](#figure_7.10)), we see that the approximate solution provides a good representation of this resonance motion.

##### 7.4.5 Stability of the Inverted Vertical Equilibrium
As a second application, we use second-order perturbation theory to investigate the inverted vertical equilibrium of the periodically driven pendulum.

Here, the procedure parallels the one just followed, but we focus on a different set of resonance terms. The terms that are slowly varying for the vertical equilibrium are those that involve /θ/ but do not involve /t/, such as cos(/θ/) and cos(2/θ/). So we want to use the generator /W/^{+} + /W/^{−} that eliminates the nonresonant terms involving combinations of /θ/ and /ωt/, while leaving the central resonance. After the Lie transform of the Hamiltonian with this generator, we write the transformed Hamiltonian as a Poisson
#page(492)
series and collect the resonant terms. The transformed resonance Hamiltonian is

$$\begin{array}{ll} {H_{V}^{\prime}\left( {\tau;\theta,t;p,p_{t}} \right)} & \\ {\,\,\,\,\,\,\,\,\, = \frac{p^{2}}{2\alpha} - \beta\cos\theta + \frac{\alpha\gamma^{2}\left( {\alpha^{2}\omega^{2} + p^{2}} \right)}{2\left( {\alpha^{2}\omega^{2} - p^{2}} \right)^{2}}\cos\left( {2\theta} \right) + \cdots.} \tag{7.85} \\ \end{array}$$

[Figure 7.14](#figure_7.14) shows contours of this resonance Hamiltonian $ H_{V}^{\prime}$(top) and a surface of section for the actual driven pendulum (bottom) for the same parameters. The behavior of the resonance Hamiltonian is indistinguishable from that of the actual driven pendulum. The theory does especially well here; there are no nearby resonances because the drive frequency is high.

We can get an analytic estimate for the stability of the inverted vertical equilibrium by carrying out a linear stability analysis of the fixed point /θ/ = /π/, /p/ = 0 of the resonance Hamiltonian. The algebra is somewhat simpler if we first make the pendulum approximation about the resonance center. The resonance Hamiltonian is then approximately

$$\begin{matrix} {H_{V}^{''}\left( {\tau;\theta,t;p,p_{t}} \right) = \frac{p^{2}}{2\alpha} - \beta\cos\theta + \frac{\gamma^{2}}{2\alpha\omega^{2}}\cos\left( {2\theta} \right) + \cdots.} \tag{7.86} \\ \end{matrix}$$

Linear stability analysis of the inverted vertical equilibrium indicates stability for

$$\begin{matrix} {\gamma^{2} > \alpha\beta\omega^{2}.} \tag{7.87} \\ \end{matrix}$$

In terms of the original physical parameters, the vertical equilibrium is linearly stable if

$$\begin{matrix} {\frac{\omega}{\omega_{s}}\frac{A}{l} > \sqrt{2},} \tag{7.88} \\ \end{matrix}$$

where $\omega_{s} = \sqrt{g/l}$, the small-amplitude oscillation frequency. For the vertical equilibrium to be stable, the scaled product of the amplitude of the drive and the drive frequency must be sufficiently large.

This analytic estimate is compared with the behavior of the driven pendulum in [figure 7.15](#figure_7.15). For any given assignment of the parameters, the driven pendulum can be tested for the linear stability of the inverted vertical equilibrium by the methods of chapter 4; this involves determining the roots of the characteristic polynomial for a reference orbit at the resonance center. In the figure the stability of the inverted vertical equilibrium was assessed at each point of a grid of assignments of the parameters. A dot is shown for combinations of parameters that are linearly stable. The diagonal line is the analytic boundary of the region of stability of the inverted equilibrium:$\left( {\omega/\omega_{s}} \right)\left( {A/l} \right) = \sqrt{2}$. We see that the boundary of the region of stability is well approximated by the analytic estimate derived from perturbation theory. Note that for very high drive amplitudes there is another region of instability, which is not captured by this perturbation analysis.

#page(493)

#Image(Art_P1200.jpg,figure_7.14)
#Caption *Figure 7.14* Contours of the resonance Hamiltonian ¶ $ H_{V}^{\prime}$ ¶ , which has been developed to study the stability of the vertical equilibrium, are shown in the upper plot. A corresponding surface of section for the actual driven pendulum is shown in the lower plot. The parameters are /m/ = 1 kg, /l/ = 1 m, /g/ = 9.8 m s^{−2}, /A/ = 0.03 m, and /ω/ = 100/ω_{s}/, where ¶ $\omega_{s} = \sqrt{g/l}$ ¶ . #CaptionEnd

#page(494)

#Image(Art_P1201.jpg,figure_7.15)
#Caption *Figure 7.15* Stability of the inverted vertical equilibrium over a range of parameters. The full parameter space displayed was sampled over a regular grid. The dots indicate parameters for which the actual driven pendulum is linearly stable; nothing is plotted in the case of instability. The diagonal line is the locus of points satisfying ¶ $\left( {\omega/\omega_{s}} \right)\left( {A/l} \right) = \sqrt{2}$ ¶ . #CaptionEnd

### 7.5 Summary
The goal of perturbation theory is to relate aspects of the motions of a given system to those of a nearby solvable system. Perturbation
#page(495)
theory can be used to predict features such as the size and location of the resonance islands and chaotic zones.

With perturbation analysis we obtain an approximation to the evolution of a system by relating the evolution of the system to that of a different system that, when approximated, can be exactly solved. We can carry this exact solution of the approximate problem back to the original system to obtain an approximate solution of our original problem. The strategy of canonical perturbation theory is to make canonical transformations that eliminate terms in the Hamiltonian that impede solution. Formulation of perturbation theory in terms of Lie series is especially convenient.

We can use first-order perturbation theory to analyze the motion of the undriven pendulum as a free rotor to which gravity is added. In this analysis we find that a small denominator in the series limits the range of applicability of the perturbative solution to regions that are away from the resonant oscillation region.

In higher-order perturbation theory for the pendulum we discover the problem of secular terms, terms that produce error that grow with time. The appearance of secular terms can be avoided by keeping track of how the frequencies change as perturbations are included. In canonical perturbation theory secular terms can be avoided by associating the average part of the perturbation with the solvable part of the Hamiltonian.

In carrying out canonical perturbation theory in higher dimensions we find that the problem of small denominators is more serious. Small denominators arise near every commensurability, and commensurabilities are common. Small denominators can be locally avoided near particular commensurabilities by incorporating the offending terms into the solvable part of the Hamiltonian. If the resonances are isolated, the resulting resonance Hamiltonian is still solvable. In many cases the resonance Hamiltonian is well approximated by a pendulum-like Hamiltonian. A global picture can be constructed by stitching together the solutions for each resonance region constructed separately.

If two resonance regions overlap---that is, if the sum of the half-widths of the resonance regions exceeds their separation---then large-scale chaos ensues. The chaotic regions associated with the separatrices of the overlapping resonances become connected. When the resonances are well approximated by pendulum-like resonances a simple analytic criterion for the appearance of large-scale chaos can be developed.

#page(496)

Higher-order perturbative descriptions can be developed to describe islands that do not correspond to particular terms in the Hamiltonian, secondary resonances, bifurcations, and so on. The theory can be extended to describe as much detail as one wishes.

### 7.6 Projects
### Exercise 7.4: Periodically driven pendulum

*a.* Work out the details of the perturbation theory for the primary driven pendulum resonances, as displayed in [figure 7.10](#figure_7.10).

*b.* Work out the details of the perturbation theory for the stability of the inverted vertical equilibrium. Derive the resonance Hamiltonian and plot its contours. Compare these contours to surfaces of section for a variety of parameters.

*c.* Carry out the linear stability analysis leading to equation (#Eqn(chapter007,7.88,7.88)). What is happening in the upper part of [figure 7.15](#figure_7.15)? Why is the system unstable when criterion (#Eqn(chapter007,7.88,7.88)) predicts stability? Use surfaces of section to investigate this parameter regime.

### Exercise 7.5: Spin-orbit coupling

A Hamiltonian for the spin-orbit problem described in [section 2.11.2](chapter002!section_2.11.2) is

$$\begin{array}{lll} {H\left( {t,\theta,p_{\theta}} \right)} & {= \frac{p_{\theta}^{2}}{2C} - \frac{n^{2}\mathit{\epsilon}^{2}C}{4}\frac{a^{3}}{R^{3}\left( t \right)}\cos 2\left( {\theta - f\left( t \right)} \right)} & \\ & {= \frac{p_{\theta}^{2}}{2C} - \frac{n^{2}\mathit{\epsilon}^{2}C}{4}(\cos\left( {2\theta - 2nt} \right) + \frac{7e}{2}\cos\left( {2\theta - 3nt} \right)} & \\ & {\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\, - \frac{e}{2}\cos\left( {2\theta - nt} \right) + \cdots)} \tag{7.89} \\ \end{array}$$

where the ignored terms are higher order in eccentricity /e/. Note that here /ϵ/ is the out-of-roundness parameter.

*a.* Find the widths and centers of the three primary resonances. Compare the predictions for the widths to the island widths seen on surfaces of section. Write the criterion for resonance overlap and compare to numerical experiments for the transition to large-scale chaos.

*b.* The fixed point of the synchronous island is offset from the average rate of rotation. This is indicative of a “forced” oscillation of the rotation of the Moon. Develop a perturbative theory for motion in the synchronous island by using a Lie transform to eliminate the two non-synchronous resonances. Predict the location of the fixed point at the center of the synchronous resonance on the surface of section, and thus predict the amplitude of the forced oscillation of the Moon.

----

#FootnoteRef(1)The “width” is measured as the range of momenta.

#FootnoteRef(2)In general, we need to include sine terms as well, but the cosine expansion is enough for this illustration.

#FootnoteRef(3)Any linearly independent combination will be acceptable here.

#FootnoteRef(4)For /W/_{+} see equations #Eqn(chapter007,7.74,7.74) and #Eqn(chapter007,7.75,7.75); for the general relationship between a term in the generator and the coordinate transformation generated see equations #Eqn(chapter007,7.48,7.48) and #Eqn(chapter007,7.49,7.49).
#FootnoteEnd

 
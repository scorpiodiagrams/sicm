!!Polyglot
## Canonical Transformations
### Chapter 5
#page(335)
#Quote(We have done considerable mountain climbing. Now we are in the   rarefied atmosphere of theories of excessive beauty and we are nearing   a high plateau on which geometry, optics, mechanics, and wave   mechanics meet on common ground. Only concentrated thinking, and a   considerable amount of re--creation, will reveal the beauty of our   subject in which the last word has not been spoken.)
#Caption Cornelius Lanczos, /The Variational Principles of Mechanics/   [29](bibliography!bib_29),   [p. 229](chapter003!p229) #CaptionEnd

One way to simplify the analysis of a problem is to express it in a form in which the solution has a simple representation. However, it may not be easy to formulate the problem in such a way initially. It is often useful to start by formulating the problem in one way, and then transform it. For example, the formulation of the problem of the motion of a number of gravitating bodies is simple in rectangular coordinates, but it is easier to understand aspects of the motion in terms of orbital elements, such as the semimajor axes, eccentricities, and inclinations of the orbits. The semimajor axis and eccentricity of an orbit depend on both the configuration and the velocity of the body. Such transformations are more general than those that express changes in configuration coordinates. Here we investigate transformations of phase-space coordinates that involve both the generalized coordinates and the generalized momenta.

Suppose we have two different Hamiltonian systems, and suppose the trajectories of the two systems are in one-to-one correspondence. In this case both Hamiltonian systems can be mathematical models of the same physical system. Some questions about the physical system may be easier to answer by reference to one model and others may be easier to answer in the other model. For example, it may be easier to formulate the physical system in one model and to discover a conserved quantity in the other. Canonical transformations are maps between Hamiltonian systems that preserve the dynamics.

#page(336)

A /canonical transformation/ is a phase-space coordinate transformation and an associated transformation of the Hamiltonian such that the dynamics given by Hamilton's equations in the two representations describe the same evolution of the system.

### 5.1 Point Transformations
A /point transformation/ is a canonical transformation that extends a possibly time-dependent transformation of the configuration coordinates to a phase-space transformation. For example, one might want to reexpress motion in terms of polar coordinates, given a description in terms of rectangular coordinates. In order to extend a transformation of the configuration coordinates to a phase-space transformation we must specify how the momenta and Hamiltonian are transformed.

We have already seen how coordinate transformations can be carried out in the Lagrangian formulation (see [section 1.6.1](chapter001!section_1.6.1)). In that case, we found that if the Lagrangian transforms by composition with the coordinate transformation, then the Lagrange equations are equivalent.

Lagrangians that differ by the addition of a total time derivative have the same Lagrange equations, but may have different momenta conjugate to the generalized coordinates. So there is more than one way to make a canonical extension of a coordinate transformation.

Here, we find the particular canonical extension of a coordinate transformation for which the Lagrangians transform by composition with the transformation, with no extra total time derivative terms added to the Lagrangian.

Let /L/ be a Lagrangian for a system. Consider the coordinate transformation /q/ = /F/ (/t/, /q/′). The velocities transform by

$$\begin{matrix} {v = \partial_{0}F\left( {t,q\prime} \right) + \partial_{1}F\left( {t,q\prime} \right)v\prime.} \tag{5.1} \\ \end{matrix}$$

We obtain a Lagrangian /L/′ in the transformed coordinates by composition of /L/ with the coordinate transformation. We require that /L/′(/t/, /q/′, /v/′) = /L/(/t/, /q/, /v/), so:

$$\begin{matrix} \begin{matrix} {L\prime\left( {t,q\prime,v\prime} \right) = L\left( {t,F\left( {t,q\prime} \right),\partial_{0}F\left( {t,q\prime} \right) + \partial_{1}F\left( {t,q\prime} \right)v\prime} \right).} \tag{5.2} \\ \end{matrix} \\ \end{matrix}$$

#page(337)

The momentum conjugate to /q/′ is

$$\begin{array}{lll} {p\prime} & {= \partial_{2}L\prime\left( {t,q\prime,v\prime} \right)} & \\  & {= \partial_{2}L\left( {t,F\left( {t,q\prime} \right),\partial_{0}F\left( {t,q\prime} \right) + \partial_{1}F\left( {t,q\prime} \right)v\prime} \right)\partial_{1}F\left( {t,q\prime} \right)} & \\  & {= p\partial_{1}F\left( {t,q\prime} \right),} \tag{5.3} \\ \end{array}$$

where we have used

$$\begin{array}{lll} p & {= \partial_{2}L\left( {t,q,v} \right)} & \\  & {= \partial_{2}L\left( {t,F\left( {t,q\prime} \right),\partial_{0}F\left( {t,q\prime} \right) + \partial_{1}F\left( {t,q\prime} \right)v\prime} \right).} \tag{5.4} \\ \end{array}$$

So, from equation (#Eqn(chapter005,5.3,5.3)#Footnote(1)) 

$$\begin{array}{ll} {p = p\prime\left( {\partial_{1}F\left( {t,q\prime} \right)} \right)^{- 1}.} \tag{5.5} \\ \end{array}$$

We can collect these results to define a canonical phase-space transformation /C/_{H}:#Footnote(2)

$$\begin{array}{lll} \left( {t,q,p} \right) & {= C_{\text{H}}\left( {t,q\prime,p\prime} \right)} & \\  & {= (t,F(t,q\prime),p\prime{(\partial_{1}F(t,q\prime))}^{- 1}).} \tag{5.6} \\ \end{array}$$

The Hamiltonian is obtained by the Legendre transform

$$\begin{array}{ll} {H\prime\left( {t,q\prime,p\prime} \right)} & \\ {\,\,\,\,\,\,\, = p\prime v\prime - L\prime\left( {t,q\prime,v\prime} \right)} & \\ {\,\,\,\,\,\,\, = (p\partial_{1}F(t,q\prime))((\partial_{1}F{(t,q\prime)}^{- 1}(v - \partial_{0}F(t,q\prime)))) - L(t,q,v)} & \\ {\,\,\,\,\,\,\, = pv - L(t,q,v) - p\partial_{0}F\left( {t,q\prime} \right)} & \\ {\,\,\,\,\,\,\, = H(t,q,p) - p\partial_{0}F\left( {t,q\prime} \right),} \tag{5.7} \\ \end{array}$$

using relations (#Eqn(chapter005,5.1,5.1)) and (#Eqn(chapter005,5.3,5.3)) in the second step. Fully expressed in terms of the transformed coordinates and momenta, the transformed
#page(338)
Hamiltonian is

$$\begin{array}{lll} {H\prime\left( {t,q\prime,p\prime} \right) =} & {H(t,F(t,q\prime),p\prime{(\partial_{1}F(t,q\prime))}^{- 1})} & \\  & {- (p\prime{(\partial_{1}F(t,q\prime))}^{- 1})\partial_{0}F\left( {t,q\prime} \right).} \tag{5.8} \\ \end{array}$$

The Hamiltonians /H/′ and /H/ are equivalent because /L/ and /L/′ have the same value for a given dynamical state and so have the same paths of stationary action. In general /H/ and /H/′ do not have the same values for a given dynamical state, but differ by a term that depends on the coordinate transformation.

For time-independent transformations, ∂_{0}/F/ = 0, there are a number of simplifications. The relationship of the velocities (#Eqn(chapter005,5.1,5.1)) becomes

$$\begin{array}{ll} {v = \partial_{1}F\left( {t,q\prime} \right)v\prime.} \tag{5.9} \\ \end{array}$$

Comparing this to the relation (#Eqn(chapter005,5.5,5.5)) between the momenta, we see that in this case the momenta transform “oppositely” to the velocities#Footnote(3)

$$\begin{array}{ll} {pv = p\prime\left( {\partial_{1}F\left( {t,q\prime} \right)} \right)^{- 1}\partial_{1}F\left( {t,q\prime} \right)v\prime = p\prime v\prime,} \tag{5.10} \\ \end{array}$$

so the product of the momenta and the velocities is not changed by the transformation. This, combined with the fact that by construction /L/(/t/, /q/, /v/) = /L/′(/t/, /q/′, /v/′), shows that

$$\begin{array}{lll} {H(t,q,p)} & {= pv - L(t,q,v)} & \\  & {= p\prime v\prime - L\prime\left( {t,q\prime,v\prime} \right)} & \\  & {= H\prime\left( {t,q\prime,p\prime} \right).} \tag{5.11} \\ \end{array}$$

For time-independent coordinate transformations the Hamiltonian transforms by composition with the associated phase-space transformation. We can also see this from the general relationship (#Eqn(chapter005,5.7,5.7)) between the Hamiltonians.

#page(339)

#### Implementing point transformations
The procedure F->CH takes a procedure F implementing a transformation of configuration coordinates and returns a procedure implementing a transformation of phase-space coordinates:#Footnote(4)
```Scheme
(define ((F->CH F) state) (up (time state) (F state) (solve-linear-right (momentum state) (((partial 1) F) state))))
```
Consider a particle moving in a central field. In rectangular coordinates a Hamiltonian is
```Scheme
(define ((H-central m V) state) (let ((x (coordinate state)) (p (momentum state))) (+ (/ (square p) (* 2 m)) (V (sqrt (square x)))))) 
```
Let's look at this Hamiltonian in polar coordinates. The phase-space transformation is obtained by applying F->CH to the procedure p->r that takes a time and a polar tuple and returns a tuple of rectangular coordinates (see [section 1.6.1](chapter001!section_1.6.1)). The transformation is time independent so the Hamiltonian transforms by composition. In polar coordinates the Hamiltonian is
```Scheme
(show-expression ((compose (H-central 'm (literal-function 'V)) (F->CH p->r)) (up 't (up 'r 'phi) (down 'p_r 'p_phi)))) 
```

$$ V(r) + \frac{\frac{1}{2}p_{r}^{2}}{m} + \frac{\frac{1}{2}p_{\varphi}^{2}}{mr^{2}}$$

There are three terms. There is the potential energy, which depends on the radius, there is the kinetic energy due to radial motion, and there is the kinetic energy due to tangential motion. As expected, the angle /φ/ does not appear and thus the angular momentum
#page(340)
is a conserved quantity. By going to polar coordinates we have decoupled one of the two degrees of freedom in the problem.

If the transformation is time varying the Hamiltonian must be adjusted by adding a correction to the composition of the Hamiltonian and the transformation (see equation #Eqn(chapter005,5.8,5.8)):

$$\begin{array}{ll} {H\prime = H \circ C_{\text{H}} + K} \tag{5.12} \\ \end{array}$$

The correction is computed by
```Scheme
(define ((F->K F) state) (- (* (solve-linear-right (momentum state) (((partial 1) F) state)) (((partial 0) F) state)))) 
```
For example, consider a transformation to coordinates translating with velocity /v/:
```Scheme
(define ((translating v) state) (+ (coordinates state) (* v (time state)))) 
```
We compute the additive adjustment required for the Hamiltonian:
```Scheme
((F->K (translating (up 'v^x 'v^y 'v^z))) (up 't (up 'x 'y 'z) (down 'p_x 'p_y 'p_z))) 
```
```Scheme
(+ (* -1 p_x v^x) (* -1 p_y v^y) (* -1 p_z v^z))
```
Notice that this is the negation of the inner product of the momentum and the velocity of the coordinate system.

Let's see how a simple free-particle Hamiltonian is transformed:
```Scheme
(define ((H-free m) s) (/ (square (momentum s)) (* 2 m))) 
```
The transformed Hamiltonian is:
```Scheme
(define H-prime (+ (compose (H-free 'm) (F->CH (translating (up 'v^x 'v^y 'v^z)))) (F->K (translating (up 'v^x 'v^y 'v^z))))) 
```
```Scheme
(H-prime (up 't (up 'xprime 'yprime 'zprime) (down 'pprime_x 'pprime_y 'pprime_z))) (+ (* -1 pprime_x v^x) (* -1 pprime_y v^y) (* -1 pprime_z v^z) (/ (* 1/2 (expt pprime_x 2)) m) (/ (* 1/2 (expt pprime_y 2)) m) (/ (* 1/2 (expt pprime_z 2)) m)) 
```
### Exercise 5.1: Galilean invariance

Is this result what you expected? Let's investigate.

Recall that in [exercise 1.29](chapter001!exercise_1.29) we showed that if the kinetic energy is $\frac{1}{2}mv^{2}$ then the translation to a uniformly moving coordinate system introduces extra terms that can be identified as a total time derivative. Since these terms do not affect the Lagrange equations, we can take the kinetic energy in the transformed coordinates to also be $\frac{1}{2}m\left( v\prime \right)^{2}$.

Let /C/_{H} be the phase space extension of the translation transformation, and /C/ be the local tuple extension. The transformed Hamiltonian is /H/′ = /H/ ∘ /C/_{H} + /K/; the transformed Lagrangian is /L/′ = /L/ ∘ /C/.

*a.* Derive the relationship between /p/ and /p/′ both from /C/_{H} and from the Lagrangians. Are they the same? Derive the relationship between /v/ and /v/′ by taking the derivative of the Hamiltonians with respect to the momenta (Hamilton's equation). Show that the Legendre transform of /L/′ gives the same /H/′.

*b.* We have shown that /L/ and /L/′ differ by a total time derivative. So for any uniformly moving coordinate system we can write the Lagrangian as $\frac{1}{2}mv^{2}$. Similarly, we would expect to always be able to write the Hamiltonian as /p/^{2}/(2/m/). Show that this differs from /H/′ by a total time derivative in the corresponding Lagrangians.

### Exercise 5.2: Rotations

Let /q/ and /q/′ be rectangular coordinates that are related by a rotation /R/: /q/ = /Rq/′. The Lagrangian for the system is $ L(t,q,v) = \frac{1}{2}mv^{2} - V(q)$. Find the corresponding phase-space transformation /C/_{H}. Compare the transformation equations for the rectangular components of the momenta to those for the rectangular components of the velocities. Are you surprised, considering equation (#Eqn(chapter005,5.10,5.10))?

#page(342)

### 5.2 General Canonical Transformations
Although we have shown how to extend any coordinate transformation of the configuration space to a canonical transformation, there are other ways to construct canonical transformations. How do we know if we have a canonical transformation? To test if a transformation is canonical we may use the fact that if the transformation is canonical, then Hamilton's equations of motion for the transformed system and the original system will be equivalent.

Consider a Hamiltonian /H/ and a phase-space transformation /C/_{H}. Let /D_{s}/ be the function that takes a Hamiltonian and gives the Hamiltonian state-space derivative:#Footnote(5)

$$\begin{array}{ll} {D_{s}H(t,q,p) = (1,\partial_{2}H(t,q,p), - \partial_{1}H(t,q,p)).} \tag{5.13} \\ \end{array}$$

Hamilton's equations are

$$\begin{array}{ll} {D\sigma = D_{s}H \circ \sigma,} \tag{5.14} \\ \end{array}$$

for any realizable phase-space path /σ/.

The transformation /C/_{H} transforms the phase-space path /σ/′ (/t/) = (/t/, /q/′ (/t/), /p/′ (/t/)) into /σ/(/t/) = (/t/, /q/(/t/), /p/(/t/)):

$$\begin{array}{ll} {\sigma = C_{\text{H}} \circ \sigma\prime.} \tag{5.15} \\ \end{array}$$

The rates of change of the phase-space coordinates are transformed by the derivative of the transformation

$$\begin{array}{ll} {D\sigma = D\left( {C_{\text{H}} \circ \sigma\prime} \right) = \left( {DC_{\text{H}} \circ \sigma\prime} \right)D\sigma\prime.} \tag{5.16} \\ \end{array}$$

The transformation is canonical if the equations of motion obtained from the new Hamiltonian are the same as those that could be obtained by transforming the equations of motion derived from the original Hamiltonian to the new coordinates:

$$\begin{array}{ll} {D\sigma = \left( {DC_{\text{H}} \circ \sigma\prime} \right)D\sigma\prime = \left( {DC_{\text{H}} \circ \sigma\prime} \right)\left( {D_{s}H\prime \circ \sigma\prime} \right).} \tag{5.17} \\ \end{array}$$

Using equation (#Eqn(chapter005,5.14,5.14)), we see that

$$\begin{array}{ll} {D_{s}H \circ \sigma = \left( {DC_{\text{H}} \circ \sigma\prime} \right)\left( {D_{s}H\prime \circ \sigma\prime} \right).} \tag{5.18} \\ \end{array}$$

#page(343)

#Image(Art_P907.jpg,figure_5.1)
#Caption *Figure 5.1* A canonical transformation /C/_{H} relates the descriptions of a dynamical system in two phase-space coordinate systems. The transformation shows how Hamilton's equations in one coordinate system may be derived from Hamilton's equations in the other coordinate system. #CaptionEnd

With /σ/ = /C/_{H} ∘ /σ/′, we find

$$\begin{array}{ll} {D_{s}H \circ C_{\text{H}} \circ \sigma\prime = \left( {DC_{\text{H}} \circ \sigma\prime} \right)\left( {D_{s}H\prime \circ \sigma\prime} \right).} \tag{5.19} \\ \end{array}$$

This condition must hold for any realizable phase-space path /σ/′. Certainly this is true if the following condition holds for every phase-space point:#Footnote(6)

$$\begin{array}{ll} {D_{s}H \circ C_{\text{H}} = DC_{\text{H}} \cdot D_{s}H\prime.} \tag{5.20} \\ \end{array}$$

Any transformation that satisfies equation (#Eqn(chapter005,5.20,5.20)) is a canonical transformation among phase-space representations of a dynamical system. In one phase-space representation the system's dynamics is characterized by the Hamiltonian /H/′ and in the other by /H/. The idea behind this equation is illustrated in [figure 5.1](#figure_5.1).

#page(344)

We can formalize this test as a program:
```Scheme
(define (canonical? C H Hprime) (- (compose (Hamiltonian->state-derivative H) C) (* (D C) (Hamiltonian->state-derivative Hprime)))) 
```
where Hamiltonian->state-derivative, which was introduced in chapter 3, implements /D_{s}/. The transformation is canonical if these residuals are zero.

For time-independent point transformations an appropriate Hamiltonian can be formed by composition with the corresponding phase-space transformation. For more general canonical transformations, we will see that if a transformation is independent of time, a suitable Hamiltonian for the transformed system can be obtained by composing the Hamiltonian with the phase-space transformation. In this case we obtain a more specific formula:

$$\begin{array}{ll} {D_{s}H \circ C_{\text{H}} = DC_{\text{H}} \cdot D_{s}(H \circ C_{\text{H}}).} \tag{5.21} \\ \end{array}$$

#### Polar-canonical transformation
The analysis of the harmonic oscillator illustrates the use of a general canonical transformation in the solution of a problem. The harmonic oscillator is a mathematical model of a simple spring-mass system. A Hamiltonian for a spring-mass system with mass /m/ and spring constant /k/ is

$$\begin{array}{ll} {H(t,x,p_{x}) = \frac{p_{x}^{2}}{2m} + \frac{1}{2}kx^{2}.} \tag{5.22} \\ \end{array}$$

Hamilton's equations of motion are

$$\begin{array}{ll} {Dx = {p_{x}/m}} & \\ {Dp_{x} = - kx,} \tag{5.23} \\ \end{array}$$

giving the second-order system

$$\begin{array}{ll} {mD^{2}x + kx = 0.} \tag{5.24} \\ \end{array}$$

The solution is

$$\begin{array}{ll} {x(t) = A\,\sin(\omega t + \varphi),} \tag{5.25} \\ \end{array}$$

#page(345)

where

$$\begin{array}{ll} {\omega = \sqrt{k/m}} \tag{5.26} \\ \end{array}$$

and where /A/ and /φ/ are determined by initial conditions.

We use the polar-canonical transformation:

$$\begin{array}{ll} {(t,x,p_{x}) = C_{\alpha}(t,\theta,I)} \tag{5.27} \\ \end{array}$$

where

$$\begin{array}{ll} {x = \sqrt{\frac{2I}{\alpha}}\sin\,\theta} \tag{5.28} \\ \end{array}$$

$$\begin{array}{ll} {p_{x} = \sqrt{2\alpha I}\,\cos\,\theta.} \tag{5.29} \\ \end{array}$$

Here /α/ is an arbitrary parameter. We define:
```Scheme
(define ((polar-canonical alpha) state) (let ((t (time state)) (theta (coordinate state)) (I (momentum state))) (let ((x (* (sqrt (/ (* 2 I) alpha)) (sin theta))) (p_x (* (sqrt (* 2 alpha I)) (cos theta)))) (up t x p_x)))) 
```
And now we just run our test:
```Scheme
(define ((H-harmonic m k) s) (+ (/ (square (momentum s)) (* 2 m)) (* 1/2 k (square (coordinate s))))) ((canonical? (polar-canonical 'alpha) (H-harmonic 'm 'k) (compose (H-harmonic 'm 'k) (polar-canonical 'alpha))) (up 't 'theta 'I)) 
```
```Scheme
(up 0 0 0) 
```
So the transformation is canonical for the harmonic oscillator.#Footnote(7)

#page(346)

Let's use our polar-canonical transformation /C_{α}/ to help us solve the harmonic oscillator. We substitute expressions (#Eqn(chapter005,5.28,5.28)) and (#Eqn(chapter005,5.29,5.29)) for /x/ and /p_{x}/ in the Hamiltonian, getting our new Hamiltonian:

$$\begin{array}{ll} {H\prime(t,\theta,I) = \frac{\alpha I}{m}{(\cos\,\theta)}^{2} + \frac{kI}{\alpha}{(\sin\,\theta)}^{2}.} \tag{5.30} \\ \end{array}$$

If we choose $\alpha = \sqrt{km}$ then we obtain

$$\begin{array}{ll} {H\prime(t,\theta,I) = \sqrt{\frac{k}{m}}I = \omega I,} \tag{5.31} \\ \end{array}$$

and the new Hamiltonian no longer depends on the coordinate. Hamilton's equation for /I/ is

$$\begin{array}{ll} {DI(t) = - \partial_{1}H\prime(t,\theta(t),I(t)) = 0,} \tag{5.32} \\ \end{array}$$

so /I/ is constant. The equation for /θ/ is

$$\begin{array}{ll} {D\theta(t) = \partial_{2}H\prime(t,\theta(t),I(t)) = \omega,} \tag{5.33} \\ \end{array}$$

so

$$\begin{array}{ll} {\theta(t) = \omega t + \varphi.} \tag{5.34} \\ \end{array}$$

In the original variables,

$$\begin{array}{lll} {x(t)} & {= \sqrt{{2I(t)}/\alpha}\,{\sin\,\theta(t)}} & \\  & {= A\,\sin(\omega t + \varphi),} \tag{5.35} \\ \end{array}$$

with the constant $ A = \sqrt{{2I(t)}/\alpha}$. So we have found the solution to the problem by making a canonical transformation to new phase-space variables for which the solution is easy and then transforming the solutions back to the original variables.

### Exercise 5.3: Trouble in Lagrangian world

Is there a Lagrangian /L/′ that corresponds to the harmonic oscillator Hamiltonian /H/′(/t/, /θ/, /I/) = /ωI/? What could this possibly mean?

### Exercise 5.4: Group properties

If we say that /C/_{H} is canonical with respect to Hamiltonians /H/ and /H/′ if and only if /D/_{s}/H/ ∘ /C/_{H} = /DC/_{H} · /D/_{s}/H/′, then:

*a.* Show that the composition of canonical transformations is canonical.

*b.* Show that composition of canonical transformations is associative.

#page(347)

*c.* Show that the identity transformation is canonical.

*d.* Show that there is an inverse for a canonical transformation and the inverse is canonical.

##### 5.2.1 Time-Dependent Transformations
We have seen that for time-dependent point transformations the Hamiltonian appropriate for the transformed system is the original Hamiltonian composed with the transformation and augmented with an additive correction. Here we find a similar decomposition for general time-dependent canonical transformations.

The key to this decomposition is to separate the time part and the phase-space part of the Hamiltonian state derivative:#Footnote(8)

$$\begin{array}{lll} {D_{s}H(s)} & {= (1, + \partial_{2}H(s), - \partial_{1}H(s))} & \\  & {= T(s) + \mathcal{D}H(s)} \tag{5.36} \\ \end{array}$$

where

$$\begin{array}{ll} {T(s) = (1,0,0),} \tag{5.37} \\ \end{array}$$

$$\begin{array}{ll} {\mathcal{D}H(s) = (0, + \partial_{2}H(s), - \partial_{1}H(s)),} \tag{5.38} \\ \end{array}$$

as code:#Footnote(9)
```Scheme
(define (T-func s) (up 1 (zero-like (coordinates s)) (zero-like (momenta s)))) (define ((D-phase-space H) s) (up 0 (((partial 2) H) s) (- (((partial 1) H) s)))) 
```
If we assume that /H/′ = /H/ ∘ /C/_{H} + /K/, then the canonical condition (#Eqn(chapter005,5.20,5.20)) becomes

$$\begin{array}{ll} {D_{s}H \circ C_{\text{H}} = DC_{\text{H}} \cdot D_{s}(H \circ C_{\text{H}} + K).} \tag{5.39} \\ \end{array}$$

Expanding the state derivative, the canonical condition is

$$\begin{array}{ll} {(T + \mathcal{D}H) \circ C_{\text{H}} = DC_{\text{H}} \cdot (T + \mathcal{D}(H \circ C_{\text{H}} + K)).} \tag{5.40} \\ \end{array}$$

#page(348)

Equation (#Eqn(chapter005,5.40,5.40)) is satisfied if the following conditions are met:

$$\begin{array}{ll} {\mathcal{D}H \circ C_{\text{H}} = DC_{\text{H}} \cdot \mathcal{D}(H \circ C_{\text{H}})} \tag{5.41} \\ \end{array}$$

$$\begin{array}{ll} {T \circ C_{\text{H}} = DC_{\text{H}} \cdot (T + \mathcal{D}K).} \tag{5.42} \\ \end{array}$$

The value of /T/ ∘ /C/_{H} does not depend on /C/_{H}, so this term is really very simple. Notice that equation (#Eqn(chapter005,5.41,5.41)) does not depend upon /K/ and that equation (#Eqn(chapter005,5.42,5.42)) does not depend upon /H/.

These can be implemented as follows:
```Scheme
(define (canonical-H? C H) (- (compose (D-phase-space H) C) (* (D C) (D-phase-space (compose H C))))) (define (canonical-K? C K) (- (compose T-func C) (* (D C) (+ T-func (D-phase-space K))))) 
```
#### Rotating coordinates
Consider a time-dependent transformation to uniformly rotating coordinates:#Footnote(10)

$$\begin{array}{ll} {q = R(\Omega)\left( {t,q\prime} \right),} \tag{5.43} \\ \end{array}$$

with components

$$\begin{array}{ll} {x = x\prime\,\cos(\Omega t) - y\prime\,\sin(\Omega t)} & \\ {y = x\prime\,\sin(\Omega t) + y\prime\,\cos(\Omega t).} \tag{5.44} \\ \end{array}$$

As a program this is
```Scheme
(define ((rotating Omega) state) (let ((t (time state)) (qp (coordinate state))) (let ((xp (ref qp 0)) (yp (ref qp 1)) (zp (ref qp 2))) (up (- (* (cos (* Omega t)) xp) (* (sin (* Omega t)) yp)) (+ (* (sin (* Omega t)) xp) (* (cos (* Omega t)) yp)) zp)))) 
```
The extension of this transformation to a phase-space transformation is
```Scheme
(define (C-rotating Omega) (F->CH (rotating Omega))) 
```
We first verify that this time-dependent transformation satisfies equation (#Eqn(chapter005,5.41,5.41)). We will try it for an arbitrary Hamiltonian with three degrees of freedom:
```Scheme
(define H-arbitrary (literal-function 'H (-> (UP Real (UP Real Real Real) (DOWN Real Real Real)) Real))) ((canonical-H? (C-rotating 'Omega) H-arbitrary) (up 't (up 'xp 'yp 'zp) (down 'pp_x 'pp_y 'pp_z))) (up 0 (up 0 0 0) (down 0 0 0)) 
```
And it works. Note that this result did not depend on any details of the Hamiltonian, suggesting that we might be able to make a test that does not require a Hamiltonian. We will see that shortly.

Since we have a point transformation, we can compute the required adjustment to the Hamiltonian:
```Scheme
((F->K (rotating 'Omega)) (up 't (up 'xp 'yp 'zp) (down 'pp_x 'pp_y 'pp_z))) (+ (* Omega pp_x yp) (* -1 Omega pp_y xp)) 
```
So, for this transformation an appropriate correction to the Hamiltonian is

$$\begin{array}{ll} {K(\Omega)\left( {t;x\prime,y\prime,z\prime;p_{x}^{\prime},p_{y}^{\prime},p_{z}^{\prime}} \right) = - \Omega\left( {x\prime p_{y}^{\prime} - y\prime p_{x}^{\prime}} \right),} \tag{5.45} \\ \end{array}$$

which is minus the rate of rotation of the coordinate system multiplied by the angular momentum. We implement /K/ as a procedure
```Scheme
(define ((K Omega) s) (let ((qp (coordinate s)) (pp (momentum s))) (let ((xp (ref qp 0)) (yp (ref qp 1)) (ppx (ref pp 0)) (ppy (ref pp 1))) (* -1 Omega (- (* xp ppy) (* yp ppx)))))) 
```
and apply the test. We find:
```Scheme
((canonical-K? (C-rotating 'Omega) (K 'Omega)) (up 't (up 'xp 'yp 'zp) (down 'pp_x 'pp_y 'pp_z))) (up 0 (up 0 0 0) (down 0 0 0)) 
```
The residuals are zero so this /K/ correctly completes the canonical transformation.

#page(350)

##### 5.2.2 Abstracting the Canonical Condition
We just saw that for the case of rotating coordinates the truth of equation (#Eqn(chapter005,5.41,5.41)) did not depend on the details of the Hamiltonian. If /C/_{H} satisfies equation (#Eqn(chapter005,5.41,5.41)) for any /H/ then we can derive a condition on /C/_{H} that is independent of /H/.

Let's start with an expanded version of equation (#Eqn(chapter005,5.41,5.41)):

$$\begin{array}{ll} {\mathcal{D}H \circ C_{\text{H}} = DC_{\text{H}} \cdot ((\mathcal{D}H \circ C_{\text{H}}) \cdot DC_{\text{H}}),} \tag{5.46} \\ \end{array}$$

using the chain rule.

We introduce a shuffle function:

$$\begin{array}{ll} {\widetilde{J}(\lbrack a,b,c\rbrack) = (0,c, - b).} \tag{5.47} \\ \end{array}$$

The argument to $\widetilde{J}$ is a down tuple of components of the derivative of a Hamiltonian-like function. The shuffle function is linear. Using $\widetilde{J}$ we can write $\mathcal{D}H = \widetilde{J} \circ DH $.

Let /J/ be the multiplier corresponding to the constant linear function $\widetilde{J}$:

$$\begin{array}{ll} {J = (D\widetilde{J})(s^{\star}),} \tag{5.48} \\ \end{array}$$

where /s/^{⋆} is an arbitrary argument, shaped like /DH/(/s/), that is compatible for multiplication with /s/. The value of /s/^{⋆} is irrelevant because /D/$\widetilde{J}$ is a constant function. Then we can rewrite equation (#Eqn(chapter005,5.46,5.46)) as

$$\begin{array}{ll} {J \cdot DH(C_{\text{H}}(s\prime)) = DC_{\text{H}}(s\prime) \cdot J \cdot (DH(C_{\text{H}}(s\prime)) \cdot DC_{\text{H}}(s\prime)).} \tag{5.49} \\ \end{array}$$

We can move the /DC/_{H}(/s/′) to the left of /DH/(/C/_{H}(/s/′)) by taking its transpose:#Footnote(11)

$$\begin{array}{ll} {J \cdot DH(C_{\text{H}}(s\prime))} & \\ {\,\,\,\,\,\,\, = DC_{\text{H}}(s\prime) \cdot J \cdot ({(DC_{\text{H}}(s\prime))}^{\mathcal{T}} \cdot DH(C_{\text{H}}(s\prime))).} \tag{5.50} \\ \end{array}$$

#page(351)

Since ${(DC_{H}(s\prime))}^{\mathcal{T}}$ is a linear transformation and multiplication is associative for the multipliers of linear transformations, we can write

$$\begin{array}{ll} {J \cdot DH(C_{\text{H}}(s\prime)) = DC_{\text{H}}(s\prime) \cdot J \cdot {(DC_{\text{H}}(s\prime))}^{\mathcal{T}} \cdot DH(C_{\text{H}}(s\prime)).} \tag{5.51} \\ \end{array}$$

This is true for any /H/ if

$$\begin{array}{ll} {J = DC_{\text{H}}(s\prime) \cdot J \cdot {(DC_{\text{H}}(s\prime))}^{\mathcal{T}}.} \tag{5.52} \\ \end{array}$$

As a program, this is: #Footnote(12)^{-}#Footnote(13)
```Scheme
(define (J-func DHs) (up 0 (ref DHs 2) (- (ref DHs 1)))) (define ((canonical-transform? C) s) (let ((J ((D J-func) (compatible-shape s))) (DCs ((D C) s))) (- J (* DCs J (transpose DCs s))))) 
```
This condition, equation (#Eqn(chapter005,5.52,5.52)), on /C/_{H}, called the /canonical condition/, does not depend on the details of /H/. This is a remarkable result: we can decide whether a phase-space transformation preserves the dynamics of Hamilton's equations without further reference to the details of the dynamical system. If the transformation is time dependent we can add a correction to the Hamiltonian to make it canonical.

#### Examples
The polar-canonical transformation satisfies the canonical condition:
```Scheme
((canonical-transform? (polar-canonical 'alpha)) (up 't 'theta 'I)) (up (up 0 0 0) (up 0 0 0) (up 0 0 0)) 
```
#page(352)

But not every transformation we might try satisfies the canonical condition. For example, we might try /x/ = /p/ sin /θ/ and /p_{x}/ = /p/ cos /θ/. The implementation is
```Scheme
(define (a-non-canonical-transform state) (let ((t (time state)) (theta (coordinate state)) (p (momentum state))) (let ((x (* p (sin theta))) (p_x (* p (cos theta)))) (up t x p_x)))) ((canonical-transform? a-non-canonical-transform) (up 't 'theta 'p)) (up (up 0 0 0) (up 0 0 (+ -1 p)) (up 0 (+ 1 (* -1 p)) 0)) 
```
So this transformation does not satisfy the canonical condition.

#### Canonical condition and Poisson brackets
The canonical condition can be written simply in terms of Poisson brackets.

The Poisson bracket can be written in terms of $\widetilde{J}$:

$$\begin{array}{ll} {\left\{ f,g \right\} = (Df) \cdot (\widetilde{J} \circ (Dg)) = (Df) \cdot J \cdot (Dg),} \tag{5.53} \\ \end{array}$$

as can be seen by writing out the components.

We break the transformation /C/_{H} into position and momentum parts:

$$\begin{array}{ll} {q = A(t,q\prime,p\prime)} \tag{5.54} \\ \end{array}$$

$$\begin{array}{ll} {p = B(t,q\prime,p\prime).} \tag{5.55} \\ \end{array}$$

In terms of the individual component functions, the canonical condition (#Eqn(chapter005,5.52,5.52)) is

$$\begin{array}{ll} {\delta_{j}^{i} = \left\{ A^{i},B_{j} \right\}} & \\ {0 = \left\{ A^{i},A^{j} \right\}} & \\ {0 = \left\{ B_{i},B_{j} \right\}} \tag{5.56} \\ \end{array}$$

where $\delta_{j}^{i}$ is 1 if /i/ = /j/ and 0 otherwise. These equations are called the /fundamental Poisson brackets/. If a transformation satisfies these Poisson bracket relations then it satisfies the canonical condition.

#page(353)

We have found that a transformation is canonical if its position-momentum part satisfies the canonical condition, but for a time-dependent transformation we may have to modify the Hamiltonian by the addition of a suitable /K/. We can rewrite these conditions in terms of Poisson brackets. If the Hamiltonian is

$$\begin{array}{ll} {H\prime(t,q\prime,p\prime) = H(t,A(t,q\prime,p\prime),B(t,q\prime,p\prime)) + K(t,q\prime,p\prime),} \tag{5.57} \\ \end{array}$$

the transformation will be canonical if the coordinate-momentum transformation satisfies the fundamental Poisson brackets, and /K/ satisfies:

$$\begin{array}{ll} {\left\{ A^{i},K \right\} + \partial_{0}A^{i} = 0} & \\ {\left\{ B_{j},K \right\} + \partial_{0}B_{j} = 0.} \tag{5.58} \\ \end{array}$$

### Exercise 5.5: Poisson bracket conditions

Fill in the details to show that the canonical condition (#Eqn(chapter005,5.52,5.52)) is equivalent to the fundamental Poisson brackets (#Eqn(chapter005,5.56,5.56)) and that the condition on /K/ (#Eqn(chapter005,5.42,5.42)) is equivalent to the Poisson bracket condition on /K/ (#Eqn(chapter005,5.58,5.58)).

#### Symplectic matrices
It is convenient to reformulate the canonical condition in terms of matrices. We can obtain a matrix representation of a structure with the utility s->m that takes a structure that represents a multiplier of a linear transformation and returns a matrix representation of the multiplier. The procedure s->m takes three arguments: (s->m ls A rs). The ls and rs specify the shapes of objects that multiply A on the left and right to give a numerical value. These specify the basis. So, the matrix representation of the multiplier corresponding to $\widetilde{J}$ is
```Scheme
(let* ((s (up 't (up 'x 'y) (down 'px 'py))) (s* (compatible-shape s)) (J ((D J-func) s*))) (s->m s* J s*)) 
```
```Scheme
(matrix-by-rows (list 0 0 0 0 0) (list 0 0 0 1 0) (list 0 0 0 0 1) (list 0 -1 0 0 0) (list 0 0 -1 0 0)) 
```
This matrix, *J*, is useful, so we supply a procedure J-matrix so that (J-matrix n) gives this matrix for an /n/ degree-of-freedom system.

#page(354)

We can now reexpress the canonical condition (#Eqn(chapter005,5.52,5.52)) as a matrix equation:

$$\begin{array}{ll} {\mathbf{J} = \mathbf{D}\mathbf{C}_{\text{H}}(s\prime) \cdot \mathbf{J} \cdot {(\mathbf{D}\mathbf{C}_{\text{H}}(s\prime))}^{\mathcal{T}}.} \tag{5.59} \\ \end{array}$$

There is a further simplification available. The elements of the first row and the first column of the matrix representation of $\widetilde{J}$ are all zeros. This has simplifying consequences. Consider a general transformation of phase-space states (for two degrees of freedom):
```Scheme
(define C-general (literal-function 'C (-> (UP Real (UP Real Real) (DOWN Real Real)) (UP Real (UP Real Real) (DOWN Real Real))))) 
```
Consider transformations for which the time does not depend on the coordinates or momenta#Footnote(14)
```Scheme
(define (C-simple-time s) (let ((cs (C-general s))) (up ((literal-function 'tau) (time s)) (coordinates cs) (momenta cs)))) 
```
For this kind of transformation the first row and the first column of the residuals of the canonical-transform? test are identically zero:
```Scheme
(let* ((s (up 't (up 'x 'y) (down 'p_x 'p_y))) (s* (compatible-shape s))) (m:nth-row (s->m s* ((canonical-transform? C-simple-time) s) s*) 0)) 
```
```Scheme
(up 0 0 0 0 0) 
```
```Scheme
(let ((s (up 't (up 'x 'y) (down 'p_x 'p_y))) (s* (compatible-shape s))) (m:nth-col (s->m s* ((canonical-transform? C-simple-time) s) s*) 0)) 
```
```Scheme
(up 0 0 0 0 0) 
```
#page(355)

But for C-general these are not zero. Since the transformations we are considering at most shift time, we need to consider only the submatrix associated with the coordinates and the momenta.

The /qp/ submatrix#Footnote(15) of dimension 2/n/ × 2/n/ of the matrix *J* is called the /symplectic unit/ for /n/ degrees of freedom:

$$\begin{array}{ll} {\mathbf{J}_{n} = \left( \begin{array}{ll} \mathbf{0}_{n \times n} & \mathbf{1}_{n \times n} \\ {- \mathbf{1}_{n \times n}} & \mathbf{0}_{n \times n} \\ \end{array} \right).} \tag{5.60} \\ \end{array}$$

The matrix *J*/_{n}/ satisfies the following identities:

$$\begin{array}{ll} {\mathbf{J}_{n}^{\mathcal{T}} = \mathbf{J}_{n}^{- 1} = - \mathbf{J}_{n}.} \tag{5.61} \\ \end{array}$$

A 2/n/ × 2/n/ matrix *A* that satisfies the relation

$$\begin{array}{ll} {\mathbf{J}_{n} = \mathbf{A}\mathbf{J}_{n}\mathbf{A}^{\mathcal{T}}} \tag{5.62} \\ \end{array}$$

is called a /symplectic matrix/. We can determine whether a matrix is symplectic:
```Scheme
(define (symplectic-matrix? M) (let ((2n (m:dimension M))) (let ((J (symplectic-unit (quotient 2n 2)))) (- J (* M J (transpose M)))))) 
```
An appropriate symplectic unit matrix of a given size is produced by the procedure symplectic-unit.

If the matrix representation of the derivative of a transformation is a symplectic matrix the transformation is a /symplectic transformation/. Here is a test for whether a transformation is symplectic:#Footnote(16)
```Scheme
(define ((symplectic-transform? C) s) (symplectic-matrix? (qp-submatrix ((D-as-matrix C) s)))) 
```
#page(356)

The procedure symplectic-transform? returns a zero matrix if and only if the transformation being tested passes the symplectic matrix test.

For example, the point transformations are symplectic. We can show this for a general possibly time-dependent two-degree-of-freedom point transformation:
```Scheme
(define (F s) ((literal-function 'F (-> (X Real (UP Real Real)) (UP Real Real))) (time s) (coordinates s))) ((symplectic-transform? (F->CH F)) (up 't (up 'x 'y) (down 'px 'py))) 
```
```Scheme
(matrix-by-rows (list 0 0 0 0) (list 0 0 0 0) (list 0 0 0 0) (list 0 0 0 0)) 
```
More generally, the phase-space part of the canonical condition is equivalent to the symplectic condition (for two degrees of freedom) even in the case of an unrestricted phase-space transformation.
```Scheme
(let* ((s (up 't (up 'x 'y) (down 'p_x 'p_y))) (s* (compatible-shape s))) (- (qp-submatrix (s->m s* ((canonical-transform? C-general) s) s*)) ((symplectic-transform? C-general) s))) 
```
```Scheme
(matrix-by-rows (list 0 0 0 0) (list 0 0 0 0) (list 0 0 0 0) (list 0 0 0 0)) 
```
### Exercise 5.6: Symplectic matrices

Let *A* be a symplectic matrix:$\mathbf{J}_{n} = \mathbf{A}\mathbf{J}_{n}\mathbf{A}^{\mathcal{T}}$. Show that $\mathbf{A}^{\mathcal{T}}$ and *A*^{−1} are symplectic.

### Exercise 5.7: Polar-canonical transformations

Let /x/, /p/ and /θ/, /I/ be two sets of canonically conjugate variables. Consider transformations of the form /x/ = /βI^{α}/ sin /θ/ and /p/ = /βI^{α}/ cos /θ/. Determine all /α/ and /β/ for which this transformation is symplectic.

#page(357)

### Exercise 5.8: Standard map

Is the standard map a symplectic transformation? Recall that the standard map is: /I/′ = /I/ + /K/ sin /θ/, with /θ/′ = /θ/ + /I/′, both modulo 2/π/.

### Exercise 5.9: Whittaker transform

Shew that the transformation /q/ = log ((sin /p/′)//q/′) with /p/ = /q/′ cot /p/′ is symplectic.

### 5.3 Invariants of Canonical Transformations
Canonical transformations allow us to change the phase-space coordinate system that we use to express a problem, preserving the form of Hamilton's equations. If we solve Hamilton's equations in one phase-space coordinate system we can use the transformation to carry the solution to the other coordinate system. What other properties are preserved by a canonical transformation?

#### Noninvariance of $pv$
We noted in equation (#Eqn(chapter005,5.10,5.10)) that point transformations that are canonical extensions of time-independent coordinate transformations preserve the value of /pv/. This does not hold for more general canonical transformations. We can illustrate this with the polar-canonical transformation. Along corresponding paths /x/, /p_{x}/ and /θ/, /I/

$$\begin{array}{rll} {x(t)} & {= \sqrt{\frac{2I(t)}{\alpha}}\sin\,\theta(t)} & \\ {p_{x}(t)} & {= \sqrt{2I(t)\alpha}\,\cos\,\theta(t),} \tag{5.63} \\ \end{array}$$

and so /Dx/ is

$$\begin{array}{ll} {Dx(t) = D\theta(t)\sqrt{\frac{2I(t)}{\alpha}}\cos\,\theta(t) + DI(t)\frac{1}{\sqrt{2I(t)\alpha}}\sin\,\theta(t).} \tag{5.64} \\ \end{array}$$

The difference of /pv/ and the transformed /p/′/v/′ is

$$\begin{array}{ll} {P_{x}(t)Dx(t) - I(t)D\theta(t)} & \\ {\,\,\,\,\,\,\, = I(t)D\theta(t)\,(2\,{\cos}^{2}\theta(t) - 1) + DI(t)\,\sin\,\theta(t)\,\cos\,\theta(t).} \tag{5.65} \\ \end{array}$$

In general this is not zero. So the product /pv/ is not necessarily invariant under general canonical transformations.

#page(358)

#### Invariance of Poisson brackets
Here is a remarkable fact: the composition of the Poisson bracket of two phase-space state functions with a canonical transformation is the same as the Poisson bracket of each of the two functions composed with the transformation separately. Loosely speaking, the Poisson bracket is invariant under canonical phase-space transformations.

Let /f/ and /g/ be two phase-space state functions. Using the $\widetilde{J}$ representation of the Poisson bracket (see [section 5.2.2](#section_5.2.2)), we deduce

$$\begin{array}{ll} \left\{ f \circ C_{\text{H}},g \circ C_{\text{H}} \right\} & \\ {\,\,\,\,\,\, = (D(f \circ C_{\text{H}})) \cdot (\widetilde{J} \circ D(g \circ C_{\text{H}}))} & \\ {\,\,\,\,\,\, = (Df \circ C_{\text{H}}) \cdot DC_{\text{H}} \cdot (\widetilde{J} \circ ((Dg \circ C_{\text{H}}) \cdot DC_{\text{H}}))} & \\ {\,\,\,\,\,\, = (Df \circ C_{\text{H}}) \cdot (\widetilde{J} \circ Dg \circ C_{\text{H}})} & \\ {\,\,\,\,\,\, = (Df \cdot (\widetilde{J} \circ Dg)) \circ C_{\text{H}}} & \\ {\,\,\,\,\,\, = \left\{ f,g \right\} \circ C_{\text{H}},} \tag{5.66} \\ \end{array}$$

where the fact that /C/_{H} satisfies equation (#Eqn(chapter005,5.41,5.41)) was used in the middle. This is

$$\begin{array}{ll} {\left\{ f \circ C_{\text{H}},g \circ C_{\text{H}} \right\} = \left\{ f,g \right\} \circ C_{\text{H}}.} \tag{5.67} \\ \end{array}$$

#### Volume preservation
Consider a canonical transformation /C/_{H}. Let /Ĉ_{t}/ be a function with parameter /t/ such that (/q/, /p/) = /Ĉ_{t}/(/q/′, /p/′) if (/t/, /q/, /p/) = /C/_{H}(/t/, /q/′, /p/′). The function /Ĉ_{t}/ maps phase-space coordinates to alternate phase-space coordinates at a given time. Consider regions /R/ in (/q/, /p/) and /R/ in (/q/′, /p/′) such that /R/ = /Ĉ_{t}/(/R/′). The volume of region /R/′ is

$$\begin{array}{ll} {V(R) = {\int_{R}\widehat{1}} = {\int_{R\prime}{\det(D{\widehat{C}}_{t}),}}} \tag{5.68} \\ \end{array}$$

where $\widehat{1}$ is the function whose value is one for every input. Now if /C/_{H} is symplectic then the determinant of /DĈ_{t}/ is one (see [section 4.2.3](chapter004!section_4.2.3)), so

$$\begin{array}{ll} {V(R) = V(R\prime).} \tag{5.69} \\ \end{array}$$

Thus, phase-space volume is preserved by symplectic transformations.

#page(359)

Liouville's theorem shows that time evolution preserves phase-space volume. Here we see that canonical transformations also preserve phase volumes. Later, we will find that time evolution actually generates a canonical transformation.

#### The symplectic 2-form
Define

$$\begin{array}{ll} {\omega(\zeta_{1},\zeta_{2}) = P(\zeta_{2})Q(\zeta_{1}) - P(\zeta_{1})Q(\zeta_{2}),} \tag{5.70} \\ \end{array}$$

where /Q/ = /I/_{1} and /P/ = /I/_{2} are the coordinate and momentum selectors, respectively. The arguments /ζ/_{1} and /ζ/_{2} are incremental phase-space states with zero time components.

The /ω/ form can also be written as a sum over degrees of freedom:

$$\begin{array}{ll} {\omega(\zeta_{1},\zeta_{2}) = {\sum\limits_{i}{(P_{i}(\zeta_{2})Q^{i}(\zeta_{1}) - P_{i}(\zeta_{1})Q^{i}(\zeta_{2})).}}} \tag{5.71} \\ \end{array}$$

Notice that the contributions for each /i/ do not mix components from different degrees of freedom.

This bilinear form is closely related to the symplectic 2-form of differential geometry. It differs in that the symplectic 2-form is formally a function of the phase-space point as well as the incremental vectors.

Under a canonical transformation /s/ = /C/_{H}(/s/′), incremental states transform with the derivative

$$\begin{array}{ll} {\zeta_{i} = DC_{\text{H}}(s\prime)\zeta_{i}^{\prime}.} \tag{5.72} \\ \end{array}$$

We will show that the 2-form is invariant under this transformation

$$\begin{array}{ll} {\omega(\zeta_{1},\zeta_{2}) = \omega(\zeta_{1}^{\prime},\zeta_{2}^{\prime}),} \tag{5.73} \\ \end{array}$$

if the time components of the $\zeta_{i}^{\prime}$ are both zero.

We have shown that condition (#Eqn(chapter005,5.41,5.41)) does not depend on the details of the Hamiltonian /H/. So if a transformation satisfies the canonical condition we can use condition (#Eqn(chapter005,5.41,5.41)) with /H/ replaced by an arbitrary function /f/ of phase-space states:

$$\begin{array}{ll} {\mathcal{D}f(C_{\text{H}}(s\prime)) = (DC_{\text{H}}(s\prime)) \cdot (\mathcal{D}(f \circ C_{\text{H}})(s\prime)).} \tag{5.74} \\ \end{array}$$

#page(360)

In terms of /ω/, the Poisson bracket is

$$\begin{array}{ll} {\left\{ f,g \right\}(s) = \omega(\mathcal{D}f(s),\mathcal{D}g(s))} \tag{5.75} \\ \end{array}$$

as can be seen by writing out the components. We use the fact that Poisson brackets are invariant under canonical transformations:

$$\begin{array}{ll} {(\left\{ f,g \right\} \circ C_{\text{H}})(s\prime) = \left\{ f \circ C_{\text{H}},g \circ C_{\text{H}} \right\}(s\prime).} \tag{5.76} \\ \end{array}$$

Using the relation (#Eqn(chapter005,5.74,5.74)) to expand the left-hand side of equation (#Eqn(chapter005,5.76,5.76)) we obtain:

$$\begin{array}{ll} {(\left\{ f,g \right\} \circ C_{\text{H}})(s\prime)} & \\ {\,\,\,\,\,\,\, = \omega((\mathcal{D}f \circ C_{\text{H}})(s\prime),(\mathcal{D}g \circ C_{\text{H}})(s\prime))} & \\ {\,\,\,\,\,\,\, = \omega((DC_{\text{H}}(s\prime)) \cdot (\mathcal{D}(f \circ C_{\text{H}})(s\prime)),} & \\ {\,\,\,\,\,\,\,\,\,\,\,\,\,\,(DC_{\text{H}}(s\prime)) \cdot (\mathcal{D}(g \circ C_{\text{H}})(s\prime))).} \tag{5.77} \\ \end{array}$$

The right-hand side of equation (#Eqn(chapter005,5.76,5.76)) is

$$\begin{array}{ll} {\left\{ f \circ C_{\text{H}},g \circ C_{\text{H}} \right\}(s\prime) = \omega(\mathcal{D}(f \circ C_{\text{H}})(s\prime),\mathcal{D}(g \circ C_{\text{H}})(s\prime)).} \tag{5.78} \\ \end{array}$$

Now the left-hand side must equal the right-hand side for any /f/ and /g/, so the equation must also be true for arbitrary $\zeta_{i}^{\prime}$ of the form

$$\begin{array}{ll} {\zeta_{1}^{\prime} = \mathcal{D}(f \circ C_{\text{H}})(s\prime)} & \\ {\zeta_{2}^{\prime} = \mathcal{D}(g \circ C_{\text{H}})(s\prime).} \tag{5.79} \\ \end{array}$$

So the $\zeta_{i}^{\prime}$ are arbitrary incremental states with zero time components.

We have proven that

$$\begin{array}{ll} {\omega(\zeta_{1}^{\prime},\zeta_{2}^{\prime}) = \omega(DC_{\text{H}}(s\prime) \cdot \zeta_{1}^{\prime},\, DC_{\text{H}}(s\prime) \cdot \zeta_{2}^{\prime}).} \tag{5.80} \\ \end{array}$$

for canonical /C/_{H} and incremental states $\zeta_{i}^{\prime}$ with zero time components. Using equation (#Eqn(chapter005,5.72,5.72)), we have

$$\begin{array}{ll} {\omega(\zeta_{1}^{\prime},\zeta_{2}^{\prime}) = \omega(\zeta_{1},\zeta_{2}).} \tag{5.81} \\ \end{array}$$

Thus the bilinear antisymmetric function /ω/ is invariant under even time-varying canonical transformations if the increments are restricted to have zero time component.

#page(361)

As a program, /ω/ is
```Scheme
(define (omega zeta1 zeta2) (- (* (momentum zeta2) (coordinate zeta1)) (* (momentum zeta1) (coordinate zeta2)))) 
```
On [page 356](chapter005!p356) we showed that point transformations are sym-plectic. Here we can see that the 2-form is preserved under these transformations for two degrees of freedom:
```Scheme
(define (F s) ((literal-function 'F (-> (X Real (UP Real Real)) (UP Real Real))) (time s) (coordinates s))) (let ((s (up 't (up 'x 'y) (down 'p_x 'p_y))) (zeta1 (up 0 (up 'dx1 'dy1) (down 'dp1_x 'dp1_y))) (zeta2 (up 0 (up 'dx2 'dy2) (down 'dp2_x 'dp2_y)))) (let ((DCs ((D (F->CH F)) s))) (- (omega zeta1 zeta2) (omega (* DCs zeta1) (* DCs zeta2))))) 0 
```
Alternatively, let *z*_{1} and *z*_{2} be the matrix representations of the /qp/ parts of /ζ/_{1} and /ζ/_{2}. The matrix representation of /ω/ is

$$\begin{array}{ll} {\omega(\zeta_{1},\zeta_{2}) = \mathbf{z}_{1}^{\mathcal{T}} \cdot \mathbf{J}_{n} \cdot \mathbf{z}_{2}.} \tag{5.82} \\ \end{array}$$

Let *A* be the matrix representation of the /qp/ part of /DC_{H}/(/s/′) Then the invariance of /ω/ is equivalent to

$$\begin{array}{ll} {\mathbf{z}_{1}^{\mathcal{T}} \cdot \mathbf{A}^{\mathcal{T}} \cdot \text{J}_{n} \cdot \mathbf{A} \cdot \mathbf{z}_{2} = \mathbf{z}_{1}^{\mathcal{T}} \cdot \mathbf{J}_{n} \cdot \mathbf{z}_{2}.} \tag{5.83} \\ \end{array}$$

But this is true if

$$\begin{array}{ll} {\mathbf{A}^{\mathcal{T}} \cdot \mathbf{J}_{n} \cdot \mathbf{A} = \mathbf{J}_{n},} \tag{5.84} \\ \end{array}$$

which is equivalent to the condition that *A* is symplectic. (If a matrix is symplectic then its transpose is symplectic. See [exercise 5.6](#exercise_5.6)).

The symplectic condition is symmetrical in that if *A* is symplec-tic then $\mathbf{A}^{\mathcal{T}}$ is symplectic, because the symplectic unit is invertible. The canonical condition

$$\begin{array}{ll} {\mathbf{J} = \mathbf{D}\mathbf{C}_{\text{H}}(s\prime) \cdot \mathbf{J} \cdot {(\mathbf{D}\mathbf{C}_{\text{H}}(s\prime))}^{\mathcal{T}},} \tag{5.85} \\ \end{array}$$

#page(362)

is satisfied by time-varying canonical transformations, and time-varying canonical transformations are symplectic. But if the transformation is time varying then

$$\begin{array}{ll} {\mathbf{J} = {(\mathbf{D}\mathbf{C}_{\text{H}}(s\prime))}^{\mathcal{T}} \cdot \mathbf{J} \cdot \mathbf{D}\mathbf{C}_{\text{H}}(s\prime),} \tag{5.86} \\ \end{array}$$

is not satisfied because *J* is not invertible. Equation (#Eqn(chapter005,5.86,5.86)) is satisfied, however, for time-independent transformations.

#### Poincaré integral invariant
The invariance of the symplectic 2-form under canonical transformations has a simple interpretation. Consider how the area of an incremental parallelogram in phase space transforms under canonical transformation. Let (Δ/q/, Δ/p/) and (/δq/, /δp/) be small increments in phase space, originating at (/q/, /p/). Consider the incremental parallelogram with vertex at (/q/, /p/) with these two phase-space increments as edges. The sum of the areas of the canonical projections of this incremental parallelogram can be written

$$\begin{array}{ll} {\sum\limits_{i}{\Delta A_{i} = {\sum\limits_{i}{(\Delta q^{i}\delta p_{i} - \Delta p_{i}\delta q^{i}).}}}} \tag{5.87} \\ \end{array}$$

The right-hand side is the sum of the areas on the canonical planes;#Footnote(17) for each /i/ the area of a parallelogram is computed from the components of the vectors defining its adjacent sides. Let /ζ/_{1} = (0, Δ/q,/ Δ/p/) and /ζ/_{2} = (0, /δq, δp/); then the sum of the areas of the incremental parallelograms is just

$$\begin{array}{ll} {\sum\limits_{i}{\Delta A_{i} = \omega(\zeta_{1},\zeta_{2}),}} \tag{5.88} \\ \end{array}$$

where /ω/ is the bilinear antisymmetric function introduced in equation (#Eqn(chapter005,5.70,5.70)). The function /ω/ is invariant under canonical transformations, so the sum of the areas of the incremental parallelograms is invariant under canonical transformations.

There is an integral version of this differential relation. Consider the oriented area of a region /R/′ in phase space (see [figure 5.2](#figure_5.2)). Suppose we make a canonical transformation from coordinates
#page(363)
(/q/′, /p/′) to (/q/, /p/) taking region /R/′ to region /R/. The boundary of the region in the transformed coordinates is just the image under the canonical transformation of the original boundary. Let $ R_{q^{i},p_{i}}$ be the projection of the region /R/ onto the /q^{i}/, /p_{i}/ plane of coordinate /q^{i}/ and conjugate momentum /p_{i}/, and let /A_{i}/ be its area. Similarly, let $ R_{q\prime^{i},p_{i}^{\prime}}^{\prime}$ be the projection of /R/′ onto the $ q\prime^{i},p_{i}^{\prime}$ plane, and let $ A_{i}^{\prime}$ be its area.

#Image(Art_P988.jpg,figure_5.2)
#Caption *Figure 5.2* A region /R/′ in phase space is mapped by a canonical transformation /C/_{H} to a region /R/. The projections of region /R/ onto the planes formed by canonical basis pairs /q_{j}/, /p_{j}/ are /R_{j}/. The projections of /R/′ are ¶ $ R_{j}^{\prime}$ ¶ . In general, the areas of the regions /R/ and /R/′ are not the same, but the sums of the areas of the canonical plane projections are the same. #CaptionEnd

The area of an arbitrary region is just the limit of the sum of the areas of incremental parallelograms that cover the region, so the sum of oriented areas is preserved by canonical transformations:

$$\begin{array}{ll} {\sum\limits_{i}{A_{i} = {\sum\limits_{i}{A_{i}^{\prime}.}}}} \tag{5.89} \\ \end{array}$$

That is, the sum of the projected areas on the canonical planes is preserved by canonical transformations. Another way to say this is

$$\begin{array}{ll} {\sum\limits_{i}{\int_{R_{q^{i},p_{i}}}{dq^{i}dp_{i} = {\sum\limits_{i}{\int_{R_{q\prime^{i},p_{i}^{\prime}}^{\prime}}{dq\prime^{i}dp_{i}^{\prime}.}}}}}} \tag{5.90} \\ \end{array}$$

#page(364)

The equality-of-areas relation (#Eqn(chapter005,5.90,5.90)) can also be written as an equality of line integrals using Stokes's theorem, for simply-connected regions $ R_{q^{i},p_{i}}$ and $ R_{q\prime^{i},p_{i}^{\prime}}^{\prime}$:

$$\begin{array}{ll} {\sum\limits_{i}{\oint_{\partial R_{q^{i},p_{i}}}{p_{i}dq^{i} = {\sum\limits_{i}{\oint_{\partial R_{q\prime^{i},p_{i}^{\prime}}^{\prime}}{p_{i}^{\prime}dq\prime^{i}.}}}}}} \tag{5.91} \\ \end{array}$$

The canonical planes are disjoint except at the origin, so the projected areas intersect in at most one point. Thus we may independently accumulate the line integrals around the boundaries of the individual projections of the region onto the canonical planes into a line integral around the unprojected region:

$$\begin{array}{ll} {\oint_{\partial R}{\sum\limits_{i}{p_{i}dq^{i} = {\oint_{\partial R\prime}{\sum\limits_{i}{p_{i}^{\prime}dq\prime^{i}.}}}}}} \tag{5.92} \\ \end{array}$$

### Exercise 5.10: Watch out

Consider the canonical transformation /C/_{H}:

$$(t,x,p) = C_{\text{H}}(t,\theta,J) = (t,\sqrt{2(J + a)}\,\sin\,\theta,\sqrt{2(J + a)}\,\cos\,\theta).$$

*a.* Show that the transformation is symplectic for any /a/.

*b.* Show that equation (#Eqn(chapter005,5.92,5.92)) is not generally satisfied for the region enclosed by a curve of constant /J/.

### 5.4 Generating Functions
We have considered a number of properties of general canonical transformations without having a method for coming up with them. Here we introduce the method of /generating functions/. The generating function is a real-valued function that compactly specifies a canonical transformation through its partial derivatives, as follows.

Consider a real-valued function /F/_{1}(/t/, /q/, /q/′) mapping configurations expressed in two coordinate systems to the reals. We will use /F/_{1} to construct a canonical transformation from one coordinate system to the other. We will show that the following relations among the coordinates, the momenta, and the Hamiltonians specify a canonical transformation:

#page(365)

$$\begin{array}{ll} {p = \partial_{1}F_{1}(t,q,q\prime)} \tag{5.93} \\ \end{array}$$

$$\begin{array}{ll} {p\prime = - \partial_{2}F_{1}(t,q,q\prime)} \tag{5.94} \\ \end{array}$$

$$\begin{array}{ll} {H\prime(t,q\prime,p\prime) - H(t,q,p) = \partial_{0}F_{1}(t,q,q\prime).} \tag{5.95} \\ \end{array}$$

The transformation will then be explicitly given by solving for one set of variables in terms of the others: To obtain the primed variables in terms of the unprimed ones, let /A/ be the inverse of ∂_{1}/F/_{1} with respect to the third argument,

$$\begin{array}{ll} {q\prime = A(t,q,\partial_{1}F_{1}(t,q,q\prime));} \tag{5.96} \\ \end{array}$$

then

$$\begin{array}{ll} {q\prime = A(t,q,p)} \tag{5.97} \\ \end{array}$$

$$\begin{array}{ll} {p\prime = - \partial_{2}F_{1}(t,q,A(t,q,p)).} \tag{5.98} \\ \end{array}$$

Let /B/ be the coordinate part of the phase-space transformation /q/ = /B/(/t/, /q/′, /p/′). This /B/ is an inverse function of ∂_{2}/F/_{1}, satisfying

$$\begin{array}{ll} {q = B(t,q\prime, - \partial_{2}F_{1}(t,q,q\prime)).} \tag{5.99} \\ \end{array}$$

Using /B/, we have

$$\begin{array}{ll} {q = B(t,q\prime,p\prime)} \tag{5.100} \\ \end{array}$$

$$\begin{array}{ll} {p = \partial_{1}F_{1}(t,B(t,q\prime,p\prime),q\prime).} \tag{5.101} \\ \end{array}$$

To put the transformation in explicit form requires that the inverse functions /A/ and /B/ exist.

We can use the above relations to verify that some given transformation from one set of phase-space coordinates (/q/, /p/) with Hamiltonian function /H/(/t/, /q/, /p/) to another set (/q/′, /p/′) with Hamiltonian function /H/′(/t/, /q/′, /p/′) is canonical by finding an /F/_{1}(/t/, /q/, /q/′) such that the above relations are satisfied. We can also use arbitrarily chosen generating functions of type /F/_{1} to generate new canonical transformations.

#### The polar-canonical transformation
The polar-canonical transformation (#Eqn(chapter005,5.27,5.27)) from coordinate and momentum (/x/, /p_{x}/) to new coordinate and new momentum (/θ/, /I/),

$$\begin{matrix} {x = \sqrt{\frac{2I}{\alpha}}\,\sin\,\theta} \tag{5.102} \\ \end{matrix}$$

$$\begin{array}{ll} {p_{x} = \sqrt{2I\alpha}\,\cos\,\theta,} \tag{5.103} \\ \end{array}$$

#page(366)

introduced earlier, is canonical. This can also be demonstrated by finding a suitable /F/_{1} generating function. The generating function satisfies a set of partial differential equations, (#Eqn(chapter005,5.93,5.93)) and (#Eqn(chapter005,5.94,5.94)):

$$\begin{array}{ll} {p{}_{x} = \partial_{1}F_{1}(t,x,\theta)} \tag{5.104} \\ \end{array}$$

$$\begin{array}{ll} {I = - \partial_{2}F_{1}(t,x,\theta).} \tag{5.105} \\ \end{array}$$

Using relations (#Eqn(chapter005,5.102,5.102)) and (#Eqn(chapter005,5.103,5.103)), which specify the transformation, equation (#Eqn(chapter005,5.104,5.104)) can be rewritten

$$\begin{array}{ll} {p_{x} = x\alpha\cot\,\theta = \partial_{1}F_{1}(t,x,\theta),} \tag{5.106} \\ \end{array}$$

which is easily integrated to yield

$$\begin{array}{ll} {F_{1}(t,x,\theta) = \frac{\alpha}{2}x^{2}\,\cot\,\theta + \varphi(t,\theta),} \tag{5.107} \\ \end{array}$$

where /φ/ is some integration “constant” with respect to the first integration. Substituting this form for /F/_{1} into the second partial differential equation (#Eqn(chapter005,5.105,5.105)), we find

$$\begin{array}{ll} {I = - \partial_{2}F_{1}(t,x,\theta) = \frac{\alpha}{2}\frac{x^{2}}{{(\sin\,\theta)}^{2}} - \partial_{1}\varphi(t,\theta),} \tag{5.108} \\ \end{array}$$

but if we set /φ/ = 0 the desired relations are recovered. So the generating function

$$\begin{array}{ll} {F_{1}(t,x,\theta) = \frac{\alpha}{2}x^{2}\,\cot\,\theta} \tag{5.109} \\ \end{array}$$

generates the polar-canonical transformation. This shows that this transformation is canonical.

##### 5.4.1 /F/_{1} Generates Canonical Transformations
We can prove directly that the transformation generated by an /F/_{1} is canonical by showing that if Hamilton's equations are satisfied in one set of coordinates then they will be satisfied in the other set of coordinates. Let /F/_{1} take arguments (/t/, /x/, /y/). The relations among the coordinates are

$$\begin{array}{ll} {p_{x} = \partial_{1}F_{1}(t,x,y)} & \\ {p_{y} = - \partial_{2}F_{1}(t,x,y)} \tag{5.110} \\ \end{array}$$

#page(367)

and the Hamiltonians are related by

$$\begin{array}{ll} {H\prime(t,y,p_{y}) = H(t,x,p_{x}) + \partial_{0}F_{1}(t,x,y).} \tag{5.111} \\ \end{array}$$

Substituting the generating function relations (#Eqn(chapter005,5.110,5.110)) into this equation, we have

$$\begin{array}{ll} {H\prime(t,y, - \partial_{2}F_{1}(t,x,y))} & \\ {\,\,\,\,\,\,\, = H(t,x,\partial_{1}F_{1}(t,x,y)) + \partial_{0}F_{1}(t,x,y).} \tag{5.112} \\ \end{array}$$

Take the partial derivatives of this equality of expressions with respect to the variables /x/ and /y/:#Footnote(18)

$$\begin{array}{ll} {- {(\partial_{2}H\prime)}^{j}{(\partial_{1}{(\partial_{2}F_{1})}_{j})}_{i}} & \\ {\,\,\,\,\,\,\, = {(\partial_{1}H)}_{i} + {(\partial_{2}H)}^{j}{(\partial_{1}{(\partial_{1}F_{1})}_{j})}_{i} + {(\partial_{1}\partial_{0}F_{1})}_{i}} & \\ {{(\partial_{1}H\prime)}_{i} - {(\partial_{2}H\prime)}^{j}{(\partial_{2}{(\partial_{2}F_{1})}_{j})}_{i}} & \\ {\,\,\,\,\,\, = {(\partial_{2}H)}^{j}{(\partial_{2}{(\partial_{1}F_{1})}_{j})}_{i} + {(\partial_{2}\partial_{0}F_{1})}_{i}} \tag{5.113} \\ \end{array}$$

where the arguments are unambiguous and have been suppressed. On solution paths we can use Hamilton's equations for the (/x/, /p_{x}/) system to replace the partial derivatives of /H/ with derivatives of /x/ and /p_{x}/, obtaining

$$\begin{array}{ll} {- {(\partial_{2}H\prime)}^{j}{(\partial_{1}{(\partial_{2}F_{1})}_{j})}_{i}} & \\ {\,\,\,\,\,\,\, = - {(Dp_{x})}_{i} + {(Dx)}^{j}{(\partial_{1}{(\partial_{1}F_{1})}_{j})}_{i} + {(\partial_{1}\partial_{0}F_{1})}_{i}} & \\ {{(\partial_{1}H\prime)}_{i} - {(\partial_{2}H\prime)}^{j}{(\partial_{2}{(\partial_{2}F_{1})}_{j})}_{i}} & \\ {\,\,\,\,\,\,\, = {(Dx)}^{j}{(\partial_{2}{(\partial_{1}F_{1})}_{j})}_{i} + {(\partial_{2}\partial_{0}F_{1})}_{i}.} \tag{5.114} \\ \end{array}$$

Now compute the derivatives of /p_{x}/ and /p_{y}/, from equations (#Eqn(chapter005,5.110,5.110)), along consistent paths:

#page(368)

$$\begin{matrix} {{(Dp_{x})}_{i} = {(\partial_{1}{(\partial_{1}F_{1})}_{i})}_{j}{(Dx)}^{j} + {(\partial_{2}{(\partial_{1}F_{1})}_{i})}_{j}{(D_{y})}^{j} + \partial_{0}{(\partial_{1}F_{1})}_{i}} \\ {{(Dp_{y})}_{i} = - {(\partial_{1}{(\partial_{2}F_{1})}_{i})}_{j}{(Dx)}^{j} - {(\partial_{2}{(\partial_{2}F_{1})}_{i})}_{j}{(D_{y})}^{j} - \partial_{0}{(\partial_{2}F_{1})}_{i}.} \\ {\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,(5.115)} \\ \end{matrix}$$

Using the fact that elementary partials commute, (∂_{2}(∂_{1}/F/_{1})/_{i}/)/_{j}/ = (∂_{1}(∂_{2}/F/_{1})/_{j}/)/_{i}/, and substituting this expression for (/Dp_{x}/)/_{i}/ into the first of equations (#Eqn(chapter005,5.114,5.114)) yields

$$\begin{array}{ll} {- {(\partial_{2}H\prime)}^{j}{(\partial_{1}{(\partial_{2}F_{1})}_{j})}_{i} = - {(\partial_{1}{(\partial_{2}F_{1})}_{j})}_{i}{(D_{y})}^{j}.} \tag{5.116} \\ \end{array}$$

Provided that ∂_{2}∂_{1}/F/_{1} is nonsingular,#Footnote(19) we have derived one of Hamilton's equations for the (/y/, /p_{y}/) system:

$$\begin{array}{ll} {D_{y}(t) = \partial_{2}H\prime(t,y(t),p_{y}(t)).} \tag{5.117} \\ \end{array}$$

Hamilton's other equation,

$$\begin{array}{ll} {Dp_{y}(t) = - \partial_{1}H\prime(t,y(t),p_{y}(t)),} \tag{5.118} \\ \end{array}$$

can be derived in a similar way. So the generating function relations indeed specify a canonical transformation.

##### 5.4.2 Generating Functions and Integral Invariants
Generating functions can be used to specify a canonical transformation by the prescription given above. Here we show how to get a generating function from a canonical transformation, and derive the generating function rules.

The generating function representation of canonical transformations can be derived from the Poincaré integral invariants, as follows. We first show that, given a canonical transformation, the integral invariants imply the existence of a function of phase-space coordinates that can be written as a path-independent line integral. Then we show that partial derivatives of this function, represented in mixed coordinates, give the generating function relations between the old and new coordinates. We need to do this only for time-independent transformations because time-dependent transformations become time independent in the extended phase space (see [section 5.5](#section_5.5)).

#page(369)

#### Generating functions of type /F/_{1}
Let /C/ be a time-independent canonical transformation, and let /C_{t}/ be the /qp/-part of the transformation. The transformation /C_{t}/ preserves the integral invariant equation (#Eqn(chapter005,5.90,5.90)). One way to express the equality of areas is as a line integral (#Eqn(chapter005,5.92,5.92)):

$$\begin{array}{ll} {\oint_{\partial R}{\sum\limits_{i}{p_{i}dq^{i} = {\oint_{\partial R\prime}{\sum\limits_{i}{p_{i}^{\prime}dq\prime^{i},}}}}}} \tag{5.119} \\ \end{array}$$

where /R/′ is a two-dimensional region in (/q/′, /p/′) coordinates at time /t/, /R/ = /C_{t}/(/R/′) is the corresponding region in (/q/, /p/) coordinates, and ∂/R/ indicates the boundary of the region /R/. This holds for any region and its boundary. We will show that this implies there is a function /F/ (/t/, /q/′, /p/′) that can be defined in terms of line integrals

$$\begin{array}{ll} {F(t,q\prime,p\prime) - F(t,q_{0}^{\prime},p_{0}^{\prime})} & \\ {\,\,\,\,\,\, = {\int_{\gamma = C_{t}(\gamma\prime)}{\sum\limits_{i}{p_{i}dq^{i} - {\int_{\gamma\prime}{\sum\limits_{i}{p_{i}^{\prime}dq\prime^{i},}}}}}}} \tag{5.120} \\ \end{array}$$

where /γ/′ is a curve in phase-space coordinates that begins at $\gamma\prime(0) = (q_{0}^{\prime},p_{0}^{\prime})$ and ends at /γ/′(1) = (/q/′, /p/′), and /γ/ is its image under /C_{t}/.

Let

$$\begin{array}{ll} {G{}_{t}(\gamma\prime) = {\int_{\gamma = C_{t}(\gamma\prime)}{\sum\limits_{i}{p_{i}dq^{i} - {\int_{\gamma\prime}{\sum\limits_{i}{p_{i}^{\prime}dq\prime^{i},}}}}}}} \tag{5.121} \\ \end{array}$$

and let $\gamma_{1}^{\prime}$ and $\gamma_{2}^{\prime}$ be two paths with the same endpoints. Then

$$\begin{array}{lll} {G_{t}(\gamma_{2}^{\prime}) - G_{t}(\gamma_{1}^{\prime})} & {= {\oint_{\partial R}{\sum{p_{i}dq^{i} - {\oint_{\partial R\prime}{\sum{p_{i}^{\prime}dq\prime^{i}}}}}}}} & \\  & {= 0.} \tag{5.122} \\ \end{array}$$

So the value of /G_{t}/(/γ/′) depends only on the endpoints of /γ/′.

Let

$$\begin{array}{ll} {{\overline{G}}_{t,q_{0}^{\prime},p_{0}^{\prime}}(q\prime,p\prime) = G_{t}(\gamma\prime),} \tag{5.123} \\ \end{array}$$

where /γ/′ is any path from $ q_{0}^{\prime},\, p_{0}^{\prime}$ to /q/′, /p/′. Changing the initial point from $ q_{0}^{\prime}\, p_{0}^{\prime}$ to $ q_{1}^{\prime}\, p_{1}^{\prime}$ changes the value of /Ḡ/ by a constant:

$$\begin{array}{ll} {{\overline{G}}_{t,q_{1}^{\prime},p_{1}^{\prime}}(q\prime,p\prime) - {\overline{G}}_{t,q_{0}^{\prime},p_{0}^{\prime}}(q\prime,p\prime) = {\overline{G}}_{t,q_{1}^{\prime},p_{1}^{\prime}}(q_{0}^{\prime},p_{0}^{\prime}).} \tag{5.124} \\ \end{array}$$

#page(370)

If we define /F/ so that

$$\begin{array}{ll} {F(t,q\prime,p\prime) = {\overline{G}}_{t,q_{1}^{\prime},p_{1}^{\prime}}(q\prime,p\prime),} \tag{5.125} \\ \end{array}$$

then

$$\begin{array}{ll} {F(t,q\prime,p\prime) - F(t,q_{0}^{\prime},p_{0}^{\prime}) = {\overline{G}}_{t,q_{0}^{\prime},p_{0}^{\prime}}(q\prime,p\prime),} \tag{5.126} \\ \end{array}$$

demonstrating equation (#Eqn(chapter005,5.120,5.120)).

The phase-space point (/q/, /p/) in unprimed variables corresponds to (/q/′, /p/′) in primed variables, at an arbitrary time /t/. Both /p/ and /q/ are determined given /q/′ and /p/′. In general, given any two of these four quantities, we can solve for the other two. If we can solve for the momenta in terms of the positions we get a particular class of generating functions.#Footnote(20) We introduce the functions

$$\begin{array}{crl} p & {= f_{p}(t,q,q\prime)} & \\ {p\prime} & {= f_{p\prime}(t,q,q\prime)} \tag{5.127} \\ \end{array}$$

that solve the transformation equations (/t/, /q/, /p/) = /C/(/t/, /q/′, /p/′) for the momenta in terms of the coordinates at a specified time. With these we introduce a function /F/_{1}(/t/, /q/, /q/′) such that

$$\begin{array}{ll} {F_{1}(t,q,q\prime) = F(t,q,f_{p}(t,q,q\prime)).} \tag{5.128} \\ \end{array}$$

The function /F/_{1} has the same value as /F/ but has different arguments. We will show that this /F/_{1} is in fact the generating function for canonical transformations introduced in [section 5.4](#section_5.4). Let's be explicit about the definition of /F/_{1} in terms of a line integral:

$$\begin{array}{ll} {F_{1}(t,q,q\prime) - F_{1}(t,q_{0},q_{0}^{\prime})} & \\ {\,\,\,\,\,\,\, = {\int_{q_{0},q_{0}^{\prime}}^{q,q\prime}{(f_{p}(t,q,q\prime)dq - f_{p\prime}(t,q,q\prime)dq\prime).}}} \tag{5.129} \\ \end{array}$$

The two line integrals can be combined into this one because they are both expressed as integrals along a curve in (/q/, /q/′).

#page(371)

We can use the path independence of /F/_{1} to compute the partial derivatives of /F/_{1} with respect to particular components and consequently derive the generating function relations for the momenta.#Footnote(21) So we conclude that

$$\begin{array}{ll} {{(\partial_{1}F_{1}(t,q,q\prime))}_{i} = f_{p_{i}}(t,q,q\prime)} \tag{5.130} \\ \end{array}$$

$$\begin{array}{ll} {{(\partial_{2}F_{1}(t,q,q\prime))}_{i} = - f_{p_{i}^{\prime}}(t,q,q\prime).} \tag{5.131} \\ \end{array}$$

These are just the configuration and momentum parts of the generating function relations for canonical transformation. So starting with a canonical transformation, we can find a generating function that gives the coordinate--momentum part of the transformation through its derivatives.

Starting from a general canonical transformation, we have constructed an /F/_{1} generating function from which the canonical transformation may be rederived. So we expect there is a generating function for every canonical transformation.#Footnote(22)

#### Generating functions of type /F/_{2}
Point transformations were excluded from the previous argument because we could not deduce the momenta from the coordinates. However, a similar derivation allows us to make a generating function for this case. The integral invariants give us an equality of area integrals. There are other ways of writing the equality-of-areas relation (#Eqn(chapter005,5.90,5.90)) as a line integral. We can also write

$$\begin{array}{ll} {\oint_{\partial R}{\sum\limits_{i}{p_{i}dq^{i} = - {\oint_{\partial R\prime}{\sum\limits_{i}{q_{i}^{\prime}dp\prime^{i}.}}}}}} \tag{5.132} \\ \end{array}$$

The minus sign arises because by flipping the axes we are traversing the area in the opposite sense. Repeating the argument just
#page(372)
given, we can define a function

$$\begin{array}{ll} {F\prime(t,q\prime,p\prime) - F\prime(t,q_{0}^{\prime},p_{0}^{\prime})} & \\ {\,\,\,\,\,\,\, = {\int_{\gamma = C(t,\gamma\prime)}{\sum\limits_{i}{p_{i}dq^{i} + {\int_{\gamma\prime}{\sum\limits_{i}{q_{i}^{\prime}dp\prime^{i}}}}}}}} \tag{5.133} \\ \end{array}$$

that is independent of the path /γ/′. If we can solve for /q/′ and /p/ in terms of /q/ and /p/′ we can define the functions

$$\begin{array}{ll} {q\prime = f_{q\prime}^{\prime}(t,q,p\prime)} & \\ {p = f_{p}^{\prime}(t,q,p\prime)} \tag{5.134} \\ \end{array}$$

and define

$$\begin{array}{ll} {F_{2}(t,q,p\prime) = F\prime(t,f_{q\prime}^{\prime}(t,q,p\prime),p\prime).} \tag{5.135} \\ \end{array}$$

Then the canonical transformation is given as partial derivatives of /F/_{2}:

$$\begin{array}{ll} {{(\partial_{1}F_{2}(t,q,p\prime))}_{i} = f_{p_{i}}^{\prime}(t,q,p\prime)} \tag{5.136} \\ \end{array}$$

and

$$\begin{array}{ll} {{(\partial_{2}F_{2}(t,q,p\prime))}^{i} = f_{q_{i}^{\prime}}^{\prime}(t,q,p\prime).} \tag{5.137} \\ \end{array}$$

#### Relationship between /F/_{1} and /F/_{2}
For canonical transformations that can be described by both an /F/_{1} and an /F/_{2}, there must be a relation between them. The alternative line integral expressions for the area integral are related. Consider the difference

$$\begin{array}{ll} {(F\prime(t,q\prime,p\prime) - F\prime(t,q_{0}^{\prime},p_{0}^{\prime})) - (F(t,q\prime,p\prime) - F(t,q_{0}^{\prime},p_{0}^{\prime}))} & \\ {\,\,\,\,\,\,\,\, = {\int_{\gamma\prime}{\sum\limits_{i}{p_{i}^{\prime}dq\prime^{i} + {\int_{\gamma\prime}{\sum\limits_{i}{q_{i}^{\prime}dp\prime^{i}}}}}}}} & \\ {\,\,\,\,\,\,\, = {\int_{\gamma\prime}{\sum\limits_{i}{d(p_{i}^{\prime}q\prime^{i})}}}} & \\ {\,\,\,\,\,\,\, = {\sum\limits_{i}{(p\prime){}_{i}{(q\prime)}^{i} - {\sum\limits_{i}{{(p_{0}^{\prime})}_{i}{(q_{0}^{\prime})}^{i}.}}}}} \tag{5.138} \\ \end{array}$$

The functions /F/ and /F/′ are related by an integrated term

$$\begin{array}{ll} {F\prime(t,q\prime,p\prime) - F(t,q\prime,p\prime) = p\prime q\prime,} \tag{5.139} \\ \end{array}$$

#page(373)

as are /F/_{1} and /F/_{2}:

$$\begin{array}{ll} {F_{2}(t,q,p\prime) - F_{1}(t,q,q\prime) = p\prime q\prime.} \tag{5.140} \\ \end{array}$$

The generating functions /F/_{1} and /F/_{2} are related by a Legendre transform:

$$\begin{array}{ll} {p\prime = - \partial_{2}F_{1}(t,q,q\prime)} \tag{5.141} \\ \end{array}$$

$$\begin{array}{ll} {p\prime q\prime = - F_{1}(t,q,q\prime) + F_{2}(t,q,p\prime)} \tag{5.142} \\ \end{array}$$

$$\begin{array}{ll} {q\prime = \partial{}_{2}F_{2}(t,q,p\prime).} \tag{5.143} \\ \end{array}$$

We have passive variables /q/ and /t/:

$$\begin{array}{ll} {- \partial_{1}F_{1}(t,q,q\prime) + \partial_{1}F_{2}(t,q,p\prime) = 0} \tag{5.144} \\ \end{array}$$

$$\begin{array}{ll} {- \partial_{0}F_{1}(t,q,q\prime) + \partial_{0}F_{2}(t,q,p\prime) = 0.} \tag{5.145} \\ \end{array}$$

But /p/ = ∂_{1}/F/_{1}(/t/, /q/, /q/′) from the first transformation, so

$$\begin{array}{ll} {p = \partial_{1}F_{2}(t,q,p\prime).} \tag{5.146} \\ \end{array}$$

Furthermore, since /H/′(/t/, /q/′, /p/′) − /H/(/t/, /q/, /p/) = ∂_{0}/F/_{1}(/t/, /q/, /q/′) we can conclude that

$$\begin{array}{ll} {H\prime(t,q\prime,p\prime) - H(t,q,p) = \partial_{0}F_{2}(t,q,p\prime).} \tag{5.147} \\ \end{array}$$

##### 5.4.3 Types of Generating Functions
We have used generating functions of the form /F/_{1}(/t/, /q/, /q/′) to construct canonical transformations:

$$\begin{array}{ll} {p = \partial_{1}F_{1}(t,q,q\prime)} \tag{5.148} \\ \end{array}$$

$$\begin{array}{ll} {p\prime = - \partial{}_{2}F_{1}(t,q,q\prime)} \tag{5.149} \\ \end{array}$$

$$\begin{array}{ll} {H\prime(t,q\prime,p\prime) - H(t,q,p) = \partial_{0}F_{1}(t,q,q\prime).} \tag{5.150} \\ \end{array}$$

We can also construct canonical transformations with generating functions of the form /F/_{2}(/t/, /q/, /p/′), where the third argument of /F/_{2} is the momentum in the primed system.#Footnote(23)

#page(374)

$$\begin{array}{ll} {p = \partial_{1}F_{2}(t,q,p\prime)} \tag{5.151} \\ \end{array}$$

$$\begin{array}{ll} {q\prime = \partial_{2}F_{2}(t,q,p\prime)} \tag{5.152} \\ \end{array}$$

$$\begin{array}{ll} {H\prime(t,q\prime,p\prime) - H(t,q,p) = \partial_{0}F_{2}(t,q,p\prime)} \tag{5.153} \\ \end{array}$$

As in the /F/_{1} case, to put the transformation in explicit form requires that appropriate inverse functions be constructed to allow the solution of the equations.

Similarly, we can construct two other forms for generating functions, named mnemonically enough /F/_{3} and /F/_{4}:

$$\begin{array}{ll} {q = - \partial_{1}F_{3}(t,p,q\prime)} \tag{5.154} \\ \end{array}$$

$$\begin{array}{ll} {p\prime = - \partial_{2}F_{3}(t,p,q\prime)} \tag{5.155} \\ \end{array}$$

$$\begin{array}{ll} {H\prime(t,q\prime,p\prime) - H(t,q,p) = \partial_{0}F_{3}(t,p,q\prime)} \tag{5.156} \\ \end{array}$$

and

$$\begin{array}{ll} {q = - \partial_{1}F_{4}(t,p,p\prime)} \tag{5.157} \\ \end{array}$$

$$\begin{array}{ll} {q\prime = \partial_{2}F_{4}(t,p,p\prime)} \tag{5.158} \\ \end{array}$$

$$\begin{matrix} {H\prime\left( {t,q\prime,p\prime} \right) - H\left( {t,q,p} \right) = \partial_{0}F_{4}\left( {t,p,p\prime} \right)} \tag{5.159} \\ \end{matrix}$$

These four classes of generating functions are called /mixed-variable generating functions/ because the canonical transformations they generate give a mixture of old and new variables in terms of a mixture of old and new variables.

In every case, if the generating function does not depend explicitly on time then the Hamiltonians are obtained from one another purely by composition with the appropriate canonical transformation. If the generating function depends on time, then there are additional terms.

The generating functions presented each treat the coordinates and momenta collectively. One could define more complicated generating functions for which the transformations of different degrees of freedom are specified by generating functions of different types.

#page(375)

##### 5.4.4 Point Transformations
Point transformations can be represented in terms of a generating function of type /F/_{2}. Equations (#Eqn(chapter005,5.6,5.6)), which define a canonical point transformation derived from a coordinate transformation /F/, are

$$\begin{array}{ll} {(t,q,p) = C(t,q\prime,p\prime) = (t,F(t,q\prime),p\prime{(\partial_{1}F(t,q\prime))}^{- 1}).} \tag{5.160} \\ \end{array}$$

Let /S/ be the inverse transformation of /F/ with respect to the second argument

$$\begin{array}{ll} {q\prime = S(t,q),} \tag{5.161} \\ \end{array}$$

so that /q/′ = /S/(/t/, /F/ (/t/, /q/′)). The momentum transformation that accompanies this coordinate transformation is

$$\begin{array}{ll} {p\prime = p{(\partial_{1}S(t,q))}^{- 1}.} \tag{5.162} \\ \end{array}$$

We can find the generating function /F/_{2} that gives this transformation by integrating equation (#Eqn(chapter005,5.152,5.152)) to get

$$\begin{array}{ll} {F_{2}(t,q,p\prime) = p\prime S(t,q) + \varphi(t,q).} \tag{5.163} \\ \end{array}$$

Substituting this into equation (#Eqn(chapter005,5.151,5.151)), we get

$$\begin{array}{ll} {p = p\prime\partial_{1}S(t,q) + \partial_{1}\varphi(t,q).} \tag{5.164} \\ \end{array}$$

We do not need the freedom provided by /φ/, so we can set it equal to zero:

$$\begin{array}{ll} {F_{2}(t,q,p\prime) = p\prime S(t,q),} \tag{5.165} \\ \end{array}$$

with

$$\begin{array}{ll} {p = p\prime\partial_{1}S(t,q).} \tag{5.166} \\ \end{array}$$

So this /F/_{2} gives the canonical transformation of equations (#Eqn(chapter005,5.161,5.161)) and (#Eqn(chapter005,5.162,5.162)).

The canonical transformation for the coordinate transformation /S/ is the inverse of the canonical transformation for /F/. By design /F/ and /S/ are inverses on the coordinate arguments. The identity function is /q/ = /I/(/q/′) = /S/(/t/, /F/ (/t/, /q/′)). Differentiating yields

#page(376)

$$\begin{array}{ll} {1 = \partial_{1}S(t,F(t,q\prime))\partial_{1}F(t,q\prime),} \tag{5.167} \\ \end{array}$$

so

$$\begin{array}{ll} {\partial_{1}F(t,q\prime) = {(\partial_{1}S(t,F(t,q\prime)))}^{- 1}.} \tag{5.168} \\ \end{array}$$

Using this, the relation between the momenta (#Eqn(chapter005,5.166,5.166)) is

$$\begin{array}{ll} {p = p\prime{(\partial_{1}F(t,q\prime))}^{- 1},} \tag{5.169} \\ \end{array}$$

showing that /F/_{2} gives a point transformation equivalent to the point transformation (#Eqn(chapter005,5.160,5.160)). So from this other point of view the point transformation is canonical.

The /F/_{1} that corresponds to the /F/_{2} for a point transformation is

$$\begin{array}{lll} {F_{1}(t,q,q\prime)} & {= F_{2}(t,q,p\prime) - p\prime q\prime} & \\  & {= p\prime S(t,q) - p\prime q\prime} & \\  & {= 0.} \tag{5.170} \\ \end{array}$$

This is why we could not use generating functions of type /F/_{1} to construct point transformations.

#### Polar and rectangular coordinates
A commonly required point transformation is the transition between polar coordinates and rectangular coordinates:

$$\begin{array}{ll} {x = r\,\cos\,\theta} \tag{5.171} \\ {y = r\,\sin\,\theta.} & \\ \end{array}$$

Using the formula for the generating function of a point transformation just derived, we find:

$$\begin{array}{ll} {F_{2}(t;r,\theta;p_{x},p_{y}) = \lbrack\begin{array}{ll} p_{x} & {p_{y}\rbrack\left( \begin{array}{l} {r\,\cos\,\theta} \\ {r\,\sin\,\theta} \\ \end{array} \right).} \\ \end{array}} \tag{5.172} \\ \end{array}$$

So the full transformation is derived:

$$\begin{array}{lll} {(x,y)} & {= \partial_{2}F_{2}(t;r,\theta;p_{x},p_{y})} & \\  & {= (r\,\cos\,\theta,r\,\sin\,\theta)} & \\ {\lbrack p_{r},p_{\theta}\rbrack} & {= \partial_{1}F_{2}(t;r,\theta;p_{x},p_{y})} & \\  & {= \lbrack p_{x}\,\cos\,\theta + p_{y}\,\sin\,\theta, - p_{x}r\,\sin\,\theta + p_{y}r\,\cos\,\theta\rbrack.} \tag{5.173} \\ \end{array}$$

#page(377)

We can isolate the rectangular coordinates to one side of the transformation and the polar coordinates to the other:

$$\begin{array}{ll} {p_{r} = \frac{1}{r}(p_{x}x + p_{y}y)} & \\ {p_{\theta} = - p_{x}y + p_{y}x.} \tag{5.174} \\ \end{array}$$

So, interpreted in terms of Newtonian vectors,$ p_{r} = \widehat{r} \cdot \overset{\rightarrow}{p}$ is the radial component of the linear momentum and $ p_{\theta} = \left\| {\overset{\rightarrow}{r} \times \overset{\rightarrow}{p}} \right\|$ is the magnitude of the angular momentum. The point transformation is time independent, so the Hamiltonian transforms by composition.

#### Rotating coordinates
A useful time-dependent point transformation is the transition to a rotating coordinate system. This is most easily accomplished in polar coordinates. Here we have

$$\begin{array}{ll} {r\prime = r} & \\ {\theta\prime = \theta - \Omega t,} \tag{5.175} \\ \end{array}$$

where Ω is the angular velocity of the rotating coordinate system. The generating function is

$$\begin{array}{ll} {F_{2}(t;r,\theta;p_{r}^{\prime},p_{\theta}^{\prime}) = \lbrack\begin{array}{ll} p_{r}^{\prime} & {p_{\theta}^{\prime}\rbrack} \\ \end{array}\left( \begin{array}{l} r \\ {\theta - \Omega t} \\ \end{array} \right).} \tag{5.176} \\ \end{array}$$

This yields the transformation equations

$$\begin{array}{lll} {r\prime} & {= r} & \\ {\theta\prime} & {= \theta - \Omega t} & \\ p_{r} & {= p_{r}^{\prime}} & \\ p_{\theta} & {= p_{\theta}^{\prime},} \tag{5.177} \\ \end{array}$$

which show that the momenta are the same in both coordinate systems. However, here the Hamiltonian is not a simple composition:

$$\begin{array}{ll} {H\prime(t;r\prime,\theta\prime;p_{r}^{\prime},p_{\theta}^{\prime}) = H(t;r\prime,\theta\prime + \Omega t;p_{r}^{\prime},p_{\theta}^{\prime}) - p_{\theta}^{\prime}\Omega.} \tag{5.178} \\ \end{array}$$

The Hamiltonians differ by the derivative of the generating function with respect to the time argument. In transforming to rotating
#page(378)
coordinates, the values of the Hamiltonians differ by the product of the angular momentum and the angular velocity of the coordinate system. Notice that this addition to the Hamiltonian is the same as was found earlier (#Eqn(chapter005,5.45,5.45)).

#### Reducing the two-body problem to the one-body problem
In this example we illustrate how canonical transformations can be used to eliminate some of the degrees of freedom, leaving a problem with fewer degrees of freedom.

Suppose that only certain combinations of the coordinates appear in the Hamiltonian. We make a canonical transformation to a new set of phase-space coordinates such that these combinations of the old phase-space coordinates are some of the new phase-space coordinates. We choose other independent combinations of the coordinates to complete the set. The advantage is that these other independent coordinates do not appear in the new Hamiltonian, so the momenta conjugate to them are conserved quantities.

Let's see how this idea enables us to reduce the problem of two gravitating bodies to the simpler problem of the relative motion of the two bodies. In the process we will discover that the momentum of the center of mass is conserved. This simpler problem is an instance of the Kepler problem. The Kepler problem is also encountered in the formulation of the more general /n/-body problem.

Consider the motion of two masses /m/_{1} and /m/_{2}, subject only to a mutual gravitational attraction described by the potential /V/ (/r/). This problem has six degrees of freedom. The rectangular coordinates of the particles are /x/_{1} and /x/_{2}, with conjugate momenta /p/_{1} and /p/_{2}. Each of these is a structure of the three rectangular components. The distance between the particles is /r/ = ‖/x/_{1} − /x/_{2}‖. The Hamiltonian for the two-body problem is

$$\begin{array}{ll} {H(t;x_{1},x_{2};p_{1},p_{2}) = \frac{p_{1}^{2}}{2m_{1}} + \frac{p_{2}^{2}}{2m_{2}} + V(r).} \tag{5.179} \\ \end{array}$$

The gravitational potential energy depends only on the relative positions of the two bodies. We do not need to specify /V/ further at this point.

#page(379)

Since the only combination of coordinates that appears in the Hamiltonian is /x/_{2} − /x/_{1}, we choose new coordinates so that one of the new coordinates is this combination:

$$\begin{array}{ll} {x = x_{2} - x_{1}.} \tag{5.180} \\ \end{array}$$

To complete the set of new coordinates we choose another to be some independent linear combination

$$\begin{array}{ll} {X = ax_{1} + bx_{2},} \tag{5.181} \\ \end{array}$$

where /a/ and /b/ are to be determined. We can use an /F/_{2}-type generating function

$$\begin{array}{ll} {F_{2}(t;x_{1},x_{2};p,P) = (x_{2} - x_{1})p + (ax_{1} + bx_{2})P,} \tag{5.182} \\ \end{array}$$

where /p/ and /P/ will be the new momenta conjugate to /x/ and /X/, respectively. We deduce

$$\begin{array}{ll} {\,\,(x,X) = \partial_{2}F_{2}(t;x_{1},x_{2};p,P) = (x_{2} - x_{1},ax_{1} + bx_{2})} & \\ {\left\lbrack {p_{1},p{}_{2}} \right\rbrack = \partial_{1}F_{2}(t;x_{1},x_{2};p,P) = \left\lbrack {- p + aP,p + bP} \right\rbrack.} \tag{5.183} \\ \end{array}$$

We can solve these for the new momenta:

$$\begin{array}{ll} {P = \frac{p_{1} + p_{2}}{a + b}} \tag{5.184} \\ \end{array}$$

$$\begin{array}{ll} {p = \frac{ap_{2} - bp_{1}}{a + b}.} \tag{5.185} \\ \end{array}$$

The generating function is not time dependent, so the new Hamiltonian is the old Hamiltonian composed with the transformation:

$$\begin{array}{lll} {H\prime(t;x,X;p,P)} & {= \frac{{( - p + aP)}^{2}}{2m_{1}} + \frac{{(p + bP)}^{2}}{2m_{2}} + V(\left\| x \right\|)} & \\  & {= \frac{p^{2}}{2m} + \frac{P^{2}}{2M} + V(\left\| x \right\|)} & \\  & {\,\,\,\,\, + \left( {\frac{b}{m_{2}} - \frac{a}{m_{1}}} \right)pP,} \tag{5.186} \\ \end{array}$$

#page(380)

with the definitions

$$\begin{array}{ll} {\frac{1}{m} = \frac{1}{m_{1}} + \frac{1}{m_{2}}} \tag{5.187} \\ \end{array}$$

and

$$\begin{array}{ll} {\frac{1}{M} = \frac{a^{2}}{m_{1}} + \frac{b^{2}}{m_{2}}.} \tag{5.188} \\ \end{array}$$

We recognize /m/ as the “reduced mass.”

Notice that if the term proportional to /pP/ were not present then the /x/ and /X/ degrees of freedom would not be coupled at all, and furthermore, the /X/ part of the Hamiltonian would be just the Hamiltonian of a free particle, which is easy to solve. The condition that the “cross terms” disappear is

$$\begin{array}{ll} {\frac{b}{m_{2}} - \frac{a}{m_{1}} = 0,} \tag{5.189} \\ \end{array}$$

which is satisfied by

$$\begin{array}{ll} {a = cm_{1}} & \\ {b = cm_{2}} \tag{5.190} \\ \end{array}$$

for any /c/. For a transformation to be defined, /c/ must be nonzero. So with this choice the Hamiltonian becomes

$$\begin{array}{ll} {H\prime(t;x,X;p,P) = H_{X}(t,X,P) + H_{x}(t,x,p)} \tag{5.191} \\ \end{array}$$

with

$$\begin{array}{ll} {H_{x}(t,x,p) = \frac{p^{2}}{2m} + V(r)} \tag{5.192} \\ \end{array}$$

and

$$\begin{array}{ll} {H_{X}(t,X,P) = \frac{P^{2}}{2M}.} \tag{5.193} \\ \end{array}$$

The reduced mass is the same as before, and now

$$\begin{array}{ll} {M = \frac{1}{c^{2}(m_{1} + m_{2})}.} \tag{5.194} \\ \end{array}$$

#page(381)

Notice that, without further specifying /c/, the problem has been separated into the problem of determining the relative motion of the two masses, and the problem of the other degrees of freedom. We did not need a priori knowledge that the center of mass might be important; in fact, only for a particular choice of /c/ = (/m/_{1} + /m/_{2})^{−1} does /X/ become the center of mass.

#### Epicyclic motion
It is often useful to compose a sequence of canonical transformations to make up the transformation we need for any particular mechanical problem. The transformations we have supplied are especially useful as components in these computations.

We will illustrate the use of canonical transformations to learn about planar motion in a central field. The strategy will be to consider perturbations of circular motion in the central field. The analysis will proceed by transforming to a rotating coordinate system that rides on a circular reference orbit, and then making approximations that restrict the analysis to orbits that differ from the circular orbit only slightly.

In rectangular coordinates we can easily write a Hamiltonian for the motion of a particle of mass /m/ in a field defined by a potential energy that is a function only of the distance from the origin as follows:

$$\begin{matrix} {H(t;\, x,\, y;p_{x},p_{y}) = \frac{p_{x}^{2} + p_{y}^{2}}{2m} + V(\sqrt{x^{2} + y^{2}}).} \tag{5.195} \\ \end{matrix}$$

In this coordinate system Hamilton's equations are easy, and they are exactly what is needed to develop trajectories by numerical integration, but the expressions are not very illuminating:

$$ Dx\begin{matrix} {= \frac{p_{x}}{m}} \tag{5.196} \\ \end{matrix}$$

$$ Dy\begin{matrix} {= \frac{p_{y}}{m}} \tag{5.197} \\ \end{matrix}$$

$$ Dp_{x}\begin{matrix} {= - DV(\sqrt{x^{2} + y^{2}})\frac{x}{\sqrt{x^{2} + y^{2}}}} \tag{5.198} \\ \end{matrix}$$

$$ Dp_{y}\begin{matrix} {= - DV(\sqrt{x^{2} + y^{2}})\frac{y}{\sqrt{x^{2} + y^{2}}}.} \tag{5.199} \\ \end{matrix}$$

#page(382)

We can learn more by converting to polar coordinates centered on the source of our field:

$$\begin{matrix} {x = r\cos\varphi} \tag{5.200} \\ \end{matrix}$$

$$\begin{matrix} {y = r\sin\varphi.} \tag{5.201} \\ \end{matrix}$$

This coordinate system explicitly incorporates the geometrical symmetry of the potential energy. Extending this coordinate transformation to a point transformation, we can write the new Hamiltonian as:

$$\begin{matrix} {H\prime(t;\, r,\,\varphi;\, p_{r},\, p_{\varphi}) = \frac{p_{r}^{2}}{2m} + \frac{p_{\varphi}^{2}}{2mr^{2}} + V(r).} \tag{5.202} \\ \end{matrix}$$

We can now write Hamilton's equations in these new coordinates, and they are much more illuminating than the equations expressed in rectangular coordinates:

$$\begin{matrix} {Dr = \frac{p_{r}}{m}} \tag{5.203} \\ \end{matrix}$$

$$\begin{matrix} {D\varphi = \frac{p_{\varphi}}{mr^{2}}} \tag{5.204} \\ \end{matrix}$$

$$\begin{matrix} {Dp_{r} = \frac{p_{\varphi}^{2}}{mr^{3}} - DV(r)} \tag{5.205} \\ \end{matrix}$$

$$\begin{matrix} {Dp_{\varphi} = 0.} \tag{5.206} \\ \end{matrix}$$

The angular momentum /p_{φ}/ is conserved, and we are free to choose its constant value, so /Dφ/ depends only on /r/. We also see that we can establish a circular orbit at any radius /R/_{0}: we choose /p_{φ}/ = /p/_{/φ/0} so that $ p_{\varphi 0}^{2}/(mR_{0}^{3}) - DV(R_{0}) = 0 $. This will ensure that /Dp_{r}/ = 0, and thus /Dr/ = 0. The square of the angular velocity of this circular orbit is

$$\Omega^{2}\begin{matrix} {= \frac{DV(R_{0})}{mR_{0}}.} \tag{5.207} \\ \end{matrix}$$

It is instructive to consider how orbits that are close to the circular orbit differ from the circular orbit. This is best done in rotating coordinates in which a body moving in the circular orbit is a stationary point at the origin. We can do this by converting to coordinates that are rotating with the circular orbit and centered on the orbiting body. We proceed in three stages. First we will
#page(383)
transform to a polar coordinate system that is rotating at angular velocity Ω. Then we will return to rectangular coordinates, and finally, we will shift the coordinates so that the origin is on the reference circular orbit.

We start by examining the system in rotating polar coordinates. This is a time-dependent coordinate transformation:

$$ r\prime\begin{matrix} {= r} \tag{5.208} \\ \end{matrix}$$

$$\varphi\prime\begin{matrix} {= \varphi - \Omega t} \tag{5.209} \\ \end{matrix}$$

$$ p_{r}^{\prime}\begin{matrix} {= pr} \tag{5.210} \\ \end{matrix}$$

$$ p_{\varphi}^{\prime}\begin{matrix} {= p_{\varphi}.} \tag{5.211} \\ \end{matrix}$$

Using equation (#Eqn(chapter005,5.178,5.178)), we can write the new Hamiltonian directly:

$$ H''(t;r\prime,\,\varphi\prime;p_{r}^{\prime},p_{\varphi}^{\prime})\begin{matrix} {= \frac{p_{r}^{\prime 2}}{2m} + \frac{p_{\varphi}^{\prime 2}}{2mr\prime^{2}} + V(r\prime) - p_{\varphi}^{\prime}\Omega.} \tag{5.212} \\ \end{matrix}$$

/H/″ is not time dependent, and therefore it is conserved. It is not the sum of the potential energy and the kinetic energy. Energy is not conserved in the moving coordinate system, but what is conserved here is a new quantity, the /Jacobi constant/, that combines the energy with the product of the angular momentum of the particle in the new coordinate and the angular velocity of the coordinate system. We will want to keep track of this term.

Next, we return to rectangular coordinates, but they are rotating with the reference circular orbit:

$$\begin{matrix} {x\prime = r\prime\cos\varphi\prime} \tag{5.213} \\ \end{matrix}$$

$$\begin{matrix} {y\prime = r\prime\sin\varphi\prime} \tag{5.214} \\ \end{matrix}$$

$$\begin{matrix} {p_{x}^{\prime} = p_{r}^{\prime}\cos\varphi\prime - \frac{p_{\varphi}^{\prime}}{r\prime}\sin\varphi\prime} \tag{5.215} \\ \end{matrix}$$

$$\begin{matrix} {p_{y}^{\prime} = p_{r}^{\prime}\sin\varphi\prime + \frac{p_{\varphi}^{\prime}}{r\prime}\cos\varphi\prime.} \tag{5.216} \\ \end{matrix}$$

The Hamiltonian is

$$\begin{array}{ll} {H'''(t;\, x\prime,\, y\prime;\, p_{x}^{\prime},\, p_{y}^{\prime})} & \\ {\,\,\, = \frac{p_{x}^{\prime 2} + p_{y}^{\prime 2}}{2m} + \Omega(y\prime p_{x}^{\prime} - x\prime p_{y}^{\prime}) + V(\sqrt{x\prime^{2} + y\prime^{2}}).} \tag{5.217} \\ \end{array}$$

#page(384)

With one more quick manipulation we shift the coordinate system so that the origin is out on our circular orbit. We define new rectangular coordinates /ξ/ and /η/ with the following simple canonical transformation of coordinates and momenta:

$$\begin{matrix} {\xi = x\prime - R_{0}} \tag{5.218} \\ \end{matrix}$$

$$\begin{matrix} {\eta = y\prime} \tag{5.219} \\ \end{matrix}$$

$$\begin{matrix} {p_{\xi} = p_{x}^{\prime}} \tag{5.220} \\ \end{matrix}$$

$$\begin{matrix} {p_{\eta} = p_{y}^{\prime}.} \tag{5.221} \\ \end{matrix}$$

In this final coordinate system the Hamiltonian is

$$\begin{array}{lll} {H\operatorname{''''}(t;\,\xi,\,\eta;p_{\xi},p_{\eta}) =} & {\frac{p_{\xi}^{2} + p_{\eta}^{2}}{2m} + \Omega(\eta p_{\xi} - (\xi + R_{0})p_{\eta})} & \\  & {+ V(\sqrt{{(\xi + R_{0})}^{2} + \eta^{2}}),} \tag{5.222} \\ \end{array}$$

and Hamilton's equations are uselessly complicated, but the next step is to consider only trajectories for which the coordinates /ξ/ and /η/ are small compared with /R/_{0}. Under this assumption we will be able to construct approximate equations of motion for these trajectories that are linear in the coordinates, thus yielding simple analyzable motion. To this point we have made no approximations. The equations above are perfectly accurate for any trajectories in a central field.

The idea is to expand the potential-energy term in the Hamiltonian as a series and to discard any term higher than second-order in the coordinates, thus giving us first-order-accurate Hamilton's equations:

$$\begin{matrix} {U(\xi,\eta) = V(\sqrt{{(\xi + R_{0})}^{2} + \eta^{2}})} \tag{5.223} \\ \end{matrix}$$

$$\begin{matrix} {= V(R_{0} + \xi + \frac{\eta^{2}}{2R_{0}} + ...)} \tag{5.224} \\ \end{matrix}$$

$$\begin{array}{ll} {= V(R_{0}) + DV(R_{0})(\xi + \frac{\eta^{2}}{2R_{0}})} & \\ {\,\,\,\,\,\, + D^{2}V(R_{0})\frac{\xi^{2}}{2} + \cdots.} \tag{5.225} \\ \end{array}$$

So the (negated) generalized forces are

$$\partial_{0}U(\xi,\eta)\begin{matrix} {= DV(R_{0}) + D^{2}V(R_{0})\xi + \cdots} \tag{5.226} \\ \end{matrix}$$

$$\partial_{1}U(\xi,\eta)\begin{matrix} {= DV(R_{0})\frac{\eta}{R_{0}} + \cdots.} \tag{5.227} \\ \end{matrix}$$

#page(385)

With this expansion we obtain the linearized Hamilton's equations:

$$\begin{matrix} {D\xi = \frac{p_{\xi}}{m} + \Omega\eta} \tag{5.228} \\ \end{matrix}$$

$$\begin{matrix} {D\eta = \frac{p_{\eta}}{m} - \Omega(\xi + R_{0})} \tag{5.229} \\ \end{matrix}$$

$$\begin{matrix} {Dp_{\xi} = - DV(R_{0}) - D^{2}V(R_{0})\xi + \cdots + \Omega p_{\eta}} \tag{5.230} \\ \end{matrix}$$

$$\begin{matrix} {Dp_{\eta} = - DV(R_{0})\frac{\eta}{R_{0}} + ... - \Omega p_{\xi}.} \tag{5.231} \\ \end{matrix}$$

Of course, once we have linear equations we know how to solve them exactly. Because the linearized Hamiltonian is conserved we cannot get exponential expansion or collapse, so the possible solutions are quite limited. It is instructive to convert these equations into a second-order system. We use Ω^{2} = /DV/(/R/_{0})/(/mR/_{0}), equation (#Eqn(chapter005,5.207,5.207)), to eliminate the /DV/ terms:

$$\begin{matrix} {D^{2}\xi - 2\Omega D\eta = (\Omega^{2} - \frac{D^{2}V(R_{0})}{m})\xi} \tag{5.232} \\ \end{matrix}$$

$$\begin{matrix} {D^{2}\eta + 2\Omega D\xi = 0.} \tag{5.233} \\ \end{matrix}$$

Combining these, we find

$$\begin{matrix} {D^{3}\xi + \omega^{2}D\xi = 0,} \tag{5.234} \\ \end{matrix}$$

where

$$\begin{matrix} {\omega^{2} = 3\Omega^{2} + \frac{D^{2}V(R_{0})}{m}.} \tag{5.235} \\ \end{matrix}$$

Thus we have a simple harmonic oscillator with frequency /ω/ as one of the components of the solution. The general solution has three parts:

$$\begin{matrix} {\begin{pmatrix} {\xi(t)} \\ {\eta(t)} \\ \end{pmatrix} = \eta_{0}\begin{pmatrix} 0 \\ 1 \\ \end{pmatrix}} \tag{5.236} \\ \end{matrix}$$

$$\begin{matrix} {+ \xi_{0}\begin{pmatrix} 1 \\ {- 2At} \\ \end{pmatrix}} \tag{5.237} \\ \end{matrix}$$

$$\begin{matrix} {+ C_{0}\begin{pmatrix} {\sin(\omega t + \varphi_{0})} \\ {\frac{2\Omega}{\omega}\cos(\omega t + \varphi_{0})} \\ \end{pmatrix}} \tag{5.238} \\ \end{matrix}$$

where

$$\begin{matrix} {A = \frac{\Omega^{2}m - D^{2}V(R_{0})}{4\Omega m}.} \tag{5.239} \\ \end{matrix}$$

#page(386)

The constants /η/_{0}, /ξ/_{0}, /C/_{0}, and /φ/_{0} are determined by the initial conditions. If /C/_{0} = 0, the particle of interest is on a circular trajectory, but not necessarily the same one as the reference trajectory. If /C/_{0} = 0 and /ξ/_{0} = 0, we have a “fellow traveler,” a particle in the same circular orbit as the reference orbit but with different phase. If /C/_{0} = 0 and /η/_{0} = 0, we have a particle in a circular orbit that is interior or exterior to the reference orbit and shearing away from the reference orbit. The shearing is due to the fact that the angular velocity for a circular orbit varies with the radius. The constant /A/ gives the rate of shearing at each radius. If both /η/_{0} = 0 and /ξ/_{0} = 0 but /C/_{0} ≠ 0, then we have “epicyclic motion.” A particle in a nearly circular orbit may be seen to move in an ellipse around the circular reference orbit. The ellipse will be elongated in the direction of circular motion by the factor 2Ω//ω/, and it will rotate in the direction opposite to the direction of the circular motion. The initial phase of the epicycle is /φ/_{0}. Of course, any combination of these solutions may exist.

The epicyclic frequency /ω/ and the shearing rate /A/ are determined by the force law (the radial derivative of the potential energy). For a force law proportional to a power of the radius,

$$\begin{matrix} {F \propto r^{1 - n},} \tag{5.240} \\ \end{matrix}$$

the epicyclic frequency is related to the orbital frequency by

$$\begin{matrix} {\frac{\omega}{\Omega} = 2\sqrt{1 - \frac{n}{4}}} \tag{5.241} \\ \end{matrix}$$

and the shearing rate is

$$\begin{matrix} {\frac{A}{\Omega} = \frac{n}{4}.} \tag{5.242} \\ \end{matrix}$$

For a few particular integer force laws we see:

[[images/Art_P1145.jpg]]

We can get some insight into the kinds of orbits produced by the epicyclic approximation by looking at a few examples. For
#page(387)
some force laws we have integer ratios of epicyclic frequency to orbital frequency. In those cases we have closed orbits. For an inverse-square force law (/n/ = 3) we get elliptical orbits with the center of the field at a focus of the ellipse. [Figure 5.3](#figure_5.3) shows how an approximation to such an orbit can be constructed by superposition of the motion on an elliptical epicycle with the motion of the same frequency on a circle. If the force is proportional to the radius (/n/ = 0) we get a two-dimensional harmonic oscillator. Here the epicyclic frequency is twice the orbital frequency. [Figure 5.4](#figure_5.4) shows how this yields elliptical orbits that are centered on the source of the central force. An orbit is closed when /ω//Ω is a rational fraction. If the force is proportional to the −3/4 power of the radius, the epicyclic frequency is 3/2 the orbital frequency. This yields the three-lobed pattern seen in [figure 5.5](#figure_5.5). For other force laws the orbits predicted by this analysis are multi-lobed patterns produced by precessing approximate ellipses. Most of the cases have incommensurate epicyclic and orbital frequencies, leading to orbits that do not close in finite time.

#Image(Art_P1146.jpg,figure_5.3)
#Caption *Figure 5.3* Epicyclic construction of an approximate orbit for /F/ ∝ /r/^{−2}. The large dotted circle is the reference circular orbit and the dotted ellipses are the epicycles. The epicycles are twice as long as they are wide. The solid ellipse is the approximate trajectory produced by a particle moving on the epicycles. The sense of orbital motion is counterclockwise, and the epicycles are rotating clockwise. The arrows represent the increment of velocity contributed by the epicycle to the circular reference orbit. #CaptionEnd

#page(388)

#Image(Art_P1147.jpg,figure_5.4)
#Caption *Figure 5.4* Epicyclic construction of an approximate orbit for /F/ ∝ /r/. The large dotted circle is the reference circular orbit and the small dotted circles are the epicycles. The solid ellipse is the approximate trajectory produced by a particle moving on the epicycles. The sense of orbital motion is counterclockwise, and the epicycles are rotating clockwise. The arrows represent the increment of velocity contributed by the epicycle to the circular reference orbit. #CaptionEnd

#Image(Art_P1148.jpg,figure_5.5)
#Caption *Figure 5.5* Epicyclic construction of an approximate orbit for /F/ ∝ /r/^{−3/4}. The large dotted circle is the reference circular orbit and the dotted ellipses are the epicycles. The epicycles have a 4:3 ratio of length to width. The solid trefoil is the approximate trajectory produced by a particle moving on the epicycles. The sense of orbital motion is counterclockwise, and the epicycles are rotating clockwise. The arrows represent the increment of velocity contributed by the epicycle to the circular reference orbit. #CaptionEnd

#page(389)

#Image(Art_P1149.jpg,figure_5.6)
#Caption *Figure 5.6* The numerically integrated orbit of a particle with a force law /F/ ∝ /r/^{−2.3}. For this law the ratio of the epicyclic frequency to the orbital frequency is about .83666---close to 5/6, but not quite. This is manifest in the nearly five-fold symmetry of the rosette-like shape and the fact that one must cross approximately six orbits to get from the inside to the outside of the rosette. #CaptionEnd

The epicyclic approximation gives a very good idea of what actual orbits look like. [Figure 5.6](#figure_5.6), drawn by numerical integration of the orbit produced by integrating the original rectangular equations of motion for a particle in the field, shows the rosette-type picture characteristic of incommensurate epicyclic and orbital frequencies for an /F/ = −/r/^{−2.3} force law.

We can directly compare a numerically integrated system with one of our epicyclic approximations. For example, the result of numerically integrating our /F/ ∝ /r/^{−3/4} system is very similar to the picture we obtained by epicycles. (See [[chapter005!figure_5.7][figure 5.7]] and compare it with [figure 5.5](#figure_5.5).)

### Exercise 5.11: Collapsing orbits

What exactly happens as the force law becomes steeper? Investigate this by sketching the contours of the Hamiltonian in /r/, /p_{r}/ space for various values of the force-law exponent, /n/. For what values of /n/ are there stable circular orbits? In the case that there are no stable circular orbits, what happens to circular and other noncircular orbits? How are these results consistent with Liouville's theorem and the nonexistence of attractors in Hamiltonian systems?

#page(390)

#Image(Art_P1150.jpg,figure_5.7)
#Caption *Figure 5.7* The numerically integrated orbit of a particle with a force law /F/ ∝ /r/^{−3/4}. For this law the ratio of the epicyclic frequency to the orbital frequency is exactly 3/2. This is manifest in the three-fold symmetry of the rosette-like shape and the fact that one must cross two orbits to get from the inside to the outside of the rosette. #CaptionEnd

##### 5.4.5 Total Time Derivatives
The addition of a total time derivative to a Lagrangian leads to the same Lagrange equations. However, the two Lagrangians have different momenta, and they lead to different Hamilton's equations. Here we find out how to represent the corresponding canonical transformation with a generating function.

Let's restate the result about total time derivatives and Lagrangians from the first chapter. Consider some function /G/(/t/, /q/) of time and coordinates. We have shown that if /L/ and /L/′ are related by

$$\begin{matrix} {L\prime(t,q,\dot{q}) = L(t,q,\dot{q}) + \partial_{0}G(t,q) + \partial_{1}G(t,q)\dot{q}} \tag{5.243} \\ \end{matrix}$$

then the Lagrange equations of motion are the same. The generalized coordinates used in the two Lagrangians are the same, but the momenta conjugate to the coordinates are different. In the usual way, define

$$\mathcal{P}\begin{matrix} {(t,q,\dot{q}) = \partial_{2}L(t,q,\dot{q})} \tag{5.244} \\ \end{matrix}$$

#page(391)

and

$$\mathcal{P}\prime\begin{matrix} {(t,q,\dot{q}) = \partial_{2}L\prime(t,q,\dot{q}).} \tag{5.245} \\ \end{matrix}$$

So we have

$$\mathcal{P}\prime\begin{matrix} {(t,q,\dot{q}) = \mathcal{P}(t,q,\dot{q}) + \partial_{1}G(t,q).} \tag{5.246} \\ \end{matrix}$$

Evaluated on a trajectory, we have

$$ p\prime\begin{matrix} {(t) = p(t) + \partial_{1}G(t,q(t)).} \tag{5.247} \\ \end{matrix}$$

This transformation is a special case of an /F/_{2}-type transformation. Let

$$ F_{2}\begin{matrix} {(t,q,p\prime) = qp\prime - G(t,q);} \tag{5.248} \\ \end{matrix}$$

then the associated transformation is

$$\begin{matrix} {q\prime = \partial_{2}F_{2}(t,\, q,\,\, p\prime) = q} \tag{5.249} \\ \end{matrix}$$

$$\begin{matrix} {p = \partial_{1}F_{2}(t,q,p\prime) = p\prime - \partial_{1}G(t,q)} \tag{5.250} \\ \end{matrix}$$

$$\begin{array}{lll} {H\prime\left( {t,q\prime,p\prime} \right)} & {= H\left( {t,q,p} \right) + \partial_{0}F_{2}\left( {t,q,p\prime} \right)} & \\  & {= H\left( {t,q,p} \right) - \partial_{0}G\left( {t,q} \right).} \tag{5.251} \\ \end{array}$$

Explicitly, the new Hamiltonian is

$$\begin{matrix} {H\prime(t,q\prime,p\prime) = H(t,q\prime,p\prime - \partial_{1}G(t,q\prime)) - \partial_{0}G(t,q\prime),} \tag{5.252} \\ \end{matrix}$$

where we have used the fact that /q/ = /q/′. The transformation is interesting in that the coordinate transformation is the identity transformation, but the new and old momenta are not the same, even in the case in which /G/ has no explicit time dependence. Suppose we have a Hamiltonian of the form

$$\begin{matrix} {H(t,x,p) = \frac{p^{2}}{2m} + V(x);} \tag{5.253} \\ \end{matrix}$$

then the transformed Hamiltonian is

$$\begin{matrix} {H\prime(t,x\prime,p\prime) = \frac{{(p\prime - \partial_{1}G(t,x\prime))}^{2}}{2m} + V(x\prime) - \partial_{0}G(t,x\prime).} \tag{5.254} \\ \end{matrix}$$

We see that this transformation may be used to modify terms in the Hamiltonian that are linear in the momenta. Starting from /H/,
#page(392)
the transformation introduces linear momentum terms; starting from /H/′, the transformation eliminates the linear terms.

#### Driven pendulum
We illustrate the use of this transformation with the driven pendulum. The Hamiltonian for the driven pendulum derived from the /T/ − /V/ Lagrangian (see [section 1.6.2](chapter001!section_1.6.2)) is

$$\begin{array}{ll} {H(t,\theta,p_{\theta})} & \\ {\,\,\,\,\,\,\, = \frac{p_{\theta}^{2}}{2ml^{2}} - glm\cos\theta} & \\ {\,\,\,\,\,\,\,\,\,\,\,\, + gmy_{s}(t) - \frac{p_{\theta}}{l}\sin\theta Dy_{s}(t) - \frac{m}{2}{(\cos\theta)}^{2}{(Dy_{s}(t))}^{2},} \tag{5.255} \\ \end{array}$$

where /y_{s}/ is the drive function. The Hamiltonian is rather messy, and includes a term that is linear in the angular momentum with a coefficient that depends on both the angular coordinate and the time. Let's see what happens if we apply our transformation to the problem to eliminate the linear term. We can identify the transformation function /G/ by requiring that the linear term in momentum be killed:

$$\begin{matrix} {G(t,\theta) = - ml\cos\theta Dy_{s}(t).} \tag{5.256} \\ \end{matrix}$$

The transformed momentum is

$$ p_{\theta}^{\prime} = p_{\theta}\begin{matrix} {+ ml\sin\theta Dy_{s}(t),} \tag{5.257} \\ \end{matrix}$$

and the transformed Hamiltonian is

$$\begin{array}{lll} {H\prime(t,\theta,p_{\theta}^{\prime}) =} & {\frac{{(p_{\theta}^{\prime})}^{2}}{2ml^{2}} - ml(g + D^{2}y_{s})\cos\theta} & \\  & {+ gmy_{s}(t) - \frac{m}{2}{(y_{s}(t))}^{2}.} \tag{5.258} \\ \end{array}$$

Dropping the last two terms, which do not affect the equations of motion, we find

$$\begin{matrix} {H\prime(t,\theta,p_{\theta}^{\prime}) = \frac{{(p_{\theta}^{\prime})}^{2}}{2ml^{2}} - ml(g + D^{2}y_{s})\cos\theta.} \tag{5.259} \\ \end{matrix}$$

So we have found, by a straightforward canonical transformation, a Hamiltonian for the driven pendulum with the rather simple form of a pendulum with gravitational acceleration that is modified
#page(393)
by the acceleration of the pivot. It is, in fact, the Hamiltonian that corresponds to the alternative form of the Lagrangian for the driven pendulum that we found earlier by inspection (see equation #Eqn(chapter001,1.120,1.120)). Here the derivation is by a simple canonical transformation, motivated by a desire to eliminate unwanted terms that are linear in the momentum.

### Exercise 5.12: Construction of generating functions

Suppose that canonical transformations $\left( {t,q,p} \right) = C_{a}\left( {t,q\prime,p\prime} \right)\,\text{and}\,\left( {t,q\prime,p\prime} \right) = C_{b}\left( {t,q'',p''} \right)$ are generated by two /F/_{1}-type generating functions, /F/_{1a}(/t/, /q/, /q/′) and /F/_{1b}(/t/, /q/′, /q/″).

*a.* Show that the generating function for the inverse transformation of /C_{a}/ is /F/_{1c}(/t/, /q/′, /q/) = −/F/_{1a}(/t/, /q/, /q/′).

*b.* Define a new kind of generating function,

/F_{x}/(/t/, /q/, /q/′, /q/″) = /F/_{1a}(/t/, /q/, /q/′) + /F/_{1b}(/t/, /q/′, /q/″).

We see that

/p/ = ∂_{1}/F/_{x}(/t/, /q/, /q/′, /q/″) = ∂_{1}/F/_{1a}(/t/, /q/, /q/′)

/p/″ = −∂_{3}/F_{x}/(/t/, /q/, /q/′, /q/″) = −∂_{2}/F/_{1b}(/t/, /q/′, /q/″)

Show that ∂_{2}/F/_{x} = 0, allowing a solution to eliminate /q/′.

*c.* Using the formulas for /p/ and /p/″ above, and the result from part *b*, Show that /F_{x}/ is an appropriate generating function for the composition transformation /C/_{a} ∘ /C/_{b}.

### Exercise 5.13: Linear canonical transformations

We consider systems with two degrees of freedom and transformations for which the Hamiltonian transforms by composition.

*a.* Consider the linear canonical transformations that are generated by $ F_{2}(t;x_{1},x_{2};p_{1}^{\prime},p_{2}^{\prime}) = p_{1}^{\prime}ax_{1} + p_{1}^{\prime}bx_{2} + p_{2}^{\prime}cx_{1} + p_{2}^{\prime}dx_{2}.$ Show that these transformations are just the point transformations, and that the corresponding /F/_{1} is zero.

*b.* Other linear canonical transformations can be generated by $ F_{1}(t;x_{1},x_{2};x_{1}^{\prime},x_{2}^{\prime}) = x_{1}^{\prime}ax_{1} + x_{1}^{\prime}bx_{2} + x_{2}^{\prime}cx_{1} + x_{2}^{\prime}dx_{2}.$ Surely we can make even more generators by constructing /F/_{3}- and /F/_{4}-type transformations analogously. Are all of the linear canonical transformations
#page(394)
obtainable in this way? If not, show one that cannot be so generated.

*c.* Can all linear canonical transformations be generated by compositions of transformations generated by the functions shown in parts *a* and *b* above?

*d.* How many independent parameters are necessary to specify all possible linear canonical transformations for systems with two degrees of freedom?

### Exercise 5.14: Integral invariants

Consider the linear canonical transformation for a system with two degrees of freedom generated by the function $ F_{1}(t;x_{1},x_{2};x_{1}^{\prime},x_{2}^{\prime}) = x_{1}^{\prime}ax_{1} + x_{1}^{\prime}bx_{2} + x_{2}^{\prime}cx_{1} + x_{2}^{\prime}dx_{2},$ and the general parallelogram with a vertex at the origin and with adjacent sides starting at the origin and extending to the phase-space points (/x/_{1a}, /x/_{2a}, /p/_{1a}, /p/_{2a}) and (/x/_{1b}, /x/_{2b}, /p/_{1b}, /p/_{2b}).

*a.* Find the area of the given parallelogram and the area of the target parallelogram under the canonical transformation. Notice that the area of the parallelogram is not preserved.

*b.* Find the areas of the projections of the given parallelogram and the areas of the projections of the target under canonical transformation. Show that the sum of the areas of the projections on the action-like planes is preserved.

### Exercise 5.15: Standard-map generating function

Find a generating function for the standard map (see [exercise 5.8](#exercise_5.8) on [page 357](chapter005!p357)).

### 5.5 Extended Phase Space
In this section we show that we can treat time as just another coordinate if we wish. Systems described by a time-dependent Hamiltonian may be recast in terms of a time-independent Hamiltonian with an extra degree of freedom. An advantage of this view is that what was a time-dependent canonical transformation can be treated as a time-independent transformation, where there are no additional conditions for adjusting the Hamiltonian.

Suppose that we have some system characterized by a time-dependent Hamiltonian, for example, a periodically driven pendulum.
#page(395)
We may imagine that there is some extremely massive oscillator, unperturbed by the motion of the relatively massless pendulum, that produces the drive. Indeed, we may think of time itself as the coordinate of an infinitely massive particle moving uniformly and driving everything else. We often consider the rotation of the Earth as exactly such a stable time reference when performing short-time experiments in the laboratory.

More formally, consider a dynamical system with /n/ degrees of freedom, whose behavior is described by a possibly time-dependent Lagrangian /L/ with corresponding Hamiltonian /H/. We make a new dynamical system with /n/ + 1 degrees of freedom by extending the generalized coordinates to include time and introducing a new independent variable. We also extend the generalized velocities to include a velocity for the time coordinate. In this new /extended state space/ the coordinates are redundant, so there is a constraint relating the time coordinate to the new independent variable.

We relate the original dynamical system to the extended dynamical system as follows: Let /q/ be a coordinate path. Let (/q_{e}/, /t/) : /τ/ ↦ (/q_{e}/(/τ/), /t/(/τ/)) be a coordinate path in the extended system where /τ/ is the new independent variable. Then /q_{e}/ = /q/ ∘ /t/, or /q_{e}/(/τ/) = /q/(/t/(/τ/)). Consequently, if /v/ = /Dq/ is the velocity along a path then /v_{e}/(/τ/) = /Dq_{e}/(/τ/) = /Dq/(/t/(/τ/)) · /Dt/(/τ/) = /v/(/t/(/τ/)) · /v_{t}/(/τ/).

We can find a Lagrangian for the extended system by requiring that the value of the action be unchanged. Introduce the extended Lagrangian action

$$\begin{matrix} {S_{e}\lbrack q_{e},t\rbrack(\tau_{1},\tau_{2}) = {\int_{\tau_{1}}^{\tau_{2}}{(L_{e} \circ \Gamma\lbrack q_{e},t\rbrack),}}} \tag{5.260} \\ \end{matrix}$$

with

$$\begin{matrix} {L_{e}(\tau;q_{e},t;v_{e},v_{t}) = L(t,q_{e},v_{e}/v_{t})v_{t}.} \tag{5.261} \\ \end{matrix}$$

We have

$$\begin{matrix} {S\lbrack q\rbrack(t(\tau_{1}),t(\tau_{2})) = S_{e}\lbrack q \circ t,t\rbrack(\tau_{1},\tau_{2}).} \tag{5.262} \\ \end{matrix}$$

The extended system is subject to a constraint that relates the time to the new independent variable. We assume the constraint is of the form /φ/(/τ/; /q_{e}/, /t/; /v_{e}/, /v_{t}/) = /t/ − /f/(/τ/) = 0. The constraint is
#page(396)
a holonomic constraint involving the coordinates and time, so we can incorporate this constraint by augmenting the Lagrangian:#Footnote(24)

$$\begin{array}{ll} {L_{e}^{\prime}(\tau;q_{e},t,\lambda;v_{e},v_{t},v_{\lambda})} & \\ {\,\,\,\,\,\,\, = L_{e}(\tau;q_{e},t;v_{e},v_{t}) + v_{\lambda}(v_{t} - Df(\tau))} & \\ {\,\,\,\,\,\,\, = L(t,q_{e},v_{e}/v_{t})v_{t} + v_{\lambda}(v_{t} - Df(\tau)).} \tag{5.263} \\ \end{array}$$

The Lagrange equations of $ L_{e}^{\prime}$ for /q_{e}/ are satisfied for the paths /q/ ∘ /t/ where /q/ is any path that satisfies the original Lagrange equations of /L/.

The momenta conjugate to the coordinates are

$$\begin{array}{ll} {\mathcal{P}_{e}(\tau;q_{e},t,\lambda;v_{e},v_{t},v_{\lambda})} & \\ {\,\,\,\,\,\,\, = \partial_{2,0}L_{e}^{\prime}(\tau;q_{e},t,\lambda;v_{e},v_{t},v_{\lambda})} & \\ {\,\,\,\,\,\,\, = \partial_{2}L(t,q_{e},v_{e}/v_{t})} & \\ {\,\,\,\,\,\,\, = \mathcal{P}(t,q_{e},v_{e}/v_{t})} \tag{5.264} \\ \end{array}$$

$$\begin{array}{ll} {\mathcal{P}_{t}(\tau;q_{e},t,\lambda;v_{e},v_{t},v_{\lambda})} & \\ {\,\,\,\,\,\, = \partial_{2,1}L_{e}^{\prime}(\tau;q_{e},t,\lambda;v_{e},v_{t},v_{\lambda})} & \\ {\,\,\,\,\,\,\, = L(t,q_{e},v_{e}/v_{t}) - \partial_{2}L(t,q_{e},v_{e}/v_{t})(v_{e}/v_{t}) + v_{\lambda}} & \\ {\,\,\,\,\,\,\, = - \mathcal{E}(t,q_{e},v_{e}/v_{t}) + v_{\lambda}} \tag{5.265} \\ \end{array}$$

$$\begin{array}{ll} {\mathcal{P}_{\lambda}(\tau;q_{e},t,\lambda;v_{e},v_{t},v_{\lambda})} & \\ {\,\,\,\,\,\,\, = \partial_{2,2}L_{e}^{\prime}(\tau;q_{e},t,\lambda;v_{e},v_{t},v_{\lambda})} & \\ {\,\,\,\,\,\,\, = v_{t} - Df(\tau).} \tag{5.266} \\ \end{array}$$

So the extended momenta have the same values as the original momenta at the corresponding states. The momentum conjugate to the time coordinate is the negation of the energy plus /v_{λ}/. The momentum conjugate to /λ/ is the constraint, which must be zero.

Next we carry out the transformation to the corresponding Hamiltonian formulation. First, note that the Lagrangian /L_{e}/ is a homogeneous form of degree one in the velocities. Thus, by Euler's theorem,

$$\begin{array}{ll} {\partial_{2}L_{e}(\tau;q_{e},t;v_{e},v_{t}) \cdot (v_{e},v_{t}) = L_{e}(\tau;q_{e},t;v_{e},v_{t}).} \tag{5.267} \\ \end{array}$$

#page(397)

The $ p\dot{q}\text{-part}$ of the Legendre transform of $ L_{e}^{\prime}$ is

$$\begin{array}{ll} {\partial_{2}L_{e}^{\prime}(\tau;q_{e},t,\lambda;v_{e},v_{t},v_{\lambda}) \cdot (v_{e},v_{t},v_{\lambda})} & \\ {\,\,\,\,\,\,\,\, = \partial_{2}L_{e}(\tau;q_{e},t;v_{e},v_{t}) \cdot (v_{e},v_{t}) + v_{\lambda}v_{t} + (v_{t} - Df(\tau))v_{\lambda}} & \\ {\,\,\,\,\,\,\,\, = L_{e}(\tau;q_{e},t;v_{e},v_{t}) + v_{\lambda}v_{t} + (v_{t} - Df(\tau))v_{\lambda}.} \tag{5.268} \\ \end{array}$$

So the Hamiltonian $ H_{e}^{\prime}$ corresponding to $ L_{e}^{\prime}$ is

$$\begin{array}{lll} {H_{e}^{\prime}(\tau;q_{e},t,\lambda;p_{e},p_{t},p_{\lambda})} & {= v_{\lambda}v_{t}} & \\  & {= (p_{t} + H(t,q_{e},p_{e}))(p_{\lambda} + Df(\tau)).} \tag{5.269} \\ \end{array}$$

We have used the fact that at corresponding states the momenta have the same values, so on paths /p_{e}/ = /p/ ∘ /t/, and

$$\begin{array}{ll} {\mathcal{E}(t,q_{e},v_{e}/v_{t}) = H(t,q_{e},p_{e}).} \tag{5.270} \\ \end{array}$$

The Hamiltonian $ H_{e}^{\prime}$ does not depend on /λ/ so we deduce that /p_{λ}/ is constant. In fact, /p_{λ}/ must be given the value zero, because it is the constraint. When there is a cyclic coordinate we can form a reduced Hamiltonian for the remaining degrees of freedom by substituting the constant value of conserved momentum conjugate to the cyclic coordinate into the Hamiltonian. The resulting Hamiltonian is

$$\begin{array}{ll} {H_{e}(\tau;q_{e},t;p_{e},p_{t}) = (p_{t} + H(t,q_{e},p_{e}))Df(\tau).} \tag{5.271} \\ \end{array}$$

This extended Hamiltonian governs the evolution of the extended system, for arbitrary /f/.#Footnote(25)

Hamilton's equations reduce to

$$\begin{array}{rll} {Dq_{e}(\tau)} & {= \partial_{2}H(t(\tau),q_{e}(\tau),p_{e}(\tau))Df(\tau)} & \\ {Dt(\tau)} & {= Df(\tau)} & \\ {Dp_{e}(\tau)} & {= - \partial_{1}H(t(\tau),q_{e}(\tau),p_{e}(\tau))Df(\tau)} & \\ {Dp_{t}(\tau)} & {= - \partial_{0}H(t(\tau),q_{e}(\tau),p_{e}(\tau))Df(\tau).} \tag{5.272} \\ \end{array}$$

#page(398)

The second equation gives the required relation between /t/ and /τ/. The first and third equations are equivalent to Hamilton's equations in the original coordinates, as we can see by using /q_{e}/ = /q/ ∘ /t/ to rewrite them:

$$\begin{array}{ll} {Dq(t(\tau))Dt(\tau) = \partial_{2}H(t(\tau),q(t(\tau)),p(t(\tau)))Df(\tau)} & \\ {Dp(t(\tau))Dt(\tau) = - \partial_{1}H(t(\tau),q(t(\tau)),p(t(\tau)))Df(\tau).} \tag{5.273} \\ \end{array}$$

Using /Dt/(/τ/) = /Df/(/τ/) and dividing these factors out, we recover Hamilton's equations.#Footnote(26)

Now consider the special case for which the time is the same as the independent variable: /f/(/τ/) = /τ/, /Df/(/τ/) = 1. In this case /q/ = /q_{e}/ and /p/ = /p_{e}/. The extended Hamiltonian becomes

$$\begin{array}{ll} {H_{e}^{\prime}(\tau;q_{e},t;p_{e},p_{t}) = p_{t} + H(t,q_{e},p_{e}).} \tag{5.274} \\ \end{array}$$

Hamilton's equation for /t/ becomes /Dt/(/τ/) = 1, restating the constraint. Hamilton's equations for /Dq_{e}/ and /Dp_{e}/ are directly Hamilton's equations:

$$\begin{array}{ll} {Dq(\tau) = \partial_{2}H(\tau,q(\tau),p(\tau))} & \\ {Dp(\tau) = - \partial_{1}H(\tau,q(\tau),p(\tau)).} \tag{5.275} \\ \end{array}$$

The extended Hamiltonian (#Eqn(chapter005,5.274,5.274)) does not depend on the independent variable, so it is a conserved quantity. Thus, up to an additive constant /p_{t}/ is equal to minus the energy. The Hamilton's equation for /Dp_{t}/ relates the change of the energy to ∂_{0}/H/. Note that in the more general case, the momentum conjugate to the time is not the negation of the energy. This choice, /t/(/τ/) = /τ/, is useful for a number of applications.

The extension transformation is canonical in the sense that the two sets of equations of motion describe equivalent dynamics. However, the transformation is not symplectic; in fact, it does not even have the same number of input and output variables.

### Exercise 5.16: Homogeneous extended Lagrangian

Verify that /L_{e}/ is homogeneous of degree one in the velocities.

#page(399)

### Exercise 5.17: Lagrange equations

*a.* Verify that the Lagrange equations for /q_{e}/ are satisfied for exactly the same trajectories that satisfy the original Lagrange equations for /q/.

*b.* Verify that the Lagrange equation for /t/ relates the rate of change of energy to ∂_{0}/L/.

### Exercise 5.18: Lorentz transformations

Investigate Lorentz transformations as point transformations in the extended phase space.

#### Restricted three-body problem
An example that shows the utility of reformulating a problem in the extended phase space is the restricted three-body problem: the motion of a low-mass particle subject to the gravitational attraction of two other massive bodies that move in some fixed orbit. The problem is an idealization of the situation where a body with very small mass moves in the presence of two bodies with much larger masses. Any effects of the smaller body on the larger bodies are neglected. In the simplest version, the motion of all three bodies is assumed to be in the same plane, and the orbits of the two massive bodies are circular.

The motion of the bodies with larger masses is not influenced by the small mass, so we model this situation as the small body moving in a time-varying field of the larger bodies undergoing a prescribed motion. This situation can be captured as a time-dependent Hamiltonian:

$$\begin{array}{ll} {H(t;x,y;p_{x},p_{y}) = \frac{p_{x}^{2} + p_{y}^{2}}{2m} - \frac{Gmm_{1}}{r_{1}(t)} - \frac{Gmm_{2}}{r_{2}(t)},} \tag{5.276} \\ \end{array}$$

where /r/_{1}(/t/) and /r/_{2}(/t/) are the distances of the small body to the larger bodies, /m/ is the mass of the small body, and /m/_{1} and /m/_{2} are the masses of the larger bodies. Note that /r/_{1}(/t/) and /r/_{2}(/t/) are quantities that depend both on the position of the small particle and the time-varying position of the massive particles.

The massive bodies are in circular orbits and maintain constant distance from the center of mass. Let /a/_{1} and /a/_{2} be the distances to the center of mass; then the distances satisfy /m/_{1}/a/_{1} = /m/_{2}/a/_{2}. The angular frequency is $\Omega = \sqrt{G(m_{1} + m_{2})/a^{3}}$ where /a/ is the distance between the masses.

#page(400)

In polar coordinates, with the center of mass of the subsystem of massive particles at the origin and with /r/ and /θ/ describing the position of the low-mass particle, the positions of the two massive bodies are /a/_{2} = /m/_{1}/a//(/m/_{1}+/m/_{2}) with /θ/_{2} = Ω/t/, /a/_{1} = /m/_{2}/a//(/m/_{1}+/m/_{2}) with /θ/_{1} = Ω/t/ + /π/. The distances to the point masses are

$$\begin{array}{ll} {{(r_{2}(t))}^{2} = r^{2} + a_{2}^{2} - 2a_{2}r\,\cos(\theta - \Omega t)} & \\ {{(r_{1}(t))}^{2} = r^{2} + a_{1}^{2} - 2a_{1}r\,\cos(\theta - \Omega t - \pi).} \tag{5.277} \\ \end{array}$$

In polar coordinates, the Hamiltonian is

$$\begin{array}{ll} {H(t;r,\theta;p_{r},p_{\theta}) = \frac{1}{2m}\left( {p_{r}^{2} + \frac{p_{\theta}^{2}}{r^{2}}} \right) - \frac{Gmm_{1}}{r_{1}(t)} - \frac{Gmm_{2}}{r_{2}(t)}.} \tag{5.278} \\ \end{array}$$

The Hamiltonian can be written in terms of some function /f/ such that

$$\begin{array}{ll} {H(t;r,\theta;p_{r},p_{\theta}) = f(r,\theta - \Omega t,p_{r},p_{\theta}).} \tag{5.279} \\ \end{array}$$

The essential feature is that /θ/ and /t/ appear in the Hamiltonian only in the combination /θ/ − Ω/t/.

One way to get rid of the time dependence is to choose a new set of variables with one coordinate equal to this combination /θ/ − Ω/t/, by making a point transformation to a rotating coordinate system. We have shown that

$$\begin{array}{ll} {r\prime = r} \tag{5.280} \\ \end{array}$$

$$\begin{array}{ll} {\theta\prime = \theta - \Omega t} \tag{5.281} \\ \end{array}$$

$$\begin{array}{ll} {p_{r}^{\prime} = p_{r}} \tag{5.282} \\ \end{array}$$

$$\begin{array}{ll} {p_{\theta}^{\prime} = p_{\theta}} \tag{5.283} \\ \end{array}$$

with

$$\begin{array}{lll} {H\prime(t;r\prime,\theta\prime;p_{r}^{\prime},p_{\theta}^{\prime})} & {= H(t;r\prime,\theta\prime + \Omega t;p_{r}^{\prime},p_{\theta}^{\prime}) - \Omega p_{\theta}^{\prime}} & \\  & {= f(r\prime,\theta\prime,p_{r}^{\prime},p_{\theta}^{\prime}) - \Omega p_{\theta}^{\prime}} \tag{5.284} \\ \end{array}$$

is a canonical transformation. The new Hamiltonian, which is not the energy, is conserved because there is no explicit time dependence. It is a useful conserved quantity---the Jacobi constant.#Footnote(27)

#page(401)

We can also eliminate the dependence on the independent time-like variable from the Hamiltonian for the restricted problem by going to the extended phase space, choosing /t/ = /τ/. The Hamiltonian

$$\begin{array}{lll} {H_{e}(\tau;r,\theta,t;p_{r},p_{\theta},p_{t})} & {= H(t;r,\theta;p_{r},p_{\theta}) + p_{t}} & \\  & {= f(r,\theta - \Omega t,p_{r},p_{\theta}) + p_{t}} \tag{5.285} \\ \end{array}$$

is autonomous and is consequently a conserved quantity. Again, we see that /θ/ and /t/ occur only in the combination /θ/ − Ω/t/, which suggests a point transformation to a new coordinate /θ/′ = /θ/ − Ω/t/. This point transformation is independent of the new independent variable /τ/. The transformation is specified in equations ([5.283](chapter005!disp_5.280][5.280]]--[[chapter005!disp_5.283)), augmented by relations specifying how the time coordinate and its conjugate momentum are handled:

$$\begin{array}{ll} {t = t\prime} \tag{5.286} \\ \end{array}$$

$$\begin{array}{ll} {p_{t} = - \Omega p_{\theta}^{\prime} + p_{t}^{\prime}.} \tag{5.287} \\ \end{array}$$

The new Hamiltonian is obtained by composing the old Hamiltonian with the transformation:

$$\begin{array}{ll} {H_{e}^{\prime}(\tau;r\prime,\theta\prime,t\prime;p_{r}^{\prime},p_{\theta}^{\prime},p_{t}^{\prime})} & \\ {\,\,\,\,\,\,\, = H_{e}(\tau;r\prime,\theta\prime + \Omega t\prime,t\prime;p_{r}^{\prime},p_{\theta}^{\prime},p_{t}^{\prime} - \Omega p_{\theta}^{\prime})} & \\ {\,\,\,\,\,\,\, = f(r\prime,\theta\prime,p_{r}^{\prime},p_{\theta}^{\prime}) + p_{t}^{\prime} - \Omega p_{\theta}^{\prime}.} \tag{5.288} \\ \end{array}$$

We recognize that the new Hamiltonian in the extended phase space, which has the same value as the original Hamiltonian in the extended phase space, is just the Jacobi constant plus $ p_{t}^{\prime}$. The new Hamiltonian does not depend on /t/′, so $ p_{t}^{\prime}$ is a constant of the motion. In fact, its value is irrelevant to the rest of the dynamical evolution, so we may set the value of $ p_{t}^{\prime}$ to zero if we like. Thus, we have found that the Hamiltonian in the extended phase space, which is conserved, is just the Jacobi constant plus an additive arbitrary constant. We have two routes to the Jacobi constant: (1) transform the original system to a rotating coordinate system to eliminate the time dependence, but in the process add extra terms to the Hamiltonian, and (2) go to the extended phase space and immediately get a conserved quantity, and by going to rotating coordinates recognize that this Hamiltonian is the same as the
#page(402)
Jacobi constant. So sometimes the Hamiltonian in the extended phase space is a useful conserved quantity.

### Exercise 5.19: Transformations in the extended phase space

In [section 5.2.1](#section_5.2.1) we found that time-dependent transformations for which the derivative of the coordinate--momentum part is symplectic are canonical only if the Hamiltonian is modified by adding a function /K/ subject to certain constraints (equation #Eqn(chapter005,5.42,5.42)). Show that the constraints on /K/ follow from the symplectic condition in the extended phase space, using the choice /t/ = /τ/.

##### 5.5.1 Poincaré--Cartan Integral Invariant
The Poincaré invariant ([section 5.3](#section_5.3)) is especially useful in the extended phase space with /t/ = /τ/. In the extended phase space the extended Hamiltonian does not depend on the independent variable. In the extended phase space canonical transformations are symplectic and the Hamiltonian transforms by composition.

For the special choice of /t/ = /τ/, equation (#Eqn(chapter005,5.90,5.90)) can be rephrased in an interesting way. Let /E/ be the value of the Hamiltonian in the original unextended phase space. Using /q^{n}/ = /t/ and /p_{n}/ = /p_{t}/ = −/E/, we can write

$$\begin{array}{ll} {\sum\limits_{i = 0}^{n - 1}{\int_{R_{i}}{dq^{i}dp_{i} - {\int_{R_{n}}{dtdE = {\sum\limits_{i = 0}^{n - 1}{{\int_{R_{i}^{\prime}}{dq\prime^{i}dp_{i}^{\prime}}} - {\int_{R_{n}^{\prime}}{dt\prime dE\prime}}}}}}}}} \tag{5.289} \\ \end{array}$$

and

$$\begin{array}{ll} {\oint_{\partial R}{({\sum\limits_{i = 0}^{n - 1}{p_{i}dq^{i} - Edt}}) = {\oint_{\partial R\prime}{({\sum\limits_{i = 0}^{n - 1}{p_{i}^{\prime}dq\prime^{i} - E\prime dt\prime}}).}}}} \tag{5.290} \\ \end{array}$$

The relations (#Eqn(chapter005,5.289,5.289)) and (#Eqn(chapter005,5.290,5.290)) are two formulations of the /Poincaré--Cartan integral invariant/.

### 5.6 Reduced Phase Space
Suppose we have a system with /n/+1 degrees of freedom described by a time-independent Hamiltonian in a (2/n/ + 2)-dimensional phase space. Here we can play the converse game: we can choose
#page(403)
any generalized coordinate to play the role of “time” and the negation of its conjugate momentum to play the role of a new /n/-degree-of-freedom time-dependent Hamiltonian in a /reduced phase space/ of 2/n/ dimensions.

More precisely, let

$$\begin{array}{ll} {q = (q^{0},\ldots,q^{n})} & \\ {p = \lbrack p_{0},\ldots,p_{n}\rbrack,} \tag{5.291} \\ \end{array}$$

and suppose we have a system described by a time-independent Hamiltonian

$$\begin{array}{ll} {H(t,q,p) = f(q,p) = E.} \tag{5.292} \\ \end{array}$$

For each solution path there is a conserved quantity /E/. Let's choose a coordinate /q^{n}/ to be the time in a reduced phase space. We define the dynamical variables for the /n/-degree-of-freedom reduced phase space:

$$\begin{array}{ll} {q_{r} = (q_{r}^{0},\ldots,q_{r}^{n - 1})} & \\ {p^{r} = \lbrack p_{0}^{r},\ldots,p_{n - 1}^{r}\rbrack.} \tag{5.293} \\ \end{array}$$

In the original phase space a coordinate such as /q^{n}/ maps time to a coordinate. In the formulation of the reduced phase space we will have to use the inverse function /τ/ = (/q^{n}/)^{−1} to map the coordinate to the time, giving the new coordinates in terms of the new time

$$\begin{array}{ll} {q_{r}^{i} = q^{i} \circ \tau} & \\ {p_{i}^{r} = p_{i} \circ \tau,} \tag{5.294} \\ \end{array}$$

and thus

$$\begin{array}{ll} {Dq_{r}^{i} = D(q^{i} \circ \tau) = (Dq^{i} \circ \tau)(D\tau) = (Dq^{i} \circ \tau)/(Dq^{n} \circ \tau)} & \\ {Dp_{i}^{r} = D(p_{i} \circ \tau) = (Dp_{i} \circ \tau)(D\tau) = (Dp_{i} \circ \tau)/(Dq^{n} \circ \tau).} \tag{5.295} \\ \end{array}$$

We propose that a Hamiltonian in the reduced phase space is the negative of the inverse of /f/(/q/^{0}, ..., /q^{n}/; /p/_{0}, ..., /p_{n}/) = /E/ with respect to the /p_{n}/ argument:

$$\begin{array}{ll} {H_{r}(x,q_{r},p^{r}) = - (\text{the}\, p_{x}\,\text{such that}\, f(q_{r},x;p^{r},p_{x}) = E).} \tag{5.296} \\ \end{array}$$

#page(404)

Note that in the reduced phase space we will have indices for the structured variables in the range 0 ... /n/−1, whereas in the original phase space the indices are in the range 0 ... /n/. We will show that /H_{r}/ is an appropriate Hamiltonian for the given dynamical system in the reduced phase space. To compute Hamilton's equations we must expand the implicit definition of /H_{r}/. We define an auxiliary function

$$\begin{array}{ll} {g(x,q_{r},p^{r}) = f(q_{r},x;p^{r}, - H_{r}(x,q_{r},p^{r})).} \tag{5.297} \\ \end{array}$$

Note that /by construction/ this function is identically a constant /g/ = /E/. Thus all of its partial derivatives are zero:

$$\begin{array}{rll} {\partial_{0}g} & {= {(\partial_{0}f)}^{n} - {(\partial_{1}f)}^{n}\partial_{0}H_{r} = 0} & \\ {(\partial_{1}g)}_{i} & {= {(\partial_{0}f)}_{i} - {(\partial_{1}f)}^{n}{(\partial_{1}H_{r})}_{i} = 0} & \\ {(\partial_{2}g)}^{i} & {= {(\partial_{1}f)}^{i} - {(\partial_{1}f)}^{n}{(\partial_{2}H_{r})}^{i} = 0,} \tag{5.298} \\ \end{array}$$

where we have suppressed the arguments. Solving for partials of /H_{r}/, we get

$$\begin{array}{ll} {{(\partial_{1}H_{r})}_{i} = {(\partial_{0}f)}_{i}/{(\partial_{1}f)}^{n} = {(\partial_{1}H)}_{i}/{(\partial_{2}H)}^{n}} & \\ {{(\partial_{2}H_{r})}^{i} = {(\partial_{1}f)}^{i}/{(\partial_{1}f)}^{n} = {(\partial_{2}H)}^{i}/{(\partial_{2}H)}^{n}.} \tag{5.299} \\ \end{array}$$

Using these relations, we can deduce the Hamilton's equations in the reduced phase space from the Hamilton's equations in the original phase space:

$$\begin{array}{lll} {Dq_{r}^{i}(x)} & {= \frac{Dq^{i}(\tau(x))}{Dq^{n}(\tau(x))}} & \\  & {= \frac{{(\partial_{2}H(\tau(x),q(\tau(x)),p(\tau(x))))}^{i}}{{(\partial_{2}H(\tau(x),q(\tau(x)),p(\tau(x))))}^{n}}} & \\  & {= {(\partial_{2}H_{r}(x,q_{r}(x),p^{r}(x)))}^{i}} \tag{5.300} \\ \end{array}$$

$$\begin{array}{lll} {Dp_{i}^{r}(x)} & {= \frac{Dp_{i}(\tau(x))}{Dq^{n}(\tau(x))}} & \\  & {= \frac{- {(\partial_{1}H(\tau(x),q(\tau(x)),p(\tau(x))))}_{i}}{{(\partial_{2}H(\tau(x),q(\tau(x)),p(\tau(x))))}^{n}}} & \\  & {= - {(\partial_{1}H_{r}(x,q_{r}(x),p^{r}(x)))}_{i}.} \tag{5.301} \\ \end{array}$$

#page(405)

#### Orbits in a central field
Consider planar motion in a central field. We have already seen this expressed in polar coordinates in equation (#Eqn(chapter003,3.100,3.100)):

$$\begin{array}{ll} {H(t;r,\varphi;p_{r},p_{\varphi}) = \frac{p_{r}^{2}}{2m} + \frac{p_{\varphi}^{2}}{2mr^{2}} + V(r).} \tag{5.302} \\ \end{array}$$

There are two degrees of freedom and the Hamiltonian is time independent. Thus the energy, the value of the Hamiltonian, is conserved on realizable paths. Let's forget about time and reparameterize this system in terms of the orbital radius /r/.#Footnote(28) To do this we solve

$$\begin{array}{ll} {H(t;r,\varphi;p_{r},p_{\varphi}) = E} \tag{5.303} \\ \end{array}$$

for /p_{r}/, obtaining

$$\begin{array}{ll} {H\prime(r,\varphi,p_{\varphi}) = - p_{r} = - \left( {2m(E - V(r)) - \frac{p_{\varphi}^{2}}{r^{2}}} \right)^{\frac{1}{2}},} \tag{5.304} \\ \end{array}$$

which is the Hamiltonian in the reduced phase space.

Hamilton's equations are now quite simple:

$$\begin{array}{ll} {\frac{d\varphi}{dr} = \frac{\partial H\prime}{\partial p_{\varphi}} = \frac{p_{\varphi}}{r^{2}}\left( {2m(E - V(r)) - \frac{p_{\varphi}^{2}}{r^{2}}} \right)^{- \frac{1}{2}}} \tag{5.305} \\ \end{array}$$

$$\begin{array}{ll} {\frac{dp_{\varphi}}{dr} = - \frac{\partial H\prime}{\partial\varphi} = 0.} \tag{5.306} \\ \end{array}$$

The momentum /p_{φ}/ is independent of /r/ (as it was with /t/), so for any particular orbit we may define a constant angular momentum /L/. Thus our problem ends up as a simple quadrature:

$$\begin{array}{ll} {\varphi(r) = {\int_{}^{r}{\frac{L}{r^{2}}\left( {2m(E - V(r)) - \frac{L^{2}}{r^{2}}} \right)^{- \frac{1}{2}}dr + \varphi_{0}.}}} \tag{5.307} \\ \end{array}$$

#page(406)

To see the utility of this procedure, we continue our example with a definite potential energy---a gravitating point mass:

$$\begin{array}{ll} {V(r) = - \frac{\mu}{r}.} \tag{5.308} \\ \end{array}$$

When we substitute this into equation (#Eqn(chapter005,5.307,5.307)) we obtain a mess that can be simplified to

$$\begin{array}{ll} {\varphi(r) = L\,{\int_{}^{r}{\frac{dr}{r\sqrt{2mEr^{2} + 2m\mu r - L^{2}}} + \varphi_{0}.}}} \tag{5.309} \\ \end{array}$$

Integrating this, we obtain another mess, which can be simplified and rearranged to obtain the following:

$$\begin{array}{ll} {\frac{1}{r} = \frac{m\mu}{L^{2}}\left( {1 - \sqrt{1 + \frac{2EL^{2}}{m\mu^{2}}}\,\sin\,(\varphi(r) - \varphi_{0})} \right).} \tag{5.310} \\ \end{array}$$

This can be recognized as the polar-coordinate form of the equation of a conic section with eccentricity /e/ and parameter /p/:

$$\begin{array}{ll} {\frac{1}{r} = \frac{1 + e\,\cos\,\theta}{p}} \tag{5.311} \\ \end{array}$$

where

$$\begin{array}{ll} \begin{array}{llll} {e = \sqrt{1 + \frac{2EL^{2}}{m\mu^{2}}},} & {p = \frac{L^{2}}{m\mu}} & \text{and} & {\theta = \varphi_{0} - \varphi(r) - \frac{\pi}{2}.} \\ \end{array} \tag{5.312} \\ \end{array}$$

In fact, if the orbit is an ellipse with semimajor axis /a/, we have

$$\begin{array}{ll} {p = a(1 - e^{2})} \tag{5.313} \\ \end{array}$$

and so we can identify the role of energy and angular momentum in shaping the ellipse:

$$\begin{array}{llll} {E = - \frac{\mu}{2a}} & \text{and} & {L = \sqrt{m\mu a(1 - e^{2})}.} \tag{5.314} \\ \end{array}$$

What we get from analysis in the reduced phase space is the geometry of the trajectory, but we lose the time-domain behavior. The reduction is often worth the price.

#page(407)

Although we have treated time in a special way so far, we have found that time is not special. It can be included in the coordinates to make a driven system autonomous. And it can be eliminated from any autonomous system in favor of any other coordinate. This leads to numerous strategies for simplifying problems, by removing time variation and then performing canonical transforms on the resulting conservative autonomous system to make a nice coordinate that we can then dump back into the role of time.

#### Generating functions in extended phase space
We can represent canonical transformations with mixed-variable generating functions. We can extend these to represent transformations in the extended phase space. Let /F/_{2} be a generating function with arguments (/t/, /q/, /p/′). Then, the corresponding $ F_{2}^{e}$ in the extended phase space can be taken to be

$$\begin{array}{ll} {F_{2}^{e}(\tau;q,t;p\prime,p_{t}^{\prime}) = tp_{t}^{\prime} + F_{2}(t,q,p).} \tag{5.315} \\ \end{array}$$

The relations between the coordinates and the momenta are the same as before. We also have

$$\begin{array}{rll} p_{t} & {= {(\partial_{1}F_{2}^{e})}_{n}(\tau;q,t;p\prime,p_{t}^{\prime}) = p_{t}^{\prime} + \partial_{0}F_{2}(t,q,p)} & \\ {t\prime} & {= {(\partial_{2}F_{2}^{e})}^{n}(\tau;q,t;p\prime,p_{t}^{\prime}) = t.} \tag{5.316} \\ \end{array}$$

The first equation gives the relationship between the original Hamiltonians:

$$\begin{array}{ll} {H\prime(t,q\prime,p\prime) = H(t,q,p) + \partial_{0}F_{2}(t,q,p),} \tag{5.317} \\ \end{array}$$

as required. Time-independent canonical transformations, where /H/′ = /H/ ∘ /C/_{H}, have symplectic /qp/ part. The generating-function representation of a time-dependent transformation does not depend on the independent variable in the extended phase space. So, in extended phase space the /qp/ part of the transformation, which includes the time and the momentum conjugate to time, is symplectic.

### Exercise 5.20: Rotating coordinates in extended phase space

In the extended phase space the time is one of the coordinates. Carry out the transformation to rotating coordinates using an /F/_{2}-type generating function in the extended phase space. Compare Hamiltonian (#Eqn(chapter005,5.178,5.178)) to the Hamiltonian obtained by composition with the transformation.

#page(408)

### 5.7 Summary
Canonical transformations can be used to reformulate a problem in coordinates that are easier to understand or that expose some symmetry of a problem.

In this chapter we have investigated different representations of a dynamical system. We have found that different representations will be equivalent if the coordinate--momentum part of the transformation has a symplectic derivative, and if the Hamiltonian transforms in a specified way. If the phase-space transformation is time independent, then the Hamiltonian transforms by composition with the phase-space transformation. The symplectic condition can be equivalently expressed in terms of the fundamental Poisson brackets. The Poisson bracket and the /ω/ function are invariant under canonical transformations. The invariance of /ω/ implies that the sum of the areas of the projections onto fundamental coordinate--momentum planes is preserved (Poincaré integral invariant) by canonical transformations.

A generating function is a real-valued function of the phase-space coordinates and time that represents a canonical transformation through its partial derivatives. We found that every canonical transformation can be represented by a generating function. The proof depends on the Poincaré integral invariant.

We can formulate an extended phase space in which time is treated as another coordinate. Time-dependent transformations are simple in the extended phase space. In the extended phase space the Poincaré integral invariant is the Poincaré--Cartan integral invariant. We can also reformulate a time-independent problem as a time-dependent problem with fewer degrees of freedom, with one of the original coordinates taking on the role of time; this is the reduced phase space.

### 5.8 Projects
### Exercise 5.21: Hierarchical Jacobi coordinates

A Hamiltonian for the /n/-body problem is

$$\begin{array}{ll} {H = T + V} \tag{5.318} \\ \end{array}$$

#page(409)

with

$$\begin{array}{ll} {T(t;x_{0,}x_{1},\ldots,x_{n - 1};p_{0},p_{1},\ldots,p_{n - 1}) = {\sum\limits_{i = 0}^{n - 1}\frac{p_{i}^{2}}{2m_{i}}}} \tag{5.319} \\ \end{array}$$

and

$$\begin{array}{ll} {V(t;x_{0},x_{1},\ldots,x_{n - 1};p_{0},p_{1},\ldots,p_{n - 1}) = {\sum\limits_{i < j}{f_{ij}\left( \left\| {x_{i} - x_{j}} \right\| \right)}},} \tag{5.320} \\ \end{array}$$

where /x_{i}/ is the tuple of rectangular coordinates for body /i/ and /p_{i}/ is the tuple of conjugate linear momenta for body /i/.

The potential energy of the system depends only on the relative positions of the bodies, so the relative motion decouples from the center of mass motion. In this problem we explore canonical transformations that achieve this decoupling.

*a.* Canonical heliocentric coordinates. The coordinates transform as follows:

$$\begin{array}{ll} {x_{0}^{\prime} = X,} \tag{5.321} \\ \end{array}$$

where /X/ is the center of mass of the system, and

$$\begin{array}{ll} {x_{i}^{\prime} = x_{i} - x_{0},} \tag{5.322} \\ \end{array}$$

for /i/ > 0, the differences of the position of body /i/ and the body with index 0 (which might be the Sun). Find the associated canonical momenta using an /F/_{2}-type generating function. Show that the potential energy can be written solely in terms of the coordinates for /i/ > 0. Show that the kinetic energy is not in the form of a sum of squares of momenta divided by mass constants.

*b.* Jacobi coordinates. The Jacobi coordinates isolate the center of mass motion, without spoiling the usual diagonal quadratic form of the kinetic energy. Define /X_{i}/ to be the center of mass of the bodies with indices less than or equal to /i/:

$$\begin{array}{ll} {X_{i} = \frac{\sum_{j = 0}^{i}{m_{j}x_{j}}}{\sum_{j = 0}^{i}m_{j}}.} \tag{5.323} \\ \end{array}$$

The Jacobi coordinates are defined by

$$\begin{array}{ll} {x_{i - 1}^{\prime} = x_{i} - X_{i - 1},} \tag{5.324} \\ \end{array}$$

for 0 < /i/ < /n/, and

$$\begin{array}{ll} {x_{n - 1}^{\prime} = X_{n - 1}.} \tag{5.325} \\ \end{array}$$

#page(410)

The coordinates $ x_{i}^{\prime}$ for 0 < /i/ < /n/ are the difference of the position of body /i/ − 1 and the center of mass of bodies with lower indices; the coordinate $ x_{n - 1}^{\prime}$ is the center of mass of the system. Complete the canonical transformation by finding the conjugate momenta using an /F/_{2}-type generating function. Show that the kinetic energy can still be written in the form

$$\begin{array}{ll} {T(t;x_{0}^{\prime},x_{1}^{\prime},\ldots,x_{n - 1}^{\prime};p_{0}^{\prime},p_{1}^{\prime},\ldots,p_{n - 1}^{\prime}) = {\sum\limits_{i = 0}^{n - 1}{\frac{{p_{i}^{\prime}}^{2}}{2m_{i}^{\prime}},}}} \tag{5.326} \\ \end{array}$$

for some constants $ m_{i}^{\prime}$, and that the potential /V/ can be written solely in terms of the Jacobi coordinates $ x_{i}^{\prime}$ with indices /i/ > 0.

*c.* Hierarchical Jacobi coordinates. Define a “body” as a tuple of a mass and a rectangular position tuple. An /n/-body “system” is a tuple of /n/ bodies: (/b/_{0}, /b/_{1}, ..., /b/_{n−1}). Define a “linking” transformation $\mathcal{L}_{jk}$ for bodies /j/ and /k/ that takes an /n/-body system and returns a new linked system:

$$\begin{array}{ll} {(b_{0}^{\prime},\ldots,b_{n - 1}^{\prime}) = \mathcal{L}_{jk}(b_{0},\ldots,b_{n - 1}).} \tag{5.327} \\ \end{array}$$

The bodies in the new system are the same as the bodies in the old system $ b_{i}^{\prime} = b_{i}$ except for bodies /j/ and /k/:

$$\begin{array}{ll} {(m_{j}^{\prime},x_{j}^{\prime}) = (m_{j}m_{k}/(m_{j} + m_{k}),x_{k} - x_{j})} & \\ {(m_{k}^{\prime},x_{k}^{\prime}) = (m_{j} + m_{k},(m_{j}x_{j} + m_{k}x_{k})/(m_{j} + m_{k})).} \tag{5.328} \\ \end{array}$$

This is a transformation to relative coordinates and center of mass for bodies /j/ and /k/. Extend this transformation to phase space and show that it preserves the form of the kinetic energy

$$\begin{array}{ll} {\sum\limits_{i}{\frac{{(p_{i})}^{2}}{2m_{i}} = {\sum\limits_{i}{\frac{{(p_{i}^{\prime})}^{2}}{2m_{i}^{\prime}}.}}}} \tag{5.329} \\ \end{array}$$

Show that the transformation to Jacobi coordinates of part *b* is generated by a composition of linking transformations:

$$\begin{array}{ll} {\mathcal{L}_{n - 2,n - 1} \circ \cdots \circ \mathcal{L}_{1,2} \circ \mathcal{L}_{0,1}.} \tag{5.330} \\ \end{array}$$

Interpret the coordinate transformation produced by such a succession of linking transformations; why do we call this a “linking” transformation? What requirement has to be satisfied for a composition of linking transformations to isolate the center of mass of the system (make it one of the coordinates)? Taking this constraint into account, find hierarchical Jacobi coordinates for a system with six bodies, arranged as two triple systems, each of which is a binary plus a third body. Verify that one of the coordinates is the center of mass of the system, and that the kinetic energy remains a sum of squares of the momenta divided by an appropriate mass constant.

----

#FootnoteRef(1) Solving for /p/ in terms of /p/′ involves multiplying equation (#Eqn(chapter005,5.3,5.3)) on the right by (∂_{1}/F/(/t/, /q/′))^{−1}. This inverse is the structure that when multiplying ∂_{1}/F/(/t/, /q/′) on the right gives an identity structure. Structures representing linear transformations may be represented in terms of matrices. In this case, the matrix representation of the inverse structure is the inverse of the matrix representing the given structure.

#FootnoteRef(2)In chapter 1 the transformation /C/ takes a local tuple in one coordinate system and gives a local tuple in another coordinate system. In this chapter /C/_{H} is a phase-space transformation.

#FootnoteRef(3)The velocities and the momenta are dual geometric objects with respect to time-independent point transformations. The velocities are coordinates of a vector field on the configuration manifold, and the momenta are coordinates of a covector field on the configuration manifold. The invariance of the inner product /pv/ under time-independent point transformations provides a motivation for our use of superscripts for velocity components and subscripts for momentum components.

#FootnoteRef(4)The procedure solve-linear-right multiplies its first argument by the inverse of its second argument on the right. So, if /u/ = /vM/ then /v/ = /uM/^{−1}; (solve-linear-right u M) produces v.

#FootnoteRef(5)/D_{s}/ is not a derivative operator. It is not linear because the time component is a nonzero constant.

#FootnoteRef(6)Sometimes we use a center dot to indicate multiplication, to avoid the ambiguity of the use of juxtaposition to indicate both multiplication and function application. This is not to be interpreted as a vector dot product.

#FootnoteRef(7)Actually, for /I/ = 0 the transform is not well defined and so it is not canonical for that value. This transformation is “locally canonical” in that it is canonical for nonzero values of /I/. We will ignore this essentially topological problem.

#FootnoteRef(8)Unlike /D_{s}/,$\mathcal{D}$ is linear and can be a derivative operator.

#FootnoteRef(9)The procedure zero-like produces a structure of zeros with the shape of its argument.

#FootnoteRef(10)This is just a rearrangement of the arguments of /R_{z}/: /R/(Ω)(/t/, /q/′) = /R_{z}/(Ω/t/)(/q/′).

#FootnoteRef(11)For each linear transformation /T/ : /A/ → /A/ of incremental phase-space states there is a unique linear transformation $ T^{\mathcal{T}}:A^{\star}\rightarrow A^{\star}$ of the dual space, called the /transpose/ of /T/, such that for every real-valued linear function /g/ : /A/ → *R* of incremental phase-space states, and for every /a/ ∈ /A/ we have $(T^{\mathcal{T}}(g))(a) = g(T(a))$. As linear multipliers ${(DT(a))}^{\mathcal{T}} \cdot Dg(a) \cdot a = Dg(a) \cdot DT(a) \cdot a $. But for arbitrary /a/ this is ${(DT(a))}^{\mathcal{T}} \cdot Dg(a) = Dg(a) \cdot DT(a)$. In our application, /DT/ (/a/) is /DC/_{H}(/s/′), and /Dg/(/a/) is /DH/(/C/_{H}(/s/′)).

#FootnoteRef(12)The procedure compatible-shape takes any structure and produces another structure that is guaranteed to multiply with the given structure to produce a numerical quantity. For example, the shape of /DH/(/s/) is a compatible shape to the shape of /s/: if they are multiplied the result is a numerical quantity. This is the /s/^{⋆} that appears in equation (#Eqn(chapter005,5.48,5.48)).

#FootnoteRef(13)The procedure transpose is simply defined for traditional matrices, but because structures that specify linear transformations may have arbitrary substructure, the procedure needs to be supplied with a template that specifies this structure. So the procedure transpose takes two arguments: (transpose ms rs), where ms is the structure to be transposed and the template rs is a structure that is appropriate for multiplication with ms on the right.

#FootnoteRef(14)Actually, this is more interesting: we allow transformations that arbitrarily distort time, as tau is an arbitrary literal function. The canonical condition is concerned only with the possibly time-dependent transformation of coordinates and momenta.

#FootnoteRef(15)The /qp/ submatrix of a square matrix of dimension 2/n/ + 1 is the 2/n/-dimensional matrix obtained by deleting the first row and the first column of the given matrix. This can be computed by:
```Scheme
(define (qp-submatrix m) (m:submatrix m 1 (m:num-rows m) 1 (m:num-cols m))) 
```

#FootnoteRef(16)The procedure D-as-matrix is defined as:
```Scheme
(define ((D-as-matrix F) s) (s->m (compatible-shape (F s)) ((D F) s) s))) 
```

#FootnoteRef(17)The /q^{i}/, /p_{i}/ plane is the /i/th /canonical plane/ in these phase-space variables.

#FootnoteRef(18)The structure ∂_{2}∂_{1}/F/_{1} is a down of downs, so it is compatible for contraction with an up on either side. But it is not symmetrical, so the associations must be specified. To solve this problem we use index notation (ugh!).

So we use indices to select particular components of structured objects. If an index symbol appears both as a superscript and as a subscript in an expression, the value of the expression is the sum over all possible values of the index symbol of the designated components (Einstein summation convention). Thus, for example, if $\dot{q}$ and /p/ are of dimension /n/ then the indicated product $ p_{i}{\dot{q}}^{i}$ is to be interpreted as $\Sigma_{i = 0}^{n - 1}p_{i}{\dot{q}}^{i}$.

#FootnoteRef(19)A structure is nonsingular if the determinant of the matrix representation of the structure is nonzero.

#FootnoteRef(20)Point transformations are not in this class: we cannot solve for the momenta in terms of the positions for point transformations, because for a point transformation the primed and unprimed coordinates can be deduced from each other, so there is not enough information in the coordinates to deduce the momenta.

#FootnoteRef(21)Let /F/ be defined as the path-independent line integral $ F\left( x \right) = {\int_{x_{0}}^{x}{\sum\limits_{i}{f_{i}\left( x \right)dx^{i} + F\left( x_{0} \right);}}}$ then ∂/_{i}F/(/x/) = /f_{i}/(/x/).

#FootnoteRef(22)There may be some singular cases and topological problems that prevent this from being rigorously true.

#FootnoteRef(23)The various generating functions are traditionally known by the names /F/_{1}, /F/_{2}, /F/_{3}, and /F/_{4}. Please don't blame us.

#FootnoteRef(24)We augment the Lagrangian with the total time derivative of the constraint so that the Legendre transform will be well defined.

#FootnoteRef(25)Once we have made this reduction, taking /p_{λ}/ to be zero, we can no longer perform a Legendre transform back to the extended Lagrangian system; we cannot solve for /p_{t}/ in terms of /v_{t}/. However, the Legendre transform in the extended system from $ H_{e}^{\prime}$ to $ L_{e}^{\prime}$, with associated state variables, is well defined.

#FootnoteRef(26)If /f/ is strictly increasing then /Df/ is never zero.

#FootnoteRef(27)Actually, the traditional Jacobi constant is /C/ = −2/H/′.

#FootnoteRef(28)We could have chosen to reparameterize in terms of /φ/, but then both /p_{r}/ and /r/ would occur in the resulting time-independent Hamiltonian. The path we have chosen takes advantage of the fact that /φ/ does not appear in our Hamiltonian, so /p_{φ}/ is a constant of the motion. This structure suggests that to solve this kind of problem we need to look ahead, as in playing chess. 
#FootnoteEnd

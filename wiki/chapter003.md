!!Polyglot
## Hamiltonian Mechanics
### Chapter 3
#page(195)
#Quote(Numerical experiments are just what their name implies: experiments.   In describing and evaluating them, one should enter the state of mind   of the experimental physicist, rather than that of the mathematician.   Numerical experiments cannot be used to prove theorems; but, from the   physicist's point of view, they do often provide convincing evidence   for the existence of a phenomenon. We will therefore follow an   informal, descriptive and non-rigorous approach. Briefly stated, our   aim will be to /understand/ the fundamental properties of dynamical   systems rather than to /prove/ them.)
#Caption Michel Hénon, “Numerical Exploration of Hamiltonian Systems,” in   /Chaotic Behavior of Deterministic Systems/   [21](bibliography!bib_21), [p. 57](chapter001!p57). #CaptionEnd

The formulation of mechanics with generalized coordinates and momenta as dynamical state variables is called the Hamiltonian formulation. The Hamiltonian formulation of mechanics is equivalent to the Lagrangian formulation; however, each presents a useful point of view. The Lagrangian formulation is especially useful in the initial formulation of a system. The Hamiltonian formulation is especially useful in understanding the evolution of a system, especially when there are symmetries and conserved quantities.

For each continuous symmetry of a mechanical system there is a conserved quantity. If the generalized coordinates can be chosen to reflect a symmetry, then, by the Lagrange equations, the momenta conjugate to the cyclic coordinates are conserved. We have seen that such conserved quantities allow us to deduce important properties of the motion. For instance, consideration of the energy and angular momentum allowed us to deduce that rotation of a free rigid body about the axis of intermediate moment of inertia is unstable, and that rotation about the other principal axes is stable. For the axisymmetric top, we used two conserved momenta to reexpress the equations governing the evolution of the tilt angle so that they involve only the tilt angle and its derivative.
#page(196)
The evolution of the tilt angle can be determined independently and has simply periodic solutions. Consideration of the conserved momenta has provided key insight. The Hamiltonian formulation is motivated by the desire to focus attention on the momenta.

In the Lagrangian formulation the momenta are, in a sense, secondary quantities: the momenta are functions of the state space variables, but the evolution of the state space variables depends on the state space variables and not on the momenta. To make use of any conserved momenta requires fooling around with the specific equations. The momenta can be rewritten in terms of the coordinates and the velocities, so, locally, we can solve for the velocities in terms of the coordinates and momenta. For a given mechanical system, and a Lagrangian describing its dynamics in a given coordinate system, the momenta and the velocities can be deduced from each other. Thus we can represent the dynamical state of the system in terms of the coordinates and momenta just as well as with the coordinates and the velocities. If we use the coordinates and momenta to represent the state and write the associated state derivative in terms of the coordinates and momenta, then we have a self-contained system. This formulation of the equations governing the evolution of the system has the advantage that if some of the momenta are conserved, the remaining equations are immediately simplified.

The Lagrangian formulation of mechanics has provided the means to investigate the motion of complicated mechanical systems. We have found that dynamical systems exhibit a bewildering variety of possible motions. The motion is sometimes rather simple and sometimes very complicated. Sometimes the evolution is very sensitive to the initial conditions, and sometimes it is not. And sometimes there are orbits that maintain resonance relationships with a drive. Consider the periodically driven pendulum: it can behave more or less as an undriven pendulum with extra wiggles, it can move in a strongly chaotic manner, or it can move in resonance with the drive, oscillating once for every two cycles of the drive or looping around once per drive cycle. Or consider the Moon. The Moon rotates synchronously with its orbital motion, always pointing roughly the same face to the Earth. However, Mercury rotates three times every two times it circles the Sun, and Hyperion rotates chaotically.

How can we make sense of this? How do we put the possible motions of these systems in relation to one another? What other
#page(197)
motions are possible? The Hamiltonian formulation of dynamics provides a convenient framework in which the possible motions may be placed and understood. We will be able to see the range of stable resonance motions and the range of states reached by chaotic trajectories, and discover other unsuspected possible motions. So the Hamiltonian formulation gives us much more than the stated goal of expressing the system derivative in terms of potentially conserved quantities.

### 3.1 Hamilton's Equations
The momenta are given by momentum state functions of the time, the coordinates, and the velocities.#Footnote(1) Locally, we can find inverse functions that give the velocities in terms of the time, the coordinates, and the momenta. We can use this inverse function to represent the state in terms of the coordinates and momenta rather than the coordinates and velocities. The equations of motion when recast in terms of coordinates and momenta are called /Hamilton's canonical equations/.

We present three derivations of Hamilton's equations. The first derivation is guided by the strategy outlined above and uses nothing more complicated than implicit functions and the chain rule. The second derivation ([section 3.1.1](#section_3.1.1)) first abstracts a key part of the first derivation and then applies the more abstract machinery to derive Hamilton's equations. The third ([section 3.1.2](#section_3.1.2)) uses the action principle.

Lagrange's equations give us the time derivative of the momentum /p/ on a path /q/:

$$\begin{array}{ll} {Dp(t) = \partial_{1}L(t,q(t),\, Dq(t)),} \tag{3.1} \\ \end{array}$$

where

$$\begin{array}{ll} {p(t) = \partial_{2}L(t,q(t),\, Dq(t)).} \tag{3.2} \\ \end{array}$$

To eliminate /Dq/ we need to solve equation (#Eqn(chapter003,3.2,3.2)) for /Dq/ in terms of /p/.

#page(198)

Let $\mathcal{V}$ be the function that gives the velocities in terms of the time, coordinates, and momenta. Defining $\mathcal{V}$ is a problem of functional inverses. To prevent confusion we use names for the variables that have no mnemonic significance. Let

$$\begin{array}{ll} {a = \partial_{2}L(b,c,d);} \tag{3.3} \\ \end{array}$$

then $\mathcal{V}$ satisfies

$$\begin{array}{ll} {d = \mathcal{V}(b,c,a).} \tag{3.4} \\ \end{array}$$

So $\mathcal{V}$ and ∂_{2}/L/ are inverses on the third argument position:

$$\begin{array}{ll} {d = \mathcal{V}(b,c,\partial_{2}L(b,c,d))} \tag{3.5} \\ \end{array}$$

$$\begin{array}{ll} {a = \partial_{2}L(b,c,\mathcal{V}(b,c,a)).} \tag{3.6} \\ \end{array}$$

The Lagrange equation (#Eqn(chapter003,3.1,3.1)) can be rewritten in terms of /p/ using $\mathcal{V}$:

$$\begin{array}{ll} {Dp(t) = \partial_{1}L(t,q(t),\,\mathcal{V}(t,q(t),p(t))).} \tag{3.7} \\ \end{array}$$

We can also use $\mathcal{V}$ to rewrite equation (#Eqn(chapter003,3.2,3.2)) as an equation for /Dq/ in terms of /t/, /q/ and /p/:

$$\begin{array}{ll} {Dq(t) = \mathcal{V}(t,q(t),p(t)).} \tag{3.8} \\ \end{array}$$

Equations (#Eqn(chapter003,3.7,3.7)) and (#Eqn(chapter003,3.8,3.8)) give the rate of change of /q/ and /p/ along realizable paths as functions of /t/, /q/, and /p/ along the paths.

Though these equations fulfill our goal of expressing the equations of motion entirely in terms of coordinates and momenta, we can find a better representation. Define the function

$$\begin{array}{ll} {\widetilde{L}(t,q,p) = L(t,q,\mathcal{V}(t,q,p)),} \tag{3.9} \\ \end{array}$$

which is the Lagrangian reexpressed as a function of time, coordinates, and momenta.#Footnote(2) For the equations of motion we need ∂_{1}/L/ evaluated with the appropriate arguments. Consider

#page(199)

$$\begin{array}{lll} {\partial_{1}\widetilde{L}(t,q,p)} & {= \partial_{1}L(t,q,\mathcal{V}(t,q,p)) + \partial_{2}L(t,q,\mathcal{V}(t,q,p))\partial_{1}\mathcal{V}(t,q,p)} & \\  & {= \partial_{1}L(t,q,\mathcal{V}(t,q,p)) + p\partial_{1}\mathcal{V}(t,q,p),} \tag{3.10} \\ \end{array}$$

where we used the chain rule in the first step and the inverse property (#Eqn(chapter003,3.6,3.6)) of $\mathcal{V}$ in the second step. Introducing the momentum selector#Footnote(3)/P/ (/t/, /q/, /p/) = /p/, and using the property ∂_{1}/P/ = 0, we have

$$\begin{array}{lll} {\partial_{1}L(t,q,\mathcal{V}(t,q,p))} & {= \partial_{1}\widetilde{L}(t,q,p) - P(t,q,p)\partial_{1}\mathcal{V}(t,q,p)} & \\  & {= \partial_{1}(\widetilde{L} - P\mathcal{V})(t,q,p)} & \\  & {= - \partial_{1}\, H(t,q,p),} \tag{3.11} \\ \end{array}$$

where the /Hamiltonian H/ is defined by#Footnote(4)

$$\begin{array}{ll} {H = P\mathcal{V} - \widetilde{L}.} \tag{3.12} \\ \end{array}$$

Using the algebraic result (#Eqn(chapter003,3.11,3.11)), the Lagrange equation (#Eqn(chapter003,3.7,3.7)) for /Dp/ becomes

$$\begin{array}{ll} {Dp(t) = - \partial_{1}H(t,q(t),p(t)).} \tag{3.13} \\ \end{array}$$

The equation for /Dq/ can also be written in terms of /H/. Consider

$$\begin{array}{lll} {\partial_{2}H(t,q,p)} & {= \partial_{2}(P\mathcal{V} - \widetilde{L})(t,q,p)} & \\  & {= \mathcal{V}(t,q,p) + p\partial_{2}\mathcal{V}(t,q,p) - \partial_{2}\widetilde{L}(t,q,p).} \tag{3.14} \\ \end{array}$$

To carry out the derivative of $\widetilde{L}$ we write it out in terms of /L/:

$$\begin{array}{ll} {\partial_{2}\widetilde{L}(t,q,p) = \partial_{2}L(t,q,\mathcal{V}(t,q,p))\partial_{2}\mathcal{V}(t,q,p) = p\partial_{2}\mathcal{V}(t,q,p),} \tag{3.15} \\ \end{array}$$

again using the inverse property (#Eqn(chapter003,3.6,3.6)) of $\mathcal{V}$. So, putting equations (#Eqn(chapter003,3.14,3.14)) and (#Eqn(chapter003,3.15,3.15)) together, we obtain

$$\begin{array}{ll} {\partial_{2}H(t,q,p) = \mathcal{V}(t,q,p).} \tag{3.16} \\ \end{array}$$

Using the algebraic result (#Eqn(chapter003,3.16,3.16)), equation (#Eqn(chapter003,3.8,3.8)) for /Dq/ becomes

$$\begin{array}{ll} {Dq(t) = \partial_{2}H(t,q(t),\, p(t)).} \tag{3.17} \\ \end{array}$$

#page(200)

Equations (#Eqn(chapter003,3.13,3.13)) and (#Eqn(chapter003,3.17,3.17)) give the derivatives of the coordinate and momentum path functions at each time in terms of the time, and the coordinates and momenta at that time. These equations are known as /Hamilton's equations/:#Footnote(5)

$$\begin{array}{ll} {Dq(t) = \partial_{2}H(t,q(t),\, p(t))} & \\ {Dp(t) = - \partial_{1}H(t,q(t),\, p(t)).} \tag{3.18} \\ \end{array}$$

The first equation is just a restatement of the relationship of the momenta to the velocities in terms of the Hamiltonian and holds for any path, whether or not it is a realizable path. The second equation holds only for realizable paths.

Hamilton's equations have an especially simple and symmetrical form. Just as Lagrange's equations are constructed from a real-valued function, the Lagrangian, Hamilton's equations are constructed from a real-valued function, the Hamiltonian. The Hamiltonian function is#Footnote(6)

$$\begin{array}{ll} {H(t,q,p) = p\mathcal{V}(t,q,p) - L(t,q,\mathcal{V}(t,q,p)).} \tag{3.19} \\ \end{array}$$

The Hamiltonian has the same value as the energy function /ℰ/ (see equation #Eqn(chapter001,1.142,1.142)), except that the velocities are expressed in terms of time, coordinates, and momenta by $\mathcal{V}$:

$$\begin{array}{ll} {H(t,q,p) = \mathcal{E}(t,q,\mathcal{V}(t,q,p)).} \tag{3.20} \\ \end{array}$$

#### Illustration
Let's try something simple: the motion of a particle of mass /m/ with potential energy /V/ (/x/, /y/). A Lagrangian is

$$\begin{array}{ll} {L(t;x,y;v_{x},v_{y}) = \frac{1}{2}m(v_{x}^{2} + v_{y}^{2}) - V(x,y).} \tag{3.21} \\ \end{array}$$

#page(201)

To form the Hamiltonian we find the momenta /p/ = ∂_{2}/L/(/t/, /q/, /v/): /p_{x}/ = /mv_{x}/ and /p_{y}/ = /mv_{y}/. Solving for the velocities in terms of the momenta is easy here:$\upsilon_{x} = {p_{x}/m}$ and $\upsilon_{y} = {p_{y}/m}$. The Hamiltonian is /H/(/t/, /q/, /p/) = /pv/ − /L/(/t/, /q/, /v/), with /v/ reexpressed in terms of (/t/, /q/, /p/):

$$\begin{array}{ll} {H(t;x,y;p_{x},p_{y}) = \frac{p_{x}^{2} + p_{y}^{2}}{2m} + V(x,y).} \tag{3.22} \\ \end{array}$$

The kinetic energy is a homogeneous quadratic form in the velocities, so the energy is /T/ + /V/ and the Hamiltonian is the energy expressed in terms of momenta rather than velocities. Hamilton's equations for /Dq/ are

$$\begin{array}{ll} {D_{x}(t) = {{p_{x}(t)}/m}} & \\ {D_{y}(t) = {{p_{y}(t)}/m}.} \tag{3.23} \\ \end{array}$$

Note that these equations merely restate the relation between the momenta and the velocities. Hamilton's equations for /Dp/ are

$$\begin{array}{ll} {Dp_{x}(t) = - \partial_{0}V(x(t),y(t))} & \\ {Dp_{y}(t) = - \partial_{1}V(x(t),y(t)).} \tag{3.24} \\ \end{array}$$

The rate of change of the linear momentum is minus the gradient of the potential energy.

### Exercise 3.1: Deriving Hamilton's equations

For each of the following Lagrangians derive the Hamiltonian and Hamilton's equations. These problems are simple enough to do by hand.

*a.* A Lagrangian for a planar pendulum:$ L(t,\theta,\dot{\theta}) = \frac{1}{2}ml^{2}{\dot{\theta}}^{2} + mgl\,\cos\theta $.

*b.* A Lagrangian for a particle of mass /m/ with a two-dimensional potential energy /V/(/x/, /y/) = (/x/^{2} + /y/^{2})/2 + /x/^{2}/y/ − /y/^{3}/3 is $ L(t;x,y;\dot{x},\dot{y}) = \frac{1}{2}m({\dot{x}}^{2} + {\dot{y}}^{2}) - V(x,y).$*c.* A Lagrangian for a particle of mass /m/ constrained to move on a sphere of radius $ R:\,\, L(t;\theta,\varphi;\dot{\theta},\dot{\varphi}) = \frac{1}{2}mR^{2}({\dot{\theta}}^{2} + {(\dot{\varphi}\sin\theta)}^{2})$, where /θ/ is the colatitude and /φ/ is the longitude on the sphere.

### Exercise 3.2: Sliding pendulum

For the pendulum with a sliding support (see [exercise 1.20](#exercise_1.20)), derive a Hamiltonian and Hamilton's equations.

#page(202)

#### Hamiltonian state
Given a coordinate path /q/ and a Lagrangian /L/, the corresponding momentum path /p/ is given by equation (#Eqn(chapter003,3.2,3.2)). Equation (#Eqn(chapter003,3.17,3.17)) expresses the same relationship in terms of the corresponding Hamiltonian /H/. That these relations are valid for any path, whether or not it is a realizable path, allows us to abstract to arbitrary velocity and momentum at a moment. At a moment, the momentum /p/ for the state tuple (/t/, /q/, /v/) is /p/ = ∂_{2}/L/(/t/, /q/, /v/). We also have /v/ = ∂_{2}/H/(/t/, /q/, /p/). In the Lagrangian formulation the state of the system at a moment can be specified by the local state tuple (/t/, /q/, /v/) of time, generalized coordinates, and generalized velocities. Lagrange's equations determine a unique path emanating from this state. In the Hamiltonian formulation the state can be specified by the tuple (/t/, /q/, /p/) of time, generalized coordinates, and generalized momenta. Hamilton's equations determine a unique path emanating from this state. The Lagrangian state tuple (/t/, /q/, /v/) encodes exactly the same information as the Hamiltonian state tuple (/t/, /q/, /p/); we need a Lagrangian or a Hamiltonian to relate them. The two formulations are equivalent in that the same coordinate path emanates from them for equivalent initial states.

The Lagrangian state derivative is constructed from the Lagrange equations by solving for the highest-order derivative and abstracting to arbitrary positions and velocities at a moment.#Footnote(7) The Lagrangian state path is generated by integration of the Lagrangian state derivative given an initial Lagrangian state (/t/, /q/, /v/). Similarly, the Hamiltonian state derivative can be constructed from Hamilton's equations by abstracting to arbitrary positions and momenta at a moment. Hamilton's equations are a set of first-order differential equations in explicit form. The Hamiltonian state derivative can be directly written in terms of them. The Hamiltonian state path is generated by integration of the Hamiltonian state derivative given an initial Hamiltonian state (/t/, /q/, /p/). If these state paths are obtained by integrating the state derivatives with equivalent initial states, then the coordinate path components of these state paths are the same and satisfy the Lagrange
#page(203)
equations. The coordinate path and the momentum path components of the Hamiltonian state path satisfy Hamilton's equations. The Hamiltonian formulation and the Lagrangian formulation are equivalent.

Given a path /q/, the Lagrangian state path and the Hamiltonian state paths can be deduced from it. The Lagrangian state path Γ[/q/] can be constructed from a path /q/ simply by taking derivatives. The Lagrangian state path satisfies:

$$\begin{array}{ll} {\Gamma\lbrack q\rbrack(t) = (t,q(t),\, Dq(t)).} \tag{3.25} \\ \end{array}$$

The Lagrangian state path is uniquely determined by the path /q/. The Hamiltonian state path Π/_{L}/[/q/] can also be constructed from the path /q/ but the construction requires a Lagrangian. The Hamiltonian state path satisfies

$$\begin{array}{ll} {\Pi_{L}\lbrack q\rbrack(t) = (t,q(t),\,\partial_{2}L(t,q(t),\, Dq(t))) = (t,q(t),p(t)).} \tag{3.26} \\ \end{array}$$

The Hamiltonian state tuple is not uniquely determined by the path /q/ because it depends upon our choice of Lagrangian, which is not unique.

The 2/n/-dimensional space whose elements are labeled by the /n/ generalized coordinates /q^{i}/ and the /n/ generalized momenta /p_{i}/ is called the /phase space/. The components of the generalized coordinates and momenta are collectively called the /phase-space components/.#Footnote(8) The dynamical state of the system is completely specified by the phase-space state tuple (/t/, /q/, /p/), given a Lagrangian or Hamiltonian to provide the map between velocities and momenta.

#### Computing Hamilton's equations
Hamilton's equations are a system of first-order ordinary differential equations. A procedural formulation of Lagrange's equations as a first-order system was presented in [section 1.7](chapter001!section_1.7). The following formulation of Hamilton's equations is analogous:
```Scheme
(define ((Hamilton-equations Hamiltonian) q p) (let ((state-path (qp->H-state-path q p))) (- (D state-path) (compose (Hamiltonian->state-derivative Hamiltonian) state-path)))) 
```
#page(204)

The Hamiltonian state derivative is computed as follows:
```Scheme
(define ((Hamiltonian->state-derivative Hamiltonian) H-state) (up 1 (((partial 2) Hamiltonian) H-state) (- (((partial 1) Hamiltonian) H-state)))) 
```
The state in the Hamiltonian formulation is composed of the time, the coordinates, and the momenta. We call this an H-state, to distinguish it from the state in the Lagrangian formulation. We can select the components of the Hamiltonian state with the selectors time, coordinate, momentum. We construct Hamiltonian states from their components with up. The first component of the state is time, so the first component of the state derivative is one, the time rate of change of time. Given procedures q and p implementing coordinate and momentum path functions, the Hamiltonian state path can be constructed with the following procedure:
```Scheme
(define ((qp->H-state-path q p) t) (up t (q t) (p t))) 
```
The Hamilton-equations procedure returns the residuals of Hamilton's equations for the given paths.

For example, a procedure implementing the Hamiltonian for a point mass with potential energy /V/ (/x/, /y/) is
```Scheme
(define ((H-rectangular m V) state) (let ((q (coordinate state)) (p (momentum state))) (+ (/ (square p) (* 2 m)) (V (ref q 0) (ref q 1))))) 
```
Hamilton's equations are
```Scheme
(show-expression (let ((V (literal-function 'V (-> (X Real Real) Real))) (q (up (literal-function 'x) (literal-function 'y))) (p (down (literal-function 'p_x) (literal-function 'p_y)))) (((Hamilton-equations (H-rectangular 'm V)) q p) 't))) 
```
#page(205)

$$\begin{pmatrix} 0 \\ \begin{pmatrix} {Dx(t) - \frac{p_{x}(t)}{m}} \\ {Dy(t) - \frac{p_{y}(t)}{m}} \\ \end{pmatrix} \\ \begin{bmatrix} {Dp_{x}(t) + \partial_{0}V(x(t),y(t))} \\ {Dp_{y}(t) + \partial_{1}V(x(t),y(t))} \\ \end{bmatrix} \\ \end{pmatrix}$$

The zero in the first element of the structure of Hamilton's equation residuals is just the tautology that time advances uniformly: the time function is just the identity, so its derivative is one and the residual is zero. The equations in the second element of the structure relate the coordinate paths and the momentum paths. The equations in the third element give the rate of change of the momenta in terms of the applied forces.

### Exercise 3.3: Computing Hamilton's equations

Check your answers to [exercise 3.1](#exercise_3.1) with the Hamilton-equations procedure.

##### 3.1.1 The Legendre Transformation
The Legendre transformation abstracts a key part of the process of transforming from the Lagrangian to the Hamiltonian formulation of mechanics---the replacement of functional dependence on generalized velocities with functional dependence on generalized momenta. The momentum state function is defined as a partial derivative of the Lagrangian, a real-valued function of time, coordinates, and velocities. The Legendre transformation provides an inverse that gives the velocities in terms of the momenta: we are able to write the velocities as a partial derivative of a different real-valued function of time, coordinates, and momenta.#Footnote(9)

Given a real-valued function /F/, if we can find a real-valued function /G/ such that /DF/ = (/DG/)^{−1}, then we say that /F/ and /G/ are related by a Legendre transform.

#page(206)

Locally, we can define the inverse function#Footnote(10)$\mathcal{V}$ of /DF/ so that $ DF \circ \mathcal{V} = I $, where /I/ is the identity function /I/(/w/) = /w/. Consider the composite function $\widetilde{F} = F \circ \mathcal{V}$. The derivative of $\widetilde{F}$ is

$$\begin{array}{ll} {D\widetilde{F} = (DF \circ \mathcal{V})D\mathcal{V} = ID\mathcal{V}.} \tag{3.27} \\ \end{array}$$

Since

$$\begin{array}{ll} {D(I\mathcal{V}) = \mathcal{V} + ID\mathcal{V},} \tag{3.28} \\ \end{array}$$

we have

$$\begin{array}{ll} {D\widetilde{F} = D(I\mathcal{V}) - \mathcal{V},} \tag{3.29} \\ \end{array}$$

or

$$\begin{array}{ll} {\mathcal{V} = D(I\mathcal{V}) - D\widetilde{F} = D(I\mathcal{V} - \widetilde{F}).} \tag{3.30} \\ \end{array}$$

The integral is determined up to a constant of integration. If we define

$$\begin{array}{ll} {G = I\mathcal{V} - \widetilde{F},} \tag{3.31} \\ \end{array}$$

then we have

$$\begin{array}{ll} {\mathcal{V} = DG.} \tag{3.32} \\ \end{array}$$

The function /G/ has the desired property that /DG/ is the inverse function $\mathcal{V}$ of /DF/. The derivation just given applies equally well if the arguments of /F/ and /G/ have multiple components.#Footnote(11)

Given a relation /w/ = /DF/ (/v/) for some given function /F/, then /v/ = /DG/(/w/) for $ G = I\mathcal{V} - F \circ \mathcal{V}$, where $\mathcal{V}$ is the inverse function of /DF/, provided it exists.

A picture may help (see [figure 3.1](#figure_3.1)). The curve is the graph of the function /DF/. Turned sideways, it is also the graph of the function /DG/, because /DG/ is the inverse function of /DF/. The integral of /DF/ from /v/_{0} to /v/ is /F/(/v/) − /F/(/v/_{0}); this is the area below the curve from /v/_{0} to /v/. Likewise, the integral of /DG/ from /w/_{0} to
#page(207)
/w/ is /G/(/w/) − /G/(/w/_{0}); this is the area to the left of the curve from /w/_{0} to /w/. The union of these two regions has area /wv/ − /w/_{0}/v/_{0}. So

#Image(Art_P626.jpg,figure_3.1)
#Caption *Figure 3.1* The Legendre transform can be interpreted in terms of geometric areas. The curve is the graph of /DF/, and viewed sideways is the graph of /DG/ = (/DF/)^{−1}. This figure should remind you of the geometric interpretation of the product rule for derivatives, or alternatively integration by parts. #CaptionEnd

$$\begin{array}{ll} {wv - w_{0}v_{0} = F(v) - F(v_{0}) + G(w) - G(w_{0}),} \tag{3.33} \\ \end{array}$$

which is the same as

$$\begin{array}{ll} {wv - F(v) - G(w) = w_{0}v_{0} - G(w_{0}) - F(v_{0}).} \tag{3.34} \\ \end{array}$$

The left-hand side depends only on the point labeled by /w/ and /v/ and the right-hand side depends only on the point labeled by /w/_{0} and /v/_{0}, so these must be constant, independent of the variable endpoints. So as the point is changed the combination /G/(/w/) + /F/(/v/) − /wv/ is invariant. Thus

$$\begin{array}{ll} {G(w) = wv - F(v) + C,} \tag{3.35} \\ \end{array}$$

with constant /C/. The requirement for /G/ depends only on /DG/ so we can choose to define /G/ with /C/ = 0.

#page(208)

#### Legendre transformations with passive arguments
Let /F/ be a real-valued function of two arguments and

$$\begin{array}{ll} {w = \partial_{1}F(x,v).} \tag{3.36} \\ \end{array}$$

If we can find a real-valued function /G/ such that

$$\begin{array}{ll} {v = \partial_{1}G(x,w)} \tag{3.37} \\ \end{array}$$

we say that /F/ and /G/ are related by a Legendre transformation, that the second argument in each function is /active/, and that the first argument is /passive/ in the transformation.

If the function ∂_{1}/F/ can be locally inverted with respect to the second argument we can define

$$\begin{array}{ll} {v = \mathcal{V}(x,w),} \tag{3.38} \\ \end{array}$$

giving

$$\begin{array}{ll} {w = \partial_{1}F(x,\mathcal{V}(x,w)) = W(x,w),} \tag{3.39} \\ \end{array}$$

where /W/ = /I/_{1} is the selector function for the second argument.

For the active arguments the derivation goes through as before. The first argument to /F/ and /G/ is just along for the ride---it is a passive argument. Let

$$\begin{array}{ll} {\widetilde{F}(x,w) = F(x,\mathcal{V}(x,w)),} \tag{3.40} \\ \end{array}$$

then define

$$\begin{array}{ll} {G = W\mathcal{V} - \widetilde{F}.} \tag{3.41} \\ \end{array}$$

We can check that /G/ has the property $\mathcal{V} = \partial_{1}G $ by carrying out the derivative:

$$\begin{array}{lll} {\partial_{1}G} & {= \partial_{1}(W\mathcal{V} - \widetilde{F})} & \\  & {= \mathcal{V} + W\partial_{1}\mathcal{V} - \partial_{1}\widetilde{F},} \tag{3.42} \\ \end{array}$$

but

$$\begin{array}{lll} {\partial_{1}\widetilde{F}(x,w)} & {= \partial_{1}F(x,\mathcal{V}(x,w))\partial_{1}\mathcal{V}(x,w)} & \\  & {= W(x,w)\partial_{1}\mathcal{V}(x,w),} \tag{3.43} \\ \end{array}$$

or

$$\begin{array}{ll} {\partial_{1}\widetilde{F} = W\partial_{1}\mathcal{V}.} \tag{3.44} \\ \end{array}$$

#page(209)

So, from equation (#Eqn(chapter003,3.42,3.42)),

$$\begin{array}{ll} {\partial_{1}G = \mathcal{V},} \tag{3.45} \\ \end{array}$$

as required. The active argument may have many components.

The partial derivatives with respect to the passive arguments are related in a remarkably simple way. Let's calculate the derivative ∂_{0}/G/ in pieces. First,

$$\begin{array}{ll} {\partial_{0}(W\mathcal{V}) = W\partial_{0}\mathcal{V}} \tag{3.46} \\ \end{array}$$

because ∂_{0}/W/ = 0. We calculate $\partial_{0}\widetilde{F}$:

$$\begin{array}{lll} {\partial_{0}\widetilde{F}(x,w)} & {= \partial_{0}F(x,\mathcal{V}(x,w)) + \partial_{1}F(x,\mathcal{V}(x,w))\partial_{0}\mathcal{V}(x,w)} & \\  & {= \partial_{0}F(x,\mathcal{V}(x,w)) + W(x,w)\partial_{0}\mathcal{V}(x,w).} \tag{3.47} \\ \end{array}$$

Putting these together, we find

$$\begin{array}{ll} {\partial_{0}G(x,w) = - \partial_{0}F(x,\mathcal{V}(x,w)) = - \partial_{0}F(x,v).} \tag{3.48} \\ \end{array}$$

The calculation is unchanged if the passive argument has many components.

We can write the Legendre transformation more symmetrically:

$$\begin{array}{rlll} w & = & {\partial_{1}F(x,v)} & \\ {wv} & = & {F(x,v) + G(x,w)} & \\ v & = & {\partial_{1}G(x,w)} & \\ 0 & = & {\partial_{0}F(x,v) + \partial_{0}G(x,w).} \tag{3.49} \\ \end{array}$$

The last relation is not as trivial as it looks, because /x/ enters the equations connecting /w/ and /v/. With this symmetrical form, we see that the Legendre transform is its own inverse.

### Exercise 3.4: Simple Legendre transforms

For each of the following functions, find the function that is related to the given function by the Legendre transform on the indicated active argument. Show that the Legendre transform relations hold for your solution, including the relations among passive arguments, if any.

*a.* /F/ (/x/) = /ax/ + /bx/^{2}, with no passive arguments.

*b.* /F/ (/x/, /y/) = /a/ sin /x/ cos /y/, with /x/ active.

*c.* /F/ (/x/, /y/, /ẋ/, /ẏ/) = /xẋ/^{2} + 3/ẋẏ/ + /yẏ/^{2}, with /ẋ/ and /ẏ/ active.

#page(210)

#### Hamilton's equations from the Legendre transformation
We can use the Legendre transformation with the Lagrangian playing the role of /F/ and with the generalized velocity slot playing the role of the active argument. The Hamiltonian plays the role of /G/ with the momentum slot active. The coordinate and time slots are passive arguments.

The Lagrangian /L/ and the Hamiltonian /H/ are related by a Legendre transformation:

$$\begin{array}{ll} {e = (\partial_{2}L)(a,b,c)} \tag{3.50} \\ \end{array}$$

$$\begin{array}{ll} {ec = L(a,b,c) + H(a,b,e)} \tag{3.51} \\ \end{array}$$

and

$$\begin{array}{ll} {c = (\partial_{2}H)(a,b,e),} \tag{3.52} \\ \end{array}$$

with passive equations

$$\begin{array}{ll} {0 = \partial_{0}L(a,b,c) + \partial_{0}H(a,b,e),} \tag{3.53} \\ \end{array}$$

$$\begin{array}{ll} {0 = \partial_{1}L(a,b,c) + \partial_{1}H(a,b,e).} \tag{3.54} \\ \end{array}$$

Presuming it exists, we can define the inverse of ∂_{2}/L/ with respect to the last argument:

$$\begin{array}{ll} {c = \mathcal{V}(a,b,e),} \tag{3.55} \\ \end{array}$$

and write the Hamiltonian

$$\begin{array}{ll} {H(a,b,c) = c\mathcal{V}(a,b,c) - L(a,b,\mathcal{V}(a,b,c)).} \tag{3.56} \\ \end{array}$$

These relations are purely algebraic in nature.

On a path /q/ we have the momentum /p/:

$$\begin{array}{ll} {p(t) = \partial_{2}L(t,q(t),Dq(t)),} \tag{3.57} \\ \end{array}$$

and from the definition of $\mathcal{V}$ we find

$$\begin{array}{ll} {Dq(t) = \mathcal{V}(t,q(t),p(t)).} \tag{3.58} \\ \end{array}$$

#page(211)

The Legendre transform gives

$$\begin{array}{ll} {Dq(t) = \partial_{2}H(t,q(t),p(t)).} \tag{3.59} \\ \end{array}$$

This relation is purely algebraic and is valid for any path. The passive equation (#Eqn(chapter003,3.54,3.54)) gives

$$\begin{array}{ll} {\partial_{1}L(t,q(t),\, Dq(t)) = - \partial_{1}H(t,q(t),p(t)),} \tag{3.60} \\ \end{array}$$

but the left-hand side can be rewritten using the Lagrange equations, so

$$\begin{array}{ll} {Dp(t) = - \partial_{1}H(t,q(t),p(t)).} \tag{3.61} \\ \end{array}$$

This equation is valid only for realizable paths, because we used the Lagrange equations to derive it. Equations (#Eqn(chapter003,3.59,3.59)) and (#Eqn(chapter003,3.61,3.61)) are Hamilton's equations.

The remaining passive equation is

$$\begin{array}{ll} {\partial_{0}L(t,q(t),\, Dq(t)) = - \partial_{0}H(t,q(t),p(t)).} \tag{3.62} \\ \end{array}$$

This passive equation says that the Lagrangian has no explicit time dependence (∂_{0}/L/ = 0) if and only if the Hamiltonian has no explicit time dependence (∂_{0}/H/ = 0). We have found that if the Lagrangian has no explicit time dependence, then energy is conserved. So if the Hamiltonian has no explicit time dependence then it is a conserved quantity.

### Exercise 3.5: Conservation of the Hamiltonian

Using Hamilton's equations, show directly that the Hamiltonian is a conserved quantity if it has no explicit time dependence.

#### Legendre transforms of quadratic functions
We cannot implement the Legendre transform in general because it involves finding the functional inverse of an arbitrary function. However, many physical systems can be described by Lagrangians that are quadratic forms in the generalized velocities. For such functions the generalized momenta are linear functions of the generalized velocities, and thus explicitly invertible.

#page(212)

More generally, we can compute a Legendre transformation for polynomial functions where the leading term is a quadratic form:

$$\begin{array}{ll} {F(v) = \frac{1}{2}v^{\mathcal{T}}Mv + bv + c.} \tag{3.63} \\ \end{array}$$

Because the first term is a quadratic form only the symmetric part of /M/ contributes to the result, so we can assume /M/ is symmetric.#Footnote(12) Let /w/ = /DF/ (/v/), then

$$\begin{array}{ll} {w = DF(v) = Mv + b.} \tag{3.64} \\ \end{array}$$

So if /M/ is invertible we can solve for /v/ in terms of /w/. Thus we may define a function $\mathcal{V}$ such that

$$\begin{array}{ll} {v = \mathcal{V}(w) = M^{- 1}(w - b)} \tag{3.65} \\ \end{array}$$

and we can use this to compute the value of the function /G/:

$$\begin{array}{ll} {G(w) = w\mathcal{V}(w) - F(\mathcal{V}(w)).} \tag{3.66} \\ \end{array}$$

#### Computing Hamiltonians
We implement the Legendre transform for quadratic functions by the procedure#Footnote(13)
```Scheme
(define (Legendre-transform F) (let ((w-of-v (D F))) (define (G w) (let ((zero (compatible-zero w))) (let ((M ((D w-of-v) zero)) (b (w-of-v zero))) (let ((v (solve-linear-left M (- w b)))) (- (* w v) (F v)))))) G)) 
```
The procedure Legendre-transform takes a procedure of one argument and returns the procedure that is associated with it by the Legendre transform. If /w/ = /DF/ (/v/), /wv/ = /F/ (/v/) + /G/(/w/), and /v/ = /DG/(/w/) specifies a one-argument Legendre transformation, then /G/ is the function associated with /F/ by the Legendre transform:$ G = I\mathcal{V} - F \circ \mathcal{V}$, where $\mathcal{V}$ is the functional inverse of /DF/.

We can use the Legendre-transform procedure to compute a Hamiltonian from a Lagrangian:
```Scheme
(define ((Lagrangian->Hamiltonian Lagrangian) H-state) (let ((t (time H-state)) (q (coordinate H-state)) (p (momentum H-state))) (define (L qdot) (Lagrangian (up t q qdot))) ((Legendre-transform L) p))) 
```
Notice that the one-argument Legendre-transform procedure is sufficient. The passive variables are given no special attention, they are just passed around.

The Lagrangian may be obtained from the Hamiltonian by the procedure:
```Scheme
(define ((Hamiltonian->Lagrangian Hamiltonian) L-state) (let ((t (time L-state)) (q (coordinate L-state)) (qdot (velocity L-state))) (define (H p) (Hamiltonian (up t q p))) ((Legendre-transform H) qdot))) 
```
Notice that the two procedures Hamiltonian->Lagrangian and Lagrangian->Hamiltonian are identical, except for the names.

For example, the Hamiltonian for the motion of the point mass with the potential energy /V/ (/x/, /y/) may be computed from the Lagrangian:
```Scheme
(define ((L-rectangular m V) local) (let ((q (coordinate local)) (qdot (velocity local))) (- (* 1/2 m (square qdot)) (V (ref q 0) (ref q 1))))) 
```
And the Hamiltonian is, as we saw in equation (#Eqn(chapter003,3.22,3.22)):
```Scheme
(show-expression ((Lagrangian->Hamiltonian (L-rectangular 'm (literal-function 'V (-> (X Real Real) Real)))) (up 't (up 'x 'y) (down 'p_x 'p_y)))) 
```

$$ V(x,y) + \frac{\frac{1}{2}p_{x}^{2}}{m} + \frac{\frac{1}{2}p_{y}^{2}}{m}$$

#page(214)

#Image(Art_P662.jpg,figure_3.2)
#Caption *Figure 3.2* A point mass on a helical track. #CaptionEnd

### Exercise 3.6: On a helical track

A uniform cylinder of mass /M/, radius /R/, and height /h/ is mounted so as to rotate freely on a vertical axis. A point mass of mass /m/ is constrained to move on a uniform frictionless helical track of pitch /β/ (measured in radians per meter of drop along the cylinder) mounted on the surface of the cylinder (see [figure 3.2](#figure_3.2). The mass is acted upon by standard gravity (/g/ = 9.8 ms^{−2}).

*a.* What are the degrees of freedom of this system? Pick and describe a convenient set of generalized coordinates for this problem. Write a Lagrangian to describe the dynamical behavior. It may help to know that the moment of inertia of a cylinder around its axis is $\frac{1}{2}MR^{2}$. You may find it easier to do the algebra if various constants are combined and represented as single symbols.

*b.* Make a Hamiltonian for the system. Write Hamilton's equations for the system. Are there any conserved quantities?

*c.* If we release the point mass at time /t/ = 0 at the top of the track with zero initial speed and let it slide down, what is the motion of the system?

### Exercise 3.7: An ellipsoidal bowl

Consider a point particle of mass /m/ constrained to move in a bowl and acted upon by a uniform gravitational acceleration /g/. The bowl
#page(215)
is ellipsoidal, with height /z/ = /ax/^{2} + /by/^{2}. Make a Hamiltonian for this system. Can you make any immediate deductions about this system?

##### 3.1.2 Hamilton's Equations from the Action Principle
The previous two derivations of Hamilton's equations made use of the Lagrange equations. Hamilton's equations can also be derived directly from the action principle.

The action is the integral of the Lagrangian along a path:

$$\begin{array}{ll} {S\lbrack q\rbrack(t_{1},t_{2}) = {\int_{t_{1}}^{t_{2}}{L \circ \Gamma\lbrack q\rbrack.}}} \tag{3.67} \\ \end{array}$$

The action is stationary with respect to variations of a realizable path that preserve the configuration at the endpoints (for Lagrangians that are functions of time, coordinates, and velocities).

We can rewrite the integrand in terms of the Hamiltonian

$$\begin{array}{ll} {L(t,q(t),p(t)) = p(t)Dq(t) - H(t,q(t),p(t)),} \tag{3.68} \\ \end{array}$$

with /p/(/t/) = ∂_{2}/L/(/t/, /q/(/t/), /Dq/(/t/)). The Legendre transformation construction gives

$$\begin{array}{ll} {Dq(t) = \partial_{2}H(t,q(t),p(t)),} \tag{3.69} \\ \end{array}$$

which is one of Hamilton's equations, the one that does not depend on the path being a realizable path.

In order to vary the action we should make the dependences on the path explicit. We introduce

$$\begin{array}{ll} {\widetilde{p}\lbrack q\rbrack(t) = \partial_{2}L(t,q(t),Dq(t)),} \tag{3.70} \\ \end{array}$$

and#Footnote(14)

$$\begin{matrix} {\Pi\lbrack q\rbrack(t) = (t,q(t),\widetilde{p}\lbrack q\rbrack(t)) = (t,q(t),p(t)).} \tag{3.71} \\ \end{matrix}$$

The integrand of the action integral is then

$$\begin{matrix} {L \circ \Gamma\lbrack q\rbrack = \widetilde{p}\lbrack q\rbrack Dq - H \circ \Pi\lbrack q\rbrack.} \tag{3.72} \\ \end{matrix}$$

#page(216)

Using the shorthand /δp/ for $\delta\widetilde{p}\lbrack q\rbrack $,#Footnote(15) and noting that $ p = \widetilde{p}\lbrack q\rbrack $, the variation of the action is

$$\begin{array}{lll} {\delta S\lbrack q\rbrack} & {(t_{1},t_{2})} & \\  & {= {\int_{t_{1}}^{t_{2}}{(\delta p\, Dq\, + p\,\,\delta Dq - (DH \circ \Pi\lbrack q\rbrack)\delta\Pi\lbrack q\rbrack)}}} & \\  & \begin{array}{l} {= {\int_{t_{1}}^{t_{2}}\left\{ \delta p\, Dq\, + p\, D\delta q \right.}} \\ {\left. \,\,\,\,\,\,\,\,\, - (\partial_{1}H \circ \Pi\lbrack q\rbrack)\delta q - (\partial_{2}H \circ \Pi\lbrack q\rbrack)\delta p \right\}.} \\ \end{array} \tag{3.73} \\ \end{array}$$

Integrating the second term by parts, using /D/(/pδq/) = /Dpδq/ + /pDδq/, we get

$$\begin{array}{lll} {\delta S\lbrack q\rbrack} & {(t_{1},t_{2}) = p\delta q|_{t_{1}}^{t_{2}}} & \\  & {+ {\int_{t_{1}}^{t_{2}}{\{\delta p\, Dq\, - Dp\,\,\delta q}}} & \\  & {\left. \,\,\,\,\,\, - (\partial_{1}H \circ \Pi\lbrack q\rbrack)\delta q - (\partial_{2}H \circ \Pi\lbrack q\rbrack)\delta p \right\}.} \tag{3.74} \\ \end{array}$$

The variations are constrained so that /δq/(/t/_{1}) = /δq/(/t/_{2}) = 0, so the integrated part vanishes. Rearranging terms, the variation of the action is

$$\begin{array}{ll} {\delta S\lbrack q\rbrack(t_{1},t_{2})} & \\ {\,\,\,\,\,\, = {\int_{t_{1}}^{t_{2}}{((Dq - \partial_{2}H \circ \Pi\lbrack q\rbrack)\,\delta p - (Dp + \partial_{1}H \circ \Pi\lbrack q\rbrack)\delta q).}}} \tag{3.75} \\ \end{array}$$

As a consequence of equation (#Eqn(chapter003,3.69,3.69)), the factor multiplying /δp/ is zero. We are left with

$$\begin{matrix} {\delta S\lbrack q\rbrack(t_{1},t_{2}) = - {\int_{t_{1}}^{t_{2}}{(Dp + \partial_{1}H \circ \Pi\lbrack q\rbrack)\,\delta q.}}} \tag{3.76} \\ \end{matrix}$$

For the variation of the action to be zero for arbitrary variations, except for the endpoint conditions, we must have

$$\begin{matrix} {Dp = - \partial_{1}H \circ \Pi\lbrack q\rbrack,} \tag{3.77} \\ \end{matrix}$$

#page(217)

or

$$\begin{matrix} {Dp = - \partial_{1}H(t,q(t),\, p(t)),} \tag{3.78} \\ \end{matrix}$$

which is the “dynamical” Hamilton equation.#Footnote(16)

##### 3.1.3 A Wiring Diagram
[Figure 3.3](#figure_3.3) shows a summary of the functional relationship between the Lagrangian and the Hamiltonian descriptions of a dynamical system. The diagram shows a “circuit” interconnecting some “devices” with “wires.” The devices represent the mathematical functions that relate the quantities on their terminals. The wires represent identifications of the quantities on the terminals that they connect. For example, there is a box that represents the Lagrangian function. Given values /t/, /q/, and $\dot{q}$, the value of the Lagrangian $ L\left( {t,q,\dot{q}} \right)$ is on the terminal labeled /L/, which is wired to an addend terminal of an adder. Other terminals of the Lagrangian carry the values of the partial derivatives of the Lagrangian function.

The upper part of the diagram summarizes the relationship of the Hamiltonian to the Lagrangian. For example, the sum of the values on the terminals /L/ of the Lagrangian and /H/ of the Hamiltonian is the product of the value on the $\dot{q}$ terminal of the Lagrangian and the value on the /p/ terminal of the Hamiltonian. This is the active part of the Legendre transform. The passive variables are related by the corresponding partial derivatives being negations of each other. In the lower part of the diagram the equations of motion are indicated by the presence of the integrators, relating the dynamical quantities to their time derivatives.

One can use this diagram to help understand the underlying unity of the Lagrangian and Hamiltonian formulations of mechanics. Lagrange's equations are just the connection of the /ṗ/ wire to the ∂_{1}/L/ terminal of the Lagrangian device. One of Hamilton's equations is just the connection of the /ṗ/ wire (through the negation
#page(218)
device) to the ∂_{1}/H/ terminal of the Hamiltonian device. The other is just the connection of the $\dot{q}$ wire to the ∂_{2}/H/ terminal of the Hamiltonian device. We see that the two formulations are consistent. One does not have to abandon any part of the Lagrangian formulation to use the Hamiltonian formulation: there are deductions that can be made using both simultaneously.

### 3.2 Poisson Brackets
Here we introduce the Poisson bracket, in terms of which Hamilton's equations have an elegant and symmetric expression. Consider a function /F/ of time, coordinates, and momenta. The value of /F/ along the path /σ/(/t/) = (/t/, /q/(/t/), /p/(/t/)) is (/F/ ∘ /σ/)(/t/) = /F/ (/t/, /q/(/t/), /p/(/t/)). The time derivative of /F/ ∘ /σ/ is

$$\begin{array}{lll} {D(F \circ \sigma)} & {= (DF \circ \sigma)D\sigma} & \\  & {= \partial_{0}F \circ \sigma + (\partial_{1}F \circ \sigma)Dq + (\partial_{2}F \circ \sigma)Dp.} \tag{3.79} \\  & & \\ \end{array}$$

If the phase-space path is a realizable path for a system with Hamiltonian /H/, then /Dq/ and /Dp/ can be reexpressed using Hamilton's equations:

$$\begin{array}{lll} {D(F \circ \sigma)} & {= \partial_{0}F \circ \sigma + (\partial_{1}F \circ \sigma)(\partial_{2}H \circ \sigma) - (\partial_{2}F \circ \sigma)(\partial_{1}H \circ \sigma)} & \\  & {= \partial_{0}F \circ \sigma + (\partial_{1}F\partial_{2}H - \partial_{2}F\partial_{1}H) \circ \sigma} & \\  & {= \partial_{0}F \circ \sigma + \left\{ F,H \right\} \circ \sigma} \tag{3.80} \\ \end{array}$$

where the /Poisson bracket/ {F, H} of /F/ and /H/ is defined by#Footnote(17)

$$\begin{array}{ll} {\left\{ F,H \right\} = \partial_{1}F\partial_{2}H - \partial_{2}F\partial_{1}H.} \tag{3.81} \\ \end{array}$$

Note that the Poisson bracket of two functions on the phase-state space is also a function on the phase-state space.

#page(219)

#Image(Art_P679.jpg,figure_3.3)
#Caption *Figure 3.3* A “wiring diagram” describing the relationships among the dynamical quantities occurring in Lagrangian and Hamiltonian mechanics. #CaptionEnd

#page(220)

The coordinate selector /Q/ = /I/_{1} is an example of a function on phase-state space: /Q/(/t/, /q/, /p/) = /q/. According to equation (#Eqn(chapter003,3.80,3.80)),

$$\begin{array}{ll} {Dq = D(Q \circ \sigma) = \left\{ Q,H \right\} \circ \sigma = \partial_{2}H \circ \sigma,} \tag{3.82} \\ \end{array}$$

but this is the same as Hamilton's equation

$$\begin{array}{ll} {Dq(t) = \partial_{2}H(t,q(t),p(t)).} \tag{3.83} \\ \end{array}$$

Similarly, the momentum selector /P/ = /I/_{2} is a function on phase-state space: /P/ (/t/, /q/, /p/) = /p/. We have

$$\begin{array}{ll} {Dp = D(P \circ \sigma) = \left\{ P,H \right\} \circ \sigma = - \partial_{1}H \circ \sigma,} \tag{3.84} \\ \end{array}$$

which is the same as Hamilton's other equation

$$\begin{array}{ll} {Dp(t) = - \partial_{1}H(t,q(t),p(t)).} \tag{3.85} \\ \end{array}$$

So the Poisson bracket provides a uniform way of writing Hamilton's equations:

$$\begin{array}{ll} {D(Q \circ \sigma) = \left\{ Q,H \right\} \circ \sigma} & \\ {D(P \circ \sigma) = \left\{ P,H \right\} \circ \sigma.} \tag{3.86} \\ \end{array}$$

The Poisson bracket of any function with itself is zero, so we recover the conservation of energy for a system that has no explicit time dependence:

$$\begin{matrix} {DE = D(H \circ \sigma) = (\partial_{0}H + \left\{ H,H \right\}) \circ \sigma = \partial_{0}H \circ \sigma.} \tag{3.87} \\ \end{matrix}$$

#### Properties of the Poisson bracket
Let /F/, /G/, and /H/ be functions of time, position, and momentum, and let /c/ be independent of position and momentum.

The Poisson bracket is antisymmetric:

$$\begin{matrix} {\left\{ F,G \right\} = - \left\{ G,F \right\}.} \tag{3.88} \\ \end{matrix}$$

It is bilinear (linear in each argument):

$$\begin{array}{rll} \left\{ {F,G + H} \right\} & {= \left\{ {F,G} \right\} + \left\{ {F,H} \right\}} \tag{3.89} \\ \end{array}$$

$$\begin{array}{rll} \left\{ {F,cG} \right\} & {= c\left\{ {F,G} \right\}} \tag{3.90} \\ \end{array}$$

$$\begin{array}{rll} \left\{ {F + G,H} \right\} & {= \left\{ {F,H} \right\} + \left\{ {G,H} \right\}} \tag{3.91} \\ \end{array}$$

$$\begin{array}{rll} \left\{ {cF,G} \right\} & {= c\left\{ {F,G} \right\}.} \tag{3.92} \\ \end{array}$$

#page(221)

The Poisson bracket satisfies Jacobi's identity:

$$\begin{matrix} {0 = \left\{ F,\left\{ \, G,H \right\} \right\} + \left\{ H,\left\{ F,G \right\} \right\} + \left\{ G,\left\{ H,F \right\} \right\}.} \tag{3.93} \\ \end{matrix}$$

All but the last of #Eqn(chapter003,3.88,3.88)--#Eqn(chapter003,3.93,3.93) can immediately be verified from the definition. Jacobi's identity requires a little more effort to verify. We can use the computer to avoid some work. Define some literal phase-space functions of Hamiltonian type:
```Scheme
(define F (literal-function 'F (-> (UP Real (UP Real Real) (DOWN Real Real)) Real))) (define G (literal-function 'G (-> (UP Real (UP Real Real) (DOWN Real Real)) Real))) (define H (literal-function 'H (-> (UP Real (UP Real Real) (DOWN Real Real)) Real))) 
```
Then we check the Jacobi identity:
```Scheme
((+ (Poisson-bracket F (Poisson-bracket G H)) (Poisson-bracket G (Poisson-bracket H F)) (Poisson-bracket H (Poisson-bracket F G))) (up 't (up 'x 'y) (down 'px 'py))) 
```
```Scheme
0 
```
The residual is zero, so the Jacobi identity is satisfied for any three phase-space state functions with two degrees of freedom.

#### Poisson brackets of conserved quantities
The Poisson bracket of conserved quantities is conserved. Let /F/ and /G/ be time-independent phase-space state functions: ∂_{0}/F/ = ∂_{0}/G/ = 0. If /F/ and /G/ are conserved by the evolution under /H/ then

$$\begin{array}{ll} {0 = D(F \circ \sigma) = \left\{ F,H \right\} \circ \sigma} & \\ {0 = D(G \circ \sigma) = \left\{ G,H \right\} \circ \sigma.} \tag{3.94} \\ \end{array}$$

So the Poisson brackets of /F/ and /G/ with /H/ are zero: {F, H} = {G, H} = 0. The Jacobi identity then implies

$$\begin{array}{ll} {\left\{ \left\{ F,\, G \right\},\, H \right\} = 0,} \tag{3.95} \\ \end{array}$$

#page(222)

and thus

$$\begin{array}{ll} {D(\left\{ F,\, G \right\} \circ \sigma) = 0,} \tag{3.96} \\ \end{array}$$

so {/F, G/} is a conserved quantity. The Poisson bracket of two conserved quantities is also a conserved quantity.

### 3.3 One Degree of Freedom
The solutions of time-independent systems with one degree of freedom can be found by quadrature. Such systems conserve the Hamiltonian: the Hamiltonian has a constant value on each realizable trajectory. We can use this constraint to eliminate the momentum in favor of the coordinate, obtaining the single equation /Dq/(/t/) = /f/(/q/(/t/)).#Footnote(18)

A geometric view reveals more structure. Time-independent systems with one degree of freedom have a two-dimensional phase space. Energy is conserved, so all orbits are level curves of the Hamiltonian. The possible orbit types are restricted to curves that are contours of a real-valued function. The possible orbits are paths of constant altitude in the mountain range on the phase plane described by the Hamiltonian.

Only a few characteristic features are possible. There are points that are stable equilibria of the dynamical system. These are the peaks and pits of the Hamiltonian mountain range. These equilibria are stable in the sense that neighboring trajectories on nearby contours stay close to the equilibrium point. There are orbits that trace simple closed curves on contours that surround a peak or pit, or perhaps several peaks. There are also trajectories lying on contours that cross at a saddle point. The crossing point is an unstable equilibrium, unstable in the sense that neighboring trajectories leave the vicinity of the equilibrium point. Such contours that cross at saddle points are called /separatrices/ (singular: /separatrix/), contours that “separate” two regions of distinct behavior.

#page(223)

At every point Hamilton's equations give a unique rate of evolution and direct the system to move perpendicular to the gradient of the Hamiltonian. At the peaks, pits, and saddle points, the gradient of the Hamiltonian is zero, so according to Hamilton's equations these are equilibria. At other points, the gradient of the Hamiltonian is nonzero, so according to Hamilton's equations the rate of evolution is nonzero. Trajectories evolve along the contours of the Hamiltonian. Trajectories on simple closed contours periodically trace the contour. At a saddle point, contours cross. The gradient of the Hamiltonian is zero at the saddle point, so a system started at the saddle point does not leave the saddle point. On the separatrix away from the saddle point the gradient of the Hamiltonian is not zero, so trajectories evolve along the contour. Trajectories on the separatrix are asymptotic forward or backward in time to a saddle point. Going forward or backward in time, such trajectories forever approach an unstable equilibrium but never reach it. If the phase space is bounded, asymptotic trajectories that lie on contours of a smooth Hamiltonian are always asymptotic to unstable equilibria at both ends (but they may be different equilibria).

These orbit types are all illustrated by the prototypical phase plane of the pendulum (see [figure 3.4](#figure_3.4)). The solutions lie on contours of the Hamiltonian. There are three regions of the phase plane; in each the motion is qualitatively different. In the central region the pendulum oscillates; above this there is a region in which the pendulum circulates in one direction; below the oscillation region the pendulum circulates in the other direction. In the center of the oscillation region there is a stable equilibrium, at which the pendulum is hanging motionless. At the boundaries between these regions, the pendulum is asymptotic to the unstable equilibrium, at which the pendulum is standing upright.#Footnote(19) There are two asymptotic trajectories, corresponding to the two ways the equilibrium can be approached. Each of these is also asymptotic to the unstable equilibrium going backward in time.

#page(224)

### 3.4 Phase Space Reduction
Our motivation for the development of Hamilton's equations was to focus attention on the quantities that can be conserved---the momenta and the energy. In the Hamiltonian formulation the generalized configuration coordinates and the conjugate momenta comprise the state of the system at a given time. We know from the Lagrangian formulation that if the Lagrangian does not depend on some coordinate then the conjugate momentum is conserved. This is also true in the Hamiltonian formulation, but there is a distinct advantage to the Hamiltonian formulation. In the Lagrangian formulation the knowledge of the conserved momentum does not lead immediately to any simplification of the problem, but in the Hamiltonian formulation the fact that momenta are conserved gives an immediate reduction in the dimension of the system to be solved. In fact, if a coordinate does not appear in the Hamiltonian then the dimension of the system of coupled equations that remain to be solved is reduced by two---the coordinate does not appear and the conjugate momentum is constant.

Let /H/(/t/, /q/, /p/) be a Hamiltonian for some problem with an /n-/dimensional configuration space and 2/n/-dimensional phase space. Suppose the Hamiltonian does not depend upon the /i/th coordinate /q^{i}/: (∂_{1}/H/)/_{i}/ = 0.#Footnote(20) According to Hamilton's equations, the conjugate momentum /p_{i}/ is conserved. Hamilton's equations of motion for the remaining 2/n/ − 2 phase-space variables do not involve /q^{i}/ (because it does not appear in the Hamiltonian), and /p_{i}/ is a constant. Thus the dimension of the difficult part of the problem, the part that involves the solution of coupled ordinary differential equations, is reduced by two. The remaining equation governing the evolution of /q^{i}/ in general depends on all the other variables, but once the reduced problem has been solved, the equation of motion for /q^{i}/ can be written so as to give /Dq^{i}/ explicitly as a function of time. We can then find /q^{i}/ as a definite integral of this function.#Footnote(21)

#page(225)

#Image(Art_P694.jpg,figure_3.4)
#Caption *Figure 3.4* Contours of the Hamiltonian for the undriven pendulum on the phase plane. The horizontal axis is the angle /θ/ and the vertical axis is the conjugate angular momentum /p_{θ}/. All realizable trajectories lie on contours of the Hamiltonian. There are three regions in this contour graph, displaying two distinct kinds of behavior. For small energy the pendulum oscillates, producing trajectories that are ovoid curves around the stable equilibrium point at the center. For larger energy the pendulum circulates, producing wavy tracks outside the eye-shaped region of oscillation. The oscillation region is separated from the circulation regions by the separatrix, which emanates from the unstable equilibrium at (±/π/, 0). The pendulum has length 1m and a bob of mass 1kg. The acceleration of gravity is 9.8 m s^{−2}. #CaptionEnd

Contrast this result with analogous results for more general systems of differential equations. There are two independent situations. One situation is that we know a constant of the motion. In general, constants of the motion can be used to reduce by one the dimension of the unsolved part of the problem. To see this, let the system of equations be

$$\begin{array}{ll} {Dz^{i}(t) = F^{i}(z^{0}(t),\, z^{1}(t),...,z^{m - 1}(t)),} \tag{3.97} \\ \end{array}$$

#page(226)

where /m/ is the dimension of the system. Assume we know some constant of the motion

$$\begin{array}{ll} {C(z^{0}(t),\, z^{1}(t),...,z^{m - 1}(t)) = 0.} \tag{3.98} \\ \end{array}$$

At least locally, we expect that we can use this equation to solve for /z/^{m−1}(/t/) in terms of all the other variables, and use this solution to eliminate the dependence on /z/^{m−1}(/t/). The first /m/−1 equations then depend only upon the first /m/ − 1 variables. The dimension of the system of equations to be solved is reduced by one. After the solution for the other variables has been found, /z/^{m−1}(/t/) can be found using the constant of the motion.

The second situation is that one of the variables, say /z^{i}/, does not appear in the equations of motion (but there is an equation for /Dz^{i}/). In this case the equations for the other variables form an independent set of equations of one dimension less than the original system. After these are solved, then the remaining equation for /z^{i}/ can be solved by definite integration.

In both situations the dimension of the system of coupled equations is reduced by one. Hamilton's equations are different in that these two situations come together. If a Hamiltonian for a system does not depend on a particular coordinate, then the equations of motion for the other coordinates and momenta do not depend on that coordinate. Furthermore, the momentum conjugate to that coordinate is a constant of the motion. An added benefit is that the use of this constant of the motion to reduce the dimension of the remaining equations is automatic in the Hamiltonian formulation. The conserved momentum is a state variable and just a parameter in the remaining equations.

So if there is a continuous symmetry it will probably be to our advantage to choose a coordinate system that explicitly incorporates the symmetry, making the Hamiltonian independent of a coordinate. Then the dimension of the phase space of the coupled system will be reduced by two for every coordinate that does not appear in the Hamiltonian.#Footnote(22)

#page(227)

#### Motion in a central potential
Consider the motion of a particle of mass /m/ in a central potential. A natural choice for generalized coordinates that reflects the symmetry is polar coordinates. A Lagrangian is (equation #Eqn(chapter001,1.69,1.69)):

$$\begin{array}{ll} {L(t;r,\varphi;\dot{r},\dot{\varphi}) = \frac{1}{2}m({\dot{r}}^{2} + r^{2}{\dot{\varphi}}^{2}) - V(r).} \tag{3.99} \\ \end{array}$$

The momenta are /p_{r}/ = /mṙ/ and $ p_{\varphi} = mr^{2}\dot{\varphi}$. The kinetic energy is a homogeneous quadratic form in the velocities, so the Hamiltonian is /T/ + /V/ with the velocities rewritten in terms of the momenta:

$$\begin{matrix} {H\left( {t;r,\varphi;p_{r},p_{\varphi}} \right) = \frac{p_{r}^{2}}{2m} + \frac{p_{\varphi}^{2}}{2mr^{2}} + V\left( r \right).} \tag{3.100} \\ \end{matrix}$$

Hamilton's equations are

$$\begin{array}{rcl} {Dr(t)} & {= \frac{p_{r}(t)}{m}} & \\ {D\varphi(t)} & {= \frac{p_{\varphi}(t)}{m{(r(t))}^{2}}} & \\ {Dp_{r}(t)} & {= \frac{{(p_{\varphi}(t))}^{2}}{m{(r(t))}^{3}} - DV(r(t))} & \\ {Dp_{\varphi}(t)} & {= 0.} \tag{3.101} \\ \end{array}$$

The potential energy depends on the distance from the origin, /r/, as does the kinetic energy in polar coordinates, but neither the potential energy nor the kinetic energy depends on the polar angle /φ/. The angle /φ/ does not appear in the Lagrangian so we know that /p/_{φ}, the momentum conjugate to /φ/, is conserved along realizable trajectories. The fact that /p/_{φ} is constant along realizable paths is expressed by one of Hamilton's equations. That /p/_{φ} has a constant value is immediately made use of in the other Hamilton's equations: the remaining equations are a self-contained subsystem with constant /p/_{φ}. To make a lower-dimensional subsystem in the Lagrangian formulation we have to use each conserved momentum to eliminate one of the other state variables, as we did for the axisymmetric top (see [section 2.10](chapter002!section_2.10)).

We can check our derivations with the computer. A procedure implementing the Lagrangian has already been introduced (below equation #Eqn(chapter001,1.69,1.69)). We can use this to get the Hamiltonian:

#page(228)
```Scheme
(show-expression ((Lagrangian->Hamiltonian (L-central-polar 'm (literal-function 'V))) (up 't (up 'r 'phi) (down 'p_r 'p_phi)))) 
```

$$ V(r) + \frac{\frac{1}{2}p_{\varphi}^{2}}{mr^{2}} + \frac{\frac{1}{2}p_{r}^{2}}{m}$$

and to develop Hamilton's equations:
```Scheme
(show-expression (((Hamilton-equations (Lagrangian->Hamiltonian (L-central-polar 'm (literal-function 'V)))) (up (literal-function 'r) (literal-function 'phi)) (down (literal-function 'p_r) (literal-function 'p_phi))) 't)) 
```

$$\begin{pmatrix} 0 \\ \begin{pmatrix} {Dr(t) - \frac{p_{r}(t)}{m}} \\ {D\varphi(t) - \frac{p_{\varphi}(t)}{m{(r(t))}^{2}}} \\ \end{pmatrix} \\ \begin{bmatrix} {Dp_{r}(t) + DV(r(t)) - \frac{{(p_{\varphi}(t))}^{2}}{m{(r(t))}^{3}}} \\ {Dp_{\varphi}(t)} \\ \end{bmatrix} \\ \end{pmatrix}$$

#### Axisymmetric top
We reconsider the axisymmetric top (see [section 2.10](chapter002!section_2.10)) from the Hamiltonian point of view. Recall that a top is a rotating rigid body, one point of which is fixed in space. The center of mass is not at the fixed point, and there is a uniform gravitational field. An axisymmetric top is a top with an axis of symmetry. We consider here an axisymmetric top with the fixed point on the symmetry axis.

The axisymmetric top has two continuous symmetries we would like to exploit. It has the symmetry that neither the kinetic nor potential energy is sensitive to the orientation of the top about
#page(229)
the symmetry axis. The kinetic and potential energy are also insensitive to a rotation of the physical system about the vertical axis, because the gravitational field is uniform. We take advantage of these symmetries by choosing coordinates that naturally express them. We already have an appropriate coordinate system that does the job---the Euler angles. We choose the reference orientation of the top so that the symmetry axis is vertical. The first Euler angle, /ψ/, expresses a rotation about the symmetry axis. The next Euler angle, /θ/, is the tilt of the symmetry axis of the top from the vertical. The third Euler angle, /φ/, expresses a rotation of the top about the fixed /ẑ/ axis. The symmetries of the problem imply that the first and third Euler angles do not appear in the Hamiltonian. As a consequence the momenta conjugate to these angles are conserved quantities. The problem of determining the motion of the axisymmetric top is reduced to the problem of determining the evolution of /θ/ and /p_{θ}/. Let's work out the details.

In terms of Euler angles, a Lagrangian for the axisymmetric top is (see [section 2.10](chapter002!section_2.10)):
```Scheme
(define ((L-axisymmetric-top A C gMR) local) (let ((q (coordinate local)) (qdot (velocity local))) (let ((theta (ref q 0)) (thetadot (ref qdot 0)) (phidot (ref qdot 1)) (psidot (ref qdot 2))) (+ (* 1/2 A (+ (square thetadot) (square (* phidot (sin theta))))) (* 1/2 C (square (+ psidot (* phidot (cos theta))))) (* -1 gMR (cos theta))))))
```
where gMR is the product of the gravitational acceleration, the mass of the top, and the distance from the point of support to the center of mass. The Hamiltonian is nicer than we have a right to expect:
```Scheme
(show-expression ((Lagrangian->Hamiltonian (L-axisymmetric-top 'A 'C 'gMR)) (up 't (up 'theta 'phi 'psi) (down 'p_theta 'p_phi 'p_psi)))) 
```
#page(230)
$\begin{array}{ll} \frac{\frac{1}{2}p_{\psi}^{2}}{C} & {+ \frac{\frac{1}{2}p_{\psi}^{2}{(\cos(\theta))}^{2}}{A\,{(\sin\,(\theta))}^{2}} + \frac{\frac{1}{2}p_{\theta}^{2}}{A} - \frac{p_{\varphi}p_{\psi}\cos(\theta)}{A\,{(\sin\,(\theta))}^{2}} + \frac{\frac{1}{2}p_{\varphi}^{2}}{A\,{(\sin\,(\theta))}^{2}}} \\  & {+ gMR\,\cos\,(\theta)} \\ \end{array}$ Note that the angles /φ/ and /ψ/ do not appear in the Hamiltonian, as expected. Thus the momenta /p/_{φ} and /p_{ψ}/ are constants of the motion.

For given values of /p/_{φ} and /p_{ψ}/ we must determine the evolution of /θ/ and /p_{θ}/. The effective Hamiltonian for /θ/ and /p_{θ}/ has one degree of freedom, and does not involve the time. Thus the value of the Hamiltonian is conserved along realizable trajectories. So the trajectories of /θ/ and /p_{θ}/ trace contours of the effective Hamiltonian. This gives us a big picture of the possible types of motion and their relationship, for given values of /p/_{φ} and /p_{ψ}/.

If the top is standing vertically then /p/_{φ} = /p_{ψ}/. Let's concentrate on the case that /p/_{φ} = /p_{ψ}/, and define /p/ = /p_{ψ}/ = /p/_{φ}. The effective Hamiltonian becomes (after a little trigonometric simplification)

$$\begin{array}{ll} {H_{p}(t,\theta,p_{\theta}) = \frac{p_{\theta}^{2}}{2A} + \frac{p^{2}}{2C} + \frac{p^{2}}{2A}{\tan}^{2}\frac{\theta}{2} + gMR\cos\theta.} \tag{3.102} \\ \end{array}$$

Defining the effective potential energy

$$\begin{array}{ll} {V_{p}(\theta) = \frac{p^{2}}{2C} + \frac{p^{2}}{2A}{\tan}^{2}\frac{\theta}{2} + gMR\cos\theta,} \tag{3.103} \\ \end{array}$$

which parametrically depends on /p/, the effective Hamiltonian is

$$\begin{array}{ll} {H_{p}(t,\theta,p_{\theta}) = \frac{p_{\theta}^{2}}{2A} + V_{p}(\theta).} \tag{3.104} \\ \end{array}$$

If /p/ is large, /V_{p}/ has a single minimum at /θ/ = 0, as seen in [figure 3.5](#figure_3.5) (top curve). For small /p/ (bottom curve) there is a minimum for finite positive /θ/ and a symmetrical minimum for negative /θ/; there is a local maximum at /θ/ = 0. There is a critical value of /p/ at which /θ/ = 0 changes from a minimum to a local maximum. Denote the critical value by /p_{c}/. A simple calculation shows $ p_{c} = \sqrt{4gMRA}$. For /θ/ = 0 we have /p/ = /Cω/, where /ω/ is the rotation rate. Thus to /p_{c}/ there corresponds a critical rotation rate

$$\begin{array}{ll} {\omega_{c} = \sqrt{4gMRA}/C.} \tag{3.105} \\ \end{array}$$

#page(231)

#Image(Art_P708.jpg,figure_3.5)
#Caption *Figure 3.5* The effective potential energy /V_{p}/ of the axisymmetric top as a function of the angle /θ/. The top curve is for an axial angular momentum /p/ > /p_{c}/. For this value the top is stable standing vertically. The bottom curve is for /p/ < /p_{c}/. Here the top is not stable standing vertically. The middle curve is for /p/ at the critical angular momentum. We see the bifurcation of the stable equilibrium of the sleeping top into three equilibrium points, one of them unstable. #CaptionEnd

For /ω/ > /ω_{c}/ the top can stand vertically; for /ω/ < /ω_{c}/ the top falls if slightly displaced from the vertical. A top that stands vertically is called a “sleeping” top. For a more realistic top, friction gradually slows the rotation; the rotation rate eventually falls below the critical rotation rate and the top “wakes up.”

We get additional insight into the sleeping top and the awake top by looking at the trajectories in the /θ/, /p_{θ}/ phase plane. The trajectories in this plane are simply contours of the Hamiltonian, because the Hamiltonian is conserved. [Figure 3.6](#figure_3.6) shows a phase portrait for /ω/ > /ω_{c}/. All of the trajectories are loops around the vertical (/θ/ = 0). Displacing the top slightly from the vertical simply places the top on a nearby loop, so the top stays nearly vertical. [Figure 3.7](#figure_3.7) shows the phase portrait for /ω/ < /ω_{c}/. Here the vertical position is an unstable equilibrium. The trajectories that approach the vertical are asymptotic---they take an infinite amount of time to reach it, just as a pendulum with just the right
#page(232)
initial conditions can approach the vertical but never reach it. If the top is displaced slightly from the vertical then the trajectories loop around another center with nonzero /θ/. A top started at the center point of the loop stays there, and one started near this equilibrium point loops stably around it. Thus we see that when the top “wakes up” the vertical is unstable, but the top does not fall to the ground. Rather, it oscillates around a new equilibrium.

#Image(Art_P709.jpg,figure_3.6)
#Caption *Figure 3.6* Trajectories of the axisymmetric top plotted on the (/θ/, /p_{θ}/) phase plane with /p/_{φ} = /p_{ψ}/ and /ω/ = 145 rad s^{−1}. The parameters are /A/ = 0.000696 kg m^{2}, /C/ = 0.000132 kg m^{2}, /gMR/ = 0.112 kg m^{2} s^{−2}. For these parameters the critical frequency /ω_{c}/ is about 133.8 rad s^{−1}. #CaptionEnd

It is also interesting to consider the axisymmetric top when /p/_{φ} = /p_{ψ}/. Consider the case /p/_{φ} ≠ /p_{ψ}/. Some trajectories in the /θ/, /p_{θ}/ plane are shown in [figure 3.8](#figure_3.8). Note that in this case trajectories do not go through /θ/ = 0. The phase portrait for /p_{φ}/ < /p_{ψ}/ is similar and is not shown.

We have reduced the motion of the axisymmetric top to quadratures by choosing coordinates that express the symmetries. It turns out that the resulting integrals can be expressed in terms of elliptic functions. Thus, the axisymmetric top can be solved
#page(233)
analytically. We do not dwell on this solution because it is not very illuminating: since most problems cannot be solved analytically, there is little profit in dwelling on the analytic solution of one of the rare problems that is analytically solvable. Rather, we have focused on the geometry of the solutions in the phase space and the use of conserved quantities to reduce the dimension of the problem. With the phase-space portrait we have found some interesting qualitative features of the motion of the top.

#Image(Art_P710.jpg,figure_3.7)
#Caption *Figure 3.7* Trajectories of the axisymmetric top plotted on the (/θ/, /p_{θ}/) phase plane with /p/_{φ} = /p_{ψ}/ and /ω/ = 120 rad s^{−1}. The other parameters are as before. #CaptionEnd

### Exercise 3.8: Sleeping top

Verify that the critical angular velocity above which an axisymmetric top can sleep is given by equation (#Eqn(chapter003,3.105,3.105)).

##### 3.4.1 Lagrangian Reduction
Suppose there are cyclic coordinates. In the Hamiltonian formulation, the equations of motion for the coordinates and momenta for the other degrees of freedom form a self-contained subsystem in
#page(234)
which the momenta conjugate to the cyclic coordinates are parameters. We can form a Lagrangian for this subsystem by performing a Legendre transform of the reduced Hamiltonian. Alternatively, we can start with the full Lagrangian and perform a Legendre transform for only those coordinates that are cyclic. The equations of motion are Hamilton's equations for those variables that are transformed and Lagrange's equations for the others. The momenta conjugate to the cyclic coordinates are conserved and can be treated as parameters in the Lagrangian for the remaining coordinates.

#Image(Art_P711.jpg,figure_3.8)
#Caption *Figure 3.8* Trajectories of the axisymmetric top plotted on the (/θ/, /p_{θ}/) phase plane with /p/_{φ} > /p_{ψ}/. Most of the parameters are as in [figure 3.6](#figure_3.6), but here /p/_{φ} = 0.0145 kg m^{2}s^{−1} and /p_{ψ}/ = 0.0119 kg m^{2}s^{−1}. #CaptionEnd

Divide the tuple /q/ of coordinates into two subtuples /q/ = (/x/, /y/). Assume /L/(/t/; /x/, /y/; /v_{x}/, /v_{y}/) is a Lagrangian for the system. Define the /Routhian R/ as the Legendre transform of /L/ with respect to the /v_{y}/ slot:

#page(235)

$$\begin{aligned} {p_{y} = \partial_{2,1}L(t;x,y;v_{x},v_{y})} \tag{3.106} \\ \end{aligned}$$

$$\begin{aligned} {p_{y}v_{y} = R(t;x,y;v_{x},p_{y}) + L(t;x,y;v_{x},v_{y})} \tag{3.107} \\ \end{aligned}$$

$$\begin{aligned} {v_{y} = \partial_{2,1}R(t;x,y;v_{x},p_{y})} \tag{3.108} \\ \end{aligned}$$

$$\begin{aligned} {0 = \partial_{0}R(t;x,y;v_{x},p_{y}) + \partial_{0}L(t;x,y;v_{x},v_{y})} \tag{3.109} \\ \end{aligned}$$

$$\begin{aligned} {0 = \partial_{1}R(t;x,y;v_{x},p_{y}) + \partial_{1}L(t;x,y;v_{x},v_{y})} \tag{3.110} \\ \end{aligned}$$

$$\begin{aligned} {0 = \partial_{2,0}R(t;x,y;v_{x},p_{y}) + \partial_{2,0}L(t;x,y;v_{x},v_{y}).} \tag{3.111} \\ \end{aligned}$$

To define the function /R/ we must solve equation (#Eqn(chapter003,3.106,3.106)) for /v_{y}/ in terms of the other variables, and substitute this into equation (#Eqn(chapter003,3.107,3.107)).

Define the state path Ξ:

$$\begin{array}{ll} {\Xi(t) = (t;x(t),y(t);Dx(t),p_{y}(t)),} \tag{3.112} \\ \end{array}$$

where

$$\begin{array}{ll} {p_{y}(t) = \partial_{2,1}L(t;x(t),y(t);Dx(t),Dy(t)).} \tag{3.113} \\ \end{array}$$

Realizable paths satisfy the equations of motion (see [exercise 3.9](#exercise_3.9))

$$\begin{array}{ll} {D(\partial_{2,0}R \circ \Xi)(t) = \partial_{1,0}R \circ \Xi(t)} \tag{3.114} \\ \end{array}$$

$$\begin{array}{ll} {Dy(t) = \partial_{2,1}R \circ \Xi(t)} \tag{3.115} \\ \end{array}$$

$$\begin{array}{ll} {Dp_{y}(t) = - \partial_{1,1}R \circ \Xi(t),} \tag{3.116} \\ \end{array}$$

which are Lagrange's equations for /x/ and Hamilton's equations for /y/ and /p_{y}/.

Now suppose that the Lagrangian is cyclic in /y/. Then ∂_{1,1}/L/ = ∂_{1,1}/R/ = 0, and /p_{y}/(/t/) is a constant /c/ on any realizable path. Equation (#Eqn(chapter003,3.114,3.114)) does not depend on /y/, by assumption, and we can replace /p_{y}/ by its constant value /c/. So equation (#Eqn(chapter003,3.114,3.114)) forms a closed subsystem for the path /x/. The Lagrangian /L_{c}/

$$\begin{array}{ll} {L_{c}(t,x,v_{x}) = - R(t;x, \bullet ;v_{x},c)} \tag{3.117} \\ \end{array}$$

describes the motion of the subsystem (the minus sign is introduced for convenience, and ● indicates that the function's value is independent of this argument). The path /y/ can be found by integrating equation (#Eqn(chapter003,3.115,3.115)) using the independently determined path /x/.

#page(236)

Define the action

$$\begin{array}{ll} {S_{c}^{\prime}\lbrack x\rbrack(t_{1},t_{2}) = {\int_{t_{1}}^{t_{2}}L_{c}} \circ \Gamma\lbrack x\rbrack.} \tag{3.118} \\ \end{array}$$

The realizable paths /x/ satisfy the Lagrange equations with the Lagrangian /L_{c}/, so the action $ S_{c}^{\prime}$ is stationary with respect to variations /ξ/ of /x/ that are zero at the end times:

$$\begin{array}{ll} {\delta_{\xi}S_{c}^{\prime}(t_{1},t_{2}) = 0.} \tag{3.119} \\ \end{array}$$

For realizable paths /q/ the action $S[q](t_{1}, t_{2})$ is stationary with respect to variations /η/ of /q/ that are zero at the end times. Along these paths the momentum /p_{y}/(/t/) has the constant value /c/. For these same paths the action $ S_{c}^{\prime}\left\lbrack x \right\rbrack\left( {t_{1},t_{2}} \right)$ is stationary with respect to variations /ξ/ of /x/ that are zero at the end times. The dimension of /ξ/ is smaller than the dimension of /η/.

The values of the actions $ S_{c}^{\prime}\left\lbrack x \right\rbrack\left( {t_{1},t_{2}} \right)$ and $S[q](t_{1}, t_{2})$ are related:

$$\begin{array}{cll} {S\lbrack q\rbrack(t_{1},t_{2})} & {= S_{c}^{\prime}\lbrack x\rbrack - {\int_{t_{1}}^{t_{2}}{cv_{y}}}} & \\  & {= S_{c}^{\prime}\lbrack x\rbrack - c(y(t_{2}) - y(t_{1})).} \tag{3.120} \\ \end{array}$$

### Exercise 3.9: Routhian equations of motion

Verify that the equations of motion are given by equations #Eqn(chapter003,3.114,3.114)--#Eqn(chapter003,3.116,3.116).

### 3.5 Phase Space Evolution
Most problems do not have enough symmetries to be reducible to quadrature. It is natural to turn to numerical integration to learn more about the evolution of such systems. The evolution in phase space may be found by numerical integration of Hamilton's equations.

As an illustration, consider again the periodically driven pendulum (see [page 74](chapter001!p74)). The Hamiltonian is
```Scheme
(show-expression ((Lagrangian->Hamiltonian (L-periodically-driven-pendulum 'm 'l 'g 'a 'omega)) (up 't 'theta 'p_theta))) 
```
#page(237)

#Image(Art_P730.jpg)
#Caption( *Figure 3.9* A trajectory of the periodically driven pendulum on the (/θ/, /p_{θ}/) phase plane. The trajectory starts in the oscillation region at (1, 0). It oscillates for a while, but then escapes into circulation, only later to be recaptured into oscillation. )$\begin{array}{l} {- \frac{1}{2}a^{2}m\omega^{2}\,{(\cos\,(\theta))}^{2}\,\sin\,{((\omega t))}^{2} + agm\,\cos\,(\omega t)} \\ {\,\,\,\frac{+ a\omega p_{\theta}\,\sin\,(\theta)\,\sin\,(\omega t)}{l} - glm\,\cos\,(\theta) + \frac{\frac{1}{2}p_{\theta}^{2}}{l^{2}m}} \\ \end{array}$ Hamilton's equations for the periodically driven pendulum are un-revealing, so we will not show them. We build a system derivative from the Hamiltonian:
```Scheme
(define (H-pend-sysder m l g a omega) (Hamiltonian->state-derivative (Lagrangian->Hamiltonian (L-periodically-driven-pendulum m l g a omega)))) 
```
Now we integrate this system, with the same initial conditions as in [section 1.7](chapter001!section_1.7) (see [figure 1.7](#figure_1.7)), but display the trajectory in phase space ( [figure 3.9](#figure 3.9) ), using a monitor procedure:
```Scheme
(define window (frame :-pi :pi -10.0 10.0)) (define ((monitor-p-theta win) state) (let ((q ((principal-value :pi) (coordinate state))) (p (momentum state))) (plot-point win q p))) 
```
We use evolve to explore the evolution of the system:
```Scheme
(let ((m 1.0) ;m=1 kg (l 1.0) ;l=1 m (g 9.8) ;g=9.8 m/s² (A 0.1) ;A=1/10 m (omega (* 2 (sqrt 9.8))) ((evolve H-pend-sysder m l g A omega) (up 0.0 ;t₀=0 1.0 ;θ₀=1 rad 0.0) ;p₀=0 kg m²/s (monitor-p-theta window) 0.01 ;plot interval 100.0 ;final time 1.0e-12))) 
```
The trajectory sometimes oscillates and sometimes circulates. The patterns in the phase plane are reminiscent of the trajectories in the phase plane of the undriven pendulum shown in [figure 3.4](#figure_3.4) on [page 225](chapter003!p225).

##### 3.5.1 Phase-Space Description Is Not Unique
We are familiar with the fact that a given motion of a system is expressed differently in different coordinate systems: the functions that express a motion in rectangular coordinates are different from the functions that express the same motion in polar coordinates. However, in a given coordinate system the evolution of the local state tuple for particular initial conditions is unique. The generalized velocity path function is the derivative of the generalized coordinate path function. On the other hand, the coordinate system alone does not uniquely specify the phase-space description. The relationship of the momentum to the coordinates and the velocities depends on the Lagrangian, and many different Lagrangians may be used to describe the behavior of the same physical system. When two Lagrangians for the same physical system are different, the phase-space descriptions of a dynamical state are different.

#page(239)

We have already seen two different Lagrangians for the driven pendulum (see [section 1.6.4](chapter001!section_1.6.4)): one was found using /L/ = /T/ −/V/ and the other was found by inspection of the equations of motion. The two Lagrangians differ by a total time derivative. The momentum /p_{θ}/ conjugate to /θ/ depends on which Lagrangian we choose to work with, and the description of the evolution in the corresponding phase space also depends on the choice of Lagrangian, even though the behavior of the system is independent of the method used to describe it. The momentum conjugate to /θ/, using the /L/ = /T/ − /V/ Lagrangian for the periodically driven pendulum, is

$$\begin{array}{ll} {p_{\theta} = ml^{2}\dot{\theta} - alm\omega\,\sin\,\theta\,\sin\,\omega t,} \tag{3.121} \\ \end{array}$$

but with the alternative Lagrangian, it is

$$\begin{array}{ll} {p_{\theta} = ml^{2}\dot{\theta}.} \tag{3.122} \\ \end{array}$$

The two momenta differ by an additive distortion that varies periodically in time and depends on /θ/. That the phase-space descriptions are different is illustrated in [figure 3.10](#figure_3.10). The evolution of the system is the same for each.

### 3.6 Surfaces of Section
Computing the evolution of mechanical systems is just the beginning of understanding the dynamics. Typically, we want to know much more than the phase space evolution of some particular trajectory. We want to obtain a qualitative understanding of the motion. We want to know what sorts of motion are possible, and how one type relates to others. We want to abstract the essential dynamics from the myriad particular evolutions that we can calculate. Paradoxically, it turns out that by throwing away most of the calculated information about a trajectory we gain essential new information about the character of the trajectory and its relation to other trajectories.

A remarkable tool that extracts the essence by throwing away information is a technique called the /surface of section/ or /Poincaré section/.#Footnote(23) A surface of section is generated by looking at successive intersections of a trajectory or a set of trajectories with a plane in the phase space. Typically, the plane is spanned by a coordinate axis and the canonically conjugate momentum axis. We will see that surfaces of section made in this way have nice properties.

#page(240)

#Image(Art_P734.jpg,figure_3.10)
#Caption *Figure 3.10* A trajectory of the periodically driven pendulum on the (/θ/, /p_{θ}/) phase plane. In the upper plot the trajectory is derived using the Lagrangian /L/ = /T/ − /V/ (see equation #Eqn(chapter001,1.88,1.88) on [page 51](chapter001!p51). In the lower plot the trajectory is derived using the alternative Lagrangian of equation (#Eqn(chapter001,1.120,1.120)) on [page 66](chapter001!p66). The evolution is the same, but the phase-space representations are not. #CaptionEnd

#page(241)

The surface of section technique was put to spectacular use in the 1964 landmark paper [22](bibliography!bib_22) by astronomers Michel Hénon and Carl Heiles. In their numerical investigations they found that some trajectories are chaotic, whereas other trajectories are regular. An essential characteristic of the chaotic motions is that initially nearby trajectories separate exponentially with time; the separation of regular trajectories is linear.#Footnote(24) They found that these two types of trajectories are typically clustered in the phase space into regions of regular motion and regions of chaotic motion.

##### 3.6.1 Periodically Driven Systems
For a periodically driven system the surface of section is a stroboscopic view of the evolution; we consider only the state of the system at the strobe times, with the period of the strobe equal to the drive period. We generate a surface of section for a periodically driven system by computing a number of trajectories and accumulating the phase-space coordinates of each trajectory whenever the drive passes through some particular phase. Let /T/ be the period of the drive; then, for each trajectory, the surface of section accumulates the phase-space points (/q/(/t/), /p/(/t/)), (/q/(/t/ + /T/), /p/(/t/ + /T/)), (/q/(/t/ + 2/T/), /p/(/t/ + 2/T/)), and so on (see [figure 3.11](#figure_3.11)). For a system with a single degree of freedom we can plot the sequence of phase-space points on a /q/, /p/ surface.

In the case of the stroboscopic section for the periodically driven system, the phase of the drive is the same for all section points;
#page(242)
thus each phase-space point in the section, with the known phase of the drive, may be considered as an initial condition for the rest of the trajectory. The absolute time of the particular section point does not affect the subsequent evolution; all that matters is that the phase of the drive have the value specified for the section. Thus we can think of the dynamical evolution as generating a map that takes a point in the phase space and generates a new point in the phase space after evolving the system for one drive period. This map of the phase space onto itself is called the /Poincaré map/.

#Image(Art_P735.jpg,figure_3.11)
#Caption *Figure 3.11* Stroboscopic surface of section for a periodically driven system. For each trajectory the surface of section accumulates the set of phase-space points after each full cycle of the drive. #CaptionEnd

[Figure 3.12](#figure_3.12) shows an example Poincaré section for the driven pendulum. We plot the section points for a number of different initial conditions. We are immediately presented with a new facet of dynamical systems. For some initial conditions, the subsequent section points appear to fill out a set of curves in the section. For other initial conditions this is not the case: rather, the set
#page(243)
of section points appear scattered over a region of the section. In fact, /all/ of the scattered points in [figure 3.12](#figure_3.12) were generated from a single initial condition. The surface of section suggests that there are qualitatively different classes of trajectories distinguished by the dimension of the subspace of the section that they explore.

#Image(Art_P736.jpg,figure_3.12)
#Caption *Figure 3.12* A surface of section for the driven pendulum on the (/θ/, /p_{θ}/) phase plane. The samples are taken at the peaks of the drive. For this section the parameters are: /m/ = 1 kg, /l/ = 1 m, /g/ = 9.8 m s^{−2}, /A/ = 0.05 m, and /ω/ = 4.2 /ω/_{0}, with ¶ $\omega_{0} = \sqrt{g/l}$ ¶ . #CaptionEnd

Trajectories that fill out curves on the surface of section are called /regular/ or /quasiperiodic/ trajectories. The curves that are filled out by the regular trajectories are /invariant curves/. They are invariant in that if any section point for a trajectory falls on an invariant curve, all subsequent points fall on the same invariant curve. Otherwise stated, the Poincaré map maps every point on an invariant curve onto the invariant curve.

The trajectories that appear to fill areas are called /chaotic/ trajectories. For these points the distance in phase space between initially nearby points grows, on average, exponentially with time.#Footnote(25)#page(244)
In contrast, for the regular trajectories, the distance in phase space between initially nearby points grows, on average, linearly with time.

The phase space seems to be grossly clumped into different regions. Initial conditions in some regions appear to predominantly yield regular trajectories, and other regions appear to predominantly yield chaotic trajectories. This gross division of the phase space into qualitatively different types of trajectories is called the /divided phase space/. We will see later that there is much more structure here than is apparent at this scale, and that upon magnification there is a complicated interweaving of chaotic and regular regions on finer and finer scales. Indeed, we shall see that many trajectories that appear to generate curves on the surface of section are, upon magnification, actually chaotic and fill a tiny area. We shall also find that there are trajectories that lie on one-dimensional curves on the surface of section, but only explore a subset of this curve formed by cutting out an infinite number of holes.#Footnote(26)

The features seen on the surface of section of the driven pendulum are quite general. The same phenomena are seen in most dynamical systems. In general, there are both regular and chaotic trajectories, and there is the clumping characteristic of the divided phase space. The specific details depend upon the system, but the basic phenomena are generic. Of course, we are interested in both aspects: the phenomena that are common to all systems, and the specific details for particular systems of interest.

The surface of section for the periodically driven pendulum has specific features that give us qualitative information about how this system behaves. The central island in [figure 3.12](#figure_3.12) is the remnant of the oscillation region for the unforced pendulum (see [figure 3.4](#figure_3.4) in [section 3.3](#section_3.3)). There is a sizable region of regular trajectories here that are, in a sense, similar to the trajectories of the unforced pendulum. In this region, the pendulum oscillates back and forth, much as the undriven pendulum does, but the drive makes it wiggle as it does so. The section points are all collected at the same phase of the drive so we do not see these wiggles on the section.

#page(245)

The central island is surrounded by a large chaotic zone. Thus the region of phase space with regular trajectories similar to the unforced trajectories has finite extent. On the section, the boundary of this “stable” region is apparently rather well defined---there is a sudden transition from smooth regular invariant curves to chaotic motion that can take the system far from this region of regular motion.

There are two other sizeable regions of regular behavior with finite angular extent. The trajectories in these regions are resonant with the drive, on average executing one full rotation per cycle of the drive. The two islands differ in the direction of the rotation. In these regions the pendulum is making complete rotations, but the rotation is locked to the drive so that points on the section appear only in the islands. The fact that points for particular trajectories loop around the islands means that the pendulum sometimes completes a cycle faster than the drive and sometimes slower than the drive, but never loses lock.

Each regular region has finite extent. So from the surface of section we can see directly the range of initial conditions that remain in resonance with the drive. Outside of the regular region initial conditions lead to chaotic trajectories that evolve far from the resonant regions.

Various higher-order resonance islands are also visible, as are nonresonant regular circulating orbits. So, the surface of section has provided us with an overview of the main types of motion that are possible and their interrelationship.

Changing the parameters shows other interesting phenomena. [Figure 3.13](#figure_3.13) shows the surface of section when the drive frequency is twice the natural small-amplitude oscillation frequency of the undriven pendulum. The section has a large chaotic zone, with an interesting set of islands. The central equilibrium has undergone an instability and instead of a central island we find two off-center islands. These islands are alternately visited one after the other. As the support goes up and down the pendulum alternately tips to one side and then the other. It takes two periods of the drive before the pendulum visits the same island. Thus, the system has “period-doubled.” An island has been replaced by a period-doubled pair of islands. Note that other islands still exist. The islands in the top and bottom of the chaotic zone are the resonant islands, in which the pendulum loops on average a full turn for
#page(246)
every cycle of the drive. Note that, as before, if the pendulum is rapidly circulating, the motion is regular.

#Image(Art_P738.jpg,figure_3.13)
#Caption *Figure 3.13* Another surface of section for the driven pendulum on the (/θ/, /p_{θ}/) phase plane. Here we see a period-doubled central island. For this section the frequency of the drive is resonant with the frequency of small-amplitude oscillations of the undriven pendulum. The angular momentum scale is −10 to 10 kg m^{2} s^{−1}. For this section the parameters are: /m/ = 1 kg, /l/ = 1 m, /g/ = 9.8 m s^{−2}, /A/ = 0.1 m, /ω/ = 2/ω/_{0}. #CaptionEnd

It is a surprising fact that if we shake the support of a pendulum fast enough then the pendulum can stand upright. This phenomenon can be visualized with the surface of section. [Figure 3.14](#figure_3.14) shows a surface of section when the drive frequency is large compared to the natural frequency. That the pendulum can stand upright is indicated by the existence of a regular island at the inverted equilibrium. The surface of section shows that the pendulum can remain upright for a range of initial displacements from the vertical.

##### 3.6.2 Computing Stroboscopic Surfaces of Section
We already have the system derivative for the driven pendulum, and we can use it to make a parametric map for constructing Poincaré sections:

#page(247)

#Image(Art_P739.jpg,figure_3.14)
#Caption *Figure 3.14* A surface of section for the rapidly driven pendulum on the (/θ/, /p_{θ}/) phase plane. Here we see the emergence of a vertical equilibrium. The angular momentum scale is −20 to 20 kg m^{2} s^{−1}. For this section the parameters are: /m/ = 1 kg, /l/ = 1 m, /g/ = 9.8 m s^{−2}, /A/ = 0.2 m, /ω/ = 10.1/ω/_{0}. #CaptionEnd
```Scheme
(define (driven-pendulum-map m l g A omega) (let ((advance (state-advancer H-pend-sysder m l g A omega)) (map-period (/ :2pi omega))) (lambda (theta ptheta return fail) (let ((ns (advance (up 0 theta ptheta) ; initial state

map-period))) ; integration interval

(return ((principal-value :pi) (coordinate ns)) (momentum ns)))))) 
```
A map procedure takes the two section coordinates (here theta and ptheta) and two “continuation” procedures. If the section coordinates given are in the domain of the map, it produces two new section coordinates and passes them to the return continuation, otherwise the map procedure calls the fail continuation procedure with no arguments.#Footnote(27)

#page(248)

The trajectories of a map can be explored with an interactive interface. The procedure explore-map lets us use a pointing device to choose initial conditions for trajectories. For example, the surface of section in [figure 3.12](#figure_3.12) was generated by plotting a number of trajectories, using a pointer to choose initial conditions, with the following program:
```Scheme
(define win (frame :-pi :pi -20 20)) (let ((m 1.0) ;m=1kg (l 1.0) ;l=1m (g 9.8) ;g=9.8m/s^2 (A 0.05)) ;A=1/20m (let ((omega0 (sqrt (/ g l)))) (let ((omega (* 4.2 omega0))) (explore-map win (driven-pendulum-map m l g A omega) 1000)))) ;1000 points for each initial condition 
```
### Exercise 3.10: Fun with phase portraits

Choose some one-degree-of-freedom dynamical system that you are curious about and that can be driven with a periodic drive. Construct a map of the sort we made for the driven pendulum and do some exploring. Are there chaotic regions? Are all of the chaotic regions connected together?

##### 3.6.3 Autonomous Systems
We illustrated the use of Poincaré sections to visualize qualitative features of the phase space for a one-degree-of-freedom system with periodic drive, but the idea is more general. Here we show how Hénon and Heiles [22](bibliography!bib_22) used the surface of section to elucidate the properties of an autonomous system.

#### Hénon--Heiles background
In the early '60s astronomers were up against a wall. Careful measurements of the motion of nearby stars in the galaxy had allowed particular statistical averages of the observed motions to be determined, and the averages were not at all what was expected. In particular, what was calculated was the velocity dispersion: the root mean square deviation of the velocity from the average. We use angle brackets to denote an average over nearby stars: < /w/ > is the average value of some quantity /w/ for the stars in the ensemble.
#page(249)
The average velocity is $< \,\dot{\overset{\rightarrow}{x}}\, >$. The components of the velocity dispersion are

$$\begin{array}{ll} {\sigma_{x} = < \,{(\dot{x} - < \,\dot{x}\, > )}^{2}\, >^{1/2}} \tag{3.123} \\ \end{array}$$

$$\begin{array}{ll} {\sigma_{y} = < \,{(\dot{y} - < \,\dot{y}\, > )}^{2}\, >^{1/2}} \tag{3.124} \\ \end{array}$$

$$\begin{array}{ll} {\sigma_{z} = < \,{(\dot{z} - < \,\dot{z}\, > )}^{2}\, >^{1/2}.} \tag{3.125} \\ \end{array}$$

If we use cylindrical polar coordinates (/r/, /θ/, /z/) and align the axes with the galaxy so that /z/ is perpendicular to the galactic plane and /r/ increases with the distance to the center of the galaxy, then two particular components of the velocity dispersion are

$$\begin{array}{ll} {\sigma_{z} = < \,{(\dot{z} - < \,\dot{z}\, > )}^{2}\, >^{1/2}} \tag{3.126} \\ \end{array}$$

$$\begin{array}{ll} {\sigma_{r} = < \,{(\dot{r} - < \,\dot{r}\, > )}^{2}\, >^{1/2}.} \tag{3.127} \\ \end{array}$$

It was expected at the time that these two components of the velocity dispersion should be equal. In fact they were found to differ by about a factor of 2: /σ_{r}/ ≈ 2/σ_{z}/. What was the problem? In the literature at the time there was considerable discussion of what could be wrong. Was the problem some observational selection effect? Were the velocities measured incorrectly? Were the assumptions used in the derivation of the expected ratio not adequately satisfied? For example, the derivation assumed that the galaxy was approximately axisymmetric. Perhaps non-axisymmetric components of the galactic potential were at fault. It turned out that the problem was much deeper. The understanding of motion was wrong.

Let's review the derivation of the expected relation among the components of the velocity dispersion. We wish to give a statistical description of the distribution of stars in the galaxy. We introduce the phase-space distribution function $ f\left( {\overset{\rightarrow}{x},\overset{\rightarrow}{p}} \right)$, which gives the probability density of finding a star at position $\overset{\rightarrow}{x}$ with momentum $\overset{\rightarrow}{p}$.#Footnote(28) Integrating this density over some finite volume of phase space gives the probability of finding a star in that phase-space volume (in that region of space within a specified region of
#page(250)
momenta). We assume the probability density is normalized so that the integral over all of phase space gives unit probability; the star is somewhere and has some momentum with certainty. In terms of /f/, the statistical average of any dynamical quantity /w/ over some volume of phase space /V/ is just

$$\begin{array}{ll} {< \, w\, >_{V} = {\int_{V}{fw}}} \tag{3.128} \\ \end{array}$$

where the integral extends over the phase-space volume /V/. In computing the velocity dispersion at some point $\overset{\rightarrow}{x}$, we would compute the averages by integrating over all momenta.

Individual stars move in the gravitational potential of the rest of the galaxy. It is not unreasonable to assume that the overall distribution of stars in the galaxy does not change much with time, or changes only very slowly. The density of stars in the galaxy is actually very small and close encounters of stars are very rare. Thus, we can model the gravitational potential of the galaxy as a fixed external potential in which individual stars move. The galaxy is approximately axisymmetric. We assume that the deviation from exact axisymmetry is not a significant effect and thus we take the model potential to be exactly axisymmetric.

Consider the motion of a point mass (a star) in an axisymmetric potential (of the galaxy). In cylindrical polar coordinates the Hamiltonian is

$$\begin{array}{ll} {T + V = \frac{1}{2m}\left\lbrack {p_{r}^{2} + \frac{p_{\theta}^{2}}{r^{2}} + p_{z}^{2}} \right\rbrack + V(r,z),} \tag{3.129} \\ \end{array}$$

where /V/ does not depend on /θ/. Since /θ/ does not appear, we know that the conjugate momentum /p_{θ}/ is constant. For the motion of any particular star we can treat /p_{θ}/ as a parameter. Thus the effective Hamiltonian has two degrees of freedom:

$$\begin{array}{ll} {\frac{1}{2m}\left\lbrack {p_{r}^{2} + p_{z}^{2}} \right\rbrack + U(r,z)} \tag{3.130} \\ \end{array}$$

where

$$\begin{array}{ll} {U(r,z) = V(r,z) + \frac{p_{\theta}^{2}}{2mr^{2}}.} \tag{3.131} \\ \end{array}$$

#page(251)

The value /E/ of the Hamiltonian is constant since there is no explicit time dependence in the Hamiltonian. Thus, we have constants of the motion /E/ and /p_{θ}/.

Jeans's “theorem” asserts that the distribution function /f/ depends only on the values of the conserved quantities, also known as /integrals of motion/. That is, we can introduce a different distribution function /f/′ that represents the same physical distribution:

$$\begin{array}{ll} {f\prime(E,p_{\theta}) = f(\overset{\rightarrow}{x},\overset{\rightarrow}{p}).} \tag{3.132} \\ \end{array}$$

At the time, there was good reason to believe that this might be correct. First, it is clear that the distribution function surely depends at least on /E/ and /p_{θ}/. The problem is, “Given an energy /E/ and angular momentum /p_{θ}/, what motion is allowed?” The conserved quantities clearly confine the evolution. Does the evolution carry the system everywhere in the phase space subject to these known constraints? In the early part of the 20th century this appeared plausible. Statistical mechanics was successful, and statistical mechanics made exactly this assumption. Perhaps there are other conserved quantities of the motion that exist, but that we have not yet discovered?

Poincaré proved an important theorem with regard to conserved quantities. Poincaré proved that most of the conserved quantities of a dynamical system typically do not persist upon perturbation of the system. That is, if a small perturbation is added to a problem, then most of the conserved quantities of the original problem do not have analogs in the perturbed problem. The conserved quantities are destroyed. However, conserved quantities that result from symmetries of the problem continue to be preserved if the perturbed system has the same symmetries. Thus angular momentum continues to be preserved upon application of any axisymmetric perturbation. Poincaré's theorem is correct, but what came next was not.

As a corollary to Poincaré's theorem, in 1920 Fermi published a proof of a theorem stating that typically the motion of perturbed problems is ergodic#Footnote(29) subject to the constraints imposed by the conserved quantities resulting from symmetries. Loosely speaking,
#page(252)
this means that trajectories go everywhere they are allowed to go by the conservation constraints. Fermi's theorem was later shown to be incorrect, but on the basis of this theorem we could expect that typically systems fully explore the phase space, subject only to the constraints imposed by the conserved quantities resulting from symmetries. Suppose then that the evolution of stars in the galactic potential is subject only to the constraints of conserving /E/ and /p_{θ}/. We shall see that this is not true, but if it were we could then conclude that the distribution function for stars in the galaxy can also depend only on /E/ and /p_{θ}/.

Given this form of the distribution function, we can deduce the stated ratios of the velocity dispersions. We note that /p_{z}/ and /p_{r}/ appear in the same way in the energy. Thus the average of any function of /p_{z}/ computed with the distribution function must equal the average of the same function of /p_{r}/. In particular, the velocity dispersions in the /z/ and /r/ directions must be equal:

$$\begin{array}{ll} {\sigma_{z} = \sigma_{r}.} \tag{3.133} \\ \end{array}$$

But this is not what was observed, which was

$$\begin{array}{ll} {\sigma_{r} \approx 2\sigma_{z}.} \tag{3.134} \\ \end{array}$$

Hénon and Heiles [22](bibliography!bib_22) approached this problem differently from others at the time. Rather than improving the models for the motion of stars in the galaxy, they concentrated on what turned out to be the central issue: What is the qualitative nature of motion? The problem had nothing to do with galactic dynamics in particular, but with the problem of motion. They abstracted the dynamical problem from the particulars of galactic dynamics.

#### The system of Hénon and Heiles
We have seen that the study of the motion of a point with mass /m/ and an axisymmetric potential energy reduces to the study of a reduced two-degree-of-freedom problem in /r/ and /z/ with potential energy /U/(/r/, /z/). Hénon and Heiles chose to study the motion in a two-degree-of-freedom system with a particularly simple potential energy so that the dynamics would be clear and the calculation uncluttered. The Hénon--Heiles Hamiltonian is

$$\begin{array}{ll} {H(t;x,y;p_{x},p_{y}) = \frac{1}{2}(p_{x}^{2} + p_{y}^{2}) + V(x,y)} \tag{3.135} \\ \end{array}$$

#page(253)

#Image(Art_P754.jpg,figure_3.15)
#Caption *Figure 3.15* Contours of the Hénon--Heiles potential energy on the (/x/, /y/) plane. The contours shown, from the inside out, are for potential energies 1/100, 1/40, 1/20, 1/12, 1/8, and 1/6. #CaptionEnd

with potential energy

$$\begin{array}{ll} {V(x,y) = \frac{1}{2}(x^{2} + y^{2}) + x^{2}y - \frac{1}{3}y^{3}.} \tag{3.136} \\ \end{array}$$

The potential energy is shaped like a distorted bowl. It has triangular symmetry, as is evident when it is rewritten in polar coordinates:

$$\begin{array}{ll} {\frac{1}{2}r^{2} + \frac{1}{3}r^{3}\,\sin\, 3\theta.} \tag{3.137} \\ \end{array}$$

Contours of the potential energy are shown in [figure 3.15](#figure_3.15). At small values of the potential energy the contours are approximately circular; as the value of the potential energy approaches 1/6 the contours become triangular, and at larger potential energies the contours open to infinity.

#page(254)

The Hamiltonian is independent of time, so energy is conserved. In this case this is the only known conserved quantity. We first determine the restrictions that conservation of energy imposes on the evolution. We have

$$\begin{array}{ll} {E = \frac{1}{2}(p_{x}^{2} + p_{y}^{2}) + V(x,y) \geq V(x,y),} \tag{3.138} \\ \end{array}$$

so the motion is confined to the region inside the contour /V/ = /E/ because the sum of the squares of the momenta cannot be negative.

Let's compute some sample trajectories. For definiteness, we investigate trajectories with energy /E/ = 1/8. There is a large variety of trajectories. There are trajectories that circulate in a regular way around the bowl, and there are trajectories that oscillate back and forth ([figure 3.16](#figure_3.16)). There are also trajectories that appear more irregular ([figure 3.17](#figure_3.17)). There is no end to the trajectories that could be computed, but let's face it, surely there is more to life than looking at trajectories.

The problem facing Hénon and Heiles was the issue of conserved quantities. Are there other conserved quantities besides the obvious ones? They investigated this issue with the surface of section technique. The surface of section is generated by looking at successive passages of trajectories through a plane in phase space.

Specifically, the surface of section is generated by recording and plotting /p_{y}/ versus /y/ whenever /x/ = 0, as shown in [figure 3.18](#figure_3.18). Given the value of the energy /E/ and a point (/y/, /p_{y}/) on the section /x/ = 0, we can recover /p_{x}/, up to a sign. If we restrict attention to intersections with the section plane that cross with, say, positive /p_{x}/, then there is a one-to-one relation between section points and trajectories. A section point thus corresponds to a unique trajectory.

How does this address the issue of the number of conserved quantities? A priori, there appear to be two possibilities: either there are hidden conserved quantities or there are not. Suppose there is no other conserved quantity besides the energy. Then the expectation was that successive intersections of the trajectory with the section plane would eventually explore all of the section plane that is consistent with conservation of energy. On the other hand, if there is a hidden conserved quantity then the successive intersections would be constrained to fall on a curve.

#page(255)

#Image(Art_P758.jpg,figure_3.16)
#Caption *Figure 3.16* Two trajectories of the Hénon--Heiles Hamiltonian projected on the (/x/, /y/) plane. The energy is /E/ = 1/8. #CaptionEnd

#page(256)

#Image(Art_P759.jpg,figure_3.17)
#Caption *Figure 3.17* Another trajectory of the Hénon--Heiles Hamiltonian projected on the (/x/, /y/) plane. The energy is /E/ = 1/8. #CaptionEnd

#### Interpretation
On the section, the energy is

$$\begin{array}{ll} {E = H(t;0,y;p_{x},p_{y}) = \frac{1}{2}(p_{x}^{2} + p_{y}^{2}) + V(0,y).} \tag{3.139} \\ \end{array}$$

Because $ p_{x}^{2}$ is positive, the trajectory is confined to regions of the section such that

$$\begin{array}{ll} {E \geq \frac{1}{2}p_{y}^{2} + V(x = 0,y).} \tag{3.140} \\ \end{array}$$

So, if there is no other conserved quantity, we might expect the points on the section eventually to fill the area enclosed by this bounding curve.

On the other hand, suppose there is a hidden extra conserved quantity /I/(/x/, /y/; /p_{x}/, /p_{y}/) = 0. Then this conserved quantity would provide further constraints on the trajectories and their intersections with the section plane. An extra conserved quantity /I/ provides
#page(257)
a constraint among the four phase-space variables /x/, /y/, /p_{x}/, and /p_{y}/. We can use /E/ to solve for /p_{x}/, so for a given /E/, /I/ gives a relation among /x/, /y/, and /p_{y}/. Using the fact that on the section /x/ = 0, the /I/ gives a relation between /y/ and /p_{y}/ on the section for a given /E/. So we expect that if there is another conserved quantity the successive intersections of a trajectory with the section plane will fall on a curve.

#Image(Art_P763.jpg,figure_3.18)
#Caption *Figure 3.18* The surface of section for the Hénon--Heiles problem is generated by recording and plotting the successive crossings of the /x/ = 0 plane in the direction of increasing /x/. #CaptionEnd

If there is no extra conserved quantity we expect the section points to fill an area; if there is an extra conserved quantity we expect the section points to be restricted to a curve. What actually happens? [Figure 3.19](#figure_3.19) shows a surface of section for /E/ = 1/12; the section points for several representative trajectories are displayed. By and large, the points appear to be restricted to curves, so there appears to be evidence for an extra conserved quantity. Look closely though. Where the “curves” cross, the lines are a little fuzzy. Hmmm.

Let's try a little larger energy, /E/ = 1/8. The appearance of the section changes qualitatively ( [figure 3.20](#figure 3.20) ). For some trajectories there still appear to be extra constraints on the motion. But other trajectories appear to fill an area of the section plane, pretty much as we expected of trajectories if there was no extra conserved quantity. In particular, all of the scattered points on this section were generated by a single trajectory. Thus, some trajectories behave as if there is an extra conserved quantity, and others don't. Wow!

#page(258)

#Image(Art_P764.jpg,figure_3.19)
#Caption *Figure 3.19* Surface of section for the Hénon--Heiles problem with energy /E/ = 1/12. #CaptionEnd

Let's go on to a higher energy, /E/ = 1/6, just at the escape energy. A section for this energy is shown in [figure 3.21](#figure_3.21). Now, a single trajectory explores most of the region of the section plane allowed by energy conservation, but not entirely. There are still trajectories that appear to be subject to extra constraints.

We seem to have all possible worlds. At low energy, the system by and large behaves as if there is an extra conserved quantity, but not entirely. At intermediate energy, the phase space is divided: some trajectories explore areas whereas others are constrained. At high energy, trajectories explore most of the energy surface; few trajectories show extra constraints. We have just witnessed our first transition to chaos.

Two qualitatively different types of motion are revealed by this surface of section, just as we saw in the Poincaré sections for the driven pendulum. There are trajectories that seem to be constrained as if by an extra conserved quantity. And there are trajectories that explore an area on the section as though there were no extra conserved quantitiess. Regular trajectories appear to be constrained by an extra conserved quantity to a one-dimensional
#page(259)
set on the section; chaotic trajectories are not constrained in this way and explore an area.#Footnote(30)

#Image(Art_P765.jpg,figure_3.20)
#Caption *Figure 3.20* Surface of section for the Hénon--Heiles problem with energy /E/ = 1/8. #CaptionEnd

The surface of section not only reveals the existence of qualitatively different types of motion, but also provides an overview of the different types of trajectories. Take the surface of section for /E/ = 1/8 ([figure 3.20](#figure_3.20)). There are four main islands, engulfed in a chaotic sea. The particular trajectories displayed above provide examples from different parts of the section. The trajectory that loops around the bowl ([figure 3.16](#figure_3.16)) belongs to the large island on the left side of the section. Similar trajectories that loop around the bowl in the other direction belong to the large island on the right side of the section. The trajectories that oscillate back and
#page(260)
forth across the bowl belong to the two islands above and below the center of the section. (By symmetry there should be three such islands. The third island is snugly wrapped against the boundary of the section.) Each of the main islands is surrounded by a chain of secondary islands. We will see that the types of orbits are inexhaustible, if we look closely enough. The chaotic trajectory ([figure 3.17](#figure_3.17)) lives in the chaotic sea. Thus the section provides a summary of the types of motion possible and how they are related to one another. It is much more useful than plots of a zillion trajectories.

#Image(Art_P766.jpg,figure_3.21)
#Caption *Figure 3.21* Surface of section for the Hénon--Heiles problem with energy /E/ = 1/6. The section is clipped on the right. #CaptionEnd

The section for a particular energy summarizes the dynamics at that energy. A sequence of sections for various energies shows how the major features change with the energy. We have already noticed that at low energy the section is dominated by regular orbits, at intermediate energy the section is divided more or less equally into regular and chaotic regions, and at high energies the section is dominated by a single chaotic zone. We will see that such transitions from regular to chaotic behavior are quite common; similar phenomena occur in widely different systems, though the details depend on the system under study.

#page(261)

##### 3.6.4 Computing Hénon--Heiles Surfaces of Section
The following procedures implement the Poincaré map for the Hénon--Heiles system:
```Scheme
(define (HHmap E dt sec-eps int-eps) (define ((make-advance advancer eps) s dt) (advancer s dt eps)) (let ((adv (make-advance (state-advancer HHsysder) int-eps))) (lambda (y py cont fail) (let ((initial-state (section->state E y py))) (if (not initial-state) (fail) (find-next-crossing initial-state adv dt sec-eps (lambda (crossing-state running-state) (cont (ref (coordinate crossing-state) 1) (ref (momentum crossing-state) 1))))))))) 
```
Besides supplying the energy E of the section we must also supply a time step for the integrator to achieve, a tolerance for a point to be on the section sec-eps, and a local truncation error specification for the integrator int-eps.

For each initial point (/y/, /p_{y}/) on the surface of section, the map first finds the initial state that has the specified energy, if one exists. The procedure section->state handles this task:
```Scheme
(define (section->state E y py) (let ((d (- E (+ (HHpotential (up 0 (up 0 y))) (* 1/2 (square py)))))) (if (>= d 0.0) (let ((px (sqrt (* 2 d)))) (up 0 (up 0 y) (down px py))) #f))) 
```
The procedure section->state returns #f (false) if there is no state consistent with the specified energy.

The Hamiltonian procedure for the Hénon--Heiles problem is
```Scheme
(define (HHHam s) (+ (* 1/2 (square (momentum s))) (HHpotential s))) 
```
with the potential energy
```Scheme
(define (HHpotential s) (let ((x (ref (coordinate s) 0)) (y (ref (coordinate s) 1))) (+ (* 1/2 (+ (square x) (square y))) (- (* (square x) y) (* 1/3 (cube y)))))) 
```
The system derivative is computed directly from the Hamiltonian.
```Scheme
(define (HHsysder) (Hamiltonian->state-derivative HHHam)) 
```
The procedure find-next-crossing advances the initial state until successive states are on opposite sides of the section plane.
```Scheme
(define (find-next-crossing state advance dt sec-eps cont) (let lp ((s state)) (let ((next-state (advance s dt))) (if (and (> (ref (coordinate next-state) 0) 0) (< (ref (coordinate s) 0) 0)) (let ((crossing-state (refine-crossing sec-eps advance s))) (cont crossing-state next-state)) (lp next-state))))) 
```
After finding states that straddle the section plane the crossing is refined by Newton's method, as implemented by the procedure refine-crossing. The procedure find-next-crossing returns both the crossing point and the next state produced by the integrator. The next state is not used in this problem but it is needed for other cases.
```Scheme
(define (refine-crossing sec-eps advance state) (let lp ((state state)) (let ((x (ref (coordinate state) 0)) (xd (ref (momentum state) 0))) (let ((zstate (advance state (- (/ x xd))))) (if (< (abs (ref (coordinate zstate) 0)) sec-eps) zstate (lp zstate)))))) 
```
To explore the Hénon--Heiles map we use explore-map as before. The following exploration generated [figure 3.20](#figure_3.20):
```Scheme
(define win (frame -0.5 0.7 -0.6 0.6)) (explore-map win (HHmap 0.125 0.1 1.0e-10 1.0e-12) 500) 
```
#page(263)
##### 3.6.5 Non-Axisymmetric Top
We have seen that the motion of an axisymmetric top can be essentially solved. A plot of the rate of change of the tilt angle versus the tilt angle is a simple closed curve. The evolution of the other angles describing the configuration can be obtained by quadrature once the tilting motion has been solved. Now let's consider a non-axisymmetric top. A non-axisymmetric top is a top with three unequal moments of inertia. The pivot is not at the center of mass, so uniform gravity exerts a torque. We assume the line between the pivot and the center of mass is one of the principal axes, which we take to be /ĉ/. There are no torques about the vertical axis, so the vertical component of the angular momentum is conserved. If we write the Hamiltonian in terms of the Euler angles, the angle /φ/, which corresponds to rotation about the vertical, does not appear. Thus the momentum conjugate to this angle is conserved. The nontrivial degrees of freedom are /θ/ and /ψ/, with their conjugate momenta.

We can make a surface of section (see [figure 3.22](#figure_3.22)) for this problem by displaying /p_{θ}/ versus /θ/ when /ψ/ = 0. There are in general two values of /p_{ψ}/ possible for given values of energy and /p/_{φ}. We plot points only if the value of /p_{ψ}/ at the crossing is the larger of the two possibilities. This makes the points of the section correspond uniquely to a trajectory.

In this section there is a large quasiperiodic island surrounding a fixed point that corresponds to the tilted equilibrium point of the awake axisymmetric top (see [figure 3.7](#figure_3.7) in [section 3.4](#section_3.4)). Surrounding this is a large chaotic zone that extends from /θ/ = 0 to angles near /π/. If this top is placed initially near the vertical, it exhibits chaotic motion that carries it to large tilt angles. If the top is started within the quasiperiodic island, the tilt is stable.

### 3.7 Exponential Divergence
Hénon and Heiles discovered that the chaotic trajectories had remarkable sensitivity to small changes in initial conditions---initially nearby chaotic trajectories separate roughly exponentially with time. On the other hand, regular trajectories do not exhibit this sensitivity---initially nearby regular trajectories separate roughly linearly with time.

#page(264)

#Image(Art_P767.jpg,figure_3.22)
#Caption *Figure 3.22* A surface of section for the non-axisymmetric top. The parameters are /A/ = 0.0003 kg m^{2}, /B/ = 0.00025 kg m^{2}, /C/ = 0.0001 kg m^{2}, /gMR/ = 0.0456 kg m^{2} s^{−2}. The energy and /p/_{φ} are those of the top initially standing vertically with rotation frequency 30 rad s^{−1}. The angle /θ/ is on the abscissa, and the momentum /p_{θ}/ is on the ordinate. #CaptionEnd

Consider the evolution of two initially nearby trajectories for the Hénon--Heiles problem, with energy /E/ = 1/8. Let /d/(/t/) be the usual Euclidean distance in the /x/, /y/, /p_{x}/, /p_{y}/ space between the two trajectories at time /t/. [Figure 3.23](#figure_3.23) shows the common logarithm of /d/(/t/)//d/(0) as a function of time /t/. We see that the divergence is well described as exponential.

On the other hand, the distance between two initially nearby regular trajectories grows much more slowly. [Figure 3.24](#figure_3.24) shows the distance between two regular trajectories as a function of time. The distance grows linearly with time.

It is remarkable that Hamiltonian systems have such radically different types of trajectories. On the surface of section the chaotic and regular trajectories differ in the dimension of the space that they explore. It is interesting that along with this dimensional difference there is a drastic difference in the way chaotic and regular trajectories separate. For higher-dimensional systems the surface of section technique is not as useful, but trajectories are still distinguished by the way neighboring trajectories diverge: some diverge
#page(265)
exponentially whereas others diverge approximately linearly. Exponential divergence is the hallmark of chaotic behavior.

#Image(Art_P768.jpg,figure_3.23)
#Caption *Figure 3.23* The common logarithm of the phase-space distance between two chaotic trajectories divided by the initial phase-space distance as a function of time. The initial distance was 10^{−10}. The logarithm of the distance grows approximately linearly; the distance grows exponentially. The two-trajectory method saturates when the distance between trajectories becomes comparable to that allowed by conservation of energy. Also displayed is the distance between trajectories calculated by integrating the linearized variational equations. This method does not saturate. #CaptionEnd

The rate of exponential divergence is quantified by the slope of the graph of log(/d/(/t/)//d/(0)). We can estimate the rate of exponential divergence of trajectories from a particular phase-space trajectory /σ/ by choosing a nearby trajectory /σ/′ and computing

$$\begin{array}{ll} {\gamma(t) = \frac{\log(d(t)/d(t_{0}))}{t - t_{0}},} \tag{3.141} \\ \end{array}$$

where /d/(/t/) = ‖/σ/′ (/t/)−/σ/(/t/)‖. A problem with this “two-trajectory” method is illustrated in [figure 3.23](#figure_3.23). For strongly chaotic trajectories two initially nearby trajectories soon find themselves as far apart as they can get. Once this happens the distance no longer grows. The estimate of the rate of divergence of trajectories is limited by this /saturation/.

#page(266)

#Image(Art_P770.jpg,figure_3.24)
#Caption *Figure 3.24* The phase-space distance between two regular trajectories divided by the initial phase-space distance as a function of time. The initial distance was 10^{−10}. The distance grows linearly. #CaptionEnd

We can improve on this method by studying a variational system of equations. Let

$$\begin{matrix} {Dz(t) = F(t,z(t))} \tag{3.142} \\ \end{matrix}$$

be the system of equations governing the evolution of the system. A nearby trajectory /z/′ satisfies

$$\begin{matrix} {Dz\prime(t) = F(t,z\prime(t)).} \tag{3.143} \\ \end{matrix}$$

The difference /ζ/ = /z/′ − /z/ between these trajectories satisfies

$$\begin{array}{cll} {D\zeta(t)} & {= F(t,z\prime(t)) - F(t,z(t))} & \\  & {= F(t,z(t) + \zeta(t)) - F(t,z(t)).} \tag{3.144} \\ \end{array}$$

If /ζ/ is small we can approximate the right-hand side by a derivative

$$\begin{matrix} {D\zeta(t) = \partial_{1}F(t,z(t))\zeta(t).} \tag{3.145} \\ \end{matrix}$$

This set of ordinary differential equations is called the /variational equations/ for the system. It is linear in /ζ/ and driven by /z/.

#page(267)

Let /d/(/t/) = ‖/ζ/(/t/)‖; then the rate of divergence can be estimated as before. The advantage of this “variational method” is that /ζ/(/t/) can become arbitrarily large and its growth still measures the divergence of nearby trajectories. We can see in [figure 3.23](#figure_3.23) that the variational method gives nearly the same result as the two-trajectory method up to the point at which the two-trajectory method saturates.#Footnote(31)

The /Lyapunov exponent/ is defined to be the infinite time limit of /γ/(/t/), defined by equation (#Eqn(chapter003,3.141,3.141)), in which the distance /d/ is computed by the variational method. Actually, for each trajectory there are many Lyapunov exponents, depending on the initial direction of the variation /ζ/. For an /N/-dimensional system, there are /N/ Lyapunov exponents. For a randomly chosen /ζ/(/t/_{0}), the subsequent growth of /ζ/(/t/) has components that grow with each of the Lyapunov exponents. In general, however, the growth of /ζ/(/t/) will be dominated by the largest exponent. The largest Lyapunov exponent thus can be interpreted as the typical rate of exponential divergence of nearby trajectories. The sum of the largest two Lyapunov exponents can be interpreted as the typical rate of growth of the area of two-dimensional elements. This interpretation can be extended to higher-dimensional elements: the rate of growth of volume elements is the sum of all the Lyapunov exponents.

In Hamiltonian systems, the Lyapunov exponents must satisfy the following constraints. Lyapunov exponents come in pairs; for every Lyapunov exponent /λ/, its negation −/λ/ is also an exponent. For every conserved quantity, one of the Lyapunov exponents is zero, as is its negation. So the Lyapunov exponents can be used to check for the existence of conserved quantities. The sum of the Lyapunov exponents for a Hamiltonian system is zero, so volume elements do not grow exponentially. We will see in the next section that phase-space volume is actually conserved for Hamiltonian systems.

#page(268)

### 3.8 Liouville's Theorem
If an ensemble of states occupies a particular volume of phase space at one moment, then the subsequent evolution of that volume by the flow described by Hamilton's equations may distort the ensemble but does not change the volume the ensemble occupies. The fact that phase-space volume is preserved by the phase flow is called /Liouville's theorem/.

We will first illustrate the preservation of phase-space volume with a simple example and then prove it in general.

#### The phase flow for the pendulum
Consider an undriven pendulum described by the Hamiltonian

$$\begin{array}{ll} {H(t,\theta,p_{\theta}) = \frac{p_{\theta}^{2}}{2l^{2}m} + glm\,\cos\,\theta.} \tag{3.146} \\ \end{array}$$

In [figure 3.25](#figure_3.25) we see the evolution of an elliptic region around a point on the /θ/-axis, in the oscillation region of the pendulum. Three later positions of the region are shown. The region is stretched and sheared by the flow, but the area is preserved. After many cycles, the starting region will be stretched to be a thin layer distributed in the phase angle of the pendulum. [Figure 3.26](#figure_3.26) shows a similar evolution (for smaller time intervals) of a region straddling the separatrix#Footnote(32) near the unstable equilibrium point. The phase-space region rapidly stretches along the separatrix, while preserving the area. The initial conditions that start in the oscillation region (inside of the separatrix) will continue to spread into a thin ring-shaped region, while the initial conditions that start outside of the separatrix will spread into a thin region of rotation on the outside of the separatrix.

#### Proof of Liouville's theorem
Consider a set of ordinary differential equations of the form

$$\begin{matrix} {Dz(t) = F(t,z(t)),} \tag{3.147} \\ \end{matrix}$$

#page(269)

#Image(Art_P777.jpg,figure_3.25)
#Caption *Figure 3.25* A swarm of initial points outlining an area in the phase space of the pendulum deforms as it evolves, but the area contained in the contour remains constant. The horizontal axis is the angle /θ/ of the pendulum from the vertical; the vertical axis is the angular momentum /p_{θ}/. The initial contour is the “ellipse” on the horizontal axis. The pendulum has length 1 m in standard gravity (9.8 m s^{−2}), so its period is approximately 2 seconds. The flow proceeds clockwise and the deformed areas are shown at .9 seconds, 1.8 seconds, and 2.7 seconds. The successive positions exhibit “shearing” of the region because the pendulum is not isochronous. #CaptionEnd

where /z/ is a tuple of /N/ state variables. Let /R/(/t/_{1}) be a region of the state space at time /t/_{1}. Each element of this region is an initial condition at time /t/_{1} for the system, and evolves to an element at time /t/_{2} according to the differential equations. The set of these elements at time /t/_{2} is the region /R/(/t/_{2}). Regions evolve to regions.

The evolution of the system for a time interval Δ/t/ defines a map /g/_{t,Δt} from the state space to itself:

$$\begin{array}{ll} {g_{t,\Delta t}(z(t)) = z(t + \Delta t).} \tag{3.148} \\ \end{array}$$

Regions map to regions by mapping each element in the region:

$$\begin{array}{ll} {g_{t,\Delta t}(R(t)) = R(t + \Delta t).} \tag{3.149} \\ \end{array}$$

#page(270)

#Image(Art_P780.jpg,figure_3.26)
#Caption *Figure 3.26* The pendulum here is the same as in the previous figure, but now the swarm of initial points surrounds the unstable equilibrium point for the pendulum in phase space, where /θ/ = /π/ and /p_{θ}/ = 0. The swarm is stretched out along the separatrix. The time interval between successively plotted contours is 0.3 seconds. #CaptionEnd

The volume /V/ (/t/) of a region /R/(/t/) is $\int_{R(t)}\,\widehat{1}$, where $\widehat{1}$ is the function whose value is one for every input. The volume of the evolved region /R/(/t/ + Δ/t/) is

$$\begin{array}{lll} {V(t + \Delta t)} & {= {\int_{R(t + \Delta t)}\widehat{1}}} & \\  & {= {\int_{g_{t,\Delta t}(R(t))}\widehat{1}}} & \\  & {= {\int_{R(t)}{\text{Jac}(g_{t,\Delta t})}},} \tag{3.150} \\ \end{array}$$

where Jac(/g/_{t,Δt}) is the Jacobian of the mapping /g/_{t,Δt}. The Jacobian is the determinant of the derivative of the mapping.

For small Δ/t/

$$\begin{array}{ll} {g_{t,\Delta t}(z(t)) = z(t) + \Delta tF(t,z(t)) + o(\Delta t^{2}),} \tag{3.151} \\ \end{array}$$

#page(271)

and thus

$$\begin{array}{ll} {Dg_{t,\Delta t}(z(t)) = DI(z(t)) + \Delta t\partial_{1}F(t,z(t)) + o(\Delta t^{2}),} \tag{3.152} \\ \end{array}$$

where /I/ is the identity function, so /DI/(/z/(/t/)) is a unit multiplier. We can use the fact that if *A* is an /N/ × /N/ square matrix then

$$\begin{array}{ll} {\det(\mathbf{1} + \mathit{\epsilon}\mathbf{A}) = 1 + \mathit{\epsilon}\,\text{trace}\,\mathbf{A} + o(\mathit{\epsilon}^{2})} \tag{3.153} \\ \end{array}$$

to show that

$$\begin{array}{ll} {\text{Jac}(g_{t,\Delta t})(z) = 1 + \Delta tG_{t}(z) + o(\Delta t^{2}),} \tag{3.154} \\ \end{array}$$

where

$$\begin{array}{ll} {G_{t}(z) = \text{trace}\,(\partial_{1}F(t,z)).} \tag{3.155} \\ \end{array}$$

Thus

$$\begin{array}{lll} {V(t + \Delta t)} & {= {\int_{R(t)}{\lbrack\widehat{1} + \Delta tG_{t} + o(\Delta t^{2})\rbrack}}} & \\  & {= V(t) + \Delta t{\int_{R(t)}{G_{t} + o(\Delta t^{2}).}}} \tag{3.156} \\ \end{array}$$

So the rate of change of the volume at time /t/ is

$$\begin{array}{ll} {DV(t) = {\int_{R(t)}{G_{t}.}}} \tag{3.157} \\ \end{array}$$

Now we compute /G_{t}/ for a system described by a Hamiltonian /H/. The components of /z/ are the components of the coordinates and the momenta: /z^{k}/ = /q^{k}/ and /z/^{k+n} = /p_{k}/ for /k/ = 0, ..., /n/ − 1. The components of /F/ are

$$\begin{array}{rll} {F^{k}(t,z)} & {= {(\partial_{2}H)}^{k}(t,q,p)} & \\ {F^{k + n}(t,z)} & {= - {(\partial_{1}H)}_{k}(t,q,p),} \tag{3.158} \\ \end{array}$$

for /k/ = 0, ..., /n/ − 1. The diagonal components of the derivative ∂_{1}/F/ are

$$\begin{array}{rll} {{(\partial_{1})}_{k}F^{k}(t,z)} & {= {(\partial_{1})}_{k}{(\partial_{2})}^{k}H(t,q,p)} & \\ {{(\partial_{1})}_{k + n}F^{k + n}(t,z)} & {= - {(\partial_{2})}^{k}{(\partial_{1})}_{k}H(t,q,p).} \tag{3.159} \\ \end{array}$$

#page(272)

The component partial derivatives commute, so the diagonal components with index /k/ and index /k/ + /n/ are equal and opposite. We see that the trace, which is the sum of these diagonal components, is zero. Thus the integral of /G_{t}/ over the region /R/(/t/) is zero, so the derivative of the volume at time /t/ is zero. Because /t/ is arbitrary, the volume does not change. This proves /Liouville's theorem/: the phase-space flow conserves phase-space volume.

Notice that the proof of Liouville's theorem does not depend upon whether or not the Hamiltonian has explicit time dependence. Liouville's theorem holds for systems with time-dependent Hamiltonians.

We may think of the ensemble of all possible states as a fluid flowing around under the control of the dynamics. Liouville's theorem says that this fluid is incompressible for Hamiltonian systems.

### Exercise 3.11: Determinants and traces

Show that equation (#Eqn(chapter003,3.153,3.153)) is correct.

#### Area preservation of stroboscopic surfaces of section
Surfaces of section for periodically driven Hamiltonian systems are area preserving if the section coordinates are the phase-space coordinate and momentum. This is an important feature of surfaces of section. It is a consequence of Liouville's theorem for one-degree-of-freedom problems.

It is also the case that surfaces of section such as those we have used for the Hénon--Heiles problem are area preserving, but we are not ready to prove this yet!

#### Poincaré recurrence
The /Poincaré recurrence theorem/ is a remarkable theorem that is a trivial consequence of Liouville's theorem. Loosely, the theorem states that almost all trajectories eventually return arbitrarily close to where they started. This is true regardless of whether the trajectories are chaotic or regular.

More precisely, consider a Hamiltonian dynamical system for which the phase space is a bounded domain /D/. We identify some initial point in the phase space, say /z/_{0}. Then, for any finite neighborhood /U/ of /z/_{0} we choose, there are trajectories that emanate from initial points in that neighborhood and eventually return to the neighborhood.

#page(273)

We can prove this by considering the successive images of /U/ under the time evolution. For simplicity, we restrict consideration to time evolution for a time interval Δ. The map of the phase space onto itself generated by time evolution for an interval Δ we call /C/. Subsequent applications of the map generate a discrete time evolution. Sets of points in phase space transform by evolving all the points in the set; the image of the set /U/ is denoted /C/(/U/). Now consider the trajectory of the set /U/, that is, the sets /C^{n}/(/U/) where /C^{n}/ indicates the /n/-times composition of /C/. Now there are two possibilities: either the successive images /C^{i}/(/U/) intersect or they do not. If they do not intersect, then with each iteration, a volume of /D/ equal to the volume of /U/ gets “used up” and cannot belong to the further image. But the volume of /D/ is finite, so we cannot fit an infinite number of non-intersecting finite volumes into it. Therefore, after some number of iterations the images intersect. Suppose /C^{i}/(/U/) intersects with /C^{j}/(/U/), with /j < i/, for definiteness. Then the pre-image of each must also intersect, since the pre-image of a point in the intersection belongs to both sets. Thus /C/^{i−1}(/U/) intersects /C/^{j−1}(/U/). This can be continued until finally we have that /C/^{i−j}(/U/) intersects /U/. So we have proven that after /i/ − /j/ iterations of the map /C/ there are a set of points initially in /U/ that return to the neighborhood /U/.

So for every neighborhood of every point in the phase space there is a subneighborhood such that the trajectories emanating from all of the points in that subneighborhood return to that subneighborhood. Thus almost every trajectory returns arbitrarily close to where it started.

#### The gas in the corner of the room
Suppose we have a collection of /N/ classical atoms in a perfectly sealed room. The phase-space dimension of this system is 6/N/. A point in this phase space is denoted /z/. Suppose that initially all the atoms are, say, within one centimeter of one corner, with arbitrarily chosen finite velocities. This corresponds to some initial point /z/_{0} in the phase space. The phase space of the system is limited in space by the room and in momentum by energy conservation; the phase space is bounded. The recurrence theorem then says that in the neighborhood of /z/_{0} there is an initial condition of the system that returns to the neighborhood of /z/_{0} after some time. For the individual atoms this means that after some time
#page(274)
all of the atoms will be found in the corner of the room again, and again, and again. Makes one wonder about the second law of thermodynamics, doesn't it?#Footnote(33)

#### Nonexistence of attractors in Hamiltonian systems
Some systems have attractors. An /attractor/ is a region of phase space that gobbles volumes of trajectories. For an attractor there is some larger region, the basin of attraction, such that sets of trajectories with nonzero volume eventually end up in the attractor and never leave it. The recurrence theorem shows that Hamiltonian systems with bounded phase space do not have attractors. Consider some candidate volume in the proposed basin of attraction. The recurrence theorem guarantees that some trajectories in the candidate volume return to the volume repeatedly. Therefore, the volume is not in a basin of attraction. Attractors do not exist in Hamiltonian systems with bounded phase space.

This does not mean that every trajectory always returns. A simple example is the pendulum. Suppose we take a blob of trajectories that spans the separatrix, the trajectory that asymptotically approaches the unstable equilibrium with the pendulum pointed up. Trajectories with more energy than the separatrix make a full loop around and return to their initial point; trajectories with lower energy than the separatrix oscillate once across and back to their initial position; but the separatrix trajectory itself leaves the initial region permanently, and continually approaches the unstable point.

#### Conservation of phase volume in a dissipative system
The definition of a dissipative system is not so clear. For some, “dissipative” implies that phase-space volume is not conserved, which is the same as saying the evolution of the system is not governed by Hamilton's equations. For others, “dissipative” implies that friction is present, representing loss of energy to unmodeled degrees of freedom. Here is a curious example. The damped harmonic oscillator is the paradigm of a dissipative system. Here we show that the damped harmonic oscillator can be described by Hamilton's equations and that phase-space volume is conserved.

#page(275)

The damped harmonic oscillator is governed by the ordinary differential equation

$$\begin{array}{ll} {mD^{2}x + \alpha Dx + kx = 0} \tag{3.160} \\ \end{array}$$

where /α/ is a coefficient of damping. We can formulate this system with the Lagrangian#Footnote(34)

$$\begin{array}{ll} {L(t,x,\dot{x}) = (\frac{m}{2}{\dot{x}}^{2} - \frac{k}{2}x^{2})e^{\frac{\alpha}{m}t}.} \tag{3.161} \\ \end{array}$$

The Lagrange equation for this Lagrangian is

$$\begin{array}{ll} {(mD^{2}x(t) + \alpha Dx(t) + kx(t))e^{\frac{\alpha}{m}t} = 0.} \tag{3.162} \\ \end{array}$$

Since the exponential is never zero this equation has the same trajectories as equation (#Eqn(chapter003,3.160,3.160)) above.

The momentum conjugate to /x/ is

$$\begin{array}{ll} {p = m\dot{x}e^{\frac{\alpha}{m}t},} \tag{3.163} \\ \end{array}$$

and the Hamiltonian is

$$\begin{array}{ll} {H(t,x,p) = (\frac{1}{2m}p^{2})e^{- \frac{\alpha}{m}t} + (\frac{k}{2}x^{2})e^{\frac{\alpha}{m}t}.} \tag{3.164} \\ \end{array}$$

For this system, the Hamiltonian is not the sum of the kinetic energy of the motion of the mass and the potential energy stored in the spring. The value of the Hamiltonian is not conserved (∂_{0}/H/ ≠ 0). Hamilton's equations are

$$\begin{array}{ll} {Dx(t) = \frac{p(t)}{m}e^{- \frac{\alpha}{m}t}} & \\ {Dp(t) = - kx(t)e^{\frac{\alpha}{m}t}.} \tag{3.165} \\ \end{array}$$

Let's consider a numerical case. Let /m/ = 5, /k/ = 1/4, /α/ = 3. Here the characteristic roots of the linear constant-coefficient ordinary differential equation (#Eqn(chapter003,3.160,3.160)) are /s/ = −1/10, −1/2. Thus the solutions are

$$\begin{array}{ll} {\left( \begin{array}{l} {x(t)} \\ {p(t)} \\ \end{array} \right) = \left( \begin{array}{ll} e^{- \frac{1}{10}t} & e^{- \frac{1}{2}t} \\ {- \frac{1}{2}e^{+ \frac{1}{2}t}} & {- \frac{5}{2}e^{+ \frac{1}{10}t}} \\ \end{array} \right)\left( \begin{array}{l} A_{1} \\ A_{2} \\ \end{array} \right),} \tag{3.166} \\ \end{array}$$

#page(276)

for /A/_{1} and /A/_{2} determined by the initial conditions

$$\begin{array}{ll} {\left( \begin{array}{l} {x(0)} \\ {p(0)} \\ \end{array} \right) = \left( \begin{array}{ll} 1 & 1 \\ {- \frac{1}{2}} & {- \frac{5}{2}} \\ \end{array} \right)\left( \begin{array}{l} A_{1} \\ A_{2} \\ \end{array} \right).} \tag{3.167} \\ \end{array}$$

Thus we can form the transformation from the initial state to the final state:

$$\begin{array}{ll} {\left( \begin{array}{l} {x(t)} \\ {p(t)} \\ \end{array} \right) = \left( \begin{array}{ll} e^{- \frac{1}{10}t} & e^{- \frac{1}{2}t} \\ {- \frac{1}{2}e^{+ \frac{1}{2}t}} & {- \frac{5}{2}e^{+ \frac{1}{10}t}} \\ \end{array} \right)\left( \begin{array}{ll} 1 & 1 \\ {- \frac{1}{2}} & {- \frac{5}{2}} \\ \end{array} \right)^{- 1}\left( \begin{array}{l} {x(0)} \\ {p(0)} \\ \end{array} \right).} \tag{3.168} \\ \end{array}$$

The transformation is linear, so the area is transformed by the determinant, which is 1 in this case. Thus, contrary to intuition, the phase-space volume is conserved. So why is this not a contradiction with the statement that there are no attractors in Hamiltonian systems? The answer is that the Poincaré recurrence argument is true only for bounded phase spaces. Here, the momentum expands exponentially with time (as the coordinate contracts), so it is unbounded.

We shouldn't really be too surprised by the way the theory protects itself from an apparent paradox---that the phase volume is conserved even though all trajectories decay to zero velocity and coordinates. The proof of Liouville's theorem allows time-dependent Hamiltonians. In this case we are able to model the dissipation by just such a time-dependent Hamiltonian.

### Exercise 3.12: Time-dependent systems

To make the fact that Liouville's theorem holds for time-dependent systems even more concrete, extend the results of [section 3.8](#section_3.8) to show how a swarm of initial points outlining an area in the phase space of the /driven/ pendulum deforms as it evolves. Construct pictures analogous to [figures 3.25](#figure_3.25) and [3.26](#figure_3.26) for one of the interesting cases where we have surfaces of section. Does the distortion look different in different parts of the phase space? How?

#### Distribution functions
We know the state of a system only approximately. It is reasonable to model our state of knowledge by a probability density function on the set of possible states. Given such incomplete knowledge, what are the probable consequences? As the system evolves, the density function also evolves. Liouville's theorem gives us a handle on this kind of problem.

#page(277)

Let /f/(/t/, /q/, /p/) be a probability density function on the phase space at time /t/. For this to be a good probability density function we require that the integral of /f/ over all coordinates and momenta be 1---it is certain that the system is somewhere.

There is a set of trajectories that pass through any particular region of phase space at a particular time. These trajectories are neither created nor destroyed, and they proceed as a bundle to another region of phase space at a later time. Liouville's theorem tells us that the volume of the source region is the same as the volume of the target region, so the density must remain constant. Thus /D/(/f/ ∘ /σ/) = 0. If we have a system described by the Hamiltonian /H/ then

$$\begin{matrix} {D(f \circ \sigma) = \partial_{0}f \circ \sigma + \left\{ f,H \right\} \circ \sigma,} \tag{3.169} \\ \end{matrix}$$

so we may conclude that

$$\begin{matrix} {\partial_{0}f \circ \sigma + \left\{ f,H \right\} \circ \sigma = 0,} \tag{3.170} \\ \end{matrix}$$

or

$$\begin{matrix} {(\partial_{0}f + \left\{ f,H \right\}) \circ \sigma = 0.} \tag{3.171} \\ \end{matrix}$$

Since this must be true at each moment and since there is a solution trajectory that emanates from every point in phase space, we may abstract from solution paths and deduce a constraint on /f/:

$$\begin{matrix} {\partial_{0}f + \left\{ f,H \right\} = 0.} \tag{3.172} \\ \end{matrix}$$

This linear partial differential equation governs the evolution of the density function, and thus shows how our state of knowledge evolves.

### 3.9 Standard Map
We have seen that the surfaces of section for a number of different problems are qualitatively very similar. They all show two qualitatively different types of motion: regular motion and chaotic motion. They show that these types of orbits are clustered: there are regions of the surface of section that have mostly regular trajectories and other regions dominated by chaotic behavior. We have also seen a transition to large-scale chaotic behavior as some
#page(278)
parameter is varied. Now we have learned that the map that takes points on a two-dimensional surface of section to new points on the surface of section is area preserving. The sole property that these maps of the section onto itself have in common (that we know of at this point) is that they preserve area. Otherwise they are quite distinct. Suppose we consider an abstract map of the section onto itself that is area preserving, without regard for whether the map is generated by some dynamical system. Do area-preserving maps typically show similar phenomena, or is the dynamical origin of the map crucial to the phenomena we have found?#Footnote(35)

Consider a map of the phase plane onto itself defined in terms of the dynamical variables /θ/ and its “conjugate momentum” /I/. The map is

$$\begin{matrix} {I\prime = (I + K\,\sin\,\theta)\,{mod}\, 2\pi} \tag{3.173} \\ \end{matrix}$$

$$\begin{matrix} {\theta\prime = (\theta + I\prime)\,{mod}\, 2\pi.} \tag{3.174} \\ \end{matrix}$$

This map is known as the “standard map.”#Footnote(36) A curious feature of the standard map is that the momentum variable /I/ is treated as an angular quantity. The derivative of the map has determinant one, implying the map is area preserving.

We can implement the standard map:
```Scheme
(define ((standard-map K) theta I return failure) (let ((nI (+ I (* K (sin theta))))) (return ((principal-value :2pi) (+ theta nI)) ((principal-value :2pi) nI)))) 
```
We use the explore-map procedure introduced earlier to use a pointing device to interactively explore the surface of section. For example, to explore the surface of section for parameter /K/ = 0.6 we use:

#page(279)

#Image(Art_P808.jpg,figure_3.27)
#Caption *Figure 3.27* Surface of section for the standard map for /K/ = 0.6. The section shows mostly regular trajectories, with a few dominant islands, but also a number of small chaotic zones. #CaptionEnd
```Scheme
(define window (frame 0.0 :2pi 0.0 :2pi)) (explore-map window (standard-map 0.6) 2000) 
```
The resulting surface of section, for a variety of orbits chosen with the pointer, is shown in [figure 3.27](#figure_3.27). The surface of section does indeed look qualitatively similar to the surfaces of section generated by dynamical systems.

The surface of section for /K/ = 1.4 (as shown in [figure 3.28](#figure_3.28)) is dominated by a large chaotic zone. The standard map exhibits a transition to large-scale chaos near /K/ = 1. So this abstract area-preserving map of the phase plane onto itself shows behavior that is similar to behavior in the sections generated by a Hamiltonian dynamical system. Evidently, the area-preservation property of the dynamics in the phase space plays a determining role for many interesting properties of trajectories of mechanical systems.

#page(280)

#Image(Art_P809.jpg,figure_3.28)
#Caption *Figure 3.28* Surface of section for the standard map for /K/ = 1.4. The dominant feature is a large chaotic zone. There are also some large islands of regular behavior. In this case there are also some interesting secondary islands---islands around islands. #CaptionEnd

### Exercise 3.13: Fun with Hénon's quadratic map

Consider the map of the plane defined by the equations:

/x/′ = /x/ cos /α/ − (/y/ − /x/^{2}) sin /α/

/y/′ = /x/ sin /α/ + (/y/ − /x/^{2}) cos /α/

*a.* Show that the map preserves area.

*b.* Implement the map as a procedure. The interesting range of /x/ and /y/ is (−1, 1). There will be orbits that escape. You should check for values of /x/ and /y/ that escape from this range and call the failure continuation when this occurs.

*c.* Explore the phase portrait of this map for a few values of the parameter /α/. The map is particularly interesting for /α/ = 1.32 and /α/ = 1.2. What happens in between?

#page(281)

### 3.10 Summary
Lagrange's equations are a system of /n/ second-order ordinary differential equations in the time, the generalized coordinates, the generalized velocities, and the generalized accelerations. Trajectories are determined by the coordinates and the velocities at a moment.

Hamilton's equations specify the dynamics as a system of first-order ordinary differential equations in the time, the generalized coordinates, and the conjugate momenta. Phase-space trajectories are determined by an initial point in phase space at a moment.

The Hamiltonian formulation and the Lagrangian formulation are equivalent in that equivalent initial conditions produce the same configuration path.

If there is a symmetry of the problem that is naturally expressed as a cyclic coordinate, then the conjugate momentum is conserved. In the Hamiltonian formulation, such a symmetry naturally results in the reduction of the dimension of the phase space of the difficult part of the problem. If there are enough symmetries, then the problem of determining the time evolution may be reduced to evaluation of definite integrals (reduced to quadratures).

Systems without enough symmetries to be reducible to quadratures may be effectively studied with the surface of section technique. This is particularly advantageous in systems for which the reduced problem has two degrees of freedom or has one degree of freedom with explicit periodic time dependence.

Surfaces of section reveal tremendous structure in the phase space. There are chaotic zones and islands of regular behavior. There are interesting transitions as parameters are varied between mostly regular motion and mostly chaotic motion.

Chaotic trajectories exhibit sensitive dependence on initial conditions, separating exponentially from nearby trajectories. Regular trajectories do not show such sensitivity. Curiously, chaotic trajectories are distinguished both by the dimension of the space they explore and by their exponential divergence.

The time evolution of a 2/n/-dimensional region in phase space preserves the volume. Hamiltonian flow is “incompressible” flow of the “phase fluid.”

#page(282)

Surfaces of section for two-degree-of-freedom systems and for periodically driven one-degree-of-freedom systems are area preserving. Abstract area-preserving maps of a phase plane onto itself show the same division of the phase space into chaotic and regular regions as surfaces of section generated by dynamical systems. They also show transitions to large-scale chaos.

### 3.11 Projects
### Exercise 3.14: Periodically driven pendulum

Explore the dynamics of the driven pendulum, using the surface of section method. We are interested in exploring the regions of parameter space over which various phenomena occur. Consider a pendulum of length 9.8 m, mass 1 kg, and acceleration of gravity /g/ = 9.8 m s^{−2}, giving /ω/_{0} = 1 rad s^{−1}. Explore the parameter plane of the amplitude /A/ and frequency /ω/ of the periodic drive.

Examples of the phenomena to be investigated:

*a.* Inverted equilibrium. Show the region of parameter space (/A, ω/) in which the inverted equilibrium is stable. If the inverted equilibrium is stable there is some range of stability, i.e., there is a maximum angle of displacement from the equilibrium that stable oscillations reach. If you have enough time, plot contours in the parameter space for different amplitudes of the stable region.

*b.* Period doubling of the normal equilibrium. For this case, plot the angular momenta of the stable and unstable equilibria as functions of the frequency for some given amplitude.

*c.* Transition to large-scale chaos. Show the region of parameter space (/A/, /ω/) for which the chaotic zones around the three principal resonance islands are linked.

### Exercise 3.15: Spin-orbit surfaces of section

Write a program to compute surfaces of section for the spin-orbit problem, with the section points being recorded at pericenter. Investigate the following:

*a.* Give a Hamiltonian formulation of the spin-orbit problem introduced in [section 2.11.2](chapter002!section_2.11.2).

*b.* For out-of-roundness parameter /ϵ/ = 0.1 and eccentricity /e/ = 0.1, measure the widths, in momentum, of the regular islands associated with the 1:1, 3:2, and 1:2 resonances.

*c.* Explore the surfaces of section for a range of /ϵ/ for fixed /e/ = 0.1. Estimate the critical value of /ϵ/ above which the main chaotic zones around the 3:2 and the 1:1 resonance islands are merged.

#page(283)

*d.* For a fixed eccentricity /e/ = 0.1 trace the location on the surface of section of the stable and unstable fixed points associated with the 1:1 resonance as a function of the out-of-roundness /ϵ/.

### Exercise 3.16: Restricted three-body problem

Investigate the dynamics of the restricted three-body problem for the equal mass case where /M/_{0} = /M/_{1}.

*a.* Derive the Hamiltonian for the restricted three-body problem, starting with Lagrangian (#Eqn(chapter001,1.150,1.150)).

*b.* The Jacobi constant, equation (#Eqn(chapter001,1.151,1.151)), is the sum of a positive definite quadratic term in the velocities and a potential energy term, equation (#Eqn(chapter001,1.152,1.152)), so the boundaries of the allowed motion are contours of the potential energy function. Write a program to display these boundaries for a given value of the Jacobi constant. Where is motion allowed relative to these contours? (Note that for some values of the Jacobi constant there is more than one allowed region of motion.)

*c.* Evolve some trajectories for a Jacobi constant of /ℰ/ = −1.75 (/C_{J}/ = 3.5). Display the trajectories on the same plot as the boundaries of allowed motion.

*d.* Write a program to compute surfaces of section for the restricted three-body problem. This program is similar to the Hénon-Heiles program starting on [page 261](chapter003!p261). Plot section points when the trajectory crosses the /y_{r}/ = 0 axis with /ẏ_{r}/ positive; plot /ẋ_{r}/ versus /x_{r}/. Note that /p_{x}/ = /mẋ_{r}/ − /m/Ω/y_{r}/, but on this section /y_{r}/ = 0, so the velocity is proportional to the momentum, and thus the section is area preserving. Plot the boundaries of the allowed motion on the surface of section for the Jacobi constant suggested above. Explore the section and plot typical orbits for each major region in the section.

----

#FootnoteRef(1)Here we restrict our attention to Lagrangians that depend only on the time, the coordinates, and the velocities.

#FootnoteRef(2)Here we are using mnemonic names /t/, /q/, /p/ for formal parameters of the function being defined. We could have used names like /a/, /b/, /c/ as above, but this would have made the argument harder to read.

#FootnoteRef(3)/P/ = /I/_{2}. See equations (#Eqn(chapter009,9.7,9.7)) in the appendix on notation.

#FootnoteRef(4)The overall minus sign in the definition of the Hamiltonian is traditional.

#FootnoteRef(5)In traditional notation, Hamilton's equations are written as a separate equation for each component:$\begin{array}{lll} {\frac{dq^{i}}{dt} = \frac{\partial H}{\partial p_{i}}} & \text{and} & {\frac{dp_{i}}{dt} = - \frac{\partial H}{\partial q^{i}}.} \\ \end{array}$

#FootnoteRef(6)Traditionally, the Hamiltonian is written $ H = p\dot{q} - L.$ This way of writing the Hamiltonian confuses the values of functions with the functions that generate them: both $\dot{q}$ and /L/ must be reexpressed as functions of time, coordinates, and momenta.

#FootnoteRef(7)In the construction of the Lagrangian state derivative from the Lagrange equations we must solve for the highest-order derivative. The solution process requires the inversion of ∂_{2}∂_{2}/L/. In the construction of Hamilton's equations, the construction of $\mathcal{V}$ from the momentum state function ∂_{2}/L/ requires the inverse of the same structure. If the Lagrangian formulation has singularities, they cannot be avoided by going to the Hamiltonian formulation.

#FootnoteRef(8)The term /phase space/ was introduced by Josiah Willard Gibbs in his formulation of statistical mechanics. The Hamiltonian plays a fundamental role in the Boltzmann--Gibbs formulation of statistical mechanics and in both the Heisenberg and Schrödinger approaches to quantum mechanics.

#FootnoteRef(9)The Legendre transformation is more general than its use in mechanics in that it captures the relationship between conjugate variables in systems as diverse as thermodynamics, circuits, and field theory.

#FootnoteRef(10)This can be done so long as the derivative is not zero.

#FootnoteRef(11)Equation (#Eqn(chapter003,3.28,3.28)) looks like an application of the product rule for derivatives,$ D\left( {I\mathcal{V}} \right) = DI\mathcal{V} + ID\mathcal{V}$. Although this works for real-valued functions, it is inadequate for functions with structured outputs. The result $ D\left( {I\mathcal{V}} \right) = \mathcal{V} + ID\mathcal{V}$ is correct, but to verify it the computation must be done after the structures are multiplied out. See [[chapter009!p522][page 522]].

#FootnoteRef(12)If *M* is the matrix representation of /M/, then *M* = *M*^{T}.

#FootnoteRef(13)The procedure solve-linear-left was introduced in footnote [75](chapter001!endnote_75) on [page 71](chapter001!p71).

#FootnoteRef(14)The function Π[/q/] is the same as Π/_{L}/[/q/] introduced on [page 203](chapter003!p203). Indeed, the Lagrangian is needed to define momentum in every case, but we are suppressing the dependency here because it does not matter in this argument.

#FootnoteRef(15)The variation of the momentum $\delta\widetilde{p}\left\lbrack q \right\rbrack $ need not be further expanded in this argument because it turns out that the factor multiplying it is zero. However, it is handy to see how it is related to the variations in the coordinate path /δq/:$\delta p = \delta\widetilde{p}\left\lbrack q \right\rbrack\left( t \right) = \partial_{1}\partial_{2}L\left( {t,q\left( t \right),Dq\left( t \right)} \right)\delta q\left( t \right) + \partial_{2}\partial_{2}L\left( {t,q\left( t \right),Dq\left( t \right)} \right)D\delta q\left( t \right).$

#FootnoteRef(16)It is sometimes asserted that the momenta have a different status in the Lagrangian and Hamiltonian formulations: that in the Hamiltonian framework the momenta are “independent” of the coordinates. From this it is argued that the variations /δq/ and /δp/ are arbitrary and independent, therefore implying that the factor multiplying each of them in the action integral (#Eqn(chapter003,3.75,3.75)) must independently be zero, apparently deriving both of Hamilton's equations. The argument is fallacious: we can write /δp/ in terms of /δq/ (see footnote [15](#endnote_15)).

#FootnoteRef(17)In traditional notation the Poisson bracket is written $\left\{ F,H \right\} = {\sum\limits_{i}{\left( {\frac{\partial F}{\partial q^{i}}\frac{\partial H}{\partial p_{i}} - \frac{\partial F}{\partial p_{i}}\frac{\partial H}{\partial q^{i}}} \right).}}$

#FootnoteRef(18)For systems with kinetic energy that is quadratic in velocity, this equation does not satisfy the Lipschitz condition at isolated points where the velocity is zero. However the solution for /q/ can be extracted using a definite integral.

#FootnoteRef(19)The pendulum has only one unstable equilibrium. Remember that the coordinate is an angle.

#FootnoteRef(20)If a Lagrangian does not depend on a particular coordinate then neither does the corresponding Hamiltonian, because the coordinate is a passive variable in the Legendre transform. Such a Hamiltonian is said to be cyclic in that coordinate.

#FootnoteRef(21)Traditionally, when a problem has been reduced to the evaluation of a definite integral it is said to be reduced to a “quadrature.” Thus, the determination of the evolution of a cyclic coordinate /q^{i}/ is reduced to a problem of quadrature.

#FootnoteRef(22)It is not always possible to choose a set of generalized coordinates in which all symmetries are simultaneously manifest. For these systems, the reduction of the phase space is more complicated. We have already encountered such a problem: the motion of a free rigid body. The system is invariant under rotation about any axis, yet no single coordinate system can reflect this symmetry. Nevertheless, we have already found that the dynamics is described by a system of lower dimension than the full phase space: the Euler equations.

#FootnoteRef(23)The surface of section technique was introduced by Poincaré in his /Méthodes Nouvelles de la Mécanique Céleste/ [35](bibliography!bib_35). Poincaré proved remarkable results about dynamical systems using the surface of section technique, and we shall return to some of these later. The surface of section technique is a key tool in the modern study of dynamical systems, for both analytical and numerical investigations.

#FootnoteRef(24)That solutions of ordinary differential equations can show exponential sensitivity to initial conditions was independently discovered by Edward Lorenz [31](bibliography!bib_31) in the context of a simplified model of convection in the Earth's atmosphere. Lorenz coined the picturesque term “butterfly effect” to describe this sensitivity: his weather system model is so sensitive to initial conditions that “the flapping of a butterfly's wings in Brazil can change the course of a typhoon in Japan.”

#FootnoteRef(25)We saw an example of this extreme sensitivity to initial conditions in [figure 1.7](#figure_1.7) ([section 1.7](chapter001!section_1.7)) and also in the double-pendulum project ([[chapter001!exercise_1.44][exercise 1.44]]).

#FootnoteRef(26)One-dimensional invariant sets with an infinite number of holes were discovered by John Mather. They are sometimes called /cantori/ (singular /cantorus/), by analogy to the Cantor sets, but it really doesn't Mather.

#FootnoteRef(27)In the particular case of the driven pendulum there is no reason to call fail. This contingency is reserved for systems where orbits escape or cease to satisfy some constraint.

#FootnoteRef(28)We will see that it is convenient to look at distribution functions in the phase-space coordinates because the consequences of conserved momenta are more apparent, and also because volume in phase space is conserved by evolution (see [section 3.8](#section_3.8)).

#FootnoteRef(29)A system is ergodic if time averages along trajectories are the same as phase-space averages over the region explored by the trajectories.

#FootnoteRef(30)As before, upon close examination we may find that trajectories that appear to be confined to a curve on the section are chaotic trajectories that explore a highly confined region. It is known, however, that some trajectories really are confined to curves on the section. Trajectories that start on these curves remain on these curves forever, and they fill these curves densely. These invariant curves are preserved by the dynamical evolution. There are also invariant subsets of curves with an infinite number of holes.

#FootnoteRef(31)In strongly chaotic systems /ζ/(/t/) may become so large that the computer can no longer represent it. To prevent this we can replace /ζ/ by /ζ///c/ whenever /ζ/(/t/) becomes uncomfortably large. The equation governing /ζ/ is linear, so except for the scale change, the evolution is unchanged. Of course we have to keep track of these scale changes when computing the average growth rate. This process is called “renormalization” to make it sound impressive.

#FootnoteRef(32)The separatrix is the curve that separates the oscillating motion from the circulating motion. It is made up of several trajectories that are asymptotic to the unstable equilibrium.

#FootnoteRef(33)It is reported that when Boltzmann was confronted with this problem he responded, “You should wait that long!”

#FootnoteRef(34)This is just the product of the Lagrangian for the undamped harmonic oscillator with an increasing exponential of time.

#FootnoteRef(35)This question was also addressed in the remarkable paper by Hénon and Heiles, but with a different map from what we use here.

#FootnoteRef(36)The standard map has been extensively studied. Early investigations were by Chirikov [12](bibliography!bib_12) and by Taylor [44](bibliography!bib_44), so the map is sometimes called the Chirikov--Taylor map. Chirikov coined the term “standard map,” which we adopt.
#FootnoteEnd

#page(284) 
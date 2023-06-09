!!Polyglot
## Canonical Evolution
### Chapter 6
#page(411)
#Quote(What, then, is time? I know well enough what it is, provided that   nobody asks me; but if I am asked what it is and try to explain, I am   baffled. All the same I can confidently say that I know that if   nothing passed, there would be no past time; if nothing were going to   happen, there would be no future time; and if nothing /were/ there   would be no present time.)
#Caption Augustine of Hippo, from /Confessions/, Book XI, Section 14. Translation by R.S. Pine-Coffin, 1961. #CaptionEnd

Time evolution generates a canonical transformation: if we consider all possible initial states of a Hamiltonian system and follow all the trajectories for the same time interval, then the map from the initial state to the final state of each trajectory is a canonical transformation. Hamilton--Jacobi theory gives a mixed-variable generating function that generates this time-evolution transformation. For the few integrable systems for which we can solve the Hamilton--Jacobi equation this transformation gets us action-angle coordinates, which form a starting point to study perturbations.

### 6.1 Hamilton--Jacobi Equation
If we could find a canonical transformation so that the transformed Hamiltonian was identically zero, then by Hamilton's equations the new coordinates and momenta would be constants. All of the time variation of the solution would be captured in the canonical transformation, and there would be nothing more to the solution. A mixed-variable generating function that does this job satisfies a partial differential equation called the Hamilton--Jacobi equation. In most cases, a Hamilton--Jacobi equation cannot be solved explicitly. When it can be solved, however, a Hamilton--Jacobi
#page(412)
equation provides a means of reducing a problem to a useful simple form.

Recall the relations satisfied by an /F/_{2}-type generating function:

$$\begin{matrix} {q\prime = \partial_{2}F_{2}\left( {t,q,p\prime} \right)} \tag{6.1} \\ \end{matrix}$$

$$\begin{matrix} {p = \partial_{1}F_{2}\left( {t,q,p\prime} \right)} \tag{6.2} \\ \end{matrix}$$

$$\begin{matrix} {H\prime\left( {t,q\prime,p\prime} \right) = H\left( {t,q,p} \right) + \partial_{0}F_{2}\left( {t,q,p\prime} \right).} \tag{6.3} \\ \end{matrix}$$

If we require the new Hamiltonian to be zero, then /F/_{2} must satisfy the equation

$$\begin{matrix} {0 = H\left( {t,q,\,\partial_{1}F_{2}\left( {t,q,p\prime} \right)} \right) + \partial_{0}F_{2}\left( {t,q,p\prime} \right).} \tag{6.4} \\ \end{matrix}$$

So the solution of the problem is “reduced” to the problem of solving an /n/-dimensional partial differential equation for /F/_{2} with unspecified new (constant) momenta /p/′. This is a Hamilton--Jacobi equation, and in some cases we can solve it.

We can also attempt a somewhat less drastic method of solution. Rather than try to find an /F/_{2} that makes the new Hamiltonian identically zero, we can seek an /F/_{2}-shaped function /W/ that gives a new Hamiltonian that is solely a function of the new momenta. A system described by this form of Hamiltonian is also easy to solve. So if we set

$$\begin{array}{lll} {H''\left( {t,q'',p''} \right)} & {= H\left( {t,q,\partial_{1}W\left( {t,q,p''} \right)} \right) + \partial_{0}W\left( {t,q,p''} \right)} & \\  & {= E\left( p'' \right)} \tag{6.5} \\ \end{array}$$

and are able to solve for /W/, then the problem is essentially solved. In this case, the primed momenta are all constant and the primed positions are linear in time. This is an alternate form of the Hamilton--Jacobi equation.

These forms are related. Suppose that we have a /W/ that satisfies the second form of the Hamilton--Jacobi equation (#Eqn(chapter006,6.5,6.5)). Then the /F/_{2} constructed from /W/

$$\begin{matrix} {F_{2}\left( {t,q,p\prime} \right) = W\left( {t,q,p\prime} \right) - E\left( p\prime \right)t} \tag{6.6} \\ \end{matrix}$$

satisfies the first form of the Hamilton--Jacobi equation (#Eqn(chapter006,6.4,6.4)). Furthermore,

$$\begin{matrix} {p = \partial_{1}F_{2}\left( {t,q,p\prime} \right) = \partial_{1}W\left( {t,q,p\prime} \right),} \tag{6.7} \\ \end{matrix}$$

#page(413)

so the primed momenta are the same in the two formulations. But

$$\begin{array}{lll} {q\prime} & {= \partial_{2}F_{2}\left( {t,q,p\prime} \right)} & \\  & {= \partial_{2}W\left( {t,q,p\prime} \right) - DE\left( p\prime \right)t} & \\  & {= q'' - DE\left( p\prime \right)t,} \tag{6.8} \\ \end{array}$$

so we see that the primed coordinates differ by a term that is linear in time---both $ p\prime\left( t \right) = p_{0}^{\prime}$ and $ q\prime\left( t \right) = q_{0}^{\prime}$ are constant. Thus we can use either /W/ or /F/_{2} as the generating function, depending on the form of the new Hamiltonian we want.

Note that if /H/ is time independent then we can often find a time-independent /W/ that does the job. For time-independent /W/ the Hamilton--Jacobi equation simplifies to

$$\begin{matrix} {E\left( p\prime \right) = H\left( {t,q,\partial_{1}W\left( {t,q,p\prime} \right)} \right).} \tag{6.9} \\ \end{matrix}$$

The corresponding /F/_{2} is then linear in time. Notice that an implicit requirement is that the energy can be written as a function of the new momenta alone. This excludes the possibility that the transformed phase-space coordinates /q/′ and /p/′ are simply initial conditions for /q/ and /p/.

It turns out that there is flexibility in the choice of the function /E/. With an appropriate choice the phase-space coordinates obtained through the transformation generated by /W/ are action-angle coordinates.

### Exercise 6.1: Hamilton--Jacobi with* /F/_{1}

We have used an /F/_{2}-type generating function to carry out the Hamilton--Jacobi transformations. Carry out the equivalent transformations with an /F/_{1}-type generating function. Find the equations corresponding to equations (#Eqn(chapter006,6.4,6.4)), (#Eqn(chapter006,6.5,6.5)), and (#Eqn(chapter006,6.9,6.9)).

##### 6.1.1 Harmonic Oscillator
Consider the familiar time-independent Hamiltonian

$$\begin{matrix} {H\left( {t,x,p} \right) = \frac{p^{2}}{2m} + \frac{kx^{2}}{2}.} \tag{6.10} \\ \end{matrix}$$

We form the Hamilton--Jacobi equation for this problem:

$$\begin{matrix} {0 = H\left( {t,x,\partial_{1}F_{2}\left( {t,x,p\prime} \right)} \right) + \partial_{0}F_{2}\left( {t,x,p\prime} \right).} \tag{6.11} \\ \end{matrix}$$

#page(414)

Using /F/_{2}(/t/, /x/, /p/′) = /W/ (/t/, /x/, /p/′) − /E/(/p/′)/t/, we find

$$\begin{matrix} {E\left( p\prime \right) = H\left( {t,x,\partial_{1}W\left( {t,x,p\prime} \right)} \right).} \tag{6.12} \\ \end{matrix}$$

Writing this out explicitly yields

$$\begin{matrix} {E\left( p\prime \right) = \frac{\left( {\partial_{1}W\left( {t,x,p\prime} \right)} \right)^{2}}{2m} + \frac{kx^{2}}{2},} \tag{6.13} \\ \end{matrix}$$

and solving for ∂_{1}/W/ gives

$$\begin{matrix} {\partial_{1}W\left( {t,x,p\prime} \right) = \sqrt{2m\,\left( {E\left( p\prime \right) - \frac{kx^{2}}{2}} \right)}.} \tag{6.14} \\ \end{matrix}$$

Integrating gives the desired /W/:

$$\begin{matrix} {W\left( {t,x,p\prime} \right) = \int^{x}\sqrt{2m\,\left( {E\left( p\prime \right) - \frac{kz^{2}}{2}} \right)}dz.} \tag{6.15} \\ \end{matrix}$$

We can use either /W/ or the corresponding /F/_{2} as the generating function. First, take /W/ to be the generating function. We obtain the coordinate transformation by differentiating:

$$\begin{array}{lll} {x\prime} & {= \partial_{2}W\left( {t,x,p\prime} \right)} & \\  & {= {\int^{x}{\frac{mDE\left( p\prime \right)}{\sqrt{2m\,\left( {E\left( p\prime \right) - \frac{kz^{2}}{2}} \right)}}dz}}} \tag{6.16} \\ \end{array}$$

and then integrating to get

$$\begin{matrix} {x\prime = \sqrt{\frac{m}{k}}DE\left( p\prime \right)\arcsin\left( \sqrt{\frac{k}{2E\left( p\prime \right)}x} \right) + C\left( p\prime \right),} \tag{6.17} \\ \end{matrix}$$

with some integration constant /C/(/p/′). Inverting this, we get the unprimed coordinate in terms of the primed coordinate and momentum:

$$\begin{matrix} {x = \sqrt{\frac{2E\left( p\prime \right)}{k}}\sin\left\lbrack {\frac{1}{DE\left( p\prime \right)}\sqrt{\frac{k}{m}}\left( {x\prime - C\left( p\prime \right)} \right)} \right\rbrack.} \tag{6.18} \\ \end{matrix}$$

The new Hamiltonian /H/′ depends only on the momentum:

$$\begin{matrix} {H\prime\left( {t,x\prime,p\prime} \right) = E\left( p\prime \right).} \tag{6.19} \\ \end{matrix}$$

#page(415)

The equations of motion are just

$$\begin{array}{ll} {Dx\prime\left( t \right) = \partial_{2}H\prime\left( {t,x\prime\left( t \right),p\prime\left( t \right)} \right) = DE\left( p\prime \right)} & \\ {Dp\prime\left( t \right) = - \partial_{1}H\prime\left( {t,x\prime\left( t \right),p\prime\left( t \right)} \right) = 0,} \tag{6.20} \\ \end{array}$$

with solution

$$\begin{array}{ll} {x\prime\left( t \right) = DE\left( p\prime \right)t + x_{0}^{\prime}} & \\ {p\prime\left( t \right) = p_{0}^{\prime}} \tag{6.21} \\ \end{array}$$

for initial conditions $ x_{0}^{\prime}$ and $ p_{0}^{\prime}$. If we plug these expressions for /x/′(/t/) and /p/′(/t/) into equation (#Eqn(chapter006,6.18,6.18)) we find

$$\begin{array}{lll} {x\left( t \right)} & {= \sqrt{\frac{2E\left( p\prime \right)}{k}}\sin\left\lbrack {\frac{1}{DE\left. (p\prime \right)}\sqrt{\frac{k}{m}}{({DE\left( p\prime \right)t + x_{0}^{\prime} - C\left( p\prime) \right.})}} \right\rbrack} & \\  & {= \sqrt{\frac{2E\left( p\prime \right)}{k}}\sin\left\lbrack {\sqrt{\frac{k}{m}}\left( {t - t_{0}} \right)} \right\rbrack} & \\  & {= A\,\sin\,\left( {\omega t + \varphi} \right),} \tag{6.22} \\ \end{array}$$

where the angular frequency is $\omega = \sqrt{k/m}$, the amplitude is $ A = \sqrt{2E\left( p\prime \right)/k}$, and the phase is $\varphi = - \omega t_{0} = \omega{({x_{0}^{\prime} - C\left( {p\prime} \right)})}/DE\left( {p\prime} \right)$.

We can also use /F/_{2} = /W/ − /Et/ as the generating function. The new Hamiltonian is zero, so both /x/′ and /p/′ are constant, but the relationship between the old and new variables is

$$\begin{array}{lll} {x\prime} & {= \partial_{2}F_{2}\left( {t,x,p\prime} \right)} & \\  & {= \partial_{2}W\left( {t,x,p\prime} \right) - DE\left( p\prime \right)t} & \\  & {= \int^{x}\frac{mDE\left( p\prime \right)}{\sqrt{2m\left( {E\left( p\prime \right) - \frac{kz^{2}}{2}} \right)}} - DE\left( p\prime \right)t} & \\  & {= \sqrt{\frac{m}{k}}DE\left( p\prime \right)\,\arcsin\,\left( {\sqrt{\frac{k}{2E\left( p\prime \right)}}x} \right) + C\left( p\prime \right) - DE\left( p\prime \right)t.} \tag{6.23} \\ \end{array}$$

Plugging in the solution $ x\prime = x_{0}^{\prime}$ and $ p\prime = p_{0}^{\prime}$ and solving for /x/, we find equation (#Eqn(chapter006,6.22,6.22)). So once again we see that the two approaches are equivalent.

It is interesting to note that the solution depends upon the constants /E/(/p/′) and /DE/(/p/′), but otherwise the motion is not dependent in any essential way on what the function /E/ actually is. The momentum /p/ is constant and the values of the constants are
#page(416)
set by the initial conditions. Given a particular function /E/, the initial conditions determine /p/′, but the solution can be obtained without further specifying the /E/ function.

If we choose particular functions /E/ we can get particular canonical transformations. For example, a convenient choice is simply

$$\begin{matrix} {E\left( p\prime \right) = \alpha p\prime,} \tag{6.24} \\ \end{matrix}$$

for some constant /α/ that will be chosen later. We find

$$\begin{matrix} {x = \sqrt{\frac{2\alpha p\prime}{k}}\,\sin\frac{\omega}{\alpha}x\prime.} \tag{6.25} \\ \end{matrix}$$

So we see that a convenient choice is $\alpha = \omega = \sqrt{k/m}$, so

$$\begin{matrix} {{x = \sqrt{\frac{2p\prime}{\beta}}\,\sin\, x\prime},} \tag{6.26} \\ \end{matrix}$$

with $\beta = \sqrt{km}$. The new Hamiltonian is

$$\begin{matrix} {{H\prime\left( {t,x\prime,p\prime} \right) = E\left( p\prime \right) = \omega p\prime}.} \tag{6.27} \\ \end{matrix}$$

The solution is just $ x\prime = \omega t + x_{0}^{\prime}$ and $ p\prime = p_{0}^{\prime}$. Substituting the expression for /x/ in terms of /x/′ and /p/′ into /H/(/t/, /x/, /p/) = /H/′(/t/, /x/′, /p/′), we derive

$$\begin{array}{l} \begin{array}{lll} p & {= \left\lbrack {2m\left( {p\prime\alpha - \frac{k}{2}x^{2}} \right)} \right\rbrack^{1/2}} & \\  & {= \sqrt{2p\prime\beta}\,\cos x\prime.} \tag{6.28} \\ \end{array} \\  \\ \end{array}$$

The two transformation equations (#Eqn(chapter006,6.26,6.26)) and (#Eqn(chapter006,6.28,6.28)) are what we have called the polar-canonical transformation (equation #Eqn(chapter005,5.29,5.29)). We have already shown that this transformation is canonical and that it solves the harmonic oscillator, but it was not derived. Here we have derived this transformation as a particular case of the solution of the Hamilton--Jacobi equation.

We can also explore other choices for the /E/ function. For example, we could choose

$$\begin{matrix} {E\left( p\prime \right) = \frac{1}{2}\alpha p\prime^{2}.} \tag{6.29} \\ \end{matrix}$$

#page(417)

Following the same steps as before, we find

$$\begin{matrix} {x = \sqrt{\frac{\alpha p\prime^{2}}{k}}\,\sin\frac{\omega}{\alpha}\frac{x\prime}{p\prime}.} \tag{6.30} \\ \end{matrix}$$

So a convenient choice is again /α/ = /ω/, leaving

$$\begin{array}{ll} {x = \frac{p\prime}{\beta}\sin\frac{x\prime}{p\prime}} & \\ {p = \beta p\prime\cos\frac{x\prime}{p\prime},} \tag{6.31} \\ \end{array}$$

with /β/ = (/km/)^{1/4}. By construction, this transformation is also canonical and also brings the harmonic oscillator problem into an easily solvable form:

$$\begin{matrix} {H\prime\left( {t,x\prime,p\prime} \right) = \frac{1}{2}\omega p\prime^{2}.} \tag{6.32} \\ \end{matrix}$$

The harmonic oscillator Hamiltonian has been transformed to what looks a lot like the Hamiltonian for a free particle. This is very interesting. Notice that whereas Hamiltonian (#Eqn(chapter006,6.27,6.27)) does not have a well defined Legendre transform to an equivalent Lagrangian, the “free particle” harmonic oscillator has a well defined Legendre transform:

$$\begin{matrix} {L\prime\left( {t,x\prime,\dot{x}\prime} \right) = \frac{\dot{x}\prime^{2}}{2\omega}.} \tag{6.33} \\ \end{matrix}$$

Of course, there may be additional properties that make one choice more useful than others for particular applications.

### Exercise 6.2: Pendulum

Formulate and solve a Hamilton--Jacobi equation for the pendulum; investigate both the circulating and oscillating regions of phase space. (Note: This is a long story and requires some knowledge of elliptic functions.)

##### 6.1.2 Hamilton--Jacobi Solution of the Kepler Problem
We can use the Hamilton--Jacobi equation to find canonical coordinates that solve the Kepler problem. This is an essential first step in doing perturbation theory for orbital problems.

#page(418)

In rectangular coordinates (/x/, /y/, /z/), the Kepler Hamiltonian is

$$\begin{matrix} {H_{r}\left( {t;x,y,z;p_{x},p_{y},p_{z}} \right) = \frac{p^{2}}{2m} - \frac{\mu}{r},} \tag{6.34} \\ \end{matrix}$$

where /r/^{2} = /x/^{2} + /y/^{2} + /z/^{2} and $ p^{2} = p_{x}^{2} + p_{y}^{2} + p_{z}^{2}$.

We try a generating function of the form $ W\left( {t;x,y,z;p_{x}^{\prime},p_{y}^{\prime},p_{z}^{\prime}} \right)$. The Hamilton--Jacobi equation is then#Footnote(1)

$$\begin{array}{l}  \\ \begin{array}{lll} {E\left( p\prime \right)} & {= \frac{1}{2m}\left\lbrack \left( {\partial_{1,0}W\left( {t;x,y,z;p_{x}^{\prime},p_{y}^{\prime},p_{z}^{\prime}} \right)} \right)^{2} \right.} & \\  & {\,\,\,\,\,\,\,\,\,\,\, + \left( {\partial_{1,1}W\left( {t;x,y,z;p_{x}^{\prime},p_{y}^{\prime},p_{z}^{\prime}} \right)} \right)^{2}} & \\  & {\left. \,\,\,\,\,\,\,\,\,\,\, + \left( {\partial_{1,2}W\left( {t;x,y,z;p_{x}^{\prime},p_{y}^{\prime},p_{z}^{\prime}} \right)} \right)^{2} \right\rbrack - \frac{\mu}{r}.} \tag{6.35} \\ \end{array} \\ \end{array}$$

This is a partial differential equation in the three partial derivatives of /W/. We stare at it a while and give up.

Next we try converting to spherical coordinates. This is motivated by the fact that the potential energy depends only on /r/. The Hamiltonian in spherical coordinates (/r/, /θ/, /φ/), where /θ/ is the colatitude and /φ/ is the longitude, is

$$\begin{matrix} {H_{s}\left( {t;r,\theta,\varphi;p_{r},p_{\theta},p_{\varphi}} \right) = \frac{1}{2m}\left\lbrack {p_{r}^{2} + \frac{p_{\theta}^{2}}{r^{2}} + \frac{p_{\varphi}^{2}}{r^{2}{({\sin\,\theta})}^{2}}} \right\rbrack - \frac{\mu}{r}.} \tag{6.36} \\ \end{matrix}$$

The Hamilton--Jacobi equation is

$$\begin{array}{l} {E{({p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}})}} \\ \begin{array}{lll}  & {= \frac{1}{2m}\,\left\lbrack {({\partial_{1,0}W{({t;r,\theta,\varphi;p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}})}})}^{2} \right.} & \\  & {\,\,\,\,\, + \frac{1}{r^{2}}{({\partial_{1,1}W{({t;r,\theta,\varphi;p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}})}})}^{2}} & \\  & {\left. \,\,\,\,\, + \frac{1}{r^{2}{({\sin\theta})}^{2}}{({\partial_{1,2}W{({t;r,\theta,\varphi;p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}})}})}^{2} \right\rbrack - \frac{\mu}{r}.} \tag{6.37} \\ \end{array} \\ \end{array}$$

#page(419)

We can solve this Hamilton--Jacobi equation by successively isolating the dependence on the various variables. Looking first at the /φ/ dependence, we see that, outside of /W/, /φ/ appears only in one partial derivative. If we write

$$\begin{matrix} {W\left( {t;r,\theta,\varphi;p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) = f\left( {r,\theta,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) + p_{2}^{\prime}\varphi,} \tag{6.38} \\ \end{matrix}$$

then $\partial_{1,2}W\left( {t;r,\theta,\varphi;p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) = p_{2}^{\prime}$, and then /φ/ does not appear in the remaining equation for /f/:

$$\begin{array}{l} {E{({p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}})}} \\ \begin{array}{lll}  & {= \frac{1}{2m}\left\{ {({\partial_{0}f{({r,\theta,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}})}})}^{2} \right.} & \\  & {\,\,\, + \frac{1}{r^{2}}\,\left\lbrack {(\partial_{1}f\,\,{({r,\theta,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}})})}^{2} + \frac{{(p_{2}^{\prime})}^{2}}{{({\sin\theta})}^{2}} \right\rbrack\left. \, \right\} - \frac{\mu}{r}.} \tag{6.39} \\ \end{array} \\ \end{array}$$

Any function of the $ p_{i}^{\prime}$ could have been used as the coefficient of /φ/ in the generating function. This particular choice has the nice feature that $ p_{2}^{\prime}$ is the /z/ component of the angular momentum.

We can eliminate the /θ/ dependence if we choose

$$\begin{matrix} {f\left( {r,\theta,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) = R\left( {r,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) + \Theta\left( {\theta,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right)} \tag{6.40} \\ \end{matrix}$$

and require that Θ be a solution to

$$\begin{matrix} {\left( {\partial_{0}\Theta\left( {\theta,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right)} \right)^{2} + \frac{\left( p_{2}^{\prime} \right)^{2}}{{({\sin\theta})}^{2}} = \left( p_{1}^{\prime} \right)^{2}.} \tag{6.41} \\ \end{matrix}$$

We are free to choose the right-hand side to be any function of the new momenta. This choice reflects the fact that the left-hand side is non-negative. It turns out that $ p_{1}^{\prime}$ is the total angular momentum. This equation for Θ can be solved by quadrature.

The remaining equation that determines /R/ is

$$\begin{matrix} {E\left( {p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) = \frac{1}{2m}\left\lbrack {\left( {\partial_{0}R\left( {r,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right)} \right)^{2} + \frac{1}{r^{2}}\left( p_{1}^{\prime} \right)^{2}} \right\rbrack - \frac{\mu}{r},} \tag{6.42} \\ \end{matrix}$$

which also can be solved by quadrature.

#page(420)

Altogether the solution of the Hamilton--Jacobi equation reads

$$\begin{array}{lll} {W\left( {r,\theta,\varphi,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right)} & {= {\int^{r}{\left( {2mE\left( {p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) + \frac{2m\mu}{r} - \frac{\left( p_{1}^{\prime} \right)^{2}}{r^{2}}} \right)^{1/2}dr}}} & \\  & {\,\,\,\, + \int^{\theta}\left( {\left( p_{1}^{\prime} \right)^{2} - \frac{{(p_{2}^{\prime})}^{2}}{{(\sin\theta)}^{2}}} \right)^{1/2}d\theta} & \\  & {\,\,\,\, + p_{2}^{\prime}\varphi.} \tag{6.43} \\ \end{array}$$

It is interesting that our solution to the Hamilton--Jacobi partial differential equation is of the form

$$\begin{array}{l} {W\left( {t;r,\theta,\varphi;p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right)} \\ \begin{array}{ll} {\,\,\,\,\,\,\,\,\,\,\, = R\left( {r,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) + \Theta\left( {\theta,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) + \Phi\left( {\varphi,p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right).} \tag{6.44} \\ \end{array} \\ {\,\,\,\,\,\,\,\,\,\,\,} \\ \end{array}$$

Thus we have a separation-of-variables technique that involves writing the solution as a sum of functions of the individual variables. This might be contrasted with the separation-of-variables technique encountered in elementary quantum mechanics and classical electrodynamics, which uses products of functions of individual variables.

The coordinates /q/′ = (/q/′^{0}, /q/′^{1}, /q/′^{2}) conjugate to the momenta $ p\prime = \left\lbrack {p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right\rbrack $ are

$$\begin{array}{ll} {q\prime^{0}} & {= \partial_{2,0}W\left( {t;r,\theta,\varphi;p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right)} \\  & {= m\partial_{0}E\left( p\prime \right)\int^{r}\left( {2mE\left( p\prime \right) + \frac{2m\mu}{r} - \frac{\left( p_{1}^{\prime} \right)^{2}}{r^{2}}} \right)^{- 1/2}dr} \\ {q\prime^{1}} & {= \partial_{2,1}W\left( {t;r,\theta,\varphi;p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right)} \\  & {= p_{1}^{\prime}\,\int^{\theta}\left( {\left( p_{1}^{\prime} \right)^{2} - \frac{\left( p_{2}^{\prime} \right)^{2}}{{({\sin\theta})}^{2}}} \right)^{- 1/2}d\theta} \\  & {+ \,\int^{r}\left( {m\partial_{1}E\left( p\prime \right) - \frac{p_{1}^{\prime}}{r^{2}}} \right)\,\left( {2mE\left( p\prime \right) + \frac{2m\mu}{r} - \frac{\left( p_{1}^{\prime} \right)^{2}}{r^{2}}} \right)^{- 1/2}dr} \\ {q\prime^{2}} & {= \partial_{2,2}W\left( {t;r,\theta,\varphi;p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right)} \\  & {= \varphi - \frac{p_{2}^{\prime}}{{({\sin\theta})}^{2}}\int^{\theta}\left( {\left( p_{1}^{\prime} \right)^{2} - \frac{\left( p_{2}^{\prime} \right)^{2}}{{({\sin\theta})}^{2}}} \right)^{- 1/2}d\theta} \\  & {\,\,\,\, + m\partial_{2}E\left( p\prime \right)\,\int^{r}\left( {2mE\left( p\prime \right) + \frac{2m\mu}{r} - \frac{\left( p_{1}^{\prime} \right)^{2}}{r^{2}}} \right)^{- 1/2}dr.} \\  & \\ \end{array}$$

#page(421)

We are still free to choose the functional form of /E/. A convenient (and conventional) choice is

$$\begin{matrix} {E\left( {p_{0}^{\prime},p_{1}^{\prime},p_{2}^{\prime}} \right) = - \frac{m\mu^{2}}{2\left( p_{0}^{\prime} \right)^{2}}.} \tag{6.45} \\ \end{matrix}$$

With this choice the momentum $ p_{0}^{\prime}$ has dimensions of angular momentum, and the conjugate coordinate is an angle.

The Hamiltonian for the Kepler problem is reduced to

$$\begin{matrix} {H\prime\left( {t,q\prime,p\prime} \right) = E\left( p\prime \right) = - \frac{m\mu^{2}}{2\left( p_{0}^{\prime} \right)2}.} \tag{6.46} \\ \end{matrix}$$

Thus

$$\begin{matrix} {q\prime^{0} = nt + \beta^{0}} \tag{6.47} \\ \end{matrix}$$

$$\begin{matrix} {q\prime^{1} = \beta^{1}} \tag{6.48} \\ \end{matrix}$$

$$\begin{matrix} {q\prime^{2} = \beta^{2},} \tag{6.49} \\ \end{matrix}$$

where $ n = m\mu^{2}/\left( p_{0}^{\prime} \right)^{3}$ and where /β/^{0}, /β/^{1}, and /β/^{2} are the initial values of the components of /q/′. Only one of the new variables changes with time.

The canonical phase-space coordinates can be written in terms of the parameters that specify an orbit. We merely summarize the results; for further explanation see [36](bibliography!bib_36) or [38](bibliography!bib_38).

Assume we have a bound orbit with semimajor axis /a/, eccentricity /e/, inclination /i/, longitude of ascending node Ω, argument of pericenter /ω/, and mean anomaly /M/. The three canonical momenta are $ p_{0}^{\prime} = \sqrt{m\mu a},p_{1}^{\prime} = \sqrt{m\mu a\left( {1 - e^{2}} \right)}$, and $ p_{2}^{\prime} = \sqrt{m\mu a\left( {1 - e^{2}} \right)}\,\cos\, i $. The first momentum is related to the energy, the second momentum is the total angular momentum, and the third momentum is the component of the angular momentum in the /ẑ/ direction. The conjugate canonical coordinates are (/q/′)^{0} = /M/, (/q/′)^{1} = /ω/, and (/q/′)^{2} = Ω.

##### 6.1.3 /F/_{2} and the Lagrangian
The solution to the Hamilton--Jacobi equation, the mixed-variable generating function that generates time evolution, is related to the action used in the variational principle. In particular, the time derivative of the generating function along realizable paths has the same value as the Lagrangian.

#page(422)

Let ${\widetilde{F}}_{2}\left( t \right) = F_{2}\left( {t,q\left( t \right),p\prime\left( t \right)} \right)$ be the value of /F/_{2} along the paths /q/ and /p/′ at time /t/. The derivative of ${\widetilde{F}}_{2}$ is

$$\begin{array}{lll} {D{\widetilde{F}}_{2}\left( t \right)} & {= \partial_{0}F_{2}\left( {t,q\left( t \right),p\prime(t)} \right)} & \\  & {\,\,\,\,\,\,\, + \partial_{1}F_{2}\left( {t,q\left( t \right),p\prime\left( t \right)} \right)Dq\left( t \right)} & \\  & {\,\,\,\,\,\,\, + \partial_{2}F_{2}\left( {t,q\left( t \right),p\prime\left( t \right)} \right)Dq\prime\left( t \right).} \tag{6.50} \\ \end{array}$$

Using the Hamilton--Jacobi equation (#Eqn(chapter006,6.4,6.4)), this becomes

$$\begin{array}{lll} {D{\widetilde{F}}_{2}\left( t \right)} & {= - H\left( {t,q\left( t \right),\partial_{1}F_{2}(t,q\left( t \right),p\prime(t))} \right)} & \\  & {\,\,\,\,\,\,\, + \partial_{1}F_{2}\left( {t,q\left( t \right),p\prime\left( t \right)} \right)Dq\left( t \right)} & \\  & {\,\,\,\,\,\,\, + \partial_{2}F_{2}\left( {t,q\left( t \right),p\prime\left( t \right)} \right)Dq\prime\left( t \right).} \tag{6.51} \\ \end{array}$$

Now, using equation (#Eqn(chapter006,6.2,6.2)), we get

$$\begin{array}{l} \begin{array}{lll} {D{\widetilde{F}}_{2}\left( t \right)} & {= - H\left( {t,q\left( t \right),p\left( t \right)} \right)} & \\  & {\,\,\,\,\, + p\left( t \right)Dq\left( t \right)} & \\  & {\,\,\,\,\, + \partial_{2}F_{2}\left( {t,q\left( t \right),p\prime\left( t \right)} \right)Dp\prime\left( t \right).} \tag{6.52} \\ \end{array} \\  \\ \end{array}$$

But $ p\left( t \right)Dq\left( t \right) - H\left( {t,q\left( t \right),p\left( t \right)} \right) = L\left( {t,q\left( t \right),Dq\left( t \right)} \right)$, so

$$\begin{matrix} {D{\widetilde{F}}_{2}\left( t \right) = L\left( {t,q\left( t \right),Dq\left( t \right)} \right) + \partial_{2}F_{2}\left( {t,q\left( t \right),p\prime(t)} \right)Dp\prime\left( t \right).} \tag{6.53} \\ \end{matrix}$$

On realizable paths we have /Dp/′(/t/) = 0, so along realizable paths the time derivative of /F/_{2} is the same as the Lagrangian along the path. The time integral of the Lagrangian along any path is the action along that path. This means that, up to an additive term that is constant on realizable paths but may be a function of the transformed phase-space coordinates /q/′ and /p/′, the /F/_{2} that solves the Hamilton--Jacobi equation has the same value as the Lagrangian action for realizable paths.

The same conclusion follows for the Hamilton--Jacobi equation formulated in terms of /F/_{1}. Up to an additive term that is constant on realizable paths but may be a function of the transformed phase-space coordinates /q/′ and /p/′, the /F/_{1} that solves the corresponding Hamilton--Jacobi equation has the same value as the Lagrangian action for realizable paths.

#page(423)

Recall that a transformation given by an /F/_{2}-type generating function is also given by an /F/_{1}-type generating function related to it by a Legendre transform (see equation #Eqn(chapter005,5.142,5.142)):

$$\begin{matrix} {F_{1}\left( {t,q,q\prime} \right) = F_{2}\left( {t,q,p\prime} \right) - q\prime p\prime,} \tag{6.54} \\ \end{matrix}$$

provided the transformations are nonsingular. In this case, both /q/′ and /p/′ are constant on realizable paths, so the additive constants that make /F/_{1} and /F/_{2} equal to the Lagrangian action differ by /q/′/p/′.

### Exercise 6.3: Harmonic oscillator

Let's check this for the harmonic oscillator (of course).

*a.* Finish the integral (#Eqn(chapter006,6.15,6.15)):$ W\left( {t,x,p\prime} \right) = \int^{x}\sqrt{2m\left( {E\left( p\prime \right) - \frac{kz^{2}}{2}} \right)}dz.$ Write the result in terms of the amplitude $ A = \sqrt{2E\left( p\prime \right)/k}$.

*b.* Check that this generating function gives the transformation $ x\prime = \partial_{2}W\left( {t,x,p\prime} \right) = \sqrt{\frac{m}{k}}DE\left( p\prime \right)\,\arcsin\left( \frac{x}{\sqrt{2E\left( p\prime \right)/k}} \right),$ which is the same as equation (#Eqn(chapter006,6.17,6.17)) for a particular choice of the integration constant. The other part of the transformation is $ p = \partial_{1}W\left( {t,x,p\prime} \right) = \sqrt{mk}\sqrt{A^{2} - x^{2}},$ with the same definition of /A/ as before.

*c.* Compute the time derivative of the associated /F/_{2} along realizable paths (/Dp/′(/t/) = 0), and compare it to the Lagrangian along realizable paths.

##### 6.1.4 The Action Generates Time Evolution
We define the function $\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right)$ to be the value of the action for a realizable path /q/ such that /q/(/t/_{1}) = /q/_{1} and /q/(/t/_{2}) = /q/_{2}. So $\overline{F}$ satisfies

$$\begin{matrix} {\overline{F}\left( {t_{1},q\left( t_{1} \right),t_{2,}q\left( t_{2} \right)} \right) = S\left\lbrack q \right\rbrack\left( {t_{1},t_{2}} \right) = {\int_{t_{1}}^{t_{2}}{L \circ \Gamma\left\lbrack q \right\rbrack}}.} \tag{6.55} \\ \end{matrix}$$

#page(424)

For variations /η/ that are not necessarily zero at the end times and for realizable paths /q/, the variation of the action is

$$\begin{array}{lll} {\delta_{\eta}S\left\lbrack q \right\rbrack\left( {t_{1},t_{2}} \right)} & {= \left( {\partial_{2}L \circ \Gamma\left\lbrack q \right\rbrack} \right)\eta|_{t_{1}}^{t_{2}}} & \\  & {= p\left( t_{2} \right)\eta\left( t_{2} \right) - p\left( t_{1} \right)\eta\left( t_{1} \right).} \tag{6.56} \\ \end{array}$$

Alternatively, the variation of /S/[/q/] in equation (#Eqn(chapter006,6.55,6.55)) gives

$$\begin{array}{lll} {\delta_{\eta}S\left\lbrack q \right\rbrack\left( {t_{1},t_{2}} \right)} & {= \partial_{1}\overline{F}\left( {t_{1},q\left( t_{1} \right),t_{2},q\left( t_{2} \right)} \right)\eta\left( t_{1} \right)} & \\  & {\,\,\,\,\,\, + \partial_{3}\overline{F}\left( {t_{1},q\left( t_{1} \right),t_{2},q\left( t_{2} \right)} \right)\eta\left( t_{2} \right).} \tag{6.57} \\ \end{array}$$

Comparing equations (#Eqn(chapter006,6.56,6.56)) and (#Eqn(chapter006,6.57,6.57)) and using the fact that the variation /η/ is arbitrary, we find

$$\begin{array}{ll} {\partial_{1}\overline{F}\left( {t_{1},q\left( t_{1} \right),t_{2},q\left( t_{2} \right)} \right) = - p\left( t_{1} \right)} & \\ {\partial_{3}\overline{F}\left( {t_{1},q\left( t_{1} \right),t_{2},q\left( t_{2} \right)} \right) = p\left( t_{2} \right).} \tag{6.58} \\ \end{array}$$

The partial derivatives of $\overline{F}$ with respect to the coordinate arguments give the momenta. Abstracting off paths, we have

$$\begin{array}{ll} {\partial_{1}\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right) = - p_{1}} & \\ {\partial_{3}\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right) = p_{2.}} \tag{6.59} \\ \end{array}$$

This looks a bit like the /F/_{1}-type generating function relations, but here there are two times. Solving equations (#Eqn(chapter006,6.59,6.59)) for /q/_{2} and /p/_{2} as functions of /t/_{2} and the initial state /t/_{1}, /q/_{1}, /p/_{1}, we get the time evolution of the system in terms of $\overline{F}$. The function $\overline{F}$ generates time evolution.

If we vary the lower limit of the action integral we get

$$\begin{matrix} {\partial_{0}\left( {S\left\lbrack q \right\rbrack} \right)\left( {t_{1},t_{2}} \right) = - L\left( {t_{1},q\left( t_{1} \right),D_{q}\left( t_{1} \right)} \right).} \tag{6.60} \\ \end{matrix}$$

Using equation (#Eqn(chapter006,6.55,6.55)), and given a realizable path /q/ such that /q/(/t/_{1}) = /q/_{1} and /q/(/t/_{2}) = /q/_{2}, we get the partial derivatives with respect to the time slots:

$$\begin{array}{lll} {\partial_{0}\left( {S\left\lbrack q \right\rbrack} \right)\left( {t_{1},t_{2}} \right)} & {= \partial_{0}\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right) + \partial_{1}\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right)Dq\left( t_{1} \right)} & \\  & {= \partial_{0}\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right) - p\left( t_{1} \right)D_{q}\left( t_{1} \right).} \tag{6.61} \\ \end{array}$$

Rearranging the terms of equation (#Eqn(chapter006,6.61,6.61)) and using equation (#Eqn(chapter006,6.60,6.60)) we get

#page(425)

$$\begin{array}{lll} {\partial_{0}\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right)} & {= H\left( {t_{1},q_{1},p_{1}} \right)} & \\  & {= H\left( {t_{1},q_{1}, - \partial_{1}\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right)} \right),} \tag{6.62} \\ \end{array}$$

and similarly

$$\begin{array}{lll} {\partial_{2}\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right)} & {= - H\left( {t_{2},q_{2},p_{2}} \right)} & \\  & {= - H\left( {t_{2},q_{2},\partial_{3}\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right)} \right).} \tag{6.63} \\ \end{array}$$

These are a pair of Hamilton--Jacobi equations, computed at the endpoints of the path.

The function $\overline{F}$ can be written in terms of an /F/_{1} that satisfies a Hamilton--Jacobi equation for /H/. We can compute time evolution by using the /F/_{1} solution of the Hamilton--Jacobi equation to express the state (/t/_{1}, /q/_{1}, /p/_{1}) in terms of the constants /q/′ and /p/′. Using the same solution we can then perform a subsequent transformation back from /q/′ /p/′ to the original state variables at a different time /t/_{2}, giving the state (/t/_{2}, /q/_{2}, /p/_{2}). The composition of these two canonical transformations is canonical (see [exercise 5.12](chapter005!exercise_5.12)).

The generating function for the composition is the difference of the generating functions for each step:

$$\begin{matrix} {{\overline{F}}_{x}\left( {t_{1},q_{1},q\prime,t_{2},q_{2}} \right) = F_{1}\left( {t_{2},q_{2},q\prime} \right) - F_{1}\left( {t_{1},q_{1},q\prime} \right),} \tag{6.64} \\ \end{matrix}$$

with the condition

$$\begin{matrix} {\partial_{2}F_{1}\left( {t_{2},q_{2},q\prime} \right) - \partial_{2}F_{1}\left( {t_{1},q_{1},q\prime} \right) = 0,} \tag{6.65} \\ \end{matrix}$$

which allows us to eliminate /q/′ in terms of /t/_{1}, /q/_{1}, /t/_{2}, and /q/_{2}. So we can write

$$\begin{matrix} {\overline{F}\left( {t_{1},q_{1},t_{2},q_{2}} \right) = F_{1}\left( {t_{2},q_{2},q\prime} \right) - F_{1}\left( {t_{1},q_{1},q\prime} \right).} \tag{6.66} \\ \end{matrix}$$

### Exercise 6.4: Uniform acceleration

*a.* Compute the Lagrangian action, as a function of the endpoints and times, for a uniformly accelerated particle. Use this to construct the canonical transformation for time evolution from a given initial state.

*b.* Solve the Hamilton--Jacobi equation for the uniformly accelerated particle, obtaining the /F/_{1} that makes the transformed Hamiltonian zero. Show that the Lagrangian action can be expressed as a difference of two applications of this /F/_{1}.

#page(426)

### 6.2 Time Evolution is Canonical
We use time evolution to generate a transformation

$$\begin{matrix} {\left( {t,q,p} \right) = \mathcal{C}_{\Delta}\left( {t\prime,q\prime,p\prime} \right)} \tag{6.67} \\ \end{matrix}$$

that is obtained in the following way. Let $\sigma\left( t \right) = \left( {t,\overline{q}\left( t \right),\overline{p}\left( t \right)} \right)$ be a solution of Hamilton's equations. The transformation $\mathcal{C}_{\Delta}$ satisfies

$$\begin{matrix} {\mathcal{C}_{\Delta}\left( {\sigma\left( t \right)} \right) = \sigma\left( {t + \Delta} \right),} \tag{6.68} \\ \end{matrix}$$

or, equivalently,

$$\begin{matrix} {\mathcal{C}_{\Delta}\left( {t,\overline{q}\left( t \right),\overline{p}\left( t \right)} \right) = (t + \Delta,\overline{q}\left( {t + \Delta} \right),\overline{p}\left( {t + \Delta} \right)).} \tag{6.69} \\ \end{matrix}$$

Notice that $\mathcal{C}_{\Delta}$ changes the time component. This is the first transformation of this kind that we have considered.#Footnote(2)

Given a state (/t/′, /q/′, /p/′), we find the phase-space path /σ/ emanating from this state as an initial condition, satisfying

$$\begin{array}{ll} {q\prime = \overline{q}\left( t\prime \right)} & \\ {p\prime = \overline{p}\left( t\prime \right).} \tag{6.70} \\ \end{array}$$

The value (/t/, /q/, /p/) of $\mathcal{C}_{\Delta}\left( {t\prime,q\prime,p\prime} \right)$ is then $\left( {t\prime + \Delta,\overline{q}\left( {t\prime + \Delta} \right),\overline{p}\left( {t\prime + \Delta} \right)} \right)$.

Time evolution is canonical if the transformation $\mathcal{C}_{\Delta}$ is symplectic and if the Hamiltonian transforms in an appropriate manner. The transformation $\mathcal{C}_{\Delta}$ is symplectic if the bilinear antisymmetric form /ω/ is invariant (see equation #Eqn(chapter005,5.73,5.73)) for a general pair of linearized state variations with zero time component.

Let /ζ/′ be an increment with zero time component of the state (/t/′, /q/′, /p/′). The linearized increment in the value of $\mathcal{C}_{\Delta}\left( {t\prime,q\prime,p\prime} \right)$ is $\zeta = D\mathcal{C}_{\Delta}\left( {t\prime,q\prime,p\prime} \right)\zeta\prime $: The image of the increment is obtained by multiplying the increment by the derivative of the transformation. On the other hand, the transformation is obtained by time evolution, so the image of the increment can also be found by the time evolution of the linearized variational system. Let

$$\begin{array}{ll} {\overline{\zeta}\left( t \right) = \left( {0,{\overline{\zeta}}_{q}\left( t \right),{\overline{\zeta}}_{p}\left( t \right)} \right)} & \\ {\overline{\zeta}\prime\left( t \right) = \left( {0,{\overline{\zeta}}_{p}^{\prime}\left( t \right),{\overline{\zeta}}_{p}^{\prime}\left( t \right)} \right)} \tag{6.71} \\ \end{array}$$

#page(427)

be variations of the state path $\sigma\left( t \right) = \left( {t,\overline{q}\left( t \right),\overline{p}\left( t \right)} \right)$; then

$$\begin{array}{ll} {\overline{\zeta}\left( {t + \Delta} \right) = D\mathcal{C}_{\Delta}\left( {t,q\left( t \right),p\left( t \right)} \right)\overline{\zeta}\left( t \right)} & \\ {\overline{\zeta}\prime\left( {t + \Delta} \right) = D\mathcal{C}_{\Delta}\left( {t,q\left( t \right),p\left( t \right)} \right)\overline{\zeta}\prime\left( t \right).} \tag{6.72} \\ \end{array}$$

The symplectic requirement is

$$\begin{matrix} {\omega\left( {\overline{\zeta}\left( t \right),\overline{\zeta}\prime\left( t \right)} \right)\, = \omega\left( {\overline{\zeta}\left( {t + \Delta} \right),\,\overline{\zeta}\prime\left( {t + \Delta} \right)} \right).} \tag{6.73} \\ \end{matrix}$$

This must be true for arbitrary Δ, so it is satisfied if the following quantity is constant:

$$\begin{array}{lll} {A\left( t \right)} & {= \omega\left( {\overline{\zeta}\left( t \right),\,\overline{\zeta}\prime\left( t \right)} \right)} & \\  & {= P\left( {\overline{\zeta}\prime\left( t \right)} \right)Q\left( {\overline{\zeta}\left( t \right)} \right) - P\left( {\overline{\zeta}\left( t \right)} \right)Q\left( {\overline{\zeta}\prime\left( t \right)} \right)} & \\  & {= {\overline{\zeta}}_{p}^{\prime}\left( t \right){\overline{\zeta}}_{q}\left( t \right) - {\overline{\zeta}}_{p}\left( t \right){\overline{\zeta}}_{q}^{\prime}\left( t \right).} \tag{6.74} \\ \end{array}$$

We compute the derivative:

$$\begin{array}{lll} {DA\left( t \right)} & {= D{\overline{\zeta}}_{p}^{\prime}\left( t \right){\overline{\zeta}}_{q}\left( t \right) + {\overline{\zeta}}_{p}^{\prime}\left( t \right)D{\overline{\zeta}}_{q}\left( t \right)} & \\  & {\,\,\,\,\, - D{\overline{\zeta}}_{p}\left( t \right){\overline{\zeta}}_{q}^{\prime}\left( t \right) - {\overline{\zeta}}_{p}\left( t \right)D{\overline{\zeta}}_{q}^{\prime}\left( t \right).} & 6.75 \\ \end{array}$$

With Hamilton's equations, the variations satisfy

$$\begin{array}{lll} {D{\overline{\zeta}}_{q}\left( t \right)} & {= \partial_{1}\partial_{2}H\left( {t,\overline{q}\left( t \right),\overline{p}\left( t \right)} \right){\overline{\zeta}}_{q}\left( t \right)} & \\  & {\,\,\,\,\, + \partial_{2}\partial_{2}H\left( {t,\overline{q}\left( t \right),\overline{p}\left( t \right)} \right){\overline{\zeta}}_{p}\left( t \right),} & \\ {D{\overline{\zeta}}_{p}\left( t \right)} & {= - \partial_{1}\partial_{1}H\left( {t,\overline{q}\left( t \right),\overline{p}\left( t \right)} \right){\overline{\zeta}}_{q}\left( t \right)} & \\  & {\,\,\,\,\, - \partial_{2}\partial_{1}H\left( {t,\overline{q}\left( t \right),\overline{p}\left( t \right)} \right){\overline{\zeta}}_{p}\left( t \right).} \tag{6.76} \\ \end{array}$$

Substituting these into /DA/ and collecting terms, we find#Footnote(3)

$$\begin{matrix} {DA\left( t \right) = 0.} \tag{6.77} \\ \end{matrix}$$

We conclude that time evolution generates a phase-space transformation with symplectic derivative.

To make a canonical transformation we must specify how the Hamiltonian transforms. The same Hamiltonian describes the evolution of a state and a time-advanced state because the latter is just another state. Thus the transformed Hamiltonian is the same as the original Hamiltonian.

#page(428)

#### Liouville's theorem, again
We deduced that volumes in phase space are preserved by time evolution by showing that the divergence of the phase flow is zero, using the equations of motion (see [section 3.8](chapter003!section_3.8)). We can also show that volumes in phase space are preserved by the evolution using the fact that time evolution is a canonical transformation.

We have shown that phase-space volume is preserved for sym-plectic transformations. Now we have shown that the transformation generated by time evolution is a symplectic transformation. Therefore, the transformation generated by time evolution preserves phase-space volume. This is an alternate proof of Liouville's theorem.

#### Another time-evolution transformation
There is another canonical transformation that can be constructed from time evolution. We define the transformation $\mathcal{C}_{\Delta}^{\prime}$ such that

$$\begin{matrix} {\mathcal{C}_{\Delta}^{\prime} = C_{\Delta} \circ S_{- \Delta},} \tag{6.78} \\ \end{matrix}$$

where /S/_{Δ}(/a/, /b/, /c/) = (/a/ + Δ, /b/, /c/) shifts the time of a phase-space state.#Footnote(4) More explicitly, given a state (/t/, /q/′, /p/′), we evolve the state that is obtained by subtracting Δ from /t/; that is, we take the state (/t/ − Δ, /q/′, /p/′) as an initial state for evolution by Hamilton's equations. The state path /σ/ satisfies

$$\begin{array}{lll} {\sigma\left( {t - \Delta} \right)} & {= \left( {t - \Delta,\overline{q}\left( {t - \Delta} \right),\overline{p}\left( {t - \Delta} \right)} \right)} & \\  & {= \left( {t - \Delta,q\prime,p\prime} \right).} \tag{6.79} \\ \end{array}$$

The output of the transformation is the state

$$\begin{matrix} {\left( {t,q,p} \right) = \sigma\left( t \right) = \left( {t,\overline{q}\left( t \right),\overline{p}\left( t \right)} \right).} \tag{6.80} \\ \end{matrix}$$

The transformation satisfies

$$\begin{matrix} {\left( {t,\overline{q}\left( t \right),\overline{p}\left( t \right)} \right) = \mathcal{C}_{\Delta}^{\prime}\left( {t,\overline{q}\left( {t - \Delta} \right),\overline{p}\left( {t - \Delta} \right)} \right).} \tag{6.81} \\ \end{matrix}$$

The arguments of $\mathcal{C}_{\Delta}^{\prime}$ are not a consistent phase-space state; the time argument must be decremented by Δ to obtain a consistent
#page(429)
state. The transformation is completed by evolution of this consistent state.

Why is this a good idea? Our usual canonical transformations do not change the time component. The $\mathcal{C}_{\Delta}$ transformation changes the time component, but $\mathcal{C}_{\Delta}^{\prime}$ does not. It is canonical and in the usual form:

$$\begin{matrix} {\left( {t,q,p} \right) = \mathcal{C}_{\Delta}^{\prime}\left( {t,q\prime,p\prime} \right).} \tag{6.82} \\ \end{matrix}$$

The $\mathcal{C}_{\Delta}^{\prime}$ transformation requires an adjustment of the Hamiltonian. The Hamiltonian $ H_{\Delta}^{\prime}$ that gives the correct Hamilton's equations at the transformed phase-space point is the original Hamiltonian composed with a function that decrements the independent variable by Δ:

$$\begin{matrix} {H_{\Delta}^{\prime}\left( {t,q,p} \right) = H\left( {t - \Delta,q,p} \right)} \tag{6.83} \\ \end{matrix}$$

or

$$\begin{matrix} {H_{\Delta}^{\prime} = H \circ S_{- \Delta}.} \tag{6.84} \\ \end{matrix}$$

Notice that if /H/ is time independent then $ H_{\Delta}^{\prime} = H $.

Assume we have a procedure C such that ((C delta-t) state) implements a time-evolution transformation $\mathcal{C}_{\Delta}$ of the state state with time interval delta-t; then the procedure Cp such that ((Cp delta-t) state) implements $\mathcal{C}_{\Delta}^{\prime}$ of the same state and time interval can be derived from the procedure C by using the procedure
```Scheme
(define ((C->Cp C) delta-t) (compose (C delta-t) (shift-t (- delta-t)))) 
```
where shift-t implements /S/_{Δ}:
```Scheme
(define ((shift-t delta-t) state) (up (+ (time state) delta-t) (coordinate state) (momentum state))) 
```
To complete the canonical transformation we have a procedure that transforms the Hamiltonian:
```Scheme
(define ((H->Hp delta-t) H) (compose H (shift-t (- delta-t)))) 
```
#page(430)

So both $\mathcal{C}$ and $\mathcal{C}\prime $ can be used to make canonical transformations by specifying how the old and new Hamiltonians are related. For $\mathcal{C}_{\Delta}$ the Hamiltonian is unchanged. For $\mathcal{C}_{\Delta}^{\prime}$ the Hamiltonian is time shifted.

### Exercise 6.5: Verification

The condition (#Eqn(chapter005,5.20,5.20)) that Hamilton's equations are preserved for $\mathcal{C}_{\Delta}$ is $ D_{s}H \circ \mathcal{C}_{\Delta} = D\mathcal{C}_{\Delta}\, D_{s}H_{\Delta}^{\prime},$ and the condition that Hamilton's equations are preserved for $\mathcal{C}_{\Delta}^{\prime}$ is $ D_{s}H \circ \mathcal{C}_{\Delta}^{\prime} = D\mathcal{C}_{\Delta}^{\prime}\, D_{s}H_{\Delta}^{\prime}.$ Verify that these conditions are satisfied.

### Exercise 6.6: Driven harmonic oscillator

We can use the simple driven harmonic oscillator to illustrate that time evolution yields a symplectic transformation that can be extended to be canonical in two ways. We use the driven harmonic oscillator because its solution can be compactly expressed in explicit form.

Suppose that we have a harmonic oscillator with natural frequency /ω/_{0} driven by a periodic sinusoidal drive of frequency /ω/ and amplitude /α/. The Hamiltonian we will consider is

$$ H\left( {t,q,p} \right) = \frac{1}{2}p^{2} + \frac{1}{2}\omega_{0}^{2}q^{2} - \alpha q\,\cos\,\omega t.$$

The general solution for a given initial state (/t/_{0}, /q/_{0}, /p/_{0}) evolved for a time Δ is

$$\begin{array}{l} \begin{array}{l} \left( \begin{array}{l} {q\left( {t_{0} + \Delta} \right)} \\ {p\left( {t_{0} + \Delta} \right)/\omega_{0}} \\ \end{array} \right) \\ {\,\,\,\,\,\,\,\,\, = \left( \begin{array}{ll} {\cos\omega_{0}\Delta} & {\sin\omega_{0}\Delta} \\ {- \sin\omega_{0}\Delta} & {\cos\omega_{0}\Delta} \\ \end{array} \right)\left( \begin{array}{l} {q_{0} - \alpha\prime\,\cos\omega t_{0}} \\ {(1/\omega_{0})\left( {p_{0} + \alpha\prime\omega\sin\omega t_{0}} \right)} \\ \end{array} \right)} \\ {\,\,\,\,\,\,\,\,\,\,\,\,\,\, + \left( \begin{array}{l} {\alpha\prime\,\cos\omega\left( {t_{0} + \Delta} \right)} \\ {- \alpha\prime\left( {\omega/\omega_{0}} \right)\,\sin\omega\left( {t_{0} + \Delta} \right)} \\ \end{array} \right)} \\ \end{array} \\ \begin{array}{l}  \\ {\,\,\,\,\,\,\,} \\  \\ \end{array} \\ \end{array}$$

where $\alpha\prime = \alpha/\left( {\omega_{0}^{2} - \omega^{2}} \right).$*a.* Fill in the details of the procedure
```Scheme
(define (((C* alpha omega omega0) delta-t) state) ... ) 
```
that implements the time-evolution transformation of the driven harmonic oscillator. Let C be (C_{*} alpha omega omega0).

*b.* In terms of C_{*}, the general solution emanating from a given state is
```Scheme
(define (((solution alpha omega omega0) state0) t) (((C* alpha omega omega0) (- t (time state0))) state0)) 
```
#page(431)

Check that the implementation of C_{*} is correct by using it to construct the solution and verifying that the solution satisfies Hamilton's equations. Further check the solution by comparing to numerical integration.

*c.* We know that for any phase-space state function /F/ the rate of change of that function along a solution path /σ/ is $ D\left( {F \circ \sigma} \right) = \partial_{0}F \circ \sigma + \left\{ {F,H} \right\} \circ \sigma.$ Show, by writing a short program to test it, that this is true of the function implemented by (C delta) for the driven oscillator. Why is this interesting?

*d.* Use the procedure symplectic-transform? to show that both C and Cp are symplectic.

*e.* Use the procedure canonical? to verify that both C and Cp are canonical with the appropriate transformed Hamiltonian.

##### 6.2.1 Another View of Time Evolution
We can also show that time evolution generates canonical transformations using the Poincaré--Cartan integral invariant.

Consider a two-dimensional region of phase-space coordinates, /R/′, at some particular time /t/′ (see [[chapter006!figure_6.1][figure 6.1]]). Let /R/ be the image of this region at time /t/ under time evolution for a time interval of Δ. The time evolution is governed by a Hamiltonian /H/. Let $\sum_{i}\, A_{i}$ be the sum of the oriented areas of the projections of /R/ onto the fundamental canonical planes.#Footnote(5) Similarly, let $\sum_{i}\, A_{i}^{\prime}$ be the sum of oriented projected areas for /R/′. We will show that $\sum_{i}\, A_{i} = \sum_{i}\, A_{i}^{\prime}$, and thus the Poincaré integral invariant is preserved by time evolution. By showing that the Poincaré integral invariant is preserved, we will have shown that the /qp/ part of the transformation generated by time evolution is symplectic. From this we can construct canonical transformations from time evolution as before.

In the extended phase space we see that the evolution sweeps out a cylindrical volume with endcaps /R/′ and /R/, each at a fixed time. Let /R/″ be the two-dimensional region swept out by the trajectories that map the boundary of region /R/′ to the boundary of region /R/. The regions /R/, /R/′, and /R/″ together form the boundary of a volume of phase-state space.

#page(432)

The Poincaré--Cartan integral invariant on the whole boundary is zero.#Footnote(6) Thus

$$\begin{matrix} {{\sum\limits_{i = 0}^{n}A_{i}} - {\sum\limits_{i = 0}^{n}A_{i}^{\prime}} + {\sum\limits_{i = 0}^{n}A_{i}^{''}} = 0,} \tag{6.85} \\ \end{matrix}$$

where the /n/ index indicates the /t/, /p_{t}/ canonical plane. The second term is negative, because in the extended phase space we take the area to be positive if the normal to the surface is outward pointing.

We will show that the Poincaré--Cartan integral invariant for a region of phase space that is generated by time evolution is zero:

$$\begin{matrix} {{\sum\limits_{i = 0}^{n}A_{i}^{''}} = 0.} \tag{6.86} \\ \end{matrix}$$

This will allow us to conclude

$$\begin{matrix} {{\sum\limits_{i = 0}^{n}A_{i}} - {\sum\limits_{i = 0}^{n}A_{i}^{\prime}} = 0.} \tag{6.87} \\ \end{matrix}$$

The areas of the projection of /R/ and /R/′ on the /t/, /p_{t}/ plane are zero because /R/ and /R/′ are at constant times, so for these regions the Poincaré--Cartan integral invariant is the same as the Poincaré integral invariant. Thus

$$\begin{matrix} {{\sum\limits_{i = 0}^{n - 1}A_{i}} = {\sum\limits_{i = 0}^{n - 1}A_{i}^{\prime}}.} \tag{6.88} \\ \end{matrix}$$

We are left with showing that the Poincaré--Cartan integral invariant for the region /R/″ is zero. This will be zero if the contribution from any small piece of /R/″ is zero. We will show this by showing that the /ω/ form (see equation #Eqn(chapter005,5.70,5.70)) on a small parallelogram in this region is zero. Let (0; /q/, /t/; /p/, /p_{t}/) be a vertex of this parallelogram. The parallelogram is specified by two edges /ζ/_{1} and /ζ/_{2} emanating from this vertex. For edge /ζ/_{1} of the parallelogram,
#page(433)
we take a constant-time phase-space increment with length Δ/q/ and Δ/p/ in the /q/ and /p/ directions. The first-order change in the Hamiltonian that corresponds to these changes is

#Image(Art_P1185.jpg,figure_6.1)
#Caption *Figure 6.1* All points in some two-dimensional region /R/′ in phase space at time /t/′ are evolved for some time interval Δ. At the time /t/ the set of points define the two-dimensional region /R/. For example, the state labeled by the phase-space coordinates (/t/′, /q/′, /p/′) evolves to the state labeled by the coordinates (/t/, /q/, /p/). #CaptionEnd

$$\begin{matrix} {\Delta H = \partial_{1}H\left( {t,q,p} \right)\Delta q + \partial_{2}H\left( {t,q,p} \right)\Delta p} \tag{6.89} \\ \end{matrix}$$

for constant time Δ/t/ = 0. The increment Δ/p_{t}/ is the negative of Δ/H/. So the extended phase-space increment is

$$\begin{matrix} {\zeta_{1} = \left( {0;\Delta q,\, 0;\,\Delta p, - \partial_{1}H\left( {t,q,p} \right)\Delta q - \partial_{2}H\left( {t,q,p} \right)\Delta p} \right).} \tag{6.90} \\ \end{matrix}$$

The edge /ζ/_{2} is obtained by time evolution of the vertex for a time interval Δ/t/. Using Hamilton's equations, we obtain

$$\begin{array}{lll} \zeta_{2} & {= \left( {0;Dq\left( t \right)\Delta t,\Delta t;Dp\left( t \right)\Delta t,Dp_{t}\left( t \right)\Delta t} \right)} & \\  & {= \left( {0;\partial_{2}H\left( {t,q,p} \right)\Delta t,\Delta t; - \partial_{1}H\left( {t,q,p} \right)\Delta t, - \partial_{0}H\left( {t,q,p} \right)\Delta t} \right).} \tag{6.91} \\ \end{array}$$

#page(434)

The /ω/ form applied to these incremental states that form the edges of this parallelogram gives the area of the parallelogram:

$$\begin{array}{l} {\omega\left( {\zeta_{1},\zeta_{2}} \right)} \\ \begin{array}{lll} {\,\, = Q\left( \zeta_{1} \right)P\left( \zeta_{2} \right) - P\left( \zeta_{1} \right)Q\left( \zeta_{2} \right)} & & \\ {\,\, = (\Delta q,0)} & & \\ {\,\,\,\,\,\,\,\,\,\,\,\,\,\,.\left( {- \partial_{1}H\left( {t,q,p} \right)\Delta t, - \partial_{0}H\left( {t,q,p} \right)\Delta t} \right)} & & \\ {\,\, - \left( {\Delta p, - \partial_{1}H\left( {t,q,p} \right)\Delta q - \partial_{2}H\left( {t,q,p} \right)\Delta p} \right)} & & \\ {\,\,\,\,\,\,\,\,\,\,\,\,\,.\left( {\partial_{2}H\left( {t,q,p} \right)\Delta t,\Delta t} \right)} & & \\ {\,\, = 0.} \tag{6.92} & \\ \end{array} \\ \end{array}$$

So we may conclude that the integral of this expression over the entire surface of the tube of trajectories is also zero. Thus the Poincaré--Cartan integral invariant is zero for any region that is generated by time evolution.

Having proven that the trajectory tube provides no contribution, we have shown that the Poincaré integral invariant of the two endcaps is the same. This proves that time evolution generates a symplectic /qp/ transformation.

#### Area preservation of surfaces of section
We can use the Poincaré--Cartan invariant to prove that for autonomous two-degree-of-freedom systems, surfaces of section (constructed appropriately) preserve area.

To show this we consider a surface of section for one coordinate (say /q/_{2}) equal to zero. We construct the section by accumulating the (/q/_{1}, /p/_{1}) pairs. We assume that all initial conditions have the same energy. We compute the sum of the areas of canonical projections in the extended phase space again. Because all initial conditions have the same /q/_{2} = 0 there is no area on the /q/_{2}, /p/_{2} plane, and because all the trajectories have the same value of the Hamiltonian the area of the projection on the /t, p_{t}/ plane is also zero. So the sum of areas of the projections is just the area of the region on the surface of section. Now let each point on the surface of section evolve to the next section crossing. For each point on the section this may take a different amount of time. Compute the sum of the areas again for the mapped region. Again, all points of the mapped region have the same /q/_{2}, so the area on the /q/_{2}, /p/_{2} plane is zero, and they continue to have the same energy, so the area on the /t, p_{t}/ plane is zero. So the area of the mapped region is
#page(435)
again just the area on the surface of section, the /q/_{1}, /p/_{1} plane. Time evolution preserves the sum of areas, so the area on the surface of section is the same as the mapped area.

Thus surfaces of section preserve area provided that the section points are entirely on a canonical plane. For example, to make the Hénon--Heiles surfaces of section (see [section 3.6.3](chapter003!section_3.6.3)) we plotted /p_{y}/ versus /y/ when /x/ = 0 with /p_{x}/ ≥ 0. So for all section points the /x/ coordinate has the fixed value 0, the trajectories all have the same energy, and the points accumulated are entirely in the /y/, /p_{y}/ canonical plane. So the Hénon--Heiles surfaces of section preserve area.

##### 6.2.2 Yet Another View of Time Evolution
We can show directly from the action principle that time evolution generates a symplectic transformation.

Recall that the Lagrangian action /S/ is

$$\begin{matrix} {S\left\lbrack q \right\rbrack\left( {t_{1},t_{2}} \right) = {\int_{t_{1}}^{t_{2}}{L \circ \Gamma\left\lbrack q \right\rbrack.}}} \tag{6.93} \\ \end{matrix}$$

We computed the variation of the action in deriving the Lagrange equations. The variation is (see equation #Eqn(chapter001,1.33,1.33))

$$\begin{matrix} {{\delta_{\eta}S\left\lbrack q \right\rbrack\left( {t_{1},t_{2}} \right) = \left( {\partial_{2}L \circ \Gamma\left\lbrack q \right\rbrack} \right)\eta}|_{t_{1}}^{t_{2}}{- {\int_{t_{1}}^{t_{2}}{\left( {\mathcal{E}\left\lbrack L \right\rbrack \circ \Gamma\left\lbrack q \right\rbrack} \right)\eta}},}} \tag{6.94} \\ \end{matrix}$$

rewritten in terms of the Euler--Lagrange operator $\mathcal{E}$. In the derivation of the Lagrange equations we considered only variations that preserved the endpoints of the path being tested. However, equation (#Eqn(chapter006,6.94,6.94)) is true of arbitrary variations. Here we consider variations that are not zero at the endpoints around a realizable path /q/ (one for which $\mathcal{E}$[/L/] ∘ Γ[/q/] = 0). For these variations the variation of the action is just the integrated term:

$$\begin{matrix} {\delta_{\eta}S\left\lbrack q \right\rbrack\left( {t_{1},t_{2}} \right) = \left( {\partial_{2}L \circ \Gamma\left\lbrack q \right\rbrack} \right)\eta|_{t_{1}}^{t_{2}} = p\left( t_{2} \right)\eta\left( t_{2} \right) - p\left( t_{1} \right)\eta\left( t_{1} \right).} \tag{6.95} \\ \end{matrix}$$

Recall that /p/ and /η/ are structures, and the product implies a sum of products of components.

Consider a continuous family of realizable paths; the path for parameter /s/ is $\widetilde{q}\left( s \right)$ and the coordinates of this path at time /t/ are $\widetilde{q}\left( s \right)\left( t \right)$. We define

η˜(s)=Dq˜(s)

; the variation of the path along
#page(436)
the family is the derivative of the parametric path with respect to the parameter. Let

$$\begin{matrix} {\widetilde{S}\left( s \right) = S\left\lbrack {\widetilde{q}\left( s \right)} \right\rbrack\left( {t_{1},t_{2}} \right)} \tag{6.96} \\ \end{matrix}$$

be the value of the action from /t/_{1} to /t/_{2} for path

q˜(s)

. The derivative of the action along this parametric family of paths is#Footnote(7)

$$\begin{array}{lll} {D\widetilde{S}\left( s \right)} & {= \delta_{\widetilde{\eta}{(s)}}S\left\lbrack {\widetilde{q}\left( s \right)} \right\rbrack} & \\  & {= \left( {\partial_{2}L \circ \Gamma\left\lbrack {\widetilde{q}\left( s \right)} \right\rbrack} \right)\widetilde{\eta}\left( s \right)|_{t_{1}}^{t_{2}} - {\int_{t_{1}}^{t_{2}}{\left( {\mathcal{E}\left\lbrack L \right\rbrack \circ \Gamma\left\lbrack {\widetilde{q}\left( s \right)} \right\rbrack} \right)\widetilde{\eta}\left( s \right).}}} \tag{6.97} \\ \end{array}$$

Because $\widetilde{q}\left( s \right)$ is a realizable path,$\mathcal{E}\left\lbrack L \right\rbrack \circ \Gamma\left\lbrack {\widetilde{q}\left( s \right)} \right\rbrack = 0 $. So

$$\begin{array}{lll} {D\widetilde{S}(s)} & {= \left( {\partial_{2}L \circ \Gamma\left\lbrack {\widetilde{q}\left( s \right)} \right\rbrack} \right)\widetilde{\eta}\left( s \right)|_{t_{1}}^{t_{2}}} & \\  & {= \widetilde{p}\left( s \right)\left( t_{2} \right)\widetilde{\eta}\left( s \right)\left( t_{2} \right) - \widetilde{p}\left( s \right)\left( t_{1} \right)\widetilde{\eta}\left( s \right)\left( t_{1} \right),} \tag{6.98} \\ \end{array}$$

where $\widetilde{p}\left( s \right)$ is the momentum conjugate to $\widetilde{q}\left( s \right)$. The integral of $ D\widetilde{S}$ is

$$\begin{array}{lll} {S\left\lbrack {\widetilde{q}\left( s_{2} \right)} \right\rbrack\left( {t_{1},t_{2}} \right) - S\left\lbrack {\widetilde{q}\left( s_{1} \right)} \right\rbrack\left( {t_{1},t_{2}} \right)} & {= {\int_{s_{1}}^{s_{2}}\left( {D\widetilde{S}} \right)}} & \\  & {= {\int_{s_{1}}^{s_{2}}{\left( {h(t_{2}) - h\left( t_{1} \right)} \right),}}} \tag{6.99} \\ \end{array}$$

where

$$\begin{matrix} {h\left( t \right)\left( s \right) = \widetilde{p}\left( s \right)\left( t \right)\widetilde{\eta}\left( s \right)\left( t \right) = \widetilde{p}\left( s \right)\left( t \right)D\widetilde{q}\left( s \right)\left( t \right).} \tag{6.100} \\ \end{matrix}$$

In conventional notation the latter line integral is written

$$\begin{matrix} {{\int_{\gamma_{2}}{\sum\limits_{i}{p_{i}dq^{i} -}}}{\int_{\gamma_{1}}{\sum\limits_{i}{p_{i}dq^{i}}}},} \tag{6.101} \\ \end{matrix}$$

where $\gamma_{1}\left( s \right) = \widetilde{q}\left( s \right)\left( t_{1} \right)\,$ and $\gamma_{2}\left( s \right) = \widetilde{q}\left( s \right)\left( t_{2} \right)$.

#page(437)

For a loop family of paths (such that $\widetilde{q}\left( s_{2} \right) = \widetilde{q}\left( s_{1} \right)$), the difference of actions at the endpoints vanishes, so we deduce

$$\begin{matrix} {\oint_{\gamma_{2}}{\sum\limits_{i}{p_{i}dq^{i} = {\oint_{\gamma_{1}}{\sum\limits_{i}{p_{i}dq^{i},}}}}}} \tag{6.102} \\ \end{matrix}$$

which is the line-integral version of the integral invariants.

In terms of area integrals, using Stokes's theorem, this is

$$\begin{matrix} \begin{matrix} {\sum\limits_{i}{\int_{R_{2}^{i}}{dp_{i}dq^{i} =}}} & {\sum\limits_{i}{\int_{R_{1}^{i}}{dp_{i}dq^{i},}}} \\ \end{matrix} \tag{6.103} \\ \end{matrix}$$

where $ R_{j}^{i}$ are the regions in the /i/th canonical plane. We have found that the time evolution preserves the integral invariants, and thus time evolution generates a symplectic transformation.

### 6.3 Lie Transforms
The evolution of a system under any Hamiltonian generates a continuous family of canonical transformations. To study the behavior of some system governed by a Hamiltonian /H/, it is sometimes appropriate to use a canonical transformation generated by evolution governed by another Hamiltonian-like function /W/ on the same phase space. Such a canonical transformation is called a /Lie transform/.

The functions /H/ and /W/ are both Hamiltonian-shaped functions defined on the same phase space. Time evolution for an interval Δ governed by /H/ is a canonical transformation $\mathcal{C}_{\Delta,H}$. Evolution by /W/ for an interval /ϵ/ is a canonical transformation $\mathcal{C}_{\mathit{\epsilon},W}^{\prime}$:

$$\begin{matrix} {\left( {t,q,p} \right) = \mathcal{C}_{\mathit{\epsilon},W}^{\prime}\left( {t,q\prime,p\prime} \right).} \tag{6.104} \\ \end{matrix}$$

The independent variable in the /H/ evolution is time, and the independent variable in the /W/ evolution is an arbitrary parameter of the canonical transformation. We chose $\mathcal{C}\prime $ for the /W/ evolution so that the canonical transformation induced by /W/ does not change the time in the system governed by /H/.

#page(438)

#Image(Art_P1186.jpg,figure_6.2)
#Caption *Figure 6.2* Time evolution of a trajectory started at the point (/t/_{0}, /q/_{0}, /p/_{0}), governed by the Hamiltonian /H/, is transformed by the Lie transform governed by the generator /W/. The time evolution of the transformed trajectory is governed by the Hamiltonian /H/′. #CaptionEnd

[Figure 6.2](#figure_6.2) shows how a Lie transform is used to transform a trajectory. We can see from the diagram that the canonical transformations obey the relation

$$\begin{matrix} {\mathcal{C}_{\mathit{\epsilon},W}^{\prime} \circ \mathcal{C}_{\Delta,H\prime} = \mathcal{C}_{\Delta,H} \circ \mathcal{C}_{\mathit{\epsilon},W}^{\prime}.} \tag{6.105} \\ \end{matrix}$$

For generators /W/ that do not depend on the independent variable, the resulting canonical transformation $\mathcal{C}_{\mathit{\epsilon},W}^{\prime}$ is time independent and symplectic. A time-independent symplectic transformation is canonical if the Hamiltonian transforms by composition:#Footnote(8)

#page(439)

$$\begin{matrix} {H\prime = H \circ \mathcal{C}_{\mathit{\epsilon},W}^{\prime}.} \tag{6.106} \\ \end{matrix}$$

We will use only Lie transforms that have generators that do not depend on the independent variable.

#### Lie transforms of functions
The value of a phase-space function /F/ changes if its arguments change. We define the function $ E_{\mathit{\epsilon},W}^{\prime}$ of a function /F/ of phase-space coordinates (/t/, /q/, /p/) by

$$\begin{matrix} {E_{\mathit{\epsilon},W}^{\prime}F = F \circ \mathcal{C}_{\mathit{\epsilon},W}^{\prime}.} \tag{6.107} \\ \end{matrix}$$

We say that $ E_{\mathit{\epsilon},W}^{\prime}F $ is the Lie transform of the function /F/.

In particular, the Lie transform advances the coordinate and momentum selector functions /Q/ = /I/_{1} and /P/ = /I/_{2}:

$$\begin{array}{ll} {\left( {E_{\mathit{\epsilon},W}^{\prime}Q} \right)\left( {t,q\prime,p\prime} \right) = \left( {Q \circ \mathcal{C}_{\mathit{\epsilon},W}^{\prime}} \right)\left( {t,q\prime,p\prime} \right) = Q\left( {t,q,p} \right) = q} & \\ {\left( {E_{\mathit{\epsilon},W}^{\prime}P} \right)\left( {t,q\prime,p\prime} \right) = \left( {P \circ \mathcal{C}_{\mathit{\epsilon},W}^{\prime}} \right)\left( {t,q\prime,p\prime} \right) = P\left( {t,q,p} \right) = p.} \tag{6.108} \\ \end{array}$$

So we may restate equation (#Eqn(chapter006,6.107,6.107)) as

$$\begin{array}{ll} {\left( {E_{\mathit{\epsilon},W}^{\prime}F} \right)\left( {t,q\prime,p\prime} \right)} & \\ {\,\,\,\,\,\,\,\,\,\,\, = F\left( {t,\left( {E_{\mathit{\epsilon},W}^{\prime}Q} \right)\left( {t,q\prime,p\prime} \right),\left( {E_{\mathit{\epsilon},W}^{\prime}P} \right)\left( {t,q\prime,p\prime} \right)} \right).} \tag{6.109} \\ \end{array}$$

More generally, Lie transforms descend into compositions:

$$\begin{matrix} {\left( {E_{\mathit{\epsilon},W}^{\prime}\left( {F \circ G} \right)} \right) = F \circ \left( {E_{\mathit{\epsilon},W}^{\prime}G} \right)} \tag{6.110} \\ \end{matrix}$$

A corollary of the fact that Lie transforms descend into compositions is:

$$\begin{array}{lll} {E_{\mathit{\epsilon}_{1},W_{1}}^{\prime}E_{\mathit{\epsilon}_{2},W_{2}}^{\prime}I} & {= \left( {E_{\mathit{\epsilon}_{1},W_{1}}^{\prime}\left( {E_{\mathit{\epsilon}_{2},W_{2}}^{\prime}I} \right)} \right) \circ I} & \\  & {= \left( {E_{\mathit{\epsilon}_{2},W_{2}}^{\prime}I} \right) \circ \left( {E_{\mathit{\epsilon}_{1},W_{1}}^{\prime}I} \right),} \tag{6.111} \\ \end{array}$$

where /I/ is the phase-space identity function: /I/(/t/, /q/, /p/) = (/t/, /q/, /p/). So the order of application of the operators is reversed from the order of composition of the functions that result from applying the operators.

In terms of $ E_{\mathit{\epsilon},W}^{\prime}$ we have the canonical transformation

$$\begin{array}{lll} {\,\,\, q} & {= \left( {E_{\mathit{\epsilon},W}^{\prime}Q} \right)\left( {t,q\prime,p\prime} \right)} & \\ {\,\,\, p} & {= \left( {E_{\mathit{\epsilon},W}^{\prime}P} \right)\left( {t,q\prime,p\prime} \right)} & \\ {H\prime} & {= E_{\mathit{\epsilon},W}^{\prime}H.} \tag{6.112} \\ \end{array}$$

#page(440)

We can also say

$$\begin{matrix} {\left( {t,q,p} \right) = \left( {E_{\mathit{\epsilon},W}^{\prime}I} \right)\left( {t,q\prime,p\prime} \right).} \tag{6.113} \\ \end{matrix}$$

Note that $ E_{\mathit{\epsilon},W}^{\prime}$ has the property:#Footnote(9)

$$\begin{matrix} {E_{\mathit{\epsilon}_{1} + \mathit{\epsilon}_{2},W}^{\prime} = E_{\mathit{\epsilon}_{1},W}^{\prime} \circ E_{\mathit{\epsilon}_{2},W}^{\prime} = E_{\mathit{\epsilon}_{2},W}^{\prime} \circ E_{\mathit{\epsilon}_{1},W}^{\prime}.} \tag{6.114} \\ \end{matrix}$$

The identity /I/ is

$$\begin{matrix} {I = E_{0,W}^{\prime}.} \tag{6.115} \\ \end{matrix}$$

We can define the inverse function

$$\begin{matrix} {\left( E_{\mathit{\epsilon},W}^{\prime} \right)^{- 1} = E_{- \mathit{\epsilon},W}^{\prime}} \tag{6.116} \\ \end{matrix}$$

with the property

$$\begin{matrix} {I = E_{\mathit{\epsilon},W}^{\prime} \circ \left( E_{\mathit{\epsilon},W}^{\prime} \right)^{- 1} = \left( E_{\mathit{\epsilon},W}^{\prime} \right)^{- 1} \circ E_{\mathit{\epsilon},W}^{\prime}.} \tag{6.117} \\ \end{matrix}$$

#### Simple Lie transforms
For example, suppose we are studying a system for which a rotation would be a helpful transformation. To concoct such a transformation we note that we intend a configuration coordinate to increase uniformly with a given rate. In this case we want an angle to be incremented. The Hamiltonian that consists solely of the momentum conjugate to that configuration coordinate always does the job. So the angular momentum is an appropriate generator for rotations.

The analysis is simple if we use polar coordinates /r/, /θ/ with conjugate momenta /p_{r}/, /p_{θ}/. The generator /W/ is just:

$$\begin{matrix} {W\left( {\tau;r,\theta;p_{r},p_{\theta}} \right) = p_{\theta}} \tag{6.118} \\ \end{matrix}$$

The family of transformations satisfies Hamilton's equations:

$$\begin{array}{ll} {\,\,\, Dr = 0} & \\ {\,\,\, D\theta = 1} & \\ {Dp_{r} = 0} & \\ {Dp_{\theta} = 0.} \tag{6.119} \\ \end{array}$$

#page(441)

The only variable that appears in /W/ is /p_{θ}/, so /θ/ is the only variable that varies as /ϵ/ is varied. In fact, the family of canonical transformations is

$$\begin{array}{ll} {\,\,\,\, r = r\prime} & \\ {\,\,\,\theta = \theta\prime + \mathit{\epsilon}} & \\ {p_{r} = p_{r}^{\prime}} & \\ {p_{\theta} = p_{\theta}^{\prime}.} \tag{6.120} \\ \end{array}$$

So angular momentum is the generator of a canonical rotation.

The example is simple, but it illustrates one important feature of Lie transformations---they give one set of variables entirely in terms of the other set of variables. This should be contrasted with the mixed-variable generating function transformations, which always give a mixture of old and new variables in terms of a mixture of new and old variables, and thus require an inversion to get one set of variables in terms of the other set of variables. This inverse can be written in closed form only for special cases. In general, there is considerable advantage in using a transformation rule that generates explicit transformations from the start. The Lie transformations are always explicit in the sense that they give one set of variables in terms of the other, but for there to be explicit expressions the evolution governed by the generator must be solvable.

Let's consider another example. This time consider a three-degree-of-freedom problem in rectangular coordinates, and take the generator of the transformation to be the /z/ component of the angular momentum:

$$\begin{matrix} {W\left( {\tau;x,y,z;p_{x},p_{y},p_{z}} \right) = xp_{y} - yp_{x}.} \tag{6.121} \\ \end{matrix}$$

The evolution equations are

$$\begin{array}{ll} {\,\,\, D_{x} = - y} & \\ {\,\,\, D_{y} = x} & \\ {\,\,\, D_{z} = 0} & \\ {Dp_{x} = - p_{y}} & \\ {Dp_{y} = p_{x}} & \\ {Dp_{z} = 0.} \tag{6.122} \\ \end{array}$$

#page(442)

We notice that /z/ and /p_{z}/ are unchanged, and that the equations governing the evolution of /x/ and /y/ decouple from those of /p_{x}/ and /p_{y}/. Each of these pairs of equations represents simple harmonic motion, as can be seen by writing them as second-order systems. The solutions are

$$\begin{array}{ll} {x = x\prime\,\cos\,\mathit{\epsilon} - y\prime\,\sin\,\mathit{\epsilon}} & \\ {y = x\prime\,\sin\,\mathit{\epsilon} + y\prime\,\cos\,\mathit{\epsilon}} & \\ {z = z\prime,} \tag{6.123} \\ \end{array}$$

$$\begin{array}{ll} {p_{x} = p_{x}^{\prime}\cos\,\mathit{\epsilon} - p_{y}^{\prime}\sin\,\mathit{\epsilon}} & \\ {p_{y} = p_{x}^{\prime}\,\sin\,\mathit{\epsilon} + p_{y}^{\prime}\cos\,\mathit{\epsilon}} & \\ {p_{z} = p_{z}^{\prime}.} \tag{6.124} \\ \end{array}$$

So we see that again a component of the angular momentum generates a canonical rotation. There was nothing special about our choice of axes, so we can deduce that the component of angular momentum about any axis generates rotations about that axis.

#### Example
Suppose we have a system governed by the Hamiltonian

$$\begin{matrix} {H\left( {t;x,y;p_{x},p_{y}} \right) = \frac{1}{2}\left( {p_{x}^{2} + p_{y}^{2}} \right) + \frac{1}{2}a\left( {x - y} \right)^{2} + \frac{1}{2}b\left( {x + y} \right)^{2}.} \tag{6.125} \\ \end{matrix}$$

Hamilton's equations couple the motion of /x/ and /y/:

$$\begin{array}{ll} {\,\,\, Dx = p_{x}} & \\ {\,\,\, Dy = p_{y}} & \\ {Dp_{x} = - a\left( {x - y} \right) - b\left( {x + y} \right)} & \\ {Dp_{y} = a\left( {x - y} \right) - b\left( {x + y} \right).} \tag{6.126} \\ \end{array}$$

We can decouple the system by performing a coordinate rotation by /π//4. This is generated by

$$\begin{matrix} {W\left( {\tau;x,y;p_{x},p_{y}} \right) = xp_{y} - yp_{x},} \tag{6.127} \\ \end{matrix}$$

which is similar to the generator for the coordinate rotation above but without the /z/ degree of freedom. Evolving (/τ/; /x/, /y/; /p_{x}, p_{y}/) by /W/ for an interval of /π//4 gives a canonical rotation:

#page(443)

$$\begin{array}{ll} {\,\, x = x\prime\cos\pi/4 - y\prime\sin\pi/4} & \\ {\,\, y = x\prime\sin\pi/4 + y\prime\cos\pi/4} & \\ {p_{x} = p_{x}^{\prime}\cos\pi/4 - p_{y}^{\prime}\sin\pi/4} & \\ {p_{y} = p_{x}^{\prime}\sin\pi/4 + p_{y}^{\prime}\cos\pi/4.} \tag{6.128} \\ \end{array}$$

Composing the Hamiltonian /H/ with this time-independent transformation gives the new Hamiltonian

$$\begin{matrix} {H\prime\left( {t;x\prime,y\prime;p_{x}^{\prime},p_{y}^{\prime}} \right) = \left( {\frac{1}{2}\left( p_{x}^{\prime} \right)^{2} + b\left( x\prime \right)^{2}} \right) + \left( {\frac{1}{2}\left( p_{y}^{\prime} \right)^{2} + a\left( y\prime \right)^{2}} \right),} \tag{6.129} \\ \end{matrix}$$

which is a Hamiltonian for two uncoupled harmonic oscillators. So the original coupled problem has been transformed by a Lie transform to a new form for which the solution is easy.

### 6.4 Lie Series
A convenient way to compute a Lie transform is to approximate it with a series. We develop this technique by extending the idea of a Taylor series.

Taylor's theorem gives us a way of approximating the value of a nice enough function at a point near to a point where the value is known. If we know /f/ and all of its derivatives at /t/ then we can get the value of /f/(/t/ + /ϵ/), for small enough /ϵ/, as follows:

$$\begin{matrix} {f\left( {t + \mathit{\epsilon}} \right) = f\left( t \right) + \mathit{\epsilon}Df\left( t \right) + \frac{1}{2}\mathit{\epsilon}^{2}D^{2}f\left( t \right) + \cdots + \frac{1}{n!}\mathit{\epsilon}^{n}D^{n}f\left( t \right) + \cdots.} \tag{6.130} \\ \end{matrix}$$

We recall that the power series for the exponential function is

$$\begin{matrix} {e^{x} = 1 + x + \frac{1}{2}x^{2} + \cdots + \frac{1}{n!}x^{n} + \cdots.} \tag{6.131} \\ \end{matrix}$$

This suggests that we can formally construct a Taylor-series operator as the exponential of a differential operator#Footnote(10)

$$\begin{matrix} {e^{\mathit{\epsilon}D} = I + \mathit{\epsilon}D + \frac{1}{2}\left( {\mathit{\epsilon}D} \right)^{2} + \cdots + \frac{1}{n!}\left( {\mathit{\epsilon}D} \right)^{n} + \cdots} \tag{6.132} \\ \end{matrix}$$

and write

$$\begin{matrix} {f\left( {t + \mathit{\epsilon}} \right) = \left( {e^{\mathit{\epsilon}D}f} \right)(t).} \tag{6.133} \\ \end{matrix}$$

#page(444)

We have to be a bit careful here: (/ϵD/)^{2} = /ϵDϵD/. We can turn it into /ϵ/^{2}/D/^{2} only because /ϵ/ is a scalar constant, which commutes with every differential operator. But with this caveat in mind we can define the differential operator

$$\begin{matrix} {\left( {e^{\mathit{\epsilon}D}f} \right)\left( t \right) = f\left( t \right) + \mathit{\epsilon}Df\left( t \right) + \frac{1}{2}\mathit{\epsilon}^{2}D^{2}f\left( t \right) + \cdots + \frac{1}{n!}\mathit{\epsilon}^{n}D^{n}f\left( t \right) + \cdots} \tag{6.134} \\ \end{matrix}$$

Before going on, it is interesting to compute with these a bit. In the code transcripts that follow we develop the series by exponentiation. We can examine the series incrementally by looking at successive elements of the (infinite) sequence of terms of the series. The procedure series:for-each is an incremental traverser that applies its first argument to successive elements of the series given as its second argument. The third argument (when given) specifies the number of terms to be traversed. In each of the following transcripts we print simplified expressions for the successive terms.

The first thing to look at is the general Taylor expansion for an unknown literal function, expanded around /t/, with increment /ϵ/. Understanding what we see in this simple problem will help us understand more complex problems later.
```Scheme
(series:for-each print-expression (((exp (* 'epsilon D)) (literal-function 'f)) 't) 6) 
```
```Scheme
(f t) (* ((D f) t) epsilon) (* 1/2 (((expt D 2) f) t) (expt epsilon 2)) (* 1/6 (((expt D 3) f) t) (expt epsilon 3)) (* 1/24 (((expt D 4) f) t) (expt epsilon 4)) (* 1/120 (((expt D 5) f) t) (expt epsilon 5)) ... 
```
We can also look at the expansions of particular functions that we recognize, such as the expansion of sin around 0.
```Scheme
(series:for-each print-expression (((exp (* 'epsilon D)) sin) 0) 6) 
```
```Scheme
0 epsilon 0 (* -1/6 (expt epsilon 3)) 0 (* 1/120 (expt epsilon 5)) ... 
```
#page(445)

It is often instructive to expand functions we usually don't remember, such as $ f\left( x \right) = \sqrt{1 + x}$.
```Scheme
(series:for-each print-expression (((exp (* 'epsilon D)) (lambda (x) (sqrt (+ x 1)))) 0) 6) 
```
```Scheme
1 (* 1/2 epsilon) (* -1/8 (expt epsilon 2)) (* 1/16 (expt epsilon 3)) (* -5/128 (expt epsilon 4)) (* 7/256 (expt epsilon 5)) ... 
```
### Exercise 6.7: Binomial series

Develop the binomial expansion of (1 + /x/)^{n} as a Taylor expansion. Of course, it must be the case that for /n/ a positive integer all of the coefficients except for the first /n/ + 1 are zero. However, in the general case, for symbolic /n/, the coefficients are rather complicated polynomials in /n/. For example, you will find that the eighth term is
```Scheme
(+ (* 1/5040 (expt n 7)) (* -1/240 (expt n 6)) (* 5/144 (expt n 5)) (* -7/48 (expt n 4)) (* 29/90 (expt n 3)) (* -7/20 (expt n 2)) (* 1/7 n)) 
```
These terms must evaluate to the entries in Pascal's triangle. In particular, this polynomial must be zero for /n/ < 7. How is this arranged?

#### Dynamics
Now, to play this game with dynamical functions we want to provide a derivative-like operator that we can exponentiate, which will give us the time-advance operator. The key idea is to write
#page(446)
the derivative of the function in terms of the Poisson bracket. Equation (#Eqn(chapter003,3.80,3.80)) shows how to do this in general:

$$\begin{matrix} {D\left( {F \circ \sigma} \right) = \left( {\left\{ {F,H} \right\} + \partial_{0}F} \right) \circ \sigma.} \tag{6.135} \\ \end{matrix}$$

We define the operator /D_{H}/ by

$$\begin{matrix} {D_{H}F = \partial_{0}F + \left\{ {F,H} \right\},} \tag{6.136} \\ \end{matrix}$$

so

$$\begin{matrix} {D_{H}F \circ \sigma = D\left( {F \circ \sigma} \right),} \tag{6.137} \\ \end{matrix}$$

and iterates of this operator can be used to compute higher-order derivatives:

$$\begin{matrix} {D^{n}\left( {F \circ \sigma} \right) = D_{H}^{n}F \circ \sigma.} \tag{6.138} \\ \end{matrix}$$

We can express the advance of the path function /f/ = /F/ ∘ /σ/ for an interval /ϵ/ with respect to /H/ as a power series in the derivative operator /D_{H}/ applied to the phase-space function /F/ and then composed with the path:

$$\begin{matrix} {f\left( {t + \mathit{\epsilon}} \right) = \left( {e^{\mathit{\epsilon}D}f} \right)\left( t \right) = \left( {e^{\mathit{\epsilon}D_{H}}F} \right) \circ \sigma\left( t \right).} \tag{6.139} \\ \end{matrix}$$

Indeed, we can implement the time-advance operator /E/_{/ϵ/,H} with this series, when it converges.

### Exercise 6.8: Iterated derivatives

Show that equation (#Eqn(chapter006,6.138,6.138)) is correct.

### Exercise 6.9: Lagrangian analog

Compare /D/_{H} with the total time derivative operator. Recall that $ D_{t}F \circ \Gamma\left\lbrack q \right\rbrack = D\left( {F \circ \Gamma\left\lbrack q \right\rbrack} \right)$ abstracts the derivative of a function of a path through state space to a function of the derivatives of the path. Define another derivative operator /D_{L}/, analogous to /D_{H}/, that would give the time derivative of functions along Lagrangian state paths that are solutions of Lagrange's equations for a given Lagrangian. How might this be useful?

For time-independent Hamiltonian /H/ and time-independent state function /F/, we can simplify the computation of the advance
#page(447)
of /F/. In this case we define the /Lie derivative operator L_{H}/ such that

$$\begin{matrix} {L_{H}F = \left\{ {F,H} \right\},} \tag{6.140} \\ \end{matrix}$$

which reads “the Lie derivative of /F/ with respect to /H/.”#Footnote(11) So

$$\begin{matrix} {D_{H} = \partial_{0} + L_{H}} \tag{6.141} \\ \end{matrix}$$

and for time-independent /F/

$$\begin{matrix} {D\left( {F \circ \sigma} \right) = L_{H}F \circ \sigma.} \tag{6.142} \\ \end{matrix}$$

We can iterate this process to compute higher derivatives. So

$$\begin{matrix} {L_{H}^{2}F = \left\{ {\left\{ {F,H} \right\},H} \right\},} \tag{6.143} \\ \end{matrix}$$

and successively higher-order Poisson brackets of /F/ with /H/ give successively higher-order derivatives when evaluated on the trajectory.

Let /f/ = /F/ ∘ /σ/. We have

$$\begin{matrix} {Df = \left( {L_{H}F} \right) \circ \sigma} \tag{6.144} \\ \end{matrix}$$

$$\begin{array}{ll} {D^{2}f = \left( {L_{H}^{2}F} \right) \circ \sigma} & \\ {\cdots.} \tag{6.145} \\ \end{array}$$

Thus we can rewrite the advance of the path function /f/ for an interval /ϵ/ with respect to /H/ as a power series in the Lie derivative operator applied to the phase-space function /F/ and then composed with the path:

$$\begin{matrix} {f\left( {t + \mathit{\epsilon}} \right) = \left( {e^{\mathit{\epsilon}D}f} \right)\left( t \right) = \left( {e^{\mathit{\epsilon}L_{H}}F} \right) \circ \sigma\left( t \right).} \tag{6.146} \\ \end{matrix}$$

We can implement the time-advance operator $ E_{\mathit{\epsilon},H}^{\prime}$ with the /Lie series/$ e^{\mathit{\epsilon}L_{H}}F $ when this series converges:

$$\begin{matrix} {E_{\mathit{\epsilon},H}^{\prime}F = e^{\mathit{\epsilon}L_{H}}F.} \tag{6.147} \\ \end{matrix}$$

#page(448)

We have shown that time evolution is canonical, so the series above are formal representations of canonical transformations as power series in the time. These series may not converge, even if the evolution governed by the Hamiltonian /H/ is well defined.

#### Computing Lie series
We can use the Lie transform as a computational tool to examine the local evolution of dynamical systems. We define the Lie derivative of /F/ as a derivative-like operator relative to the given Hamiltonian function, /H/:#Footnote(12)
```Scheme
(define ((Lie-derivative H) F) (Poisson-bracket F H)) 
```
We also define a procedure to implement the Lie transform:#Footnote(13)
```Scheme
(define (Lie-transform H t) (exp (* t (Lie-derivative H)))) 
```
Let's start by examining the beginning of the Lie series for the position of a simple harmonic oscillator of mass /m/ and spring constant /k/. We can implement the Hamiltonian as
```Scheme
(define ((H-harmonic m k) state) (+ (/ (square (momentum state)) (* 2 m)) (* 1/2 k (square (coordinate state))))) 
```
We make the Lie transform (series) by passing the Lie-transform operator an appropriate Hamiltonian function and an interval to evolve for. The resulting operator is then given the coordinate procedure, which selects the position coordinates from the phase-space state. The Lie transform operator returns a procedure that, when given a phase-space state composed of a dummy time, a
#page(449)
position x0, and a momentum p0, returns the position resulting from advancing that state by the interval dt.
```Scheme
(series:for-each print-expression (((Lie-transform (H-harmonic 'm 'k) 'dt) coordinate) (up 0 'x0 'p0)) 6)
```
```Scheme
x0 (/ (* dt p0) m) (/ (* -1/2 (expt dt 2) k x0) m) (/ (* -1/6 (expt dt 3) k p0) (expt m 2)) (/ (* 1/24 (expt dt 4) (expt k 2) x0) (expt m 2)) (/ (* 1/120 (expt dt 5) (expt k 2) p0) (expt m 3)) ... 
```
We should recognize the terms of this series. We start with the initial position /x/_{0}. The first-order correction (/p/_{0}//m/)/dt/ is due to the initial velocity. Next we find an acceleration term (−/kx/_{0}/2/m/)/dt/^{2} due to the restoring force of the spring at the initial position.

The Lie transform is just as appropriate for showing us how the momentum evolves over the interval:
```Scheme
(series:for-each print-expression (((Lie-transform (H-harmonic 'm 'k) 'dt) momentum) (up 0 'x0 'p0)) 6) 
```
```Scheme
p0 (* -1 dt k x0) (/ (* -1/2 (expt dt 2) k p0) m) (/ (* 1/6 (expt dt 3) (expt k 2) x0) m) (/ (* 1/24 (expt dt 4) (expt k 2) p0) (expt m 2)) (/ (* -1/120 (expt dt 5) (expt k 3) x0) (expt m 2)) ... 
```
In this series we see how the initial momentum /p/_{0} is corrected by the effect of the restoring force −/kx/_{0}/dt/, etc.

What is a bit more fun is to see how a more complex phase-space function is treated by the Lie series expansion. In the experiment below we examine the Lie series developed by advancing the harmonic-oscillator Hamiltonian, by means of the transform generated by the same harmonic-oscillator Hamiltonian:
```Scheme
(series:for-each print-expression (((Lie-transform (H-harmonic 'm 'k) 'dt) (H-harmonic 'm 'k)) (up 0 'x0 'p0)) 6) 
```
```Scheme
(/ (+ (* 1/2 k m (expt x0 2)) (* 1/2 (expt p0 2))) m) 0 0 0 0 0 ... 
```
As we would hope, the series shows us the original energy expression $\left( {k/2} \right)x_{0}^{2} + \left( {1/2m} \right)p_{0}^{2}$ as the first term. Each subsequent correction term turns out to be zero---because the energy is conserved.

Of course, the Lie series can be used in situations where we want to see the expansion of the motion of a system characterized by a more complex Hamiltonian. The planar motion of a particle in a general central field (see equation #Eqn(chapter003,3.100,3.100)) is a simple problem for which the Lie series is instructive. In the following transcript we can see how rapidly the series becomes complicated. It is worth one's while to try to interpret the additive parts of the third (acceleration) term shown below:
```Scheme
(series:for-each print-expression (((Lie-transform (H-central-polar 'm (literal-function 'U)) 'dt) coordinate) (up 0 (up 'r_0 'phi_0) (down 'p_r_0 'p_phi_0))) 4) 
```
```Scheme
(up r_0 phi_0) (up (/ (* dt p_r_0) m) (/ (* dt p_phi_0) (* m (expt r_0 2)))) (up (+ (/ (* -1/2 ((D U) r_0) (expt dt 2)) m) (/ (* 1/2 (expt dt 2) (expt p_phi_0 2)) (* (expt m 2) (expt r_0 3)))) (/ (* -1 (expt dt 2) p_phi_0 p_r_0) (* (expt m 2) (expt r_0 3)))) (up (+ (/ (* -1/6 (((expt D 2) U) r_0) (expt dt 3) p_r_0) (expt m 2)) (/ (* -1/2 (expt dt 3) (expt p_phi_0 2) p_r_0) (* (expt m 3) (expt r_0 4))))) (+ (/ (* 1/3 ((D U) r_0) (expt dt 3) p_phi_0) (* (expt m 2) (expt r_0 3)))) (/ (* -1/3 (expt dt 3) (expt p_phi_0 3)) (* (expt m 3) (expt r_0 6))) (/ (* (expt dt 3) p_phi_0 (expt p_r_0 2)) (* (expt m 3) (expt_r_0 4))) ... 
```
#page(451)

Of course, if we know the closed-form Lie transform it is probably a good idea to take advantage of it, but when we do not know the closed form the Lie series representation of it can come in handy.

### 6.5 Exponential Identities
The composition of Lie transforms can be written as products of exponentials of Lie derivative operators. In general, Lie derivative operators do not commute. If /A/ and /B/ are non-commuting operators, then the exponents do not combine in the usual way:

$$\begin{matrix} {e^{A}e^{B} \neq e^{A + B}.} \tag{6.148} \\ \end{matrix}$$

So it will be helpful to recall some results about exponentials of non-commuting operators.

We introduce the commutator

$$\begin{matrix} {\left\lbrack {A,B} \right\rbrack = AB - BA.} \tag{6.149} \\ \end{matrix}$$

The commutator is bilinear and satisfies the Jacobi identity

$$\begin{matrix} {\left\lbrack {A,\left\lbrack {B,C} \right\rbrack} \right\rbrack + \left\lbrack {B,\left\lbrack {C,A} \right\rbrack} \right\rbrack + \left\lbrack {C,\left\lbrack {A,B} \right\rbrack} \right\rbrack = 0,} \tag{6.150} \\ \end{matrix}$$

which is true for all /A/, /B/, and /C/.

We introduce a notation Δ/_{A}/ for the commutator with respect to the operator /A/:

$$\begin{matrix} {\Delta_{A}B = \left\lbrack {A,B} \right\rbrack.} \tag{6.151} \\ \end{matrix}$$

#page(452)

In terms of Δ the Jacobi identity is

$$\begin{matrix} {\left\lbrack {\Delta_{A},\Delta_{B}} \right\rbrack = \Delta_{\lbrack{A,B}\rbrack}.} \tag{6.152} \\ \end{matrix}$$

An important identity is

$$\begin{array}{lll} {e^{C}Ae^{- C}} & {= e^{\Delta C}A} & \\  & {= A + \left\lbrack {C,A} \right\rbrack + \frac{1}{2}\left\lbrack {C,\left\lbrack {C,A} \right\rbrack} \right\rbrack + \cdots.} \tag{6.153} \\ \end{array}$$

We can check this term by term.

We see that

$$\begin{matrix} {e^{C}A^{2}e^{- C} = e^{C}Ae^{- C}e^{C}Ae^{- C} = \left( {e^{C}Ae^{- C}} \right)^{2},} \tag{6.154} \\ \end{matrix}$$

using /e/^{−C}/e^{C}/ = /I/, the identity operator. Using the same trick, we find

$$\begin{matrix} {e^{C}A^{n}e^{- C} = \left( {e^{C}Ae^{- C}} \right)^{n}.} \tag{6.155} \\ \end{matrix}$$

More generally, if /f/ can be represented as a power series then

$$\begin{matrix} {e^{C}f\left( {A,B,\cdots} \right)e^{- C} = f\left( {e^{C}Ae^{- C},e^{C}Be^{- C},\cdots} \right).} \tag{6.156} \\ \end{matrix}$$

For instance, applying this to the exponential function yields

$$\begin{matrix} {e^{C}e^{A}e^{- C} = e^{e^{C}Ae^{- C}}.} \tag{6.157} \\ \end{matrix}$$

Using equation (#Eqn(chapter006,6.153,6.153)), we can rewrite this as

$$\begin{matrix} {e^{\Delta C}e^{A} = e^{e^{\Delta C}A}.} \tag{6.158} \\ \end{matrix}$$

### Exercise 6.10: Commutators of Lie derivatives

*a.* Let /W/ and /W/′ be two phase-space state functions. Use the Poisson-bracket Jacobi identity (#Eqn(chapter003,3.93,3.93)) to show

$$\begin{matrix} {\left\lbrack {L_{W,}L_{W\prime}} \right\rbrack = - L_{\{{W,W\prime}\}}.} \tag{6.159} \\ \end{matrix}$$

*b.* Consider the phase-space state functions that give the components of the angular momentum in terms of rectangular canonical coordinates $\begin{matrix} {J_{x}\left( {t;x,y,z;p_{x},p_{y},p_{z}} \right) = yp_{z} - zp_{y}} \\ {J_{y}\left( {t;x,y,z;p_{x},p_{y},p_{z}} \right) = zp_{x} - xp_{z}} \\ {J_{z}\left( {t;x,y,z;p_{x},p_{y},p_{z}} \right) = xp_{y} - yp_{x.}} \\ \end{matrix}$#page(453)

Show

$$\begin{matrix} {\left\lbrack {L_{J_{x}},L_{J_{y}}} \right\rbrack + L_{J_{z}} = 0.} \tag{6.160} \\ \end{matrix}$$

*c.* Relate the Jacobi identity for operators to the Poisson-bracket Jacobi identity.

### Exercise 6.11: Baker--Campbell--Hausdorff

Derive the rule for combining exponentials of non-commuting operators:

$$\begin{matrix} {e^{A}e^{B} = e^{A + B + \frac{1}{2}{\lbrack{A,B}\rbrack} + \cdots}.} \tag{6.161} \\ \end{matrix}$$

### 6.6 Summary
The time evolution of any Hamiltonian system induces a canonical transformation: if we consider all possible initial states of a Hamiltonian system and follow all of the trajectories for the same time interval, then the map from the initial state to the final state of each trajectory is a canonical transformation. This is true for any interval we choose, so time evolution generates a continuous family of canonical transformations.

We generalized this idea to generate continuous canonical transformations other than those generated by time evolution. Such transformations will be especially useful in support of perturbation theory.

In rare cases a canonical transformation can be made to a representation in which the problem is easily solvable: when all coordinates are cyclic and all the momenta are conserved. Here we investigated the Hamilton--Jacobi method for finding such canonical transformations. For problems for which the Hamilton--Jacobi method works, we find that the time evolution of the system is given as a canonical transformation.

### 6.7 Projects
### Exercise 6.12: Symplectic integration

Consider a system for which the Hamiltonian /H/ can be split into two parts, /H/_{0} and /H/_{1}, each of which describes a system that can be efficiently evolved:

$$\begin{matrix} {H = H_{0} + H_{1}.} \tag{6.162} \\ \end{matrix}$$

#page(454)

Symplectic integrators construct approximate solutions for the Hamiltonian /H/ from those of /H/_{0} and /H/_{1}.

We construct a map of the phase space onto itself in the following way (see [47](bibliography!bib_47), [48](bibliography!bib_48), [49](bibliography!bib_49)). Define /δ/_{2/π/}(/t/) to be an infinite sum of Dirac delta functions, with interval 2/π/,

$$\begin{matrix} {\delta_{2\pi}\left( t \right) = {\sum\limits_{n = - \infty}^{\infty}{\delta\left( {t - 2\pi n} \right),}}} \tag{6.163} \\ \end{matrix}$$

with representation as a Fourier series

$$\begin{matrix} {2\pi\delta_{2\pi}\left( t \right) = {\sum\limits_{n = - \infty}^{\infty}{\cos\left( {nt} \right).}}} \tag{6.164} \\ \end{matrix}$$

Recall that a /δ/ function has the property that $\int_{- a}^{a}{f\delta = f{(0)}}$ for any positive /a/ and continuous real-valued function /f/. It is fruitful to think of the delta function as a limit of a function Δ_{/>h/} that has the value Δ_{h}(/t/) = 1//h/ in the interval −/h//2 < /t/ < /h//2 and zero otherwise. Now consider the mapping Hamiltonian

$$\begin{matrix} {H_{m}\left( {t,q,p} \right) = H_{0}\left( {t,q,p} \right) + 2\pi\delta_{2\pi}\left( {\Omega t} \right)H_{1}\left( {t,q,p} \right).} \tag{6.165} \\ \end{matrix}$$

The evolution of the system between the delta functions is governed solely by /H/_{0}. To understand how the system evolves across the delta functions think of the delta functions in terms of Δ_{h} as /h/ goes to zero. Hamilton's equations contain terms from /H/_{1} with the factor 1//h/, which is large, and terms from /H/_{0} that are independent of /h/. So as /h/ goes to zero, /H/_{0} makes a negligible contribution to the evolution. The evolution across the delta functions is governed solely by /H/_{1}. The evolution of /H_{m}/ is obtained by alternately evolving the system according to the Hamiltonian /H/_{0} for an interval Δ/t/ = 2/π//Ω and then evolving the system according to the Hamiltonian /H/_{1} for the same time interval. The longer-term evolution of /H_{m}/ is obtained by iterating this map of the phase space onto itself. Fill in the details to show this.

*a.* In terms of Lie series, the evolution of /H_{m}/ for one delta function cycle Δ/t/ is generated by

$$\begin{matrix} {e^{\Delta t\, L_{H_{m}}}I = \left( {e^{\Delta t\, L_{H_{1}}}I} \right) \circ \left( {e^{\Delta t\, L_{H_{0}}}I} \right).} \tag{6.166} \\ \end{matrix}$$

The evolution of /H_{m}/ approximates the evolution of /H/. Identify the noncommuting operator /A/ with $ L_{H_{0}}$ and /B/ with $ L_{H_{1}}$.

Use the Baker--Campbell--Hausdorff identity (equation #Eqn(chapter006,6.161,6.161)) to deduce that the local truncation error (the error in the state after one step Δ/t/) is proportional to (Δ/t/)^{2}. This mapping is a first-order integrator.

*b.* By merely changing the phase of the delta functions, we can reduce the truncation error of the map, and the map becomes a second-order
#page(455)
integrator. Instead of making a map by alternating a full step Δ/t/ governed by /H/_{0} with a full step Δ/t/ governed by /H/_{1}, we can make a map by evolving the system for a half step Δ/t//2 governed by /H/_{0}, then for a full step Δ/t/ governed by /H/_{1}, and then for another half step Δ/t//2 governed by /H/_{0}. In terms of Lie series the second-order map is generated by

$$\begin{matrix} {e^{\Delta tL_{H_{m}}}I = \left( {e^{{({\Delta t/2})}L_{H_{0}}}I} \right) \circ \left( {e^{\Delta tL_{H_{1}}}I} \right) \circ \left( {e^{{({\Delta t/2})}L_{H_{0}}}I} \right).} \tag{6.167} \\ \end{matrix}$$

Confirm that the Hamiltonian governing the evolution of this map is the same as the one above but with the phase of the delta functions shifted. Show that the truncation error of one step of this second-order map is indeed proportional to (Δ/t/)^{3}.

*c.* Consider the Hénon--Heiles system. We can split the Hamiltonian (equation #Eqn(chapter003,3.135,3.135) on [page 252](chapter003!p252)) into two solvable Hamiltonians in the following way:

$$\begin{array}{ll} {H_{0}\left( {t;x,y;p_{x},p_{y}} \right) = \left( {p_{x}^{2} + p_{y}^{2}} \right)/2 + \left( {x^{2} + y^{2}} \right)/2} & \\ {H_{1}\left( {t;x,y;p_{x},p_{y}} \right) = x^{2}y - y^{3}/3.} \tag{6.168} \\ \end{array}$$

Hamiltonian /H/_{0} is the Hamiltonian of two uncoupled linear oscillators; Hamiltonian /H/_{1} is a nonlinear coupling. The trajectories of the systems described by each of these Hamiltonians can be expressed in closed form, so we do not need the Lie series for actually integrating each part. The Lie series expansions are used only to determine the order of the integrator.

Write programs that implement first-order and second-order maps for the Hénon--Heiles problem. Note that these maps cannot be of the same form as the Poincaré maps that we used to make surfaces of section, because these maps must take and return the entire state. (Why?) An appropriate template for such a map is (1st-order-map state dt). This procedure must return a state.

*d.* Examine the evolution of the energy for both chaotic and quasiperiodic initial conditions. How does the magnitude of the energy error scale with the step size? Is this consistent with the order of the integrator deduced above? How does the energy error grow with time?

*e.* The generation of surfaces of section from these maps is complicated by the fact that these maps have to maintain their state even though a plotting point might be required between two samples. The maps you made in part *c* regularly sample the state with the integrator timestep. If we must plot a point between two steps we cannot restart the integrator at the state of the plotted point, because that would lose the phase of the integrator step. To make this work the map must plot points but keep its rhythm, so we have to work around the fact that explore-map restarts at each plotted point. Here is some code that can be used to construct a Poincaré-type map that can be used with the explorer:
```Scheme
(define ((HH-collector win advance E dt sec-eps n) x y done fail) (define (monitor last-crossing-state state) (plot-point win (ref (coordinate last-crossing-state) 1) (ref (momentum last-crossing-state) 1))) (define (pmap x y cont fail) (find-next-crossing y advance dt sec-eps cont)) (define collector (default-collector monitor pmap n)) (cond ((and (up? x) (up? y)) ;passed states (collector x y done fail)) ((and (number? x) (number? y)) ;initialization (let ((initial-state (section->state E x y))) (if (not initial-state) (fail) (collector initial-state initial-state done fail)))) (else (error "bad input to HH-collector" x y)))) 
```
You will notice that the iteration of the map and the plotting of the points is included in this collector, so the map that this produces must replace these parts of the explorer. The #f argument to explore-map allows us to replace the appropriate parts of the explorer with our combination map iterator and plotter HH-collector.
```Scheme
(explore-map win (HH-collector win 1st-order-map 0.125 0.1 1.e-10 1000) #f) 
```
Generate surfaces of section using the second-order map. Does the map preserve the chaotic or quasiperiodic character of trajectories?

----

#FootnoteRef(1)Remember that ∂_{1,0} means the derivative with respect to the first coordinate position.

#FootnoteRef(2)Our theorems about which transformations are canonical are still valid, because a shift of time does not affect the symplectic condition. See footnote [14](chapter005!endnote_14) in [Chapter 5](chapter005).

#FootnoteRef(3)Partial derivatives of structured arguments do not generally commute, so this deduction is not as simple as it may appear.

#FootnoteRef(4)The transformation /S/_{Δ} is an identity on the /qp/ components, so it is symplectic. Although it adjusts the time, it is not a time-dependent transformation in that the /qp/ components do not depend upon the time. Thus, if we adjust the Hamiltonian by composition with /S/_{Δ} we have a canonical transformation.

#FootnoteRef(5)By Stokes's theorem we may compute the area of a region by a line integral around the boundary of the region. We define the positive sense of the area to be the area enclosed by a curve that is traversed in a counterclockwise direction, when drawn on a plane with the coordinate on the abscissa and the momentum on the ordinate.

#FootnoteRef(6)We can see this as follows. Let /γ/ be any closed curve in the boundary. This curve divides the boundary into two regions. By Stokes's theorem the integral invariant over both of these pieces can be written as a line integral along this boundary, but they have opposite signs, because /γ/ is traversed in opposite directions to keep the surface on the left. So we conclude that the integral invariant over the entire surface is zero.

#FootnoteRef(7)Let /f/ be a path-dependent function,$\widetilde{\eta}\left( s \right) = D\widetilde{q}\left( s \right)$, and $ g\left( s \right) = f\left\lbrack {\widetilde{q}\left( s \right)} \right\rbrack $. The variation of /f/ at $\widetilde{q}\left( s \right)$ in the direction $\widetilde{\eta}\left( s \right)$ is $\delta_{\widetilde{\eta}{(s)}}f\left\lbrack {\widetilde{q}\left( s \right)} \right\rbrack = Dg\left( s \right)$.

#FootnoteRef(8)In general, the generator /W/ could depend on its independent variable. If so, it would be necessary to specify a rule that gives the initial value of the independent variable for the /W/ evolution. This rule may or may not depend upon the time. If the specification of the independent variable for the /W/ evolution does not depend on time, then the resulting canonical transformation $\mathcal{C}_{\mathit{\epsilon},W}^{\prime}$ is time independent and the Hamiltonians transform by composition. If the generator /W/ depends on its independent variable and the rule for specifying its initial value depends on time, then the transformation $\mathcal{C}_{\mathit{\epsilon},W}^{\prime}$ is time dependent. In this case there may need to be an adjustment to the relation between the Hamiltonians /H/ and /H/′. In the extended phase space all these complications disappear: There is only one case. We can assume all generators /W/ are independent of the independent variable.

#FootnoteRef(9)The set of transformations $ E_{\mathit{\epsilon},W}^{\prime}$ with the operation composition and with parameter /ϵ/ is a one-parameter Lie group.

#FootnoteRef(10)We are playing fast and loose with differential operators here. In a formal treatment it is essential to prove that these games are mathematically well defined and have appropriate convergence properties.

#FootnoteRef(11)Our /L_{H}/ is a special case of what is referred to as a Lie derivative in differential geometry. The more general idea is that a vector field defines a flow. The Lie derivative of an object with respect to a vector field gives the rate of change of the object as it is dragged along with the flow. In our case the flow is the evolution generated by Hamilton's equations, with Hamiltonian /H/.

#FootnoteRef(12)Actually, we define the Lie derivative slightly differently, as follows:
```Scheme
(define ((Lie-derivative-procedure H) F) (Poisson-bracket F H)) (define Lie-derivative (make-operator Lie-derivative-procedure 'Lie-derivative)) 
```
The reason is that we want Lie-derivative to be an /operator/, which is just like a function except that the product of operators is interpreted as composition, whereas the product of functions is the function computing the product of their values.

#FootnoteRef(13)The Lie-transform procedure here is also defined to be an operator, just like Lie-derivative. 
#FootnoteEnd
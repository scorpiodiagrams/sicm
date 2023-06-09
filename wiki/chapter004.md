!!Polyglot
## Phase Space Structure
### Chapter 4
#page(285)
#Quote(When we try to represent the figure formed by these two curves and their intersections in a finite number, each of which corresponds to a doubly asymptotic solution, these intersections form a type of trellis, tissue, or grid with infinitely serrated mesh. Neither of these two curves must ever cut across itself again, but it must bend back upon itself in a very complex manner in order to cut across all of the meshes in the grid an infinite number of times. The complexity of this figure will be striking, and I shall not even try to draw it.)
#Caption Henri Poincaré, /New Methods of Celestial Mechanics, volume III/ [35](bibliography!bib_35), chapter XXXIII, section 397#CaptionEnd

We have seen rather complicated features appear as part of the Poincaré sections of a variety of systems. We have seen fixed points, invariant curves, resonance islands, and chaotic zones in systems as diverse as the driven pendulum, the non-axisymmetric top, the Hénon--Heiles system, and the spin-orbit coupling of a satellite. Indeed, even in the standard map, where there is no continuous process sampled by the surface of section, the phase space shows similar features.

The motion of other systems is simpler. For some systems conserved quantities can be used to reduce the solution to the evaluation of definite integrals. Such a system is traditionally called /integrable/. An example is the axisymmetric top. Two symmetries imply the existence of two conserved momenta, and time independence of the Hamiltonian implies energy conservation. With these conserved quantities, determining the motion is reduced to the evaluation of definite integrals of the periodic motion of the tilt angle as a function of time. Such systems do not exhibit chaotic behavior; on a surface of section the conserved quantities constrain the points to fall on curves. If points on a surface of section do not apparently fall on curves then we may take this as
#page(286)
evidence that not enough conserved quantities exist to reduce the solution to quadratures.

We have seen a number of instances in which the behavior of a system changes qualitatively with the inclusion of additional effects. The free rigid body can be reduced to quadratures, but the addition of gravity-gradient torques in the spin-orbit system yields the familiar mixture of regular and chaotic motions. The motion of an axisymmetric top is also reducible to quadratures, but if the top is made non-axisymmetric then the divided phase space appears. The system studied by Hénon and Heiles, with the classic divided phase space, can be thought of as a solvable pair of harmonic oscillators with nonlinear coupling terms. The pendulum is solvable, but the driven pendulum has the divided phase space.

We observe that as additional effects are turned on, qualitative changes occur in the phase space. Resonance islands appear, chaotic zones appear, some invariant curves disappear, but others persist. Why do resonance islands appear? How does chaotic behavior arise? When do invariant curves persist? Can we draw any general conclusions?

### 4.1 Emergence of the Divided Phase Space
We can get some insight into these qualitative changes of behavior by considering systems in which the additional effects are turned on by varying a parameter. For some value of the parameter the system has enough conserved quantities to be reducible to quadratures; as we vary the parameter away from this value we can study how the divided phase space appears. The driven pendulum offers an archetypal example of such a system. If the amplitude of the drive is zero, then solutions of the driven pendulum are the same as the solutions of the undriven pendulum. We have seen surfaces of section for the strongly driven pendulum, illustrating the divided phase space. Here we crank up the drive slowly and study how the phase portrait changes.

The motion of the driven pendulum with zero-amplitude drive is the same as that of an undriven pendulum, as described in [section 3.3](#section_3.3). Energy is conserved, so all orbits are level curves of the Hamiltonian in the phase plane (see [figure 4.1](#figure_4.1)). There are three regions of the phase plane that have qualitatively different types
#page(287)
of motion: the region in which the pendulum oscillates, the region in which the pendulum circulates in one direction, and the region of circulation in the other direction. In the center of the oscillation region there is a stable equilibrium, at which the pendulum is hanging motionless. At the boundaries between these regions the pendulum is asymptotic to the unstable equilibrium, at which the pendulum is standing upright. There are two asymptotic trajectories, corresponding to the two ways the equilibrium can be approached. Each of these is also asymptotic to the unstable equilibrium going backward in time.

#Image(Art_P812.jpg,figure_4.1)
#Caption *Figure 4.1* The phase plane of the undriven pendulum has three regions displaying two distinct kinds of behavior. Trajectories lie on the contours of the Hamiltonian. Trajectories may oscillate, making ovoid curves around the equilibrium point, or they may circulate, producing wavy tracks outside the eye-shaped region. The eye-shaped region is delimited by the separatrix. This pendulum has length 1 m and a bob of mass 1 kg, and the acceleration of gravity is 9.8 m s^{−2}. #CaptionEnd

#### Driven pendulum sections with zero-amplitude drive
Now consider the periodically driven pendulum, but with zero-amplitude drive. The state of the driven pendulum is specified by an angle coordinate, its conjugate momentum, and the phase of the periodic drive. With zero-amplitude drive the evolution of the “driven” pendulum is the same as the undriven pendulum. The
#page(288)
phase of the drive does not affect the evolution, but we consider the phase of the drive as part of the state so we can give a uniform description that allows us to include the zero-amplitude drive case with the nonzero-amplitude case.

#Image(Art_P813.jpg,figure_4.2)
#Caption *Figure 4.2* A surface of section for the driven pendulum, with zero-amplitude drive. The effect is to sample the trajectories of the undriven pendulum, which lie on the contours of the Hamiltonian. Only a small number of points are plotted for each trajectory to illustrate the fact that for zero-amplitude drive the surface of section samples the continuous trajectories of the undriven pendulum. #CaptionEnd

For the driven pendulum we make stroboscopic surfaces of section by sampling the state at the drive period and plotting the angular momentum versus the angle (see [figure 4.2](#figure_4.2)). For zero-amplitude drive, the section points are confined to the curves traced by trajectories of the undriven pendulum. For each kind of orbit that we saw for the undriven pendulum, there are orbits of the driven pendulum that generate a corresponding pattern of points on the section.

The two stationary orbits at the equilibrium points of the pendulum appear as points on the surface of section. Equilibrium points are fixed points of the Poincaré map.

Section points for the oscillating orbits of the pendulum fall on the corresponding contour of the Hamiltonian. Section points for
#page(289)
the circulating orbits of the pendulum are likewise confined to the corresponding contour of the Hamiltonian. We notice that the pattern of the points generated by orbits varies from contour to contour. Typically, if we collected more points on the surface of section the points would eventually fill in the contours. However, there are actually two possibilities. Remember that the period of the pendulum is different for different trajectories. If the period of the pendulum is commensurate with the period of the drive, then only a finite number of points will appear on the section. Two periods are commensurate if one is a rational multiple of the other. If the two periods are incommensurate then the section points never repeat. In fact, the points fill the contour densely, coming arbitrarily close to every point on the contour.

Section points for the asymptotic trajectories of the pendulum fall on the contour of the Hamiltonian containing the saddle point. Each asymptotic orbit generates a sequence of isolated points that accumulate near the fixed point. No individual orbit fills the sep-aratrix on the section.

#### Driven pendulum sections for small drive
Now consider the surface of section for small-amplitude drive (see [figure 4.3](#figure_4.3)). The amplitude of the drive is /A/ = 0.001 m; the drive frequency is 4.2 /ω/_{0}, where $\omega_{0} = \sqrt{g/l}$. The overall appearance of the surface of section is similar to the section with zero-amplitude drive. Many orbits appear to lie on invariant curves similar to the invariant curves of the zero-drive case. However, there are several new features.

There are now resonance regions that correspond to the pendulum rotating in lock with the drive. These features are found in the upper and lower circulating region of the surface of section. Each island has a fixed point for which the pendulum rotates exactly once per cycle of the drive. In general, fixed points on the surface of section correspond to periodic motions of the system in the full phase space. The fixed point is at ±/π/, indicating that the pendulum is vertical at the section phase of the drive. For orbits in the resonance region away from the fixed point the points on the section apparently generate curves that surround the fixed point.#Footnote(1) For these orbits the pendulum rotates on average once per
#page(290)
drive, but the phase of the pendulum is sometimes ahead of the drive and sometimes behind it.

There are other islands that appear with nonzero-amplitude drive. In the central oscillation region there is a sixfold chain of secondary islands. For this orbit the pendulum is oscillating, and the period of the oscillation is commensurate with the drive. The six islands are all generated by a single orbit. In fact, the islands are visited successively in a clockwise direction. After six cycles of the drive the section point returns to the same island but falls at a different point on the island curve, accumulating the island curve after many iterations. The motion of the pendulum is not periodic, but is locked in a resonance so that on average it oscillates once for every six cycles of the drive.

Another feature that appears is a narrow chaotic region near where the separatrix was in the zero-amplitude drive pendulum. We find that chaotic behavior typically makes its most prominent appearance near separatrices. This is not surprising because the difference in velocities that distinguish whether the pendulum rotates or oscillates is small for orbits near the separatrix. As the pendulum approaches the top, whether it receives the extra nudge it needs to go over the top depends on the phase of the drive.

Actually, the apparent separatrices of the resonance islands for which the pendulum period is equal to the drive period are each generated by a chaotic orbit. To see that this orbit appears to occupy an area one would have to magnify the picture by about a factor of 10^{4}.

As the drive amplitude is increased the main qualitative changes are the appearance of resonance islands and chaotic zones. Some qualitative characteristics of the zero-amplitude case remain. For instance, many orbits appear to lie on invariant curves. This behavior is not peculiar to the driven pendulum; similar features quite generally arise as additional effects are added to problems that are reducible to quadratures. This chapter is devoted to understanding in greater detail how these generic features arise.

### 4.2 Linear Stability
Qualitative changes are associated with fixed points of the surface of section. As the drive is turned on, chaotic zones appear at fixed points on separatrices of the undriven system, and we observe the
#page(291)
appearance of new fixed points and periodic points associated with resonance islands. Here we investigate the behavior of systems near fixed points. We can distinguish two types of fixed points on a surface of section: there are fixed points that correspond to equilibria of the system and there are fixed points that correspond to periodic orbits of the system. We first consider the stability of equilibria of systems governed by differential equations, then discuss the stability of fixed points of maps.

#Image(Art_P815.jpg,figure_4.3)
#Caption *Figure 4.3* A surface of section for the driven pendulum, with nonzero drive amplitude /A/ = 0.001 m and drive frequency 4.2 /ω/_{0}. Many trajectories apparently generate invariant curves, as in the zero-amplitude drive case. Here, in addition, some orbits belong to island chains and others are chaotic. The most apparent chaotic orbit is near the separatrix of the undriven pendulum. #CaptionEnd

##### 4.2.1 Equilibria of Differential Equations
Consider first the case of an equilibrium of a system of differential equations. If a system is initially at an equilibrium point, the system remains there. What can we say about the evolution of the system for points near such an equilibrium point? This is actually a very difficult question, which has not been completely answered. We can, however, understand quite a lot about the motion
#page(292)
of systems near equilibrium. The first step is to investigate the evolution of a linear approximation to the differential equations near the equilibrium. This part is easy, and is the subject of linear stability analysis. Later, we will address what the linear analysis implies for the actual problem.

Consider a system of ordinary differential equations

$$\begin{matrix} {Dz(t) = F(t,z(t))} \tag{4.1} \\ \end{matrix}$$

with components

$$\begin{matrix} {Dz^{i}(t) = F^{i}(t,z^{0}(t),\ldots,z^{n - 1}(t)),} \tag{4.2} \\ \end{matrix}$$

where /n/ is the dimension. An equilibrium point of this system of equations is a point /z_{e}/ for which the state derivative is zero:

$$\begin{matrix} {0 = F(t,z_{e}).} \tag{4.3} \\ \end{matrix}$$

That this is zero at all moments for the equilibrium solution implies ∂_{0}/F/ (/t/, /z_{e}/) = 0.

Next consider a path /z/′ that passes near the equilibrium point. The path displacement /ζ/ is defined so that at time /t/

$$\begin{matrix} {z\prime(t) = z_{e} + \zeta(t).} \tag{4.4} \\ \end{matrix}$$

We have

$$\begin{matrix} {D\zeta(t) = Dz\prime(t) = F(t,z_{e} + \zeta(t)).} \tag{4.5} \\ \end{matrix}$$

If /ζ/ is small we can write the right-hand side as a Taylor series in /ζ/:

$$\begin{matrix} {D\zeta(t) = F(t,z_{e}) + \partial_{1}F(t,z_{e})\zeta(t) + \cdots,} \tag{4.6} \\ \end{matrix}$$

but the first term is zero because /z_{e}/ is an equilibrium point, so

$$\begin{matrix} {D\zeta(t) = \partial_{1}F(t,z_{e})\zeta(t) + \cdots.} \tag{4.7} \\ \end{matrix}$$

If /ζ/ is small the evolution is approximated by the linear terms. Linear stability analysis investigates the evolution of the approximate equation

$$\begin{matrix} {D\zeta(t) = \partial_{1}F(t,z_{e})\zeta(t).} \tag{4.8} \\ \end{matrix}$$

#page(293)

These are the variational equations (#Eqn(chapter003,3.145,3.145)) with the equilibrium solution substituted for the reference trajectory. The relationship of the solutions of this linearized system to the full system is a difficult mathematical problem, which has not been fully resolved.

If we restrict attention to autonomous systems (∂_{0}/F/ = 0), then the variational equations at an equilibrium are a linear system of ordinary differential equations with constant coefficients.#Footnote(2) Such systems can be solved analytically. To simplify the notation, let /M/ = ∂_{1}/F/(/t/, /z_{e}/), so

$$\begin{matrix} {D\zeta(t) = M\zeta(t).} \tag{4.9} \\ \end{matrix}$$

We seek a solution of the form

$$\begin{matrix} {\zeta(t) = \alpha e^{\lambda t},} \tag{4.10} \\ \end{matrix}$$

where /α/ is a structured constant with the same number of components as /ζ/, and /λ/ is a complex number called a /characteristic exponent/. Substituting, we find

$$\begin{matrix} {\lambda\alpha e^{\lambda t} = M\alpha e^{\lambda t}.} \tag{4.11} \\ \end{matrix}$$

The exponential factor is not zero, so we find

$$\begin{matrix} {M\alpha = \lambda\alpha,} \tag{4.12} \\ \end{matrix}$$

which is an equation for the eigenvalue /λ/ and (normalized) eigen-vector /α/. In general, there are /n/ eigenvalues and /n/ eigenvectors, so we must add a subscript to both /α/ and /λ/ indicating the particular solution. The general solution is an arbitrary linear combination of these individual solutions. The eigenvalues are solutions of the characteristic equation

$$\begin{matrix} {0 = \det(\mathbf{M} - \lambda\mathbf{I})} \tag{4.13} \\ \end{matrix}$$

where *M* is the matrix representation of /M/, and *I* is the identity matrix of the same dimension. The elements of *M* are real, so we know that the eigenvalues /λ/ either are real or come in complex-conjugate pairs. We assume the eigenvalues are all distinct.#Footnote(3)

#page(294)

If the eigenvalue is real then the solution is exponential, as assumed. If the eigenvalue /λ/ > 0 then the solution expands exponentially along the direction /α/; if /λ/ < 0 then the solution contracts exponentially along the direction /α/.

If the eigenvalue is complex we can form real solutions by combining the two solutions for the complex-conjugate pair of eigenvalues. Let /λ/ = /a/ + /ib/, with real /a/ and /b/, be one such complex eigenvalue. Let /α/ = /u/ + /iv/, where /u/ and /v/ are real, be the eigen-vector corresponding to it. So there is a complex solution of the form

$$\begin{array}{lll} {\zeta_{c}(t)} & {= (u + iv)e^{(a + ib)t}} & \\ & {= (u + iv)e^{at}(\cos\, bt + i\,\sin\, bt)} & \\ & {= e^{at}(u\,\cos\, bt - v\,\sin\, bt) + ie^{at}(u\,\sin\, bt + v\,\cos\, bt).} \tag{4.14} \\ \end{array}$$

The complex conjugate of this solution is also a solution, because the ordinary differential equation is linear with real linear coefficients. This complex-conjugate solution is associated with the eigenvalue that is the complex conjugate of the original complex eigenvalue. So the real and imaginary parts of /ζ_{c}/ are real solutions:

$$\begin{array}{lll} {\zeta_{a}(t)} & {= e^{at}(u\,\cos\, bt - v\,\sin\, bt)} & \\ {\zeta_{b}(t)} & {= e^{at}(u\,\sin\, bt + v\,\cos\, bt).} \tag{4.15} \\ \end{array}$$

These two solutions reside in the plane containing the vectors /u/ and /v/. If /a/ is positive both solutions spiral outwards exponentially, and if /a/ is negative they both spiral inwards. If /a/ is zero, both solutions trace the same ellipse, but with different phases.

Again, the general solution is an arbitrary linear combination of the particular real solutions corresponding to the various eigenvalues. So if we denote the /k/th real eigensolution /ζ_{k}/(/t/), then the general solution is

$$\begin{array}{ll} {\zeta(t) = {\sum\limits_{k}{A_{k}\zeta_{k}(t),}}} \tag{4.16} \\ \end{array}$$

where /A_{k}/ may be determined by the initial conditions (the state at a given time).

### Exercise 4.1: Pendulum

Carry out the details of finding the eigensolutions for the two equilibria of the pendulum (/θ/ = 0 and /θ/ = /π/, both with /p_{θ}/ = 0). How is the
#page(295)
small-amplitude oscillation frequency related to the eigenvalues? How are the eigendirections related to the contours of the Hamiltonian?

##### 4.2.2 Fixed Points of Maps
Fixed points on a surface of section correspond either to equilibrium points of the system or to a periodic motion of the system. Linear stability analysis of fixed points of maps is similar to the linear stability analysis for equilibrium points of systems governed by differential equations.

Let /T/ be a map of the state space onto itself, as might be generated by a surface of section. A trajectory sequence is generated by successive iteration of the map /T/. Let /x/(/n/) be the /n/th point of the sequence. The map carries one point of the trajectory sequence to the next: /x/(/n/ + 1) = /T/(/x/(/n/)). We can represent successive iterations of the map by a superscript, so that /T ^{i}/ indicates /T/ composed /i/ times. For example, /T/^{2}(/x/) = /T/ (/T/(/x/)). Thus /x/(/n/) = /T^{n}/(/x/(0)).#Footnote(4)

A /fixed point x/_{0} of the map /T/ satisfies

$$\begin{array}{ll} {x_{0} = T(x_{0}).} \tag{4.17} \\ \end{array}$$

A /periodic point/ of the map /T/ is a point that is visited every /k/ iterations of /T/. Thus it is a fixed point of the map /T^{k}/. So the behavior near a periodic point can be ascertained by looking at the behavior near an associated fixed point of /T^{k}/.

Let /x/ be some trajectory initially near the fixed point /x/_{0} of /T/, and /ξ/ be the deviation from /x/_{0}: /x/(/n/) = /x/_{0} + /ξ/(/n/). The trajectory satisfies

$$\begin{array}{ll} {x_{0} + \xi(n + 1) = T(x_{0} + \xi(n)).} \tag{4.18} \\ \end{array}$$

Expanding the right-hand side as a Taylor series, we obtain

$$\begin{array}{ll} {x_{0} + \xi(n + 1) = T(x_{0}) + DT(x_{0})\xi(n) + \cdots,} \tag{4.19} \\ \end{array}$$

but /x/_{0} = /T/(/x/_{0}) so

$$\begin{array}{ll} {\xi(n + 1) = DT(x_{0})\xi(n) + \cdots.} \tag{4.20} \\ \end{array}$$

#page(296)

Linear stability analysis considers the evolution of the system truncated to the linear terms

$$\begin{array}{ll} {\xi(n + 1) = DT(x_{0})\xi(n).} \tag{4.21} \\ \end{array}$$

This is a system of linear difference equations, with constant coefficients /DT/(/x/_{0}).

We assume there are solutions of the form

$$\begin{array}{ll} {\xi(n) = \rho^{n}\alpha,} \tag{4.22} \\ \end{array}$$

where /ρ/ is some (complex) number, called a /characteristic multiplier/.#Footnote(5) Substituting this solution into the linearized evolution equation, we find

$$\begin{array}{ll} {\rho\alpha = DT(x_{0})\alpha,} \tag{4.23} \\ \end{array}$$

or

$$\begin{array}{ll} {(DT(x_{0}) - \rho I)\alpha = 0,} \tag{4.24} \\ \end{array}$$

where /I/ is the identity multiplier. We see that /ρ/ is an eigenvalue of the linear transformation /DT/(/x/_{0}) and /α/ is the associated (normalized) eigenvector. Let /M/ = /DT/(/x/_{0}), and *M* be its matrix representation. The eigenvalues are determined by

$$\begin{array}{ll} {\det(\mathbf{M} - \rho\mathbf{I}) = 0.} \tag{4.25} \\ \end{array}$$

The elements of *M* are real, so the eigenvalues /ρ/ are either real or come in complex-conjugate pairs.#Footnote(6)

For the real eigenvalues the solutions are just exponential expansion or contraction along the associated eigenvector /α/:

$$\begin{array}{ll} {\xi(n) = \rho^{n}\alpha.} \tag{4.26} \\ \end{array}$$

The solution is expanding if |/ρ/| > 1 and contracting if |/ρ/| < 1.

If the eigenvalues are complex, then the solution is complex, but the complex solutions corresponding to the complex-conjugate pair of eigenvalues can be combined to form two real solutions, as was done for the equilibrium solutions. Let /ρ/ = /e/^{A+/iB/} with real
#page(297)
/A/ and /B/, and /α/ = /u/ + /iv/. A calculation similar to that for the equilibrium case shows that there are two real solutions

$$\begin{array}{lll} {\xi_{a}(n)} & {= \text{e}^{An}\,(u\,\cos\, Bn - v\,\sin\, Bn)} & \\ {\xi_{b}(n)} & {= \text{e}^{An}\,(u\,\sin\, Bn + v\,\cos\, Bn).} \tag{4.27} \\ \end{array}$$

We see that if /A/ > 0 then the solution exponentially expands, and if /A/ < 0 the solution exponentially contracts. Exponential expansion, /A/ > 0, corresponds to |/ρ/| > 1; exponential contraction, /A/ < 0, corresponds to |/ρ/| < 1. If /A/ = 0 then the two real solutions trace an ellipse and any linear combination of them traces an ellipse.

The general solution is an arbitrary linear combination of the eigensolutions. Let /ξ_{k}/ be the /k/th real eigensolution. The general solution is

$$\begin{array}{ll} {\xi(n) = {\sum\limits_{k}{A_{k}\xi_{k}(n),}}} \tag{4.28} \\ \end{array}$$

where /A_{k}/ may be determined by the initial conditions.

### Exercise 4.2: Elliptical oscillation

Show that the arbitrary linear combination of /ξ_{a}/ and /ξ_{b}/ traces an ellipse for /A/ = 0.

### Exercise 4.3: Standard map

The standard map (see [section 3.9](chapter003!section_3.9)) has fixed points at /I/ = 0 for /θ/ = 0 and /θ/ = /π/. Find the full eigensolutions for these two fixed points. For what ranges of the parameter /K/ are the fixed points linearly stable or unstable?

##### 4.2.3 Relations Among Exponents
For maps that are generated by stroboscopic sampling of the evolution of a system of autonomous differential equations, equilibrium points are fixed points of the map. The eigensolutions of the equilibrium of the flow and the eigensolutions of the map at the fixed point are then related. Let /τ/ be the sampling period. Then $\rho_{i} = e^{\lambda_{i}\tau}$.

The Lyapunov exponent is a measure of the rate of exponential divergence of nearby trajectories from a reference trajectory. If the reference trajectory is an equilibrium of a flow, then the Lyapunov exponents are the real parts of the linearized characteristic
#page(298)
exponents /λ_{i}/. If the reference trajectory is a fixed point of a map generated by a flow (either a periodic orbit or an equilibrium), then the Lyapunov exponents are real parts of the logarithm of the characteristic multipliers, divided by the period of the map. So if the characteristic multiplier is /ρ/ = /e/^{A+/iB/} and the period of the map is /τ/, then the Lyapunov exponent is /A///τ/. A positive Lyapunov exponent of a fixed point indicates linear instability of the fixed point.

The Lyapunov exponent has less information than the characteristic multipliers or exponents because the imaginary part is lost. However, the Lyapunov exponent is more generally applicable in that it is well defined even for reference trajectories that are not periodic.

In the linear analysis of the fixed point, each characteristic multiplier corresponds to a subspace of possible linear solutions. For instance, for a real characteristic multiplier there is a corresponding eigendirection, and for any initial displacement along this direction successive iterates are also along this direction. Complex-conjugate pairs of multipliers correspond to a plane of solutions. For a displacement initially on this plane, successive iterates are also on this plane.

It turns out that something like this is also the case for the linearized solutions near a reference trajectory that is not at a fixed point. For each nonzero Lyapunov exponent there is a twisting subspace, so that for an initial displacement in this subspace successive iterates also belong to the subspace. At different points along the reference trajectory the unit displacement vector that characterizes the direction of this subspace is different.

#### Hamiltonian specialization
For Hamiltonian systems there are additional constraints among the eigenvalues.

Consider first the case of two-dimensional surfaces of section. We have seen that Hamiltonian surfaces of section preserve area. As we saw in the proof of Liouville's theorem, area preservation implies that the determinant of the derivative of the transformation is 1. At a fixed point /x/_{0} the linearized map is /ξ/(/n/ + 1) = /DT/(/x/_{0})/ξ/(/n/). So /M/ = /DT/(/x/_{0}) has unit determinant. The determinant is the product of the eigenvalues, so for a fixed point on a Hamiltonian surface of section the two eigenvalues must be inverses of each other. We also have the constraint that if an eigen-value is complex then the complex conjugate of the eigenvalue is also an eigenvalue. These two conditions imply that the eigenvalues must either be real and inverses, or be complex-conjugate pairs on the unit circle (see [figure 4.4](#figure_4.4)).

#page(299)

#Image(Art_P845.jpg,figure_4.4)
#Caption *Figure 4.4* The eigenvalues for fixed points of a two-dimensional Hamiltonian map. The eigenvalues either are real or are complex-conjugate pairs that lie on the unit circle. For each eigenvalue the inverse is also an eigenvalue. #CaptionEnd

Fixed points for which the characteristic multipliers all lie on the unit circle are called /elliptic/ fixed points. The solutions of the linearized variational equations trace ellipses around the fixed point. Elliptic fixed points are linearly stable.

Fixed points with positive real characteristic multipliers are called /hyperbolic/ fixed points. For two-dimensional maps, there is an exponentially expanding subspace and an exponentially contracting subspace. The general solution is a linear combination of these. Fixed points for which the characteristic multipliers are negative are called /hyperbolic with reflection/.

The edge case of a double root of the characteristic equation is called /parabolic/. In this case the general solution grows linearly. This happens at points of bifurcation where elliptic points become hyperbolic points or vice versa.

#page(300)

#Image(Art_P846.jpg,figure_4.5)
#Caption *Figure 4.5* If there is more than one degree of freedom the eigenvalues for fixed points of a Hamiltonian map may lie in a quartet, with two complex-conjugate pairs. The magnitudes of the pairs must be inverses. This enforces the constraint that the expansion produced by the roots with magnitude greater than one is counterbalanced by the contraction produced by the roots with magnitude smaller than one. #CaptionEnd

For two-dimensional Hamiltonian maps these are the only possibilities. For higher-dimensional Hamiltonian maps, we can get combinations of these: some characteristic multipliers can be real and others complex-conjugate pairs. We might imagine that in addition there would be many other types of fixed points that occur in higher dimensions. In fact, there is only one additional type, shown in [figure 4.5](#figure_4.5). For Hamiltonian systems of arbitrary dimensions it is still the case that for each eigenvalue the complex conjugate and the inverse are also eigenvalues. We can prove this starting from a result in chapter 5. Consider the map /T_{β}/ of the phase space onto itself that is generated by time evolution of a Hamiltonian system by time increment /β/. Let /z/ = (/q/, /p/); then the map /T_{β}/ satisfies /z/(/t/ + /β/) = /T_{β}/(/z/(/t/)) for solutions /z/ of Hamilton's equations. We will show in chapter 5 that the derivative of the
#page(301)
map /T_{β}/ is symplectic, whether or not the starting point is at a fixed point. A 2/n/ × 2/n/ matrix *M* is /symplectic/ if it satisfies

$$\begin{array}{ll} {\mathbf{MJ}\mathbf{M}^{\mathcal{T}} = \mathbf{J},} \tag{4.29} \\ \end{array}$$

where *J* is the 2/n/-dimensional symplectic unit:

$$\begin{matrix} {\mathbf{J} = \left( \begin{array}{ll} \mathbf{0}_{n \times n} & \mathbf{1}_{n \times n} \\ {\mathbf{-}\mathbf{1}_{n \times n}} & \mathbf{0}_{n \times n} \\ \end{array} \right),} \tag{4.30} \\ \end{matrix}$$

with the /n/ × /n/ unit matrix *1*_{n×n} and the /n/ × /n/ zero matrix *0*_{n×n}.

Using the symplectic property, we can show that in general for each eigenvalue its inverse is also an eigenvalue. Assume /ρ/ is an eigenvalue, so that /ρ/ satisfies det(*M* − /ρ/*I*) = 0. This equation is unchanged if *M* is replaced by its transpose, so /ρ/ is also an eigenvalue of $\mathbf{M}^{\mathcal{T}}$:

$$\begin{array}{ll} {\mathbf{M}^{\mathcal{T}}\mathbf{\alpha}\prime = \rho\mathbf{\alpha}\prime.} \tag{4.31} \\ \end{array}$$

From this we can see that

$$\begin{array}{ll} {\frac{1}{\rho}\mathbf{\alpha}\prime = {(\mathbf{M}^{\mathcal{T}})}^{- 1}\mathbf{\alpha}\prime.} \tag{4.32} \\ \end{array}$$

Now, from the symplectic property we have

$$\begin{array}{ll} {\mathbf{MJ} = \mathbf{J}{(\mathbf{M}^{\mathcal{T}})}^{- 1}.} \tag{4.33} \\ \end{array}$$

So

$$\begin{array}{ll} {\mathbf{MJ}\mathbf{\alpha}\prime = \mathbf{J}{(\mathbf{M}^{\mathcal{T}})}^{- 1}\mathbf{\alpha}\prime = \frac{1}{\rho}\mathbf{J}\mathbf{\alpha}\prime,} \tag{4.34} \\ \end{array}$$

and we can conclude that 1//ρ/ is an eigenvalue of *M* with the eigenvector *J/α/′*. From the fact that for every eigenvalue its inverse is also an eigenvalue we deduce that the determinant of the transformation *M*, which is the product of the eigenvalues, is one.

Thus the constraints that the eigenvalues must be associated with inverses and complex conjugates yields exactly one new pattern of eigenvalues in higher dimensions. [Figure 4.5](#figure_4.5) shows the only new pattern that is possible.

We have seen that the Lyapunov exponents for fixed points are related to the characteristic multipliers for the fixed points,
#page(302)
so the Hamiltonian constraints on the multipliers correspond to Hamiltonian constraints for Lyapunov exponents at fixed points. For each characteristic multiplier, the inverse is also a characteristic multiplier. This means that at fixed points, for each positive Lyapunov exponent there is a corresponding negative Lyapunov exponent with the same magnitude. It turns out that this is also true if the reference trajectory is not at a fixed point. For Hamiltonian systems, for each positive Lyapunov exponent there is a corresponding negative exponent of equal magnitude.

### Exercise 4.4: Quartet

Describe (perhaps by drawing cross sections) the orbits that are possible with quartets.

#### Linear and nonlinear stability
A fixed point that is linearly unstable indicates that the full system is unstable at that point. This means that trajectories starting near the fixed point diverge from the fixed point. On the other hand, linear stability of a fixed point does not generally guarantee that the full system is stable at that point. For a two-degree-of-freedom Hamiltonian system, the Kolmogorov--Arnold--Moser theorem proves under certain conditions that linear stability implies nonlinear stability. In higher dimensions, though, it is not known whether linear stability implies nonlinear stability.

### 4.3 Homoclinic Tangle
For the driven pendulum we observe that as the amplitude of the drive is increased the separatrix of the undriven pendulum is where the most prominent chaotic zone appears. Here we examine in great detail the motion in the vicinity of the separatrix. What emerges is a remarkably complicated picture, first discovered by Henri Poincaré. Indeed, Poincaré stated (see the epigraph to this chapter) that the picture that emerged was so complicated that he was not even going to attempt to draw it. We will review the argument leading to the picture, and compute enough of it to convince ourselves of its reality.

The separatrix of the undriven pendulum is made up of two trajectories that are asymptotic to the unstable equilibrium. In the driven pendulum with zero drive, an infinite number of distinct
#page(303)
orbits lie on the separatrix; they are distinguished by the phase of the drive. These orbits are asymptotic to the unstable fixed point both forward and backward in time.

#Image(Art_P853.jpg,figure_4.6)
#Caption *Figure 4.6* The stable and unstable manifolds of the unstable fixed point for the pendulum are compared to the stable and unstable manifolds of the linearized variational system in the vicinity of the fixed point. The axes are centered at the fixed point (±/π/, 0). The linear stable and unstable manifolds are labeled by V^{s} and V^{u} respectively; the nonlinear stable and unstable manifolds are labeled by W^{s} and W^{u}. #CaptionEnd

Notice that close to the unstable fixed point the sets of points that are asymptotic to the unstable equilibrium must be tangent to the linear variational eigenvectors at the fixed point. (See [figure 4.6](#figure_4.6).) In a sense, the sets of orbits that are asymptotic to the fixed point are extensions to the nonlinear problem of the sets of orbits that are asymptotic to the fixed point in the linearized problem.

The set of points that are asymptotic to an unstable fixed point forward in time is called the /stable manifold/ of the fixed point. The set of points that are asymptotic to an unstable fixed point backward in time is called the /unstable manifold/. For the driven pendulum with zero-amplitude drive, all points on the separatrix are asymptotic both forward and backward in time to the unstable
#page(304)
fixed point. So in this case the stable and unstable manifolds coincide.

If the drive amplitude is nonzero then there are still one-dimensional sets of points that are asymptotic to the unstable fixed point forward and backward in time: there are still stable and unstable manifolds. Why? The behavior near the fixed point is described by the linearized variational system. For the linear variational system, points in the space spanned by the unstable eigenvector, when mapped backwards in time, are asymptotic to the fixed point. Points slightly off this curve may initially approach the unstable equilibrium, but eventually will fall away to one side or the other. For the driven system with small drive, there must still be a curve that separates the points that fall away to one side from the points that fall away to the other side. Points on the dividing curve must be asymptotic to the unstable equilibrium. The dividing set cannot have positive area because the map is area preserving.

For the zero-amplitude drive case, the stable and unstable manifolds are contours of the conserved Hamiltonian. For nonzero amplitude the Hamiltonian is no longer conserved, and the stable manifolds and unstable manifolds no longer coincide. This is generally true for non-integrable systems: stable and unstable manifolds do not coincide.

If the stable and unstable manifolds no longer coincide, where do they go? A stable manifold cannot cross another stable manifold, and an unstable manifold cannot cross another unstable manifold, because the crossing point would be asymptotic to two different fixed points. A stable manifold or unstable manifold may not cross itself, as shown below. However, a stable and an unstable manifold may cross one another.

Actually, the stable and unstable manifolds must cross at some point. The only other possibilities are that they run off to infinity or spiral around. We will see that in general there are barriers to running away. Area preservation excludes the existence of attractors, and this can be used to exclude the spiraling case. A finite region of initial conditions between two successive arms of the spiral will eventually run out of area as the spiral progresses.

So the only possibility is that the stable and unstable manifolds cross, as is illustrated in [figure 4.7](#figure_4.7). The point of crossing of a stable and unstable manifold is called a /homoclinic intersection/ if the stable and unstable manifolds belong to the same unstable
#page(305)
fixed point. It is called a /heteroclinic intersection/ if the stable and unstable manifolds belong to different fixed points.

#Image(Art_P854.jpg,figure_4.7)
#Caption *Figure 4.7* For nonzero drive the stable and unstable manifolds no longer coincide and in general cross. The dashed circle indicates the central intersection. Forward and backward images of this intersection are themselves intersections. Because the orbits are asymptotic to the fixed point there is an infinity of such intersections. #CaptionEnd

If the stable and unstable manifolds cross once then there is an infinite number of other crossings. The intersection point belongs to both the stable and unstable manifolds. That it is on the unstable manifold means that all images forward and backward in time also belong to the unstable manifold, and likewise for points on the stable manifold. Thus all images of the intersection belong to both the stable and unstable manifolds. So these images must be additional crossings of the two manifolds.

We can deduce that there are still more intersections of the stable and unstable manifolds. The maps we are considering not only preserve area but also orientation. In the proof of Liouville's theorem we showed that the determinant of the transformation is one, not just magnitude one. If we consider little segments of the stable and unstable manifolds near the intersection point, then these segments must map near the image of the intersection point. That the map preserves orientation implies that the manifolds are crossing one another in the same sense as at the previous intersection. Therefore there must have been at least one more crossing of the stable and unstable manifolds in between these two. This
#page(306)
is illustrated in [figure 4.8](#figure_4.8). Of course, all forward and backward images of these intermediate intersections are also intersections.

#Image(Art_P855.jpg,figure_4.8)
#Caption *Figure 4.8* Orientation preservation implies that between an intersection of the stable and unstable manifolds and the image of this intersection there is another intersection. Thus there are two alternating families of intersections. The central intersection and its pre-images and post-images are labeled A_{i}. Another family is labeled B_{i}. #CaptionEnd

As the picture gets more complicated, keep in mind that the stable manifold cannot cross itself and the unstable manifold cannot cross itself. Suppose one did, say by making a little loop. The image of this loop under the map must also be a loop. So if there were a loop there would have to be an infinite number of loops. That would be okay, but what happens as the loop gets close to the fixed point? There would still have to be loops, but then the stable and unstable manifolds would not have the right behavior: the stable and unstable manifolds of the linearized map do not have loops. Therefore, the stable and unstable manifolds cannot cross themselves.#Footnote(7)

We are not done yet! The lobes that are defined by successive crossings of the stable and unstable manifolds enclose a certain area. The map is area preserving so all images of these lobes must have the same area. As the lobes approach the fixed point, we get an infinite number of lobes with a base of exponentially shrinking length. The stable and unstable manifolds cannot cross
#page(307)
themselves, so to pack these lobes together on the plane the lobes must stretch out to preserve area. We see that the length of the lobe must grow roughly exponentially (it may not be uniform in width so it need not be exactly exponential). This exponential lengthening of the lobes no doubt bears some responsibility for the exponential divergence of nearby trajectories of chaotic orbits, but does not prove it. It does, however, suggest a connection between the fact that chaotic orbits appear to occupy an area on the section and the fact that nearby chaotic orbits diverge exponentially.

Actually, the situation is even more complicated. As the lobes stretch, they form tendrils that wrap around the separatrix region. The tendrils of the unstable manifold can cross the tendrils of the stable manifold. Each point of crossing is a new homoclinic intersection, and so each pre- and post-image of this point belongs to both the stable and unstable manifolds, indicating another crossing of these curves. We could go on and on. No wonder Poincaré refused to draw this mess.

### Exercise 4.5: Homoclinic paradox

How do we fit an infinite number of copies of a finite area in a finite region, without allowing the stable and unstable manifolds to cross themselves? Resolve this apparent paradox.

##### 4.3.1 Computation of Stable and Unstable Manifolds
The homoclinic tangle is not just a bad dream. We can actually compute it.

Very close to an unstable fixed point the stable and unstable manifolds become indistinguishable from the rays along the eigen-vectors of the linearized system. So one way to compute the unstable manifold is to take a line of initial conditions close to the fixed point along the unstable manifold of the linearized system and evolve them forward in time. Similarly, the stable manifold can be constructed by taking a line of initial conditions along the stable manifold of the linearized system and evolving them backward in time.

We can do better than this by choosing a parameter (like arc length) along the manifold and for each value of the parameter deciding how many iterations of the map would be required to take the point back to within some small region of the fixed point. We then choose an initial condition along the linearized eigenvectors
#page(308)
and iterate the point back with the map. This idea is implemented in the following program:#Footnote(8)
```Scheme
(define ((unstable-manifold T xe ye dx dy rho eps) param) (let ((n (floor->exact (/ (log (/ param eps)) (log rho))))) ((iterated-map T n) (+ xe (* dx (/ param (expt rho n)))) (+ ye (* dy (/ param (expt rho n)))) make-point (lambda () (error "Failed"))))) 
```
where T is the map, xe and ye are the coordinates of the fixed point, dx and dy are components of the linearized eigenvector, rho is the characteristic multiplier, eps is a scale within which the linearized map is a good enough approximation to T, and param is a continuous parameter along the manifold. The procedure make-point, supplied as the success continuation for the iterated map, packages two numbers. They can be split with abscissa and ordinate.

The program assumes that there is a basic exponential divergence along the manifold---that is why we take the logarithm of param to get initial conditions in the linear regime. This assumption is not exactly true, but it is good enough for now.

The curve is generated by a call to plot-parametric-fill, which recursively subdivides intervals of the parameter until there are enough points to get a smooth curve.
```Scheme
(define (plot-parametric-fill win f a b near?) (let loop ((a a) (xa (f a)) (b b) (xb (f b))) (if (not (close-enuf? a b (* 10 *machine-epsilon*))) (let ((m (/ (+ a b) 2))) (let ((xm (f m))) (plot-point win (abscissa xm) (ordinate xm)) (if (not (near? xa xm)) (loop a xa m xm)) (if (not (near? xb xm)) (loop m xm b xb)))))))
```
The near? argument is a test for whether two points are within a given distance of each other in the graph. Because some coordinates are angle variables, this may involve a principal value comparison. For example, for the driven pendulum section, the
#page(309)
horizontal axis is an angle but the vertical axis is not, so the picture is on a cylinder:
```Scheme
(define (cylinder-near? eps) (let ((eps2 (square eps))) (lambda (point1 point2) (< (+ (square ((principal-value pi) (- (abscissa point1) (abscissa point2)))) (square (- (ordinate point1) (ordinate point2)))) eps2)))) 
```
[Figure 4.9](#figure_4.9) shows a computation of the homoclinic tangle for the driven pendulum. The parameters are /m/ = 1 kg, /g/ = 9.8 m s^{−2}, /l/ = 1 m,$\omega = 4.2\sqrt{g/l}$, and amplitude /A/ = 0.05 m. For reference, [figure 4.9](#figure_4.9) shows a surface of section for these parameters on the same scale.

### Exercise 4.6: Computing homoclinic tangles

*a.* Compute stable and unstable manifolds for the standard map.

*b.* Identify the features on the homoclinic tangle that entered the argument about its existence, such as the central crossing of the stable and unstable manifolds, etc.

*c.* Investigate the errors in the process. Are the computed manifolds really correct or a figment of wishful thinking? One could imagine that the errors are exponential and the computed manifolds have nothing to do with the actual manifolds.

*d.* How much actual space is taken up by the homoclinic tangle? Consider a value of the coupling constant /K/ = 0.8. Does the homoclinic tangle actually fill out the apparent chaotic zone?

### 4.4 Integrable Systems
Islands appear near commensurabilities, and commensurabilities are present even in integrable systems.#Footnote(9) In integrable systems an infinite number of periodic orbits are associated with each commensurability, but upon perturbation only a finite number of periodic orbits survive. How does this happen? First we have to learn more about integrable systems.

#page(310)

#Image(Art_P857.jpg,figure_4.9)
#Caption *Figure 4.9* The computed homoclinic tangle for the driven pendulum exhibits the features described in the text. Notice how the excursions of the stable and unstable manifolds become longer and thinner as they approach the unstable fixed point. A surface of section with the same parameters is also shown. #CaptionEnd

#page(311)

If an /n/-degree-of-freedom system has /n/ independent conserved quantities then the solution of the problem can be reduced to quadratures. Such a system is called /integrable/. Typically, the phase space of integrable systems is divided into regions of qualitatively different behavior. For example, the motion of a pendulum is reducible to quadratures and has three distinct types of solutions: the oscillating solutions and the clockwise and counterclockwise circulating solutions. The different regions of the pendulum phase space are separated by the trajectories that are asymptotic to the unstable equilibrium. It turns out that for any system that is reducible to quadratures, a set of phase-space coordinates can be chosen for each region of the phase space so that the Hamiltonian describing the motion in that region depends only on the momenta. Furthermore, if the phase space is bounded then the generalized coordinates can be chosen to be angles (that are 2/π/-periodic). The configuration space described by /n/ angles is an /n/-torus. The momenta conjugate to these angles are called /actions/. Such phase-space coordinates are called /action-angle/ coordinates. We will see later how to reformulate systems in this way. Here we explore the consequences of such a formulation; this formulation is especially useful for finding out what happens as additional effects are added to integrable problems.

#### Orbit types in integrable systems
Suppose we have a time-independent /n/-degree-of-freedom system that is reducible to quadratures. For each region of phase space there is a local formulation of the system so that the evolution of the system is described by a time-independent Hamiltonian that depends only on the momenta. Suppose further that the coordinates are all angles. Let /θ/ be the tuple of angles and /J/ be the tuple of conjugate momenta. The Hamiltonian is

$$\begin{array}{ll} {H(t,\theta,J) = f(J).} \tag{4.35} \\ \end{array}$$

Hamilton's equations are simply

$$\begin{array}{ll} {DJ(t) = - \partial_{1}H(t,\theta(t),J(t)) = 0} & \\ {D\theta(t) = \,\,\,\,\,\partial_{2}H(t,\theta(t),J(t)) = \omega(J(t)),} \tag{4.36} \\ \end{array}$$

where /ω/(/J/) = /Df/(/J/) is a tuple of frequencies with a component for each degree of freedom. The momenta are all constant because
#page(312)
the Hamiltonian does not depend on any of the coordinates. The motion of the coordinate angles is uniform; the rates of change of the angles are the frequencies /ω/, which depend only on the constant momenta. Given initial values /θ/(/t/_{0}) and /J/(/t/_{0}) at time /t/_{0}, the solutions are simple:

$$\begin{array}{ll} {J(t) = J(t_{0})} & \\ {\theta(t) = \omega(J(t_{0}))(t - t_{0}) + \theta(t_{0}).} \tag{4.37} \\ \end{array}$$

Though the solutions are simple, there are two distinct orbit types: periodic orbits and quasiperiodic orbits, depending on the frequency ratios.

A solution is /periodic/ if all the coordinates (and momenta) of the system return to their initial values at some later time. Each coordinate /θ^{i}/ with nonzero frequency /ω^{i}/(/J/(/t/_{0})) is periodic with a period /τ_{i}/ = 2/π///ω^{i}/(/J/(/t/_{0})). The period of the system must therefore be an integer multiple /k_{i}/ of each of the individual coordinate periods /τ_{i}/. If the system is periodic with some set of integer multiples, then it is also periodic with any common factors divided out. Thus the period of the system is /τ/ = (/k_{i}///d/)/τ_{i}/ where /d/ is the greatest common divisor of the integers /k_{i}/.

For a system with two degrees of freedom, a solution is periodic if there exists a pair of relatively prime integers /k/ and /j/ such that /kω/^{0}(/J/(/t/_{0})) = /jω/^{1}(/J/(/t/_{0})). The period of the system is /τ/ = 2/πj///ω/^{0}(/J/(/t/_{0})) = 2/πk///ω/^{1}(/J/(/t/_{0})); the frequency is /ω/^{0}(/J/(/t/_{0}))//j/ = /ω/^{1}(/J/(/t/_{0}))//k/. A periodic motion on the 2-torus is illustrated in [figure 4.10](#figure_4.10).

If the frequencies /ω^{i}/(/J/(/t/_{0})) satisfy an integer-coefficient relation $\sum_{i}{n_{i}\omega^{i}(J(t_{0})) = 0}$, we say that the frequencies satisfy a /commen-surability/. If there is no commensurability for any nonzero integer coefficients, we say that the frequencies are linearly independent (with respect to the integers) and the solution is /quasiperiodic/. One can prove that for /n/ incommensurate frequencies all solutions come arbitrarily close to every point in the configuration space.#Footnote(10)

For a system with two degrees of freedom the solutions in a region described by a particular set of action-angle variables are
#page(313)
either periodic or quasiperiodic.#Footnote(11) For systems with more than two degrees of freedom there are trajectories that are neither periodic nor quasiperiodic with /n/ frequencies. These are quasiperiodic with fewer frequencies and dense over a corresponding lower-dimensional torus.

#Image(Art_P862.jpg,figure_4.10)
#Caption *Figure 4.10* The solid and dotted lines show two periodic trajectories on the configuration coordinate plane. For commensurate frequencies the configuration motion is periodic, independent of the initial angles. In this illustration the frequencies satisfy 2/ω/^{0}(/J/(/t/_{0})) = 3/ω/^{1}(/J/(/t/_{0})). The orbits close after three cycles of /θ/^{0} and two cycles of /θ/^{1}, for any initial /θ/^{0} and /θ/^{1}. #CaptionEnd

#### Surfaces of section for integrable systems
As we have seen, in action-angle coordinates the angles move with constant angular frequencies, and the momenta are constant. Thus surfaces of section in action-angle coordinates are particularly simple. We can make surfaces of section for time-independent two-degree-of-freedom systems or one-degree-of-freedom systems
#page(314)
with periodic drive. In the latter case, one of the angles in the action-angle system is the phase of the drive. We make surfaces of section by accumulating points in one pair of canonical coordinates as the other coordinate goes through some particular value, such as zero. If we plot the section points with the angle coordinate on the abscissa and the conjugate momentum on the ordinate then the section points for all trajectories lie on horizontal lines, as illustrated in [figure 4.11](#figure_4.11).

#Image(Art_P863.jpg,figure_4.11)
#Caption *Figure 4.11* On surfaces of section for systems in action-angle coordinates a trajectory generates points on a horizontal line. Trajectories with frequencies that are commensurate with the sampling frequency produce a finite number of points, independent of the initial angle. Here we use different symbols to indicate section points for distinct trajectories with the same momentum /J/_{0}. Trajectories with frequencies that are incommensurate with the sampling frequency fill out a horizontal line densely. #CaptionEnd

For definiteness, let the plane of the surface of section be the (/θ/^{0}, /J/_{0}) plane, and the section condition be /θ/^{1} = 0. The other momentum /J/_{1} is chosen so that all the trajectories have the same energy. The momenta are all constant, so for a given trajectory all points that are generated are constrained to a line of constant /J/_{0}.

#page(315)

The time between section points is the period of /θ/^{1}: Δ/t/ = 2/π///ω/^{1}(/J/(/t/_{0})) because a section point is generated for every cycle of /θ/^{1}. The angle between successive points on the section is /ω/^{0}(/J/(/t/_{0}))Δ/t/ = /ω/^{0}(/J/(/t/_{0}))2/π///ω/^{1}(/J/(/t/_{0})) = 2/πν/(/J/(/t/_{0})), where /ν/(/J/) = /ω/^{0}(/J/)//ω/^{1}(/J/) is called the /rotation number/ of the trajectory. Let $\widehat{\theta}\left( i \right)$ and /Ĵ/(/i/) be the /i/th point (/i/ is an integer) in a sequence of points on the surface of section generated by a solution trajectory:

$$\begin{array}{ll} {\widehat{\theta}(i) = \theta^{0}(i\Delta t + t_{0})} & \\ {\widehat{J}(i) = J_{0}(i\Delta t + t_{0}),} \tag{4.38} \\ \end{array}$$

where the system is assumed to be on the section at /t/ = /t/_{0}. Along a trajectory, the map from one section point $(\widehat{\theta}\left( i \right),\widehat{J}\left( i \right))$ to the next $\left( {\widehat{\theta}\left( {i + 1} \right),\widehat{J}\left( {i + 1} \right)} \right)$ is of the form:#Footnote(12)

$$\begin{array}{ll} {\left( \begin{array}{l} {\widehat{\theta}(i + 1)} \\ {\widehat{J}(i + 1)} \\ \end{array} \right) = T\left( \begin{array}{l} {\widehat{\theta}(i)} \\ {\widehat{J}(i)} \\ \end{array} \right) = \left( \begin{array}{l} {\widehat{\theta}(i) + 2\pi\widehat{\nu}(\widehat{J}(i))} \\ {\widehat{J}(i)} \\ \end{array} \right).} \tag{4.39} \\ \end{array}$$

As a function of the action on the section, the rotation number is $\widehat{v}\left( {\widehat{J}{(0)}} \right) = v\left( {\widehat{J}{(0)},J_{1}\left( t_{0} \right)} \right)$, where /J/_{1}(/t/_{0}) has the value required to be on the section, as for example by giving the correct energy. If the rotation number function $\widehat{\nu}$ is strictly monotonic in the action coordinate on the section then the map is called a /twist map/.#Footnote(13)

On a surface of section the different types of orbits generate different patterns. If the two frequencies are commensurate, then the trajectory is periodic and only a finite number of points are generated on the surface of section. Each of the periodic solutions illustrated in [figure 4.10](#figure_4.10) generates two points on the surface of section defined by /θ/^{1} = 0. If the frequencies are commensurate they satisfy a relation of the form /kω/^{0}(/J/(/t/_{0})) = /jω/^{1}(/J/(/t/_{0})), where /J/(/t/_{0}) = (/Ĵ/(0), /J/_{1}(/t/_{0})) is the initial and constant value of the momentum tuple. The motion is periodic with frequency /ω/^{0}(/J/(/t/_{0}))//j/ = /ω/^{1}(/J/(/t/_{0}))//k/, so the period is 2/πj///ω/^{0}(/J/(/t/_{0})) = 2/πk///ω/^{1}(/J/(/t/_{0})). Thus this periodic orbit generates /k/ points on this
#page(316)
surface of section. For trajectories with commensurate frequencies the rotation number is rational:$\widehat{v}\left( {\widehat{J}{(0)}} \right) = v\left( {\widehat{J}{(0)},J_{1}\left( t_{0} \right)} \right) = j/k $. The coordinate /θ/^{1} makes /k/ cycles while the coordinate /θ/^{0} makes /j/ cycles ([figure 4.10](#figure_4.10) shows a system with a rotation number of 3/2). The frequencies depend on the momenta but not on the coordinates, so the motion is periodic with the same period and rotation number for all initial angles given these momenta. Thus there is a continuous family of periodic orbits with different initial angles.

If the two frequencies are incommensurate, then the 2-torus is filled densely. Thus the line on which the section points are generated is filled densely. Again, this is the case for any initial coordinates, because the frequencies depend only on the momenta. There are infinitely many such orbits that are distinct for a given set of frequencies.#Footnote(14)

### 4.5 Poincaré--Birkhoff Theorem
How does this picture change if we add additional effects?

One peculiar feature of the orbits in integrable systems is that there are continuous families of periodic orbits. The initial angles do not matter; the frequencies depend only on the actions. Contrast this with our earlier experience with surfaces of section in which periodic points are isolated, and associated with island chains. Henri Poincaré and George Birkhoff investigated periodic orbits of near-integrable systems, and found that typically for each rational rotation number there are a finite number of periodic points, half of which are linearly stable and half linearly unstable. Here we show how to construct the Poincaré--Birkhoff periodic points.

Consider an integrable system described in action-angle coordinates by the Hamiltonian /H/_{0}(/t/, /θ/, /J/) = /f/(/J/). We add some small additional effect described by the term /H/_{1} in the Hamiltonian

$$\begin{matrix} {H = H_{0} + \mathit{\epsilon}H_{1}.} \tag{4.40} \\ \end{matrix}$$

An example of such a system is the periodically driven pendulum with small-amplitude drive. For zero-amplitude drive the driven
#page(317)
pendulum is integrable, but not for small drive. Unfortunately, we do not yet have the tools to develop action-angle coordinates for the pendulum. A simpler problem that is already in action-angle form is the driven rotor, which is just the driven pendulum with gravity turned off. We can implement this by turning our driven pendulum on its side, making the plane of the pendulum horizontal. A Hamiltonian for the driven rotor is

$$\begin{matrix} {H(t,\theta,p_{\theta}) = \frac{p_{\theta}^{2}}{2ml^{2}} + mlA\omega^{2}\,\cos\,\omega t\,\cos\,\theta,} \tag{4.41} \\ \end{matrix}$$

where /A/ is the amplitude of the drive with frequency /ω/, /m/ is the mass of the bob, and /l/ is the length of the rotor. For zero amplitude, the Hamiltonian is already in action-angle form in that it depends only on the momentum /p_{θ}/ and the coordinate is an angle.

For an integrable system, the map generated on the surface of section is of the twist map form (#Eqn(chapter004,4.39,4.39)). With the addition of a small perturbation to the Hamiltonian, small corrections are added to the map

$$\begin{array}{lll} \left( \begin{array}{l} {\widehat{\theta}(i + 1)} \\ {\widehat{J}(i + 1)} \\ \end{array} \right) & {= T_{\mathit{\epsilon}}\left( \begin{array}{l} {\widehat{\theta}(i)} \\ {\widehat{J}(i)} \\ \end{array} \right)} & \\ & {= \left( \begin{array}{l} {\widehat{\theta}(i) + 2\pi\widehat{\nu}(\widehat{J}(i)) + \mathit{\epsilon}f(\widehat{\theta}(i),\widehat{J}(i))} \\ {\widehat{J}(i) + \mathit{\epsilon}g(\widehat{\theta}(i),\widehat{J}(i))} \\ \end{array} \right).} \tag{4.42} \\ \end{array}$$

Both the map /T/ and the perturbed map /T_{ϵ}/ are area preserving because the maps are generated as surfaces of section for Hamiltonian systems.

Suppose we are interested in determining whether periodic orbits of a particular rational rotation number $\widehat{v}\left( {\widehat{J}{(0)}} \right) = j/k $ exist in some interval of the action /α/ < /Ĵ/(0) < /β/. If the rotation number is strictly monotonic in this interval and orbits with the rotation number $\widehat{v}\left( {\widehat{J}{(0)}} \right)$ occur in this interval for the unperturbed map /T/, then by a simple construction we can show that periodic orbits with this rotation number also exist for /T_{ϵ}/ for sufficiently small /ϵ/.

If a point is periodic for rational rotation number $\widehat{v}\left( {\widehat{J}{(0)}} \right) = j/k $, with relatively prime /j/ and /k/, we expect /k/ distinct images of the point to appear on the section. So if we consider the /k/th iterate of the map then the point is a fixed point of the map. For rational rotation number /j///k/ the map /T^{k}/ has a fixed point for every initial angle.

#page(318)

#Image(Art_P869.jpg,figure_4.12)
#Caption *Figure 4.12* The map /T^{k}/ has a line of fixed points if the rotation number is the rational /j///k/. Points above this line map to larger /θ/^{0}; points below this line map to smaller /θ/^{0}. #CaptionEnd

#Image(Art_P870.jpg,figure_4.13)
#Caption *Figure 4.13* The map ¶ $ T_{\mathit{\epsilon}}^{k}$ ¶ is slightly different from /T^{k}/, but above the central region points still map to larger /θ/^{0} and below the central region they map to smaller /θ/^{0}. By continuity there are points between for which /θ/^{0} does not change. #CaptionEnd

The rotation number of the map /T/ is strictly monotonic. Suppose for definiteness we assume the rotation number $\widehat{v}\left( {\widehat{J}{(0)}} \right)$ increases with /Ĵ/(0). For some /Ĵ/^{∗} such that /α/ < /Ĵ/^{∗} < /β/ the rotation number is /j///k/, and (${\widehat{\theta}}^{\ast},{\widehat{J}}^{\ast}$) is a fixed point of /T^{k}/ for any initial ${\widehat{\theta}}^{\ast}$. For /Ĵ/^{∗} the rotation number of /T^{k}/ is zero. The rotation number of the map /T/ is monotonically increasing so for /Ĵ/(0) > /Ĵ/^{∗} the rotation number of /T^{k}/ is positive, and for /Ĵ/(0) < /Ĵ/^{∗} the rotation number of /T^{k}/ is negative, as long as /Ĵ/(0) is not too far from /Ĵ/^{∗}. See [figure 4.12](#figure_4.12).

#page(319)

#Image(Art_P871.jpg,figure_4.14)
#Caption *Figure 4.14* The solid curve /C/_{0} consists of points that map to the same /θ/^{0} under ¶ $ T_{\mathit{\epsilon}}^{k}$ ¶ . The image /C/_{1} of /C/_{0} under ¶ $ T_{\mathit{\epsilon}}^{k}$ ¶ is the dotted curve. Area preservation implies that these curves cross. #CaptionEnd

Now consider the map $ T_{\mathit{\epsilon}}^{k}$. In general, for small /ϵ/, points map to slightly different points under /T_{ϵ}/ than they do under /T/, but not too different. So we can expect that there is still some interval in /Ĵ/(0) near /Ĵ/^{∗} such that for /Ĵ/(0) in the upper end of the interval,$ T_{\mathit{\epsilon}}^{k}$ maps points to larger /θ/^{0}, and for points in the lower end of the interval,$ T_{\mathit{\epsilon}}^{k}$ maps points to smaller /θ/^{0}. If this is the case then for every $\widehat{\theta}{(0)}$ there is a point somewhere in the interval, some ${\widehat{J}}^{+}\left( {\widehat{\theta}{(0)}} \right)$, for which /θ/^{0} does not change, by continuity. These are not fixed points because the momentum /J/_{0} generally changes. See [figure 4.13](#figure_4.13).

The map is continuous, so we can expect that /Ĵ/^{+} is a continuous function of the /θ/^{0}. The twist-map condition (see footnote [13](#footnote_13)) ensures that /Ĵ/^{+} is periodic, so /Ĵ/^{+}(0) = /Ĵ/^{+}(2/π/). The twist-map condition also guarantees that for sufficiently small perturbations there cannot be more than one radially-mapping point for any angle. So the set of points that do not change /θ/^{0} under $ T_{\mathit{\epsilon}}^{k}$ form some periodic function of /θ/^{0}. Call this curve /C/_{0}. See [figure 4.14](#figure_4.14).

The map $ T_{\mathit{\epsilon}}^{k}$ takes the curve /C/_{0} to another curve /C/_{1} that, like /C/_{0}, is continuous and periodic. The two curves /C/_{0} and /C/_{1} must cross each other, as a consequence of area preservation. How do we see this? Typically, there is a lower boundary or upper boundary in /J/_{0} for the evolution. In some situations, we have such a lower boundary because /J/_{0} cannot be negative. For example, in action-angle variables for motion near an elliptic fixed point we will see
#page(320)
that the action is the area enclosed on the phase plane, which cannot be negative. For other situations, we might use the fact that there are invariant curves for large positive or negative /J/_{0}. In any case, suppose there is such a barrier /B/. Then the area of the region between the barrier and /C/_{0} must be equal to the area of the image of this region, which is the region between the barrier and /C/_{1}. So if /C/_{0} and /C/_{1} are not the same curve they must cross to contain the same area. In fact, they must cross an even number of times: they are both periodic, so if they cross once they must cross again to get back to the same side they started on. The points at which the curves /C/_{0} and /C/_{1} cross are fixed points because the angle does not change (that is what it means to be on /C/_{0}) and the action does not change (that is what it means for /C/_{0} and /C/_{1} to be the same at this point). So we have deduced that there must be an even number of fixed points of $ T_{\mathit{\epsilon}}^{k}$. For each fixed point of $ T_{\mathit{\epsilon}}^{k}$ there are /k/ images of this fixed point generated on the surface of section for the map /T_{ϵ}/. Each of these image points is a periodic point of the map /T_{ϵ}/.

#Image(Art_P873.jpg,figure_4.15)
#Caption *Figure 4.15* The fixed point on the left is linearly unstable. The one on the right is linearly stable. #CaptionEnd

We can deduce the stability of these fixed points of $ T_{\mathit{\epsilon}}^{k}$ just from the construction. The fixed points come in two types, elliptic and hyperbolic. An elliptic (stable) fixed point appears where the steps from /C/_{0} to /C/_{1} join with the flow of the background twist map to encircle the fixed point. A hyperbolic (unstable) fixed point appears where the steps from /C/_{0} to /C/_{1} join with the flow of the background twist map to move away from the fixed point. So just from the way the arrows connect we can determine the character of the fixed point. See [figure 4.15](#figure_4.15).

As we develop a Poincaré section, we find that some orbits leave traces that circulate around the stable fixed points, resulting in the
#page(321)
Poincaré--Birkhoff islands. If we look at a particular island we see that orbits in the island circulate around the fixed point at a rate that is monotonically dependent upon the distance from the fixed point. In the vicinity of the fixed point the evolution is governed by a twist map. So the entire Poincaré--Birkhoff construction can be carried out again. We expect that there will be concentric families of stable periodic points surrounded by islands and separated by separatrices emanating from unstable periodic points. Around each of these stable periodic orbits, the construction is repeated. So the Poincaré--Birkhoff construction is recursive, leading to the development of an infinite hierarchy of structure.

##### 4.5.1 Computing the Poincaré--Birkhoff Construction
There are so many conditions in our construction of the fixed points that one might be suspicious. We can make the construction more convincing by actually computing the various pieces for a specific problem. Consider the periodically driven rotor, with Hamiltonian (#Eqn(chapter004,4.41,4.41)). We set /m/ = 1 kg, /l/ = 1 m, /A/ = 0.1 m,$\omega = 4.2\sqrt{9.8}\,\text{rad}\,\text{s}^{- 1}$.

We call points that map to the same angle “radially mapping points.” We find them with a simple bisection search:
```Scheme
(define (radially-mapping-points Tmap Jmin Jmax phi eps) (bisect (lambda (J) ((principal-value pi) (Tmap phi J (lambda (phip Jp) (- phi phip)) (lambda () (error "should not get here"))))) Jmin Jmax eps)) 
```
The procedure Tmap implements some map, which may be an iterate of some more primitive map. We give the procedure an angle phi to study, a range of actions Jmin to Jmax to search, and a tolerance eps for the solution.

In [figure 4.16](#figure_4.16) we show the Poincaré--Birkhoff construction of the fixed points for the driven rotor. These particular curves are constructed for the two 1:1 commensurabilities between the rotation and the drive. One set of fixed points is constructed for each sense of rotation. The corresponding section is in [figure 4.17](#figure_4.17). We see that the section shows the existence of fixed points exactly where the Poincaré--Birkhoff construction shows the crossing of the curves /C/_{0} and /C/_{1}. Indeed, the nature of the fixed point is
#page(322)
clearly reflected in the relative configuration of the /C/_{0} and /C/_{1} curves.

In [figure 4.18](#figure_4.18) we show the result for a rotation number of 1/3. The curves are the radially mapping points for the third iterate of the section map (solid) and the images of these points (dotted). These curves are distorted by their proximity to the 1:1 islands shown in [figure 4.17](#figure_4.17). The corresponding section is shown in [figure 4.19](#figure_4.19).

### Exercise 4.7: Computing the Poincaré--Birkhoff construction

Consider [figure 3.27](#figure_3.27). Find the fixed points for the three major island chains, using the Poincaré--Birkhoff construction.

### 4.6 Invariant Curves
We started with an integrable system, where there are invariant curves. Do any invariant curves survive if a perturbation is added?

The Poincaré--Birkhoff construction for twist maps shows that invariant curves with rational rotation number typically do not survive perturbation. Upon perturbation the invariant curves with rational rotation numbers are replaced by an alternating sequence of stable and unstable periodic orbits. So if there are invariant curves that survive perturbation they must have irrational rotation numbers.

The perturbed system has chains of alternating stable and unstable fixed points for every rational rotation number. Each stable fixed point is surrounded by an island that occupies some region of the section. Each irrational is arbitrarily close to a rational, so it is not obvious that any invariant curve can survive an arbitrarily small perturbation.

Nevertheless, the Kolmogorov--Arnold--Moser (KAM) theorem proves that invariant curves do exist if the perturbation is small enough that the perturbed problem is “close enough” to an integrable problem, and if the rotation number is “irrational enough.” We will not prove this theorem here. Instead we will develop methods for finding particular invariant curves.

Stable periodic orbits have a stable island surrounding them on the surface of section. The largest islands are associated with rationals with small denominators. In general, the size of the island is limited to a size that decreases as the denominator increases. These islands are a local indication of the effect of the perturbation. Similarly, the chaotic zones appear near unstable periodic orbits and their homoclinic tangles. The homoclinic tangle is a continuous curve so it cannot cross an invariant curve, which is also continuous. If we are looking for invariant curves that persist upon perturbation, we would be wise to avoid regions of phase space where the islands or homoclinic tangles are major features.

#page(323)

#Image(Art_P875.jpg,figure_4.16)
#Caption *Figure 4.16* The curves /C/_{0} (solid) and /C/_{1} (dotted) for the 1:1 commensurability. #CaptionEnd

#Image(Art_P876.jpg,figure_4.17)
#Caption *Figure 4.17* A surface of section displaying the 1:1 commensurability. #CaptionEnd

#page(324)

#Image(Art_P877.jpg,figure_4.18)
#Caption *Figure 4.18* The curves /C/_{0} (solid) and /C/_{1} (dotted) for the 1:3 commensurability. The angle runs from −/π/ to /π/. The momentum runs from 3.5 to 4.5 in appropriate units. #CaptionEnd

#Image(Art_P878.jpg,figure_4.19)
#Caption *Figure 4.19* A surface of section displaying the 1:3 commensurability. The angle runs from −/π/ to /π/. The momentum runs from 3.5 to 4.5 in appropriate units. #CaptionEnd

#page(325)

The Poincaré--Birkhoff islands are ordered by rotation number. Because of the twist condition, the rotation number is monotonic in the momentum of the unperturbed problem. If there is an invariant curve with a given rotation number, it is sandwiched between island chains associated with rational rotation numbers. The rotation number of the invariant curve must be between the rotation numbers of the island chains on either side of it.

The fact that the size of the islands decreases with the size of the denominator suggests that invariant curves with rotation numbers for which nearby rationals require large denominators are the most likely to exist. So we will begin our search for invariant curves by examining rotation numbers that are not near rationals with small denominators.

Any irrational can be approximated by a sequence of rationals, and for each of these rationals we expect there to be stable and unstable periodic orbits with stable islands and homoclinic tangles. An invariant curve for a given rotation number has the best chance of surviving if the size of the islands associated with each rational approximation to the rotation number is smaller than the separation of the islands from that invariant curve.

For any particular size denominator, the best rational approximation to an irrational number is given by an initial segment of a simple continued fraction. If the approximating continued fraction converges slowly to the irrational number, then that number is not near rationals with small denominators. Thus, we will look for invariant curves with rotation numbers that have slowly converging continued-fraction approximations. The continued fractions that converge most slowly have tails that are all one. Such a number is called a /golden number/. For example, the golden ratio,

$$\begin{matrix} {\phi = \frac{1 + \sqrt{5}}{2} = 1 + \frac{1}{1 + \frac{1}{1 + \frac{1}{1 + \cdots}}},} \tag{4.43} \\ \end{matrix}$$

is just such a number.

#page(326)

##### 4.6.1 Finding Invariant Curves
Invariant curves, if there are any, are characterized by a particular rotation number. Points on the invariant curve map to points on the invariant curve. Neighboring points map to neighboring points, preserving the order.

On the section for the unperturbed integrable system, the angle between successive section points is constant: Δ/θ/ = 2/πν/(/J/) for rotation number /ν/(/J/). This map of the circle onto itself with constant angular step we call a /uniform circle map/.

For a given rotation number, points on the section are laid down in a particular order characteristic of the rotation number only. As a perturbation is turned on, the invariant curve with a particular rotation number will be distorted and the angle between successive points will no longer be constant. All that is required to have a particular rotation number is that the average change in angle be Δ/θ/. Nevertheless, the ordering of the points on the surface of section is preserved, and is characteristic of the rotation number.

The fact that the sequence of points on the surface of section for an invariant curve with a given rotation number must have a particular order can be used to find the invariant curve. At a specified angle we perform a bisection search for the momentum that lies on the invariant curve. We can tell whether the initial point is on the desired invariant curve or which side of the invariant curve it is on by evolving a candidate initial point with both the perturbed map and the uniform circle map and comparing the ordering of the sequences of points that are generated.

A program to implement this plan of attack is#Footnote(15)
```Scheme
(define (find-invariant-curve the-map rn theta0 Jmin Jmax eps) (bisect (lambda (J) (which-way? rn theta0 J the-map)) Jmin Jmax eps)) 
```
Since ordering inconsistencies are found near the initial angle we do not need to keep the whole list of angles. Instead, we can keep track of a small list of angles near the initial angle. In fact, keeping
#page(327)
track of the nearest angle on either side of the initial angle works well.

The procedure which-way? is implemented as a simple loop with state variables for the two orbits and the endpoints of the intervals. The z variables keep track of the angle of the uniform circle map; the x variables keep track of the angle of the map under study. The y variable is the momentum for the map under study. On each iteration we determine if the angle of the uniform circle map is in the interval of interest below or above the initial angle. If it is in neither interval then the map is further iterated. However, if it is in the region of interest then we check to see if the angle of the other map is in the corresponding interval. If so, the intervals for the uniform circle map and the other map are narrowed and the iteration proceeds. If the angle is not in the required interval, a discrepancy is noted and the sign of the discrepancy is reported. For this process to make sense the differences between the angles for successive iterations of both maps must be less than /π/.
```Scheme
(define (which-way? rotation-number x0 y0 the-map) (let ((pv (principal-value ( x0 pi)))) (let lp ((z x0) (zmin (- x0 :2pi)) (zmax (+ x0 :2pi)) (x x0) (xmin (- x0 :2pi)) (xmax (+ x0 :2pi)) (y y0)) (let ((nz (pv (+ z (* :2pi rotation-number))))) (the-map x y (lambda (nx ny) (let ((nx (pv nx))) (cond ((< x0 z zmax) (if (< x0 x xmax) (lp nz zmin z nx xmin x ny) (if (> x xmax) 1 -1))) ((< zmin z x0) (if (< xmin x x0) (lp nz z zmax nx x xmax ny) (if (< x xmin) -1 1))) (else (lp nz zmin zmax nx xmin xmax ny))))) (lambda () (error "Map failed" x y))))))) 
```
With this method of comparing rotation numbers we can find the initial momentum (for a given initial angle) for an invariant curve with a given rotation number to high precision.

#page(328)

#Image(Art_P880.jpg,figure_4.20)
#Caption *Figure 4.20* A surface of section displaying the invariant curve at rotation number 1 − 1//ϕ/ for the standard map with /K/ = .95. The invariant curve is in context: there is a chaotic region that almost eats the curve. The angle and momentum run from 0 to 2/π/. #CaptionEnd

We search the standard map for an invariant curve with a golden rotation number:#Footnote(16)

| (find-invariant-curve | (standard-map 0.95)      | |                       | (- 1 (/ 1 golden-ratio)) | |                       | 0.0                      | |                       | 2.0                      | |                       | 2.2                      | |                       | 1e-16)                   |

;Value: 2.1144605494391726

Using initial conditions computed in this way, we can produce the invariant curve (see [figure 4.20](#figure_4.20)). If we expand the putative
#page(329)
invariant curve it should remain a curve for all magnifications---it should show no sign of chaotic fuzziness (see [figure 4.21](#figure_4.21)).

#Image(Art_P881.jpg,figure_4.21)
#Caption *Figure 4.21* Here is a small portion of the invariant curve shown in [figure 4.20](#figure_4.20), magnified by 2/π/ × 10^{7}. We see that even at this magnification the points appear to lie on a line. We also see that the visitation frequency of points is highly nonuniform. #CaptionEnd

### Exercise 4.8: Invariant curves in the standard map

Find an invariant curve of the standard map with a different golden rotation number. Expand it to show that it retains the features of a curve at high magnification.

##### 4.6.2 Dissolution of Invariant Curves
As can be seen in [figure 4.21](#figure_4.21), the points on an invariant curve are not uniformly visited, unlike the picture we would get plotting the angles for the uniform circle map. This is because an interval may be expanded or compressed when mapped. We can compute the relative probability density for visitation of each angle on the invariant curve. A crude way to obtain this result is to count the number of points that fall into equal incremental angle bins. It is more effective to use the linear variational map constructed from the map being investigated to compute the change in incremental
#page(330)
angle from one point to its successor. Since all of the points in a small interval around the source point are mapped to points (in the same order) in a small interval around the target point, the relative probability density at a point is inversely proportional to the size of the incremental interval around that point. In order to get this started we need a good estimate of the initial slope for the invariant curve. We can estimate the slope by a difference quotient of the momentum and angle increments for the interval that we used to refine the momentum of the invariant curve with a given rotation number.

[Figures 4.22](#figure_4.22) and [4.23](#figure_4.23) show the relative probability density of visitation as a function of angle for the invariant curve of golden rotation number in the standard map for three different values of the parameter /K/. As /K/ increases, certain angles become less likely. Near /K/ = 0.971635406 some angles are never visited. But the invariant curve must be continuous. Thus it appears that for larger /K/ the invariant curve with this rotation number will not exist. Indeed, if the invariant set persists with the given rotation number it will have an infinite number of holes (because it has an irrational rotation number). Such a set is sometimes called a /cantorus/ (plural /cantori/).

### 4.7 Summary
Surfaces of section of a typical Hamiltonian system exhibit a menagerie of features including fixed points, invariant curves, resonance islands, and chaotic zones. Integrable systems have much simpler surfaces of section. By adding small effects to integrable systems we get insight into how this complicated behavior emerges.

Surfaces of section for integrable systems display only certain characteristic orbit types. There are fixed points, which correspond to equilibria or periodic orbits. A fixed point may be stable or unstable, depending on the stability of the corresponding equilibrium or orbit. There are sets of points on the section that are asymptotic forward and backward in time to the unstable fixed point. And there are sets of trajectories that fall on invariant curves. If the rotation number of the invariant curve is irrational, each of these trajectories densely covers the invariant curve; if the rotation number is rational, then each trajectory visits only a finite number of points on the invariant curve.

#page(331)

#Image(Art_P882.jpg,figure_4.22)
#Caption *Figure 4.22* The relative probability density of visitation as a function of angle for the invariant curve of golden rotation number in the standard map with /K/ = 0.95 (above) and /K/ = 0.97 (below). As /K/ increases, the function becomes more complex and certain angles become less likely to be visited. #CaptionEnd

#page(332)

#Image(Art_P883.jpg,figure_4.23)
#Caption *Figure 4.23* The relative probability density of visitation as a function of angle for the invariant curve of golden rotation number in the standard map with /K/ = 0.971635406. Here the function is very complex and appears self-similar. The valleys appear to reach to zero, so there are discrete angles that are never visited. #CaptionEnd

Linear stability analysis addresses the nature of the motion near the fixed points on the section. These points correspond to either equilibrium points or periodic orbits. There are characteristic frequencies of the motion, each with an associated characteristic direction. For Hamiltonian systems only certain patterns of characteristic frequencies are possible. On two-dimensional area-preserving surfaces of section, as generated by Hamiltonian systems, fixed points are linearly stable (elliptic fixed points) or linearly unstable (hyperbolic fixed points).

With the addition of small effects, the surface of section changes in certain typical ways. One characteristic change occurs near the unstable fixed points. The stable and unstable manifolds, those curves consisting of the sets of points that are asymptotic to the unstable fixed points forward and backward in time, no longer join smoothly, but instead cross. A first crossing implies that there are an infinite number of other crossings, and the stable and unstable manifolds develop an extremely complicated tangle.

#page(333)

The Poincaré--Birkhoff construction shows how the infinite number of periodic orbits on an invariant curve with rational rotation number that is characteristic of an integrable system degenerates into a finite number of alternating stable and unstable fixed points when the system becomes nonintegrable. This phenomenon is recursive, so we find that it develops an infinite hierarchy of structure: The region around every stable fixed point is itself filled with commensurabilities with alternating stable and unstable fixed points.

Some invariant curves survive the addition of small effects to an integrable system. The Kolmogorov--Arnold--Moser theorem proves that some invariant curves persist upon perturbation. We can find invariant curves of particular rotation numbers by comparing the pattern of points generated for a candidate initial point on the invariant curve to the expected pattern of points for the invariant curve being sought. As the additional effect is made stronger, the invariant curves that survive longest are those with the most irrational rotation number. At the point of breakup, the probability of visitation of various points on the invariant curve develops a self-similar appearance. For larger perturbations, the invariant curve disappears, leaving an invariant set with an infinite number of holes.

### 4.8 Projects
### Exercise 4.9: Secondary islands

In [figure 4.3](#figure_4.3) ([section 4.1](#section_4.1)) we see a chain of six secondary islands in the oscillation region. Carry out the Poincaré--Birkhoff construction to obtain the alternating sequence of stable and unstable fixed points for this island chain.

### Exercise 4.10: Invariant curves of the standard map

*a.* Make programs that reproduce [figures 4.22](#figure_4.22) and [4.23](#figure_4.23). You will need to develop an effective method of estimating the probability of visitation. There is one suggestion of how to do that in the text, but you may find a better way.

*b.* As the parameter /K/ is increased beyond the critical value, the golden invariant curve ceases to exist. Investigate how the method for finding invariant curves fails beyond the critical value of /K/.

----

#FootnoteRef(1)Keep in mind that the abscissa is an angle.

#FootnoteRef(2)Actually, all we need is ∂_{0}∂_{1}/F/ (/t/, /z_{e}/) = 0.

#FootnoteRef(3)If the eigenvalues are not distinct then the form of the solution is modified.

#FootnoteRef(4)The map /T/ is being used as an operator: multiplication is interpreted as composition.

#FootnoteRef(5)A characteristic multiplier is also sometimes called a Floquet multiplier.

#FootnoteRef(6)We assume for now that the eigenvalues are distinct.

#FootnoteRef(7)Sometimes it is argued that the stable and unstable manifolds cannot cross themselves on the basis of the uniqueness of solutions of differential equations. This argument is incorrect. The stable and unstable manifolds are not themselves solutions of a differential equation, they are sets of points whose solutions are asymptotic to the unstable fixed points.

#FootnoteRef(8)The procedure iterated-map takes a map and an integer n. It returns a new map that is the result of iterating the given map n times.

#FootnoteRef(9)A commensurability occurs when the frequencies involved are not linearly independent over the integers. We will define this carefully on [page 312](chapter004!p312).

#FootnoteRef(10)Motion with /n/ incommensurate frequencies is dense on the /n/-torus. Furthermore, such motion is /ergodic/ on the /n/-torus. This means that time averages of time-independent phase-space functions computed along trajectories are equal to the phase-space average of the same function over the torus.

#FootnoteRef(11)For time-independent systems with two degrees of freedom the boundary between regions described by different action-angle coordinates has asymptotic solutions and unstable periodic orbits or equilibrium points. The solutions on the boundary are not described by the action-angle Hamiltonian.

#FootnoteRef(12)The coordinate $\widehat{\theta}\left( i \right)$ is an angle. It can be brought to a standard interval such as 0 to 2/π/.

#FootnoteRef(13)For a map to be a twist map we require that there is a positive number /K/ such that |/Dν/(/J/)| > /K/ > 0 over some interval of /J/.

#FootnoteRef(14)The section points for any particular orbit are countable and dense, but they have zero measure on the line.

#FootnoteRef(15)This method depends on the assumptions that Jmin and Jmax bracket the actual momentum, and that the rotation number is sufficiently continuous in momentum in that region.

#FootnoteRef(16)There is no invariant curve in the standard map that has rotation number /ϕ/ = 1.618.... However, 1 − 1//ϕ/ has the same continued-fraction tail as /ϕ/ and this rotation number appears in the standard map.
#FootnoteEnd

#page(334) 
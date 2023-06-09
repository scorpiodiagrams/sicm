!!Polyglot
## Our Notation
### Chapter 9
#page(509)
#Quote(An adequate notation should be understood by at least two people, one of whom may be the author.)
#Caption Abdus Salam (1950#).#CaptionEnd

We adopt a /functional mathematical notation/ that is close to that used by Spivak in his /Calculus on Manifolds/ [40](bibliography!bib_40). The use of functional notation avoids many of the ambiguities of traditional mathematical notation; the ambiguities of traditional notation that can impede clear reasoning in classical mechanics. Functional notation carefully distinguishes the function from the value of the function when applied to particular arguments. In functional notation mathematical expressions are unambiguous and self-contained.

We adopt a /generic arithmetic/ in which the basic arithmetic operations, such as addition and multiplication, are extended to a wide variety of mathematical types. Thus, for example, the addition operator + can be applied to numbers, tuples of numbers, matrices, functions, etc. Generic arithmetic formalizes the common informal practice used to manipulate mathematical objects.

We often want to manipulate aggregate quantities, such as the collection of all of the rectangular coordinates of a collection of particles, without explicitly manipulating the component parts. Tensor arithmetic provides a traditional way of manipulating aggregate objects: Indices label the parts; conventions, such as the summation convention, are introduced to manipulate the indices. We introduce a /tuple arithmetic/ as an alternative way of manipulating aggregate quantities that usually lets us avoid labeling the parts with indices. Tuple arithmetic is inspired by tensor arithmetic but it is more general: not all of the components of a tuple need to be of the same size or type.

The mathematical notation is in one-to-one correspondence with expressions of the computer language /Scheme/ [24](bibliography!bib_24). Scheme is based on the /λ/-calculus [13](bibliography!bib_13) and directly supports the manipulation of functions. We augment Scheme with symbolic, numerical,
#page(510)
and generic features to support our applications. For a simple introduction to Scheme, see the Scheme appendix. The correspondence between the mathematical notation and Scheme requires that mathematical expressions be unambiguous and self-contained. Scheme provides immediate feedback in verification of mathematical deductions and facilitates the exploration of the behavior of systems.

#### Functions
The value of the function /f/, given the argument /x/, is written /f/(/x/). The expression /f/(/x/) denotes the value of the function at the given argument; when we wish to denote the function we write just /f/. Functions may take several arguments. For example, we may have the function that gives the Euclidean distance between two points in the plane given by their rectangular coordinates:

$$\begin{matrix} {d(x_{1},y_{1},x_{2},y_{2}) = \sqrt{\left( {x_{2} - x_{1}} \right)^{2} + \left( {y_{2} - y_{1}} \right)^{2}}.} \tag{9.1} \\ \end{matrix}$$

In Scheme we can write this as:
```Scheme
(define 
  (d x1 y1 x2 y2) 
  (sqrt 
    (+ 
      (square 
        (- x2 x1)) 
      (square 
        (- y2 y1))))) 
```
Functions may be composed if the range of one overlaps the domain of the other. The composition of functions is constructed by passing the output of one to the input of the other. We write the composition of two functions using the ∘ operation:

$$\begin{matrix} \left. (f \circ g):x\mapsto(f \circ g)(x) = f(g(x)). \right. \tag{9.2} \\ \end{matrix}$$

A procedure h that computes the cube of the sine of its argument may be defined by composing the procedures cube and sin:
```Scheme
(define h (compose cube sin)) (h 2) 
```
```Scheme
.7518269446689928 
```
which is the same as
```Scheme
(cube (sin 2)) 
```
```Scheme
.7518269446689928 
```
#page(511)

Arithmetic is extended to the manipulation of functions: the usual mathematical operations may be applied to functions. Examples are addition and multiplication; we may add or multiply two functions if they take the same kinds of arguments and if their values can be added or multiplied:

$$\begin{array}{rll} {(f + g)(x)} & {= f(x) + g(x)} & \\ {(fg)(x)} & {= f(x)g(x).} \tag{9.3} \\ \end{array}$$

A procedure g that multiplies the cube of its argument by the sine of its argument is
```Scheme
(define g (* cube sin)) (g 2) 
```
```Scheme
7.274379414605454 
```
```Scheme
(* (cube 2) (sin 2)) 
```
```Scheme
7.274379414605454 
```
#### Symbolic values
As in usual mathematical notation, arithmetic is extended to allow the use of symbols that represent unknown or incompletely specified mathematical objects. These symbols are manipulated as if they had values of a known type. By default, a Scheme symbol is assumed to represent a real number. So the expression 'a is a literal Scheme symbol that represents an unspecified real number:
```Scheme
((compose cube sin) 'a) (expt (sin a) 3) 
```
The default printer simplifies the expression and displays it in a readable form.#Footnote(1) We can use the simplifier to verify a trigonometric identity:
```Scheme
((- (+ (square sin) (square cos)) 1) 'a) 
```
```Scheme
0 
```
#page(512)

Just as it is useful to be able to manipulate symbolic numbers, it is useful to be able to manipulate symbolic functions. The procedure literal-function makes a procedure that acts as a function having no properties other than its name. By default, a literal function is defined to take one real argument and produce one real value. For example, we may want to work with a function /f/ : *R* → *R*:
```Scheme
((literal-function 'f) 'x) 
```
```Scheme
(f x) 
```
```Scheme
(compose 
  (literal-function 'f) 
  (literal-function 'g)) 
'x) 
```
```Scheme
(f (g x)) 
```
We can also make literal functions of multiple, possibly structured arguments that return structured values. For example, to denote a literal function named g that takes two real arguments and returns a real value (/g/ : *R* × *R* → *R*) we may write:
```Scheme
(define g (literal-function 'g (-> (X Real Real) Real))) (g 'x 'y) 
```
```Scheme
(g x y) 
```
We may use such a literal function anywhere that an explicit function of the same type may be used.

There is a whole language for describing the type of a literal function in terms of the number of arguments, the types of the arguments, and the types of the values. Here we describe a function that maps pairs of real numbers to real numbers with the expression (-> (X Real Real) Real). Later we will introduce structured arguments and values and show extensions of literal functions to handle these.

#### Tuples
There are two kinds of tuples: /up/ tuples and /down/ tuples. We write tuples as ordered lists of their components; a tuple is delimited by parentheses if it is an up tuple and by square brackets if it is a down tuple. For example, the up tuple /v/ of velocity components /v/^{0}, /v/^{1}, and /v/^{2} is

$$\begin{matrix} {v = \left( {v^{0},v^{1},v^{2}} \right).} \tag{9.4} \\ \end{matrix}$$

The down tuple /p/ of momentum components /p/_{0}, /p/_{1}, and /p/_{2} is

$$\begin{matrix} {p = \lbrack p_{0},p_{1},p_{2}\rbrack.} \tag{9.5} \\ \end{matrix}$$

#page(513)

A component of an up tuple is usually identified by a superscript. A component of a down tuple is usually identified by a subscript. We use zero-based indexing when referring to tuple elements. This notation follows the usual convention in tensor arithmetic.

We make tuples with the constructors up and down:
```Scheme
(define v (up 'v^0 'v^1 'v^2)) v 
```
```Scheme
(up v^0 v^1 v^2) 
```
```Scheme
(define p (down 'p_0 'p_1 'p_2)) p 
```
```Scheme
(down p_0 p_1 p_2) 
```
Tuple arithmetic is different from the usual tensor arithmetic in that the components of a tuple may also be tuples and different components need not have the same structure. For example, a tuple structure /s/ of phase-space states is

$$\begin{matrix} {s = (t,(x,y),\lbrack p_{x},p_{y}\rbrack).} \tag{9.6} \\ \end{matrix}$$

It is an up tuple of the time, the coordinates, and the momenta. The time /t/ has no substructure. The coordinates are an up tuple of the coordinate components /x/ and /y/. The momentum is a down tuple of the momentum components /p_{x}/ and /p_{y}/. This is written:
```Scheme
(define s (up 't (up 'x 'y) (down 'p_x 'p_y))) 
```
In order to reference components of tuple structures there are selector functions, for example:

$$\begin{array}{rll} {I(s)} & {= s} & \\ {I_{0}(s)} & {= t} & \\ {I_{1}(s)} & {= (x,y)} & \\ {I_{2}(s)} & {= \left\lbrack p_{x},p_{y} \right\rbrack} & \\ {I_{1,0}(s)} & {= x} & \\  & \ldots & \\ {I_{2,1}(s)} & {= p_{y}.} \tag{9.7} \\ \end{array}$$

The sequence of integer subscripts on the selector describes the access chain to the desired component.

#page(514)

The procedure component is the general selector procedure that implements the selector functions. For example, /I/_{0,1} is implemented by (component 0 1):
```Scheme
((component 0 1) (up (up 'a 'b) (up 'c 'd))) 
```
```Scheme
b 
```
To access a component of a tuple we may also use the selector procedure ref, which takes a tuple and an index and returns the indicated element of the tuple:
```Scheme
(ref (up 'a 'b 'c) 1) 
```
```Scheme
b 
```
We use zero-based indexing everywhere. The procedure ref can be used to access any substructure of a tree of tuples:
```Scheme
(ref 
  (up 
    (up 'a 'b) 
    (up 'c 'd)) 
  0 1) 
```
```Scheme
b 
```
Two up tuples of the same length may be added or subtracted, elementwise, to produce an up tuple, if the components are compatible for addition. Similarly, two down tuples of the same length may be added or subtracted, elementwise, to produce a down tuple, if the components are compatible for addition.

Any tuple may be multiplied by a number by multiplying each component by the number. Numbers may, of course, be multiplied. Tuples that are compatible for addition form a vector space.

For convenience we define the square of a tuple to be the sum of the squares of the components of the tuple. Tuples can be multiplied, as described below, but the square of a tuple is not the product of the tuple with itself.

The meaning of multiplication of tuples depends on the structure of the tuples. Two tuples are compatible for contraction if they are of opposite types, they are of the same length, and corresponding elements have the following property: either they are both tuples and are compatible for contraction, or one of them is not a tuple. If two tuples are compatible for contraction then generic multiplication is interpreted as contraction: the result is the sum of the products of corresponding components of the tuples. For example, /p/ and /v/ introduced in equations (#Eqn(chapter009,9.4,9.4)) and (#Eqn(chapter009,9.5,9.5)) above are compatible for contraction; the product is

#page(515)

$$\begin{matrix} {pv = p_{0}v^{0} + p_{1}v^{1} + p_{2}v^{2}.} \tag{9.8} \\ \end{matrix}$$

So the product of tuples that are compatible for contraction is an inner product. Using the tuples p and v defined above gives us
```Scheme
(* p v) 
```
```Scheme
(+ 
  (* p_0 v^0) 
  (* p_1 v^1) 
  (* p_2 v^2)) 
```
Contraction of tuples is commutative: /pv/ = /vp/. Caution: Multiplication of tuples that are compatible for contraction is, in general, not associative. For example, let /u/ = (5, 2), /v/ = (11, 13), and /g/ = [[3, 5], [7, 9]]. Then /u/(/gv/) = 964, but (/ug/)/v/ = 878. The expression /ugv/ is ambiguous. An expression that has this ambiguity does not occur in this book.

The rule for multiplying two structures that are not compatible for contraction is simple. If /A/ and /B/ are not compatible for contraction, the product /AB/ is a tuple of type /B/ whose components are the products of /A/ and the components of /B/. The same rule is applied recursively in multiplying the components. So if /B/ = (/B/^{0}, /B/^{1}, /B/^{2}), the product of /A/ and /B/ is

$$\begin{matrix} {AB = (AB^{0},AB^{1},AB^{2}).} \tag{9.9} \\ \end{matrix}$$

If /A/ and /C/ are not compatible for contraction and /C/ = [/C/_{0}, /C/_{1}, /C/_{2}], the product is

$$\begin{matrix} {AC = \left\lbrack {AC_{0},AC_{1},AC_{2}} \right\rbrack.} \tag{9.10} \\ \end{matrix}$$

Tuple structures can be made to represent linear transformations. For example, the rotation commonly represented by the matrix

$$\begin{matrix} \begin{bmatrix} {\cos\theta} & {- \sin\theta} \\ {\sin\theta} & {\cos\theta} \\ \end{bmatrix} \tag{9.11} \\ \end{matrix}$$

can be represented as a tuple structure:#Footnote(2)

#page(516)

$$\begin{matrix} {\begin{bmatrix} \begin{pmatrix} {\cos\theta} \\ {\sin\theta} \\ \end{pmatrix} & \begin{pmatrix} {- \sin\theta} \\ {\cos\theta} \\ \end{pmatrix} \\ \end{bmatrix}.} \tag{9.12} \\ \end{matrix}$$

Such a tuple is compatible for contraction with an up tuple that represents a vector. So, for example:

$$\begin{matrix} {\begin{bmatrix} \begin{pmatrix} {\cos\theta} \\ {\sin\theta} \\ \end{pmatrix} & \begin{pmatrix} {- \sin\theta} \\ {\cos\theta} \\ \end{pmatrix} \\ \end{bmatrix}\,\begin{pmatrix} x \\ y \\ \end{pmatrix} = \begin{pmatrix} {x\cos\theta - y\sin\theta} \\ {x\sin\theta + y\cos\theta} \\ \end{pmatrix}.} \tag{9.13} \\ \end{matrix}$$

Two tuples that represent linear transformations, though not compatible for contraction, may also be combined by multiplication. In this case the product represents the composition of the linear transformations. For example, the product of the tuples representing two rotations is

$$\begin{matrix} {{\begin{bmatrix} \begin{pmatrix} {\cos\theta} \\ {\sin\theta} \\ \end{pmatrix} & \begin{pmatrix} {- \sin\theta} \\ {\cos\theta} \\ \end{pmatrix} \\ \end{bmatrix}\,}\begin{bmatrix} \begin{pmatrix} {\cos\varphi} \\ {\sin\varphi} \\ \end{pmatrix} & \begin{pmatrix} {- \sin\varphi} \\ {\cos\varphi} \\ \end{pmatrix} \\ \end{bmatrix}} & \\ {= \begin{bmatrix} \begin{pmatrix} {\cos(\theta + \varphi)} \\ {\sin(\theta + \varphi)} \\ \end{pmatrix} & \begin{pmatrix} {- \sin(\theta + \varphi)} \\ {\cos(\theta + \varphi)} \\ \end{pmatrix} \\ \end{bmatrix}.} \tag{9.14} \\ \end{matrix}$$

Multiplication of tuples that represent linear transformations is associative but generally not commutative, just as the composition of the transformations is associative but not generally commutative.

#### Derivatives
The derivative of a function /f/ is a function, denoted by /Df/. Our notational convention is that /D/ is a high-precedence operator. Thus /D/ operates on the adjacent function before any other application occurs: /Df/(/x/) is the same as (/Df/)(/x/). Higher-order derivatives are described by exponentiating the derivative operator. Thus the /n/th derivative of a function /f/ is notated as /D^{n}f/.

The procedure for producing the derivative of a function is named D. The derivative of the sin procedure is a procedure that computes cos:
```Scheme
(define derivative-of-sine (D sin)) (derivative-of-sine 'x) 
```
```Scheme
(cos x) 
```
The derivative of a function /f/ is the function /Df/ whose value for a particular argument is something that can be multiplied by an increment Δ/x/ in the argument to get a linear approximation to the increment in the value of /f/:

$$\begin{matrix} {f(x + \Delta x) \approx f(x) + D\, f(x)\Delta x.} \tag{9.15} \\ \end{matrix}$$

#page(517)

For example, let /f/ be the function that cubes its argument (/f/(/x/) = /x/^{3}); then /Df/ is the function that yields three times the square of its argument (/Df/(/y/) = 3/y/^{2}). So /f/(5) = 125 and /Df/(5) = 75. The value of /f/ with argument /x/ + Δ/x/ is

$$\begin{matrix} {f(x + \Delta x) = {(x + \Delta x)}^{3} = x^{3} + 3x^{2}\Delta x + 3x\Delta x^{2} + \Delta x^{3}} \tag{9.16} \\ \end{matrix}$$

and

$$\begin{matrix} {Df(x)\Delta x = 3x^{2}\Delta x.} \tag{9.17} \\ \end{matrix}$$

So /Df/(/x/) multiplied by Δ/x/ gives us the term in /f/(/x/ + Δ/x/) that is linear in Δ/x/, providing a good approximation to /f/(/x/ + Δ/x/) − /f/(/x/) when Δ/x/ is small.

Derivatives of compositions obey the chain rule:

$$\begin{matrix} {D(f \circ g) = ((Df) \circ g) \cdot Dg.} \tag{9.18} \\ \end{matrix}$$

So at /x/,

$$\begin{matrix} {(D(f \circ g))(x) = Df(g(x)) \cdot Dg(x).} \tag{9.19} \\ \end{matrix}$$

D is an example of an /operator/. An operator is like a function except that multiplication of operators is interpreted as composition, whereas multiplication of functions is multiplication of the values (see equation #Eqn(chapter009,9.3,9.3)). If /D/ were an ordinary function, then the rule for multiplication would imply that /D/^{2}/f/ would just be the product of /Df/ with itself, which is not what is intended. A product of a number and an operator scales the operator. So, for example
```Scheme
(((* 5 D) cos) 'x) 
```
```Scheme
(* -5 (sin x)) 
```
Arithmetic is extended to allow manipulation of operators. A typical operator is (/D/+/I/)(/D/−/I/) = /D/^{2}−/I/, where /I/ is the identity operator, which subtracts a function from its second derivative. Such an operator can be constructed and used as follows:
```Scheme
(((* (+ D I) (- D I)) (literal-function 'f)) 'x)
```
```Scheme
(+ (((expt D 2) f) x) (* -1 (f x))) 
```
#page(518)

#### Derivatives of functions of multiple arguments
The derivative generalizes to functions that take multiple arguments. The derivative of a real-valued function of multiple arguments is an object whose contraction with the tuple of increments in the arguments gives a linear approximation to the increment in the function's value.

A function of multiple arguments can be thought of as a function of an up tuple of those arguments. Thus an incremental argument tuple is an up tuple of components, one for each argument position. The derivative of such a function is a down tuple of the partial derivatives of the function with respect to each argument position.

Suppose we have a real-valued function /g/ of two real-valued arguments, and we want to approximate the increment in the value of /g/ from its value at /x/, /y/. If the arguments are incremented by the tuple (Δ/x,/ Δ/y/) we compute:

$$\begin{array}{lll} {Dg(x,y) \cdot (\Delta x,\Delta y)} & {= \lbrack\partial_{0}g(x,y),\partial_{1}g(x,y)\rbrack \cdot (\Delta x,\Delta y)} & \\  & {= \partial_{0}g(x,y)\Delta x + \partial_{1}g(x,y)\Delta y.} \tag{9.20} \\ \end{array}$$

Using the two-argument literal function g defined on [page 512](chapter009!p512), we have:
```Scheme
((D g) 'x 'y) 
```
```Scheme
(down (((partial 0) g) x y) (((partial 1) g) x y)) 
```
In general, partial derivatives are just the components of the derivative of a function that takes multiple arguments (or structured arguments or both; see below). So a partial derivative of a function is a composition of a component selector and the derivative of that function.#Footnote(3) Indeed:

$$\begin{matrix} {\partial_{0}g = I_{0} \circ Dg} \tag{9.21} \\ \end{matrix}$$

$$\begin{matrix} {\partial_{1}g = I_{1} \circ Dg.} \tag{9.22} \\ \end{matrix}$$

Concretely, if

$$\begin{matrix} {g(x,y) = x^{3}y^{5}} \tag{9.23} \\ \end{matrix}$$

#page(519)

then

$$\begin{matrix} {Dg(x,y) = \left\lbrack {3x^{2}y^{5},5x^{3}y^{4}} \right\rbrack} \tag{9.24} \\ \end{matrix}$$

and the first-order approximation of the increment for changing the arguments by Δ/x/ and Δ/y/ is

$$\begin{array}{lll} {g(x + \Delta x,y + \Delta y) - g(x,y)} & {\approx \left\lbrack {3x^{2}y^{5},5x^{3}y^{4}} \right\rbrack \cdot (\Delta x,\Delta y)} & \\  & {= 3x^{2}y^{5}\Delta x + 5x^{3}y^{4}\Delta y.} \tag{9.25} \\ \end{array}$$

Partial derivatives of compositions also obey a chain rule:

$$\begin{matrix} {\partial_{i}(f \circ g) = ((D\, f) \circ g) \cdot \partial_{i}g.} \tag{9.26} \\ \end{matrix}$$

So if /x/ is a tuple of arguments, then

$$\begin{matrix} {(\partial_{i}(f \circ g))(x) = Df(g(x)) \cdot \partial_{i}g(x).} \tag{9.27} \\ \end{matrix}$$

Mathematical notation usually does not distinguish functions of multiple arguments and functions of the tuple of arguments. Let /h/((/x/, /y/)) = /g/(/x/, /y/). The function /h/, which takes a tuple of arguments /x/ and /y/, is not distinguished from the function /g/ that takes arguments /x/ and /y/. We use both ways of defining functions of multiple arguments. The derivatives of both kinds of functions are compatible for contraction with a tuple of increments to the arguments. Scheme comes in handy here:
```Scheme
(define (h s) (g (ref s 0) (ref s 1))) (h (up 'x 'y)) 
```
```Scheme
(g x y) 
```
```Scheme
((D g) 'x 'y) 
```
```Scheme
(down (((partial 0) g) x y) (((partial 1) g) x y)) 
```
```Scheme
((D h) (up 'x 'y)) 
```
```Scheme
(down (((partial 0) g) x y) (((partial 1) g) x y)) 
```
A phase-space state function is a function of time, coordinates, and momenta. Let /H/ be such a function. The value of /H/ is /H/(/t,/ (/x/, /y/), [/p_{x}/, /p_{y}/]) for time /t/, coordinates (/x/, /y/), and momenta [/p_{x}/, /p_{y}/]. Let /s/ be the phase-space state tuple as in (#Eqn(chapter009,9.6,9.6)):

$$\begin{matrix} {s = \left( {t,(x,y),\left\lbrack {p_{x},p_{y}} \right\rbrack} \right).} \tag{9.28} \\ \end{matrix}$$

#page(520)

The value of /H/ for argument tuple /s/ is /H/(/s/). We use both ways of writing the value of /H/.

We often show a function of multiple arguments that include tuples by indicating the boundaries of the argument tuples with semicolons and separating their components with commas. If /H/ is a function of phase-space states with arguments /t/, (/x/, /y/), and [/p_{x}/, /p_{y}/], we may write /H/(/t/; /x/, /y/; /p_{x}/, /p_{y}/). This notation loses the up#/down distinction, but our semicolon-and-comma notation is convenient and reasonably unambiguous.

The derivative of /H/ is a function that produces an object that can be contracted with an increment in the argument structure to produce an increment in the function's value. The derivative is a down tuple of three partial derivatives. The first partial derivative is the partial derivative with respect to the numerical argument. The second partial derivative is a down tuple of partial derivatives with respect to each component of the up-tuple argument. The third partial derivative is an up tuple of partial derivatives with respect to each component of the down-tuple argument:

$$\begin{array}{lll} {DH(s)} & {= \left\lbrack {\partial_{0}H(s),\partial_{1}H(s),\partial_{2}H(s)} \right\rbrack} & \\  & {= \left\lbrack {\partial_{0}H(s),\left\lbrack {\partial_{1,0}H(s),\partial_{1,1}H(s)} \right\rbrack,\left( {\partial_{2,0}H(s),\partial_{2,1}H(s)} \right)} \right\rbrack,} \tag{9.29} \\ \end{array}$$

where ∂_{1,0} indicates the partial derivative with respect to the first component (index 0) of the second argument (index 1) of the function, and so on. Indeed, ∂/_{z}F/ = /I_{z}/ ∘ /DF/ for any function /F/ and access chain /z/. So, if we let Δ/s/ be an incremental phase-space state tuple,

$$\begin{matrix} {\Delta s = (\Delta t,(\Delta x,\Delta y),\lbrack\Delta p_{x},\Delta p_{y}\rbrack),} \tag{9.30} \\ \end{matrix}$$

then

$$\begin{array}{lll} {DH(s)\Delta s} & {= \partial_{0}H(s)\Delta t} & \\  & {\,\,\, + \partial_{1,0}H(s)\Delta x + \partial_{1,1}H(s)\Delta y} & \\  & {\,\,\, + \partial_{2,0}H(s)\Delta p_{x} + \partial_{2,1}H(s)\Delta p_{y}.} \tag{9.31} \\ \end{array}$$

Caution: Partial derivative operators with respect to different structured arguments generally do not commute.

#page(521)

In Scheme we must make explicit choices. We usually assume that phase-space state functions are functions of the tuple. For example,
```Scheme
(define H (literal-function 'H (-> (UP Real (UP Real Real) (DOWN Real Real)) Real))) (H s) 
```
```Scheme
(H (up t (up x y) (down p_x p_y))) 
```
```Scheme
((D H) s) 
```
```Scheme
(down 
  ( ( (partial 0) 
    H) 
    (up t 
      (up x y) 
      (down p_x p_y))) 
  (down 
    ( ( (partial 1 0)
        H) 
      (up t 
        (up x y) 
        (down p_x p_y))) 
    ( ( (partial 1 1) 
        H) 
      (up t 
        (up x y) 
        (down p_x p_y)))) 
  (up 
    ( ( (partial 2 0) 
        H) 
      (up t 
        (up x y) 
        (down p_x p_y))) 
    ( ( (partial 2 1) 
        H) 
      (up t 
        (up x y) 
        (down p_x p_y))))) 
```
#### Structured results
Some functions produce structured outputs. A function whose output is a tuple is equivalent to a tuple of component functions each of which produces one component of the output tuple.

For example, a function that takes one numerical argument and produces a structure of outputs may be used to describe a curve through space. The following function describes a helical path around the /z/-axis in three-dimensional space:

$$\begin{matrix} {h(t) = (\cos t,\sin t,t) = (\cos,\sin,I)(t).} \tag{9.32} \\ \end{matrix}$$

The derivative is just the up tuple of the derivatives of each component of the function:

$$\begin{matrix} {Dh(t) = ( - \sin t,\cos t,1).} \tag{9.33} \\ \end{matrix}$$

We can write
```Scheme
(define (helix t) (up (cos t) (sin t) t)) 
```
or just
```Scheme
(define helix (up cos sin identity)) 
```
#page(522)

Its derivative is just the up tuple of the derivatives of each component of the function:
```Scheme
((D helix) 't) 
```
```Scheme
(up (* -1 (sin t)) (cos t) 1) 
```
In general, a function that produces structured outputs is just treated as a structure of functions, one for each of the components. The derivative of a function of structured inputs that produces structured outputs is an object that when contracted with an incremental input structure produces a linear approximation to the incremental output. Thus, if we define function /g/ by

$$\begin{matrix} {g(x,y) = \left( {\left( {x + y} \right)^{2},\left( {y - x} \right)^{3},e^{x + y}} \right),} \tag{9.34} \\ \end{matrix}$$

then the derivative of /g/ is

$$\begin{matrix} {Dg(x,y) = \left\lbrack {\begin{pmatrix} {2(x + y)} \\ {- 3{(y - x)}^{2}} \\ e^{x + y} \\ \end{pmatrix},\begin{pmatrix} {2(x + y)} \\ {3{(y - x)}^{2}} \\ e^{x + y} \\ \end{pmatrix}} \right\rbrack.} \tag{9.35} \\ \end{matrix}$$

In Scheme:
```Scheme
(define (g x y) (up (square (+ x y)) (cube (- y x)) (exp (+ x y)))) ((D g) 'x 'y) 
```
```Scheme
(down (up (+ (* 2 x) (* 2 y)) (+ (* -3 (expt x 2)) (* 6 x y) (* -3 (expt y 2))) (* (exp y) (exp x))) ( (+ (* 2 x) (* 2 y)) (+ (* 3 (expt x 2)) (* -6 x y) (* 3 (expt y 2))) (* (exp y) (exp x)))) 
```
Caution must be exercised when taking the derivative of the product of functions that each produce structured results. The problem is that the usual product rule does not hold. Let /f/ and /g/ be functions of /x/ whose results are compatible for contraction to a number. The increment of /f/ for an increment Δ/x/ of /x/ is /Df/(/x/)Δ/x/, and similarly for /g/. The increment of the product /fg/ is /D/(/fg/)(/x/)Δ/x/, but expanded in terms of the derivative of /f/ and /g/ the increment is (/Df/(/x/)Δ/x/)/g/(/x/) + /f/(/x/)(/Dg/(/x/)Δ/x/). It is not ((/Df/)(/x/)/g/(/x/) + /f/(/x/)(/Dg/(/x/)))Δ/x/. The reason is that the shape of the derivative of /f/ is such that /Df/(/x/) should be multiplied by Δ/x/ rather than /g/(/x/).

#page(523)

### Exercise 9.1: Chain rule

Let /F/ (/x/, /y/) = /x/^{2}/y/^{3}, /G/(/x/, /y/) = (/F/ (/x/, /y/), /y/), and /H/(/x/, /y/) = /F/ (/F/ (/x/, /y/), /y/), so that /H/ = /F/ ∘ /G/.

 **a.** Compute ∂_{0}/F/ (/x/, /y/) and ∂_{1}/F/ (/x/, /y/).
 **b.** Compute ∂_{0}/F/ (/F/ (/x/, /y/), /y/) and ∂_{1}/F/ (/F/ (/x/, /y/), /y/).
 **c.** Compute ∂_{0}/G/(/x/, /y/) and ∂_{1}/G/(/x/, /y/).
 **d.** Compute /DF/ (/a/, /b/), /DG/(3, 5) and /DH/(3/a/^{2}, 5/b/^{3}).

### Exercise 9.2: Computing derivatives

We can represent functions of multiple arguments as procedures in several ways, depending upon how we wish to use them. The simplest idea is to identify the procedure arguments with the function's arguments.

For example, we could write implementations of the functions that occur in [exercise 9.1](#exercise_9.1) as follows:
```Scheme
(define (f x y) (* (square x) (cube y))) (define (g x y) (up (f x y) y)) (define (h x y) (f (f x y) y)) 
```
With this choice it is awkward to compose a function that takes multiple arguments, such as /f/, with a function that produces a tuple of those arguments, such as /g/. Alternatively, we can represent the function arguments as slots of a tuple data structure, and then composition with a function that produces such a data structure is easy. However, this choice requires the procedures to build and take apart structures.

For example, we may define procedures that implement the functions above as follows:
```Scheme
(define (f v) (let ((x (ref v 0)) (y (ref v 1))) (* (square x) (cube y)))) (define (g v) (let ((x (ref v 0)) (y (ref v 1))) (up (f v) y))) (define h (compose f g)) 
```
Repeat [exercise 9.1](#exercise_9.1) using the computer. Explore both implementations of multiple-argument functions.

----

#FootnoteRef(1)The procedure print-expression can be used in a program to print a simplified version of an expression. The default printer in the user interface incorporates the simplifier.

#FootnoteRef(2)To emphasize the relationship of simple tuple structures to matrix notation we often format up tuples as vertical arrangements of components and down tuples as horizontal arrangements of components. However, we could just as well have written this tuple as [(cos /θ/, sin /θ/), (− sin /θ/, cos /θ/)].

#FootnoteRef(3)Partial derivative operators such as (partial 2) are operators, so (expt (partial 1) 2) is a second partial derivative.
#FootnoteEnd

#page(524) 
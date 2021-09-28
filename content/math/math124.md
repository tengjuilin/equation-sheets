---
title: "MATH 124 Calculus I"
date: 2021-08-17T00:00:00+08:00
---

## Limits and Continuity

### Limits

|Description|Equations|
|-:|:-|
|Limit|$\lim\limits_{x\to a} f(x) = L$|
|Left-hand limit|$\lim\limits_{x\to a^-} f(x) = L$|
|Right-hand limit|$\lim\limits_{x\to a^+} f(x) = L$|
|Infinite limit|$\lim\limits_{x\to a} f(x) = \pm\infin$|
|Limit at infinity|$\lim\limits_{x\to \pm\infin} f(x) = L$|
|Limit existence|$\lim\limits_{x\to a^-} f(x) = L = \lim\limits_{x\to a^+} f(x)$ <br/> $\iff \lim\limits_{x\to a} f(x) = L$|
|Limit non-existence|1. $\lim\limits_{x\to a^-} f(x) \not= \lim\limits_{x\to a^+} f(x)$ <br/> 2. $\lim\limits_{x\to a} f(x) = \pm\infin$ <br/> 3. oscillation|

### Limit laws

|Description|Equations|
|-:|:-|
|Limit addition and subtraction|$\lim\limits_{x\to a} [f(x) \pm g(x)] = \lim\limits_{x\to a} f(x) \pm \lim\limits_{x\to a} g(x)$|
|Limit constant multiplication|$\lim\limits_{x\to a} [cf(x)] = c \lim\limits_{x\to a} f(x)$|
|Limit multiplication|$\lim\limits_{x\to a} [f(x)g(x)] = \lim\limits_{x\to a} f(x) \cdot \lim\limits_{x\to a} g(x)$|
|Limit division|$\lim\limits_{x\to a} \dfrac{f(x)}{g(x)} = \dfrac{\lim\limits_{x\to a} f(x)}{\lim\limits_{x\to a} g(x)} \text{ if } \lim\limits_{x\to a} g(x) \not= 0$|
|Limit power law <br/> ($n$ is positive integer)|$\lim\limits_{x\to a} [f(x)]^n = [\lim\limits_{x\to a} f(x)]^n$|
|Limit at infinity of inverse power <br/> $(r>0)$|$\lim\limits_{x\to \pm\infin} \dfrac{1}{x^r} = 0$|
|Limit root law <br/> ($n$ is positive integer; limit > 0 for even $n$)|$\lim\limits_{x\to a} \sqrt[n]{f(x)} = \sqrt[n]{\lim\limits_{x\to a} f(x)}$|
|Direct substitution property of limit|If $f$ is a polynomial or rational function, <br/> then $\lim\limits_{x\to a} f(x) = f(a)$|
|Limit of functions with holes|If $f(x) = g(x)$ when $x\not= a$, <br/> then $\lim\limits_{x\to a} f(x) = \lim\limits_{x\to a} g(x)$ if it exists|
|The squeeze theorem|If $f(x) \le g(x) \le h(x)$ when $x$ is near $a$ and if $\lim\limits_{x\to a} f(x) = \lim\limits_{x\to a} h(x) = L$, <br/> then $\lim\limits_{x\to a} g(x) = L$|

### Continuity

|Description|Equations|
|-:|:-|
|Continuous at a number $a$|$\lim\limits_{x\to a} f(x) = f(a)$|
|Continuous from the left at a number $a$|$\lim\limits_{x\to a^-} f(x) = f(a)$|
|Continuous from the right at a number $a$|$\lim\limits_{x\to a^+} f(x) = f(a)$|
|Continuous operations|addition, subtraction, multiplication, division|
|Continuous functions in their domain|polynomials, rational, root, trigonometric, inverse trigonometric, exponential, logarithmic functions|
|Types of discontinuity|1. removable discontinuity <br/> 2. jump discontinuity <br/> 3. infinite discontinuity|
|Continuity of function inputs and outputs|If $f$ is continuous at $b$ and $\lim\limits_{x\to a} g(x) = b$, <br/> then $\lim\limits_{x\to a} f(g(x)) = f(\lim\limits_{x\to a} g(x))$|
|Continuity of composite functions|If $g$ is continuous at $a$ and <br/> if $f$ is continuous at $g(a)$, <br/> then $(f\circ g)(x) = f(g(x))$ is continuous|
|Intermediate value theorem|If $f$ is continuous on the closed interval $[a, b]$, and let N be any number between $f(a)$ and $f(b)$, where $f(a) \not= f(b)$, <br/> then there exist a number $c$ in $(a, b)$ such that $f(c) = N$|

## Differentiation

### Derivatives

|Description|Equations|
|-:|:-|
|Derivative of a function $f$ at number $a$|$f'(a) = \lim\limits_{h \to 0} \dfrac{f(a+h) - f(a)}{h}$: <br/> $f'(a) = \lim\limits_{x \to a} \dfrac{f(x) - f(a)}{x-a}$|
|Derivative as a function|$f'(x) = \lim\limits_{h \to 0}\dfrac{f(x+h) - f(x)}{h}$|
|Geometric interpretation of derivatives|The tangent line of $y = f(x)$ at $(a, f(a))$ has a slope of $f'(a)$ <br/> $m = \lim\limits_{x \to a} \dfrac{f(x) - f(a)}{x-a} = f'(a)$|
|Derivatives and instantaneous rate of change|The derivative $f'(a)$ is the instantaneous rate of change of $y=f(x)$ with respect to $x$ when $x=a$: <br/> $v(a) = \lim\limits_{h \to 0} \dfrac{f(a+h) - f(a)}{h} = f'(a)$|
|Differentiation and continuity|If $f$ is differentiable at $a$, <br/> then $f$ is continuous at $a$.|
|Non-differentiable conditions|1. a corner <br/> 2. a discontinuity <br/> 3. a vertical tangent|

### Differentiation rules

|Description|Equations|
|-:|:-|
|Constant multiple rule|$\frac{d}{dx}[cf(x)] = c\frac{d}{dx}f(x)$|
|Addition and subtraction rule|$\frac{d}{dx}[f(x)\pm g(x)] = \frac{d}{dx}f(x) \pm \frac{d}{dx}g(x)$|
|Product rule|$\frac{d}{dx}[f(x)g(x)] = f'(x)g(x) + f(x)g'(x)$|
|Quotient rule <br/> (best practice: use product rule)|$\frac{d}{dx}\dfrac{f(x)}{g(x)} = \dfrac{f'(x)g(x) - f(x)g'(x)}{g(x)^2}$|
|Constant rule|$\frac{d}{dx}c = 0$|
|Power rule|$\frac{d}{dx} x^n = nx^{n-1}$|
|Chain rule|$\dfrac{dy}{dx} = \dfrac{dy}{du}\dfrac{du}{dx} \newline \frac{d}{dx} f(g(x)) = f'(g(x))\cdot g'(x)$|
|Linear approximations|$f(x) \approx f(a) + f'(a)(x-a)$|
|Differentials|$dy = f'(x) \ dx$|

### Special limits

|Description|Equations|
|-:|:-|
|Limit associated with sine|$\lim\limits_{\theta \to 0}\dfrac{\sin\theta}{\theta} = 1$|
|Limit associated with cosine|$\lim\limits_{\theta\to 0}\dfrac{\cos\theta - 1}{\theta} = 0$|
|Definition of $e$|$\lim\limits_{h\to 0}\dfrac{e^h - 1}{h} = 1$|
|$e$ as a limit|$e = \lim\limits_{x\to 0} (1+x)^{1/x}$|
|$e$ as a limit|$e = \lim\limits_{n\to \infin} (1+\frac{1}{n})^{n}$|

### Table of derivatives

|Function $f(x)$|Derivative $f'(x)$|Function $f(x)$|Derivative $f'(x)$|
|-:|:-|-:|:---|
|$c$|$0$|$x^n$|$nx^{n-1}$|
|$x$|$1$|$\lvert x \rvert$|$\dfrac{x}{\lvert x \rvert}$|
|$e^x$|$e^x$|$\ln x$|$\dfrac{1}{x}$|
|$a^x$|$a^x\ln(a)$|$\log_{a}x$|$\dfrac{1}{x\ln(a)}$|
|$\sin x$|$\cos x$|$\sec x$|$\sec x \tan x$|
|$\cos x$|$-\sin x$|$\csc x$|$-\csc x \cot x$|
|$\tan x$|$\sec^2 x$|$\cot x$|$-\csc^2 x$|
|$\arcsin x$|$\dfrac{1}{\sqrt{1-x^2}}$|$\arctan x$|$\dfrac{1}{1+x^2}$|
|$\arccos x$|$\dfrac{-1}{\sqrt{1-x^2}}$

## Applications of Differentiation

### Absolute extreme values

|Description|Equations|
|-:|:-|
|Extreme values|Maximum and minimum values of $f$|
|Absolute maximum|$f(a) \ge f(x)$ for all $x \in D$|
|Absolute maximum|$f(a) \le f(x)$ for all $x \in D$|
|Local maximum|$f(a) \ge f(x)$ for $x$ near $a$|
|Local minimum|$f(a) \le f(x)$ for $x$ near $a$|
|Critical number $c$|$f'(c) = 0$ or <br/> $f'(c)$ does not exist|
|Extreme value theorem|If $f$ is continuous on a closed interval $[a, b]$, <br/> then $f$ attains an absolute maximum $f(c)$ and absolute minimum $f(d)$ at some number $c, d \in [a, b]$ |
|Fermat's theorem|If $f$ has a local maximum or minimum at $c$, <br/> then $c$ is a critical number of f|
|Closed interval method <br/> (Finding the absolute max and min in $[a,b]$)|1. Find the values of $f$ at critical numbers of $f$ in $(a, b)$ <br/> 2. Find the values of $f$ at the endpoints of the interval <br/> 3. Compare the values. The largest is the abs max; the smallest is the abs min|

### The mean value theorem

|Description|Equations|
|-:|:-|
|Rolle's theorem|If $f$ is continuous on $[a,b]$, differentiable on $(a,b)$, and endpoints $f(a) = f(b)$, <br/> then there is a number $c \in (a,b)$ such that $f'(c) = 0$|
|The mean value theorem|If $f$ is continuous on $[a,b]$, differentiable on $(a,b)$, <br/> then there is a number $c \in (a,b)$ such that $f'(c) = \dfrac{f(b) - f(a)}{b-a}$|
|Functions with derivative of zero are constants|If $f'(x) = 0$ for all $x \in (a,b)$, <br/> then $f$ is constant on $(a,b)$|
|Functions with same derivatives are vertical translations of each other|If $f'(x) = g'(x)$ for all $x \in (a,b)$, <br/> then $f(x) = g(x) + c$ on $(a,b)$|

### Local extreme values

|Description|Equations|
|-:|:-|
|Increasing|$f(x_1) < f(x_2)$ for $x_1 < x_2$ in $I$|
|Deceasing|$f(x_1) > f(x_2)$ for $x_1 < x_2$ in $I$|
|Increasing/decreasing test|(a) If $f'(x)>0$ on an interval, then $f$ is increasing on that interval. <br/> (b) If $f'(x)<0$ on an interval, then $f$ is decreasing on that interval.|
|First derivative test|If $c$ is a critical value of continuous function $f$, then <br/> (a) If $f'$ changes $+ \to -$ at c, <br/> then $f$ has a local max at $c$ <br/> (b) If $f'$ changes $- \to +$ at c, <br/> then $f$ has a local min at $c$ <br/> (c) If $f'$ has no sign change at c, <br/> then $f$ has no local max/min at $c$|
|Concave upward|If the graph of $f$ lies above all its tangents on an interval $I$ (slope increases)|
|Concave downward|If the graph of $f$ lies below all its tangents on an interval $I$ (slope decreases)|
|Inflection point|The point at which the curve changes concavity|
|Concavity test|(a) If $f''(x)>0$ on an interval, then $f$ is concave upward on that interval. <br/> (b) If $f''(x)<0$ on an interval, then $f$ is concave downward on that interval.|
|Second derivative test|If $f''$ is continuous near $c$, <br/> (a) If $f'(c) = 0$ and $f''(c)>0$, <br/> then $f$ has a local min at $c$ <br/> (b) If $f'(c) = 0$ and $f''(c)<0$, <br/> then $f$ has a local max at $c$ |

### L'Hospital's rule

|Description|Equations|
|-:|:-|
|Indeterminate forms|$\lim\limits_{x\to a}\dfrac{f}{g} = \dfrac{0}{0}, \dfrac{\infin}{\infin}$|
|L'Hospital's rule|If $f$ and $g$ are differentiable and $g'(x) \not= 0$ on open interval $I$ that contains $a$, and if the division has indeterminate form of $\frac{0}{0}$ or $\frac{\infin}{\infin}$, <br/> then $\lim\limits_{x \to a}\dfrac{f(x)}{g(x)} = \lim\limits_{x \to a}\dfrac{f'(x)}{g'(x)}$|
|Indeterminate products|$\lim\limits_{x\to a}fg = 0 \cdot \infin \newline \lim\limits_{x\to a}fg = \dfrac{f}{1/g} = \dfrac{g}{1/f}$|
|Indeterminate differences|$\lim\limits_{x\to a}(f-g) = \infin-\infin$|
|Indeterminate powers|$\lim\limits_{x\to a}[f(x)]^{g(x)} = 0^0, \infin^0, 1^{\infin} \newline y \equiv [f(x)]^{g(x)} \newline \ln y = g(x) \ln f(x)$|

### Newton's method

|Description|Equations|
|-:|:-|
|Newton's method|$x_{n+1} = x_{n} - \dfrac{f(x_n)}{f'(x_n)}$|

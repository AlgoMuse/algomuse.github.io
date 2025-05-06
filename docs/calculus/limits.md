---
layout: default
title: Limits
nav_order: 2
parent: Calculus
---


# Limits



### Vanilla application of L'Hospital
{: .d-inline-block }

A3, 2010
{: label .label-blue}

Evaluate the limit:

\\[ \lim_{x \rightarrow 1}\left(\frac{n- \displaystyle \sum_{k=1}^n x^{k}}{1-x}\right) \\]


<details><summary>Solution</summary>

We apply the L'Hospital's rule and differentiate both the numerator and the denominator.

\begin{array}{rl}
 \lim_{x\rightarrow 1}&\displaystyle \frac{-n x^{n-1}-(n-1) x^{n-2}-\cdots-2x-1}{-1}  \\
 =&\frac{n(n+1)}{2}
\end{array}


</details>


<p></p>

<details><summary>Practice Problem</summary>
<p>
Explain what is wrong with the use of L'Hospital's rule. Find the correct limit.

\[\lim_{x \rightarrow 1} \frac{2 x^{3}-3 x+1}{x^{4}-1}=\lim_{x \rightarrow 1} \frac{6 x^{2}-3}{4 x^{3}}=\lim_{x \rightarrow 1} \frac{12 x}{12 x^{2}}=\lim_{x \rightarrow 1} \frac{1}{x}=1\]

</p>
</details>



---


### L'Hospital again
{: .d-inline-block}

A4, 2012
{: .label}


<p>
Prove the following limit.
</p>

<p>
\[ \lim_{x \rightarrow \infty} \frac{x^{100} \ln (x)}{e^{x} \arctan \left(\frac{\pi}{3}+\sin x\right)}=0 \]
</p>

<details><summary>Solution</summary>

<p>
For some positive constant \(k\) we can ensure that \(\arctan \left(\frac{\pi}{3}+\sin x\right)> k\) for any \(x\).

For example, \(k=\arctan(0.0001)\) will work. This is because \(\pi>3.142, \sin (x) \geq-1\) and \(\arctan\) is an increasing function.
</p>

<p>
Further, \(\ln (x)< x\) for \(x> 0\). So the given ratio must lie between 0 and \(x^{101} / c e^{x} \). If we apply the L'Hospital's rule 102 times, we get the result.
</p>


</details>


---

### Absolute value in the denominator
{: .d-inline-block }

A6, 2022
{: .label }

<p>
Which of the options are true about the function \(f\) as defined below:
\[ f(x) = \frac{1}{|\ln x|} \left( \frac{1}{x} + \cos x  \right) \] 
<ol>
<li> As \(x\rightarrow \infty\), the sign of \(f\) changes infinitely many times.</li>
<li> \(\lim_{x\rightarrow \infty} f(x) \) does not exist.</li>
<li> \(\lim_{x\rightarrow 1} f(x) = \infty \).</li>
<li> \(\lim_{x\rightarrow 0^+} f(x) = 1\).</li>
</ol>
</p>


<details><summary>Solution</summary>
<li> TRUE. </li>
<li> FALSE. </li>
<li> TRUE. </li>
<li> FALSE. </li>
</details>


---

### Tower expression
{: .d-inline-block }

A7, 2022
{: .label }

<p>
Let \(f_0(x) = x\),\(f_1(x)=x^x\),\(f_2(x) = x^{x^x}\), etc. For \(x>0\) which of the following options are true?
<ol>
<li> \(\lim_{x\rightarrow 0^+} f_1(x) = 1\)</li>
<li> \(\lim_{x\rightarrow 0^+} f_2(x) = 1\)</li>
<li> \( \int_0^{1} f_3 dx = 1  \)</li>
<li> \( f_{123}^\prime(1) = 1  \)</li>
</ol>
</p>

<details><summary>Solution</summary>
<li> TRUE. </li>
<li> FALSE. </li>
<li> FALSE. </li>
<li> TRUE. </li>
</details>


---

### Limit of \\(x^{x^{x}}\\)
{: .d-inline-block }

B1a, 2017
{: .label }

<p>
(a) Evaluate \( \lim_{x \rightarrow 0^{+}}\left(x^{x^{x}}-x^{x}\right) \)
</p>


<details><summary>Solution</summary>

<p>
First consider the limit
\[
\begin{align}
\lim_{x \rightarrow 0^{+}} x^{x}  \\
&=\lim_{x \rightarrow 0^{+}}\left(e^{x\log x}\right) \\
&=\lim_{x \rightarrow 0^{+}}\left(e^{\frac{\log x}{1 / x}}\right)
\end{align}
\]
</p>


<p>Now consider just the exponent:
\[
\begin{align}
\lim_{x \rightarrow 0^{+}} \frac{\log x}{1 / x} \\
&=\lim_{x \rightarrow 0} \frac{1 / x}{-1 / x^{2}} \\
&=0
\end{align}
\]
substituting the value 0 from (2) in equation (1) we get that the limit is 1.
</p>


<p>
Now
\[
\begin{align}
\lim_{x \rightarrow 0^{+}}\left(x^{x^{x}}-x^{x}\right) \\
&=\lim_{x \rightarrow 0^{+}} x^{x^{x}}-\lim_{x \rightarrow 0^{+}} x^{x} \\
&=\lim_{x \rightarrow 0^{+}} x^{\lim_{x \rightarrow 0^{+}} x^{x}}-\lim_{x \rightarrow 0^{+}} x^{x} \\
&=0-1 \\
&=-1
\end{align}
\]
</p>

</details>

<p><i><b>Reference</b>. This problem is based on a general result: A tower of even number of \(x\)s tends to zero
and a tower of odd number of \(x\)s tends to one [1].<br>

[1] <a href="http://math.depaul.edu/~mash/limitofx%5ex%5e.pdf">The limit of x** as x tends to zero</a> J. Marshall Ash,  Mathematics Magazine, 69 (1996), 207-209.</i></p>


---

### Simple limits
{: .d-inline-block }

A9, 2021
{: .label}


<p>Let \(f\) and \(g\) be function defined as follows:<br>

\[ f(x) = \frac{x}{x+\sin x} \]

\[ g(x) = \frac{x^4+x^6}{e^x-1-x^2} \]

(a) \(\lim_{x\rightarrow 0} f(x) = 1/2\)<br>
(b) \(\lim_{x\rightarrow \infty} f(x)\) does not exist.<br>
(c) \(\lim_{x\rightarrow \infty} g(x) \) is finite.<br>
(d) \(\lim_{x\rightarrow 0} g(x) = 720 \).<br>

</p>

<details><summary>Solution</summary>
(a) True. \(\sin x \approx x\) as \(x\rightarrow 0\).<br>
(b) False. The limit is 1.<br>
(c) True. Numerator is polynomial, while the denominator is exponential.<br>
(d) False. The limit is zero. (L'Hosptial's rule is not applicable).
</details>

---

### Smallest prime factor function
{: .d-inline-block }

A9, 2017
{: .label}

<p>
Let \(f\) be a continuous function from \(\mathbb{R}\) to \(\mathbb{R}\) (where \(\mathbb{R}\) is the set of all real numbers) that satisfies the following property: <br>
</p>

<p>
For every natural number \(n\)
</p>

<p>
\[ f(n)= \text{the smallest prime factor of }n \]
</p>


<p>
For example, \(f(12)=2, f(105)=3 .\) Calculate the following.
</p>

<p>
(a) \(\lim_{x \rightarrow \infty} f(x)\)
</p>

<p>
(b) The number of solutions to the equation \(f(x)=2016\)
</p>

<details><summary>Solution</summary>

<p>
(a) \(f(x)\) will take value 2 for all even \(x\). At the same time, primes provide an increasing infinite sequence of positive integers for which \(f(x)=x .\) Thus \(\lim_{x \rightarrow \infty} f(x)\) does not exist.
</p>

<p>
(b) By intermediate value theorem, for each prime \(p> 2016\) there is an \(x\) between \(p\) and \(p+1\) such that \(f(x)=2016\)
</p>

</details>

---



### Limit of a log of an exponent
{: .d-inline-block}

A9, 2019
{: .label}

<p>Consider \(f: \mathbb{R} \times \mathbb{R} \rightarrow \mathbb{R}\) defined as follows:</p>

<p>\[ f(a, b):=\lim_{n \rightarrow \infty} \frac{1}{n} \log_{e}\left[e^{n a}+e^{n b}\right] \]</p>

<p>(a) \(f\) is not onto i.e. the range of \(f\) is not all of \(\mathbb{R}\).</p>
<p>(b) For every \(a\) the function \(x \mapsto f(a, x)\) is continuous everywhere.</p>
<p>(c) For every \(b\) the function \(x \mapsto f(x, b)\) is differentiable everywhere.</p>
<p>(d) We have \(f(0, x)=x\) for all \(x \geq 0\)</p>


<details><summary>Solution</summary>
<p>
Without loss of generality, assume that \(a >  b\).
</p>

<p>
\begin{align*}
    f(a, b) &=\lim_{n \rightarrow \infty} \frac{1}{n} \log\left(e^{n a}+e^{n b} \right) \\
     & =\lim_{n \rightarrow \infty} \frac{1}{n} \log \left( e^{na}( 1 +e^{n(b-a)} ) \right) \\
     & =\lim_{n \rightarrow \infty} \frac{1}{n} \log e^{na} + \log ( 1 +e^{n(b-a)} )\\
     & = a + \lim_{n\rightarrow \infty} \frac{1}{n} \log ( 1 + e^{-\infty} ) \\
     & = a + \lim_{n\rightarrow \infty} \frac{1}{n} \log ( 1 )\\
     & = a
\end{align*}
</p>

<p>
Similary, if \(b \geq a\), \(f (a,b) = b \).  Thus, we have:
\[ f(a,b) = \max(a,b) \]

<ol>
    <li> False. \(f(x,x) = x \) so \(f\) is onto.</li>
    <li> True. \(g(x) = \max(x,a) \) which is continuous everywhere.</li>
    <li> False. \( h(x) =  \max(x,b) \) is not  differentiable at \(x = b\). More explicitly, \( \lim_{x \rightarrow b^+} = 1 \) and \( \lim_{x \rightarrow b^-} = 0 \).</li>
    <li> True. \( \max(x,0) = x \) for all \(x \geq 0 \).</li>
</ol>

</p>

</details>

---

###  Polynomial and limits
{: .d-inline-block}

B1, 2015
{: .label}


<p>(a) For any polynomial \(p(t),\) the limit \(\lim_{t \rightarrow \infty} \frac{p(t)}{e^{t}}\) is independent of the polynomial \(p .\) Justify this statement and find the value of the limit.</p>
<p>(b) Consider the function defined by</p>

<p>
\begin{align}
q(x) &=e^{-1 / x} \text { when } x>0 \\
&=0 \text { when } x=0 \\
&=e^{1 / x} \text { when } x<0
\end{align}
</p>

<p>Show that \(q^{\prime}(0)\) exists and find its value. Why is it enough to calculate the relevant limit from only one side?
</p>

<p>(c) Now for any positive integer \(n,\) show that \(q^{(n)}(0)\) exists and find its value. Here \(q(x)\) is the function in part (b) and \(q^{(n)}(0)\) denotes its \(n\) -th derivative at \(x=0\).
</p>

<details><summary>Solution</summary>

 <p>(a) If \(p(t)\) is constant, then the limit \(=0 .\) Otherwise we get a form \(\frac{\pm \infty}{\infty}\). Using L'Hospital's rule, we get \(\lim_{t \rightarrow \infty} \frac{p(t)}{e^{t}}=\lim_{t \rightarrow \infty} \frac{p^{\prime}(t)}{e^{t}}=0\) by induction on the degree of \(t\) (or apply
L'Hospital's rule repeatedly).</p>

<br>

<p>(b) The right side derivative \(=\lim_{h \rightarrow 0^{+}} \frac{q(h)-q(0)}{h}=\lim_{h \rightarrow 0^{+}} \frac{e^{-1 / h}}{h}=\lim_{h \rightarrow 0^{+}} \frac{1 / h}{e^{1 / h}}=\lim_{t \rightarrow+\infty} \frac{t}{e^{t}} \cdot\) (Let \(t=1 / h .\) As \(\left.h \rightarrow 0^{+}, t \rightarrow+\infty .\right)\) This limit is \(0,\) e.g. by part \((\mathrm{a})\) Now \(q\) is an even function, so letting \(k=-h,\) the left side derivative \(=\lim_{h \rightarrow 0^{-}} \frac{q(h)-q(0)}{h}=\) \(\lim_{k \rightarrow 0^{+}} \frac{q(-k)}{-k}=\lim_{k \rightarrow 0^{+}} \frac{q(k)}{-k} .\) Using the earlier calculation this also equals \(-0=0\) Note: It is wrong to argue that \(q^{\prime}(0)=\lim_{x \rightarrow 0} q^{\prime}(x)\) because to do so, we first need to know that \(q^{\prime}\) is continuous at \(0,\) but we have not even shown that \(q^{\prime}(0)\) exists! For the same reason it is wrong to argue below that \(q^{(n)}(0)=\lim_{x \rightarrow 0} q^{(n)}(x)\)</p>

<br>

<p>
(c) We will show by induction on \(n\) that \(q^{(n)}(0)=0 .\) The case \(n=1\) is done. (We can even start the induction at \(n=0\) by interpreting \(q^{(0)}(x)=q(x) .\) ) Assuming that we are done up to \(n\) and to prove the statement for \(n+1,\) we need to calculate \(\lim_{h \rightarrow 0} \frac{q^{(n)}(h)-q^{(n)}(0)}{h}=\) \(\lim_{h \rightarrow 0} \frac{q^{(n)}(h)}{h},\) because \(q^{(n)}(0)=0\) by induction. Therefore it is good to examine \(q^{(n)}(h)\) for \(h \neq 0 .\) This is easy to calculate by the usual rules, but the formulas will be different for positive and negative \(h .\) For \(h \neq 0,\) as \(q\) is even, \(q^{\prime}\) is odd, so \(q^{\prime \prime}\) is even, etc. and in general \(q^{(n)}(h)=(-1)^{n} q^{(n)}(-h) .\) Therefore, just as for part (b), it suffices to show that \(\lim_{h \rightarrow 0^{+}} \frac{q^{(n)}(h)}{h}=0 .\) By another induction, we see easily that for \(h>0, q^{(n)}(h)=p(1 / h) e^{-1 / h}\)
for some polynomial \(p .\left[\right.\) Proof: \(q^{\prime}(h)=\left(\frac{1}{h^{2}}\right) e^{-1 / h} .\) Assuming the result for \(n,\) we have \(q^{(n+1)}(h)=\left[p(1 / h) e^{-1 / h}\right]^{\prime}=-\frac{1}{h^{2}}\left(-p(1 / h)+p^{\prime}(1 / h)\right) e^{-1 / h},\) which has the desired form.
</p>

<p>
So we have \(\lim_{h \rightarrow 0^{+}} \frac{q^{(n)}(h)}{h}=\lim_{h \rightarrow 0^{+}} \frac{p(1 / h) e^{-1 / h}}{h}=\lim_{t \rightarrow \infty} t p(t) e^{-t}=\lim_{t \rightarrow \infty} \frac{t p(t)}{e^{t}}=0\) by part (a). Here we have again substituted \(t=1 / h\)
</p>

</details>





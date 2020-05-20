---
description: An infinite integral; a satisfying solution.
---

# Infinite Integral

### Behold, the subject:

$$
\int \sqrt{x\sqrt[3]{x\sqrt[4]{x...}}}dx
$$

Oh jeez... this integral looks intimidating. A typical approach to solving any nested infinite function would be to just solve for the case $$y=f(y)$$. Unfortunately in this case, the integrand function changes the further it's nested. Thus we must start with some algebraic manipulation in order to turn it into a form we can work with. Notice how we can take the radicals and rewrite them as nested exponents.

$$
\Rightarrow\int \left(x\left(x\left(x...\right)^{\frac{1}{4}}\right)^{\frac{1}{3}}\right)^{\frac{1}{2}}dx
$$

Now we can distribute the exponent through the nest. All we do is multiply all the exponents inside a bracket by the outer exponent. Each exponent is now just a reciprocal factorial of it's original, but more importantly it's no longer nested.

$$
\Rightarrow\int x^{\frac{1}{2}}x^{\frac{1}{6}}x^{\frac{1}{24}}...dx
$$

We can try to integrate it now, but that would still be a pain to do. We should first combine all the $$x$$ variables.

$$
\Rightarrow\int x^{\frac{1}{2}+\frac{1}{6}+\frac{1}{24}}...dx
$$

Since we know that each term in the sum is just a factorial, we can rewrite it using summation notation.

$$
\Rightarrow\int x^{\sum_{n=2}^\infty{\frac{1}{n!}}}dx
$$

This still doesn't look very nice though. What we need is to turn the sum into something we know how to integrate. As it turns out, the sum is actually related to something very interesting. Notice that $$e=\sum_{n=0}^\infty{\frac{1}{n!}}$$ , so that means $$e - 2=\sum_{n=2}^\infty{\frac{1}{n!}}$$. Now we can substitute this into the integral.

$$
\Rightarrow\int x^{e-2}dx
$$

Here we have an integral which we can easily solve using the power rule, thus we arrive at our answer!

$$
\int \sqrt{x\sqrt[3]{x\sqrt[4]{x...}}}dx = \frac{x^{e-1}} {e-1}+c
$$


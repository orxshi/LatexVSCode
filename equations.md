---
layout: default
title: Equations
nav_order: 5
description: "Typing equations"
---

# Equations

There are two types of equations in LaTeX: Inline and display. Inline equations are written within a line of text, while display equations are centered on a new line.

There are multiple ways of typing equations in LaTeX but only some of them will be shown here.

Put the inline equation between two dollar signs `$`. For example, the code

```
Bla bla bla $a^2 + b^2 = c^2$.
```

will produce the following output:

Bla bla bla $a^2 + b^2 = c^2$.

To write a display equation, put the equation in `equation` environment as shown below:

```
\begin{equation}
    a^2 + b^2 = c^2
\end{equation}
```

This will produce the following output:

$$
    \label{eq:pythagorean}
    \begin{equation}
        a^2 + b^2 = c^2
    \end{equation}
$$

Notice the equation number on the right side of the equation. Numbering is automatic and LaTeX will do the bookkeeping.

The `\label` command is optional but it is useful for referencing the equation later in the text. You can give any name to the label but it is a good practice to use a prefix such as `eq:` to indicate that this label is for an equation. Use `\ref` command to refer to the equation. For example,


```
The Pythagorean theorem is given by equation \ref{eq:pythagorean}.
```

This will produce the following output: $The Pythagorean theorem is given by equation \ref{eq:pythagorean}$.

## Multi-line Equations

For multi-line equations, use the `equation` environment with `aligned` environment inside it as shown below:

```
\begin{equation}
    \begin{aligned}
        a^2 + b^2 &= c^2 \\
        x^2 + y^2 &= z^2
    \end{aligned}
\end{equation}
```

This will produce the following output:

$$
    \begin{equation}
        \begin{aligned}
            a^2 + b^2 &= c^2 \\
            x^2 + y^2 &= z^2
        \end{aligned}
    \end{equation}
$$

If the equation is related to a parapraph above, do not put a blank line between the paragraph and the `equation` environment. Otherwise, the equation will not be part of the paragraph and will be separated from it by a vertical space.

Display equations are numbered by default. The ``align`` environment will number each line of a multi-line equation. One of the ways to give only one equation number to a multi-line equation is to use the ``aligned`` environment inside the ``equation`` environment as shown below:

```
    \begin{equation}
        \begin{aligned}
            a^2 + b^2 &= c^2 \\
            x^2 + y^2 &= z^2
        \end{aligned}
    \end{equation}
```

This will produce the following output:

$$
    \begin{equation}
        \begin{aligned}
            a^2 + b^2 &= c^2 \\
            x^2 + y^2 &= z^2
        \end{aligned}
    \end{equation}
$$

## Un-numbered Equations

To write an un-numbered equation, use the ``equation*`` or ``align*`` environment as shown below:

```
\begin{equation*}
    a^2 + b^2 = c^2
\end{equation*}
```

## Shorter Ways of Writing Equations

There are shorter ways of writing equations in LaTeX such as using double dollar signs ``$$`` for display equations. Here is an example:

```
$$
    a^2 + b^2 = c^2
$$
```
    
There is one more way of writing display equations using the `\[` and `\]` symbols as shown below:

```
\[
    a^2 + b^2 = c^2
\]
```

For inline equations, you can also use the `\(` and `\)` symbols as shown below:

```
Bla bla bla \( a^2 + b^2 = c^2 \).
```

## Typing Some of the Math Symbols

It is impossible to list all the math symbols in LaTeX but here are some of the most common ones:

### Greek Letters

Lowercase Greek letters are written using a backslash followed by the name of the letter. For example, `\alpha` produces $\alpha$, `\beta` produces $\beta$, and so on. Uppercase Greek letters are written using a backslash followed by the name of the letter with the first letter capitalized. For example, `\Gamma` produces $\Gamma$, `\Delta` produces $\Delta$, and so on.

### Subscripts and Superscripts

Use the underscore symbol `_` for subscripts and the caret symbol `^` for superscripts. For example, `a_i` produces $a_i$ and `a^2` produces $a^2$.

### Fractions

Use the `\frac` command to write fractions. The syntax is `\frac{numerator}{denominator}`. For example, `\frac{a}{b}` produces $\frac{a}{b}$. If you want to write a fraction in inline math mode, you can use the `\dfrac` command instead of `\frac` to make the fraction larger and more readable. For example, `\dfrac{a}{b}` produces $\dfrac{a}{b}$.

### Derivatives

The syntax for ordinary derivatives is `\frac{dy}{dx}` and for partial derivatives is `\frac{\partial f}{\partial x}`. For example, `\frac{dy}{dx}` produces $\frac{dy}{dx}$ and `\frac{\partial f}{\partial x}` produces $\frac{\partial f}{\partial x}$.

### Square Roots

Use the `\sqrt` command to write square roots. The syntax is `\sqrt{expression}`. For example, `\sqrt{a}` produces $\sqrt{a}$.

### Integrals

Use the `\int` command to write integrals. The syntax is `\int_{lower}^{upper} expression \, dx`. For example, `\int_a^b f(x) \, dx` produces $\int_a^b f(x) \, dx$.

### Summations

Use the `\sum` command to write summations. The syntax is `\sum_{lower}^{upper} expression`. For example, `\sum_{i=1}^n a_i` produces $\sum_{i=1}^n a_i$.

### Limits

Use the `\lim` command to write limits. The syntax is `\lim_{x \to value} expression`. For example, `\lim_{x \to \infty} f(x)` produces $\lim_{x \to \infty} f(x)$.

### Exponential and Logarithmic Functions

Use the `\exp` command for the exponential function and the `\log` command for the logarithmic function. For example, `\exp(x)` produces $\exp(x)$ and `\log(x)` produces $\log(x)$. You can also use the caret symbol `^` to write exponential functions. For example, `e^x` produces $e^x$. Use the `\ln` command for the natural logarithm. For example, `\ln(x)` produces $\ln(x)$.

### Matrices

Use the `\begin{matrix}` and `\end{matrix}` commands to write matrices. The syntax is as follows:

```
\begin{matrix}
    a & b \\
    c & d
\end{matrix}
```
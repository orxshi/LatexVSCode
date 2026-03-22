# Plotting

Use ``pgfplots`` to create plots in LaTeX. Copilot will help you write the code for the plots from the context of your LaTeX document. Here is the plot of $y = x^2$:

```
\documentclass{article}
\usepackage{pgfplots}
\pgfplotsset{compat=1.18}

\begin{document}

\begin{tikzpicture}
    \begin{axis}[
        xlabel=$x$,
        ylabel=$y$,
    ]
        \addplot[blue, thick] {x^2};
    \end{axis}
\end{tikzpicture}

\end{document}
```

It is recommended to guide Copilot by writing comments in your LaTeX document to indicate what you want to plot. For example, you can write a comment like this:

```
% Plot the function y = x^2 for x = 0, 1, 2, 3
```
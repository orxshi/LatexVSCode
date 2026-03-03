Plotting
========

Use ``pgfplots`` to create plots in LaTeX. Copilot will help you write the code for the plots from the context of your LaTeX document. Here is an example of a simple plot created using ``pgfplots``:

.. code-block:: latex

    \documentclass{article}
    \usepackage{pgfplots}

    \begin{document}

        Let's plot the function \(y = x^2\) for \(x\) values from 0 to 3.

        \begin{tikzpicture}
            \begin{axis}[
                xlabel={$x$},
                ylabel={$y$},
                title={Simple Plot},
            ]
            \addplot[color=blue,mark=*] coordinates {
                (0,0)
                (1,1)
                (2,4)
                (3,9)
            };
            \end{axis}
        \end{tikzpicture}

    \end{document}

The environment ``tikzpicture`` will be provided by Copilot. If you want to center the plot, you can wrap the ``tikzpicture`` environment with a ``center`` environment as shown below:
.. code-block:: latex

    \begin{center}
        \begin{tikzpicture}
            \begin{axis}[
                xlabel={$x$},
                ylabel={$y$},
                title={Simple Plot},
            ]
            \addplot[color=blue,mark=*] coordinates {
                (0,0)
                (1,1)
                (2,4)
                (3,9)
            };
            \end{axis}
        \end{tikzpicture}
    \end{center}

You can use ``figure`` environment to add a caption and a label to the plot. Consult to a chat-based AI tool for more information.
# Background and justification of selected algorithm

Text describing background

Example figure. Figure numbering should be chronological, following the numbering of the figures in previous chapters.

Starting points for the optimisation are sampled on a length-angle
regular grid around point $(0,0)$ as on {numref}`startpoints`.


```{figure} ./startpoints.png
--- 
name: startpoints
---
Location of the preliminary function evaluations for choosing starting points to the Nelder Mead algorithm. The circle locates the limit of vality domain $\mathbf{D}$.
```

We can also refer to the figure this way: {ref}`Starting points for the optimisation <startpoints>`

Here is a math block
$
  \int_0^\infty \frac{x^3}{e^x-1}\,dx = \frac{\pi^4}{15}
$

Here are labeled and numbered equations

```{math}
:label: my_label
w_{t+1} = (1 + r_{t+1}) s(w_t) + y_{t+1}
```

```{math}
:label: my_other_label
w_{t+2} = (1 + r_{t+2}) s(w_t) + y_{t+2}
```

# Introduction, purpose and scope

Here comes an introduction and the purpose and scope of the ATBD


```{note}
This is an example of a note
```

##### Here is an example of a table with a label
(gridsCDR)=
 | Id  |  $\mathbf{n}_{x}$  |  $\mathbf{n}_{y}$  |  $\mathbf{A}_{x}$ \[km\] |  $\mathbf{A}_{y}$ \[km\]  | $\mathbf{B}_{x}$ \[km\]  | $\mathbf{B}_{y}$ \[km\]|
 | ----- | ----- | ----- | ------ | ----- | ----- |-----|
 | `nh_ease2-750`, `sh_ease2-750`  |  144 |  144  |   75.0   |    75.0  | -5375.0  |   5375.0|
 | `nh_ease2-250`, `sh_ease2-250`  |  432  | 432   |    25.0 |  25.0 |   -5387.5  |      5387.5|
 | `nh_ease2-125`, `sh_ease2-125`  |  864 |  864    |          12.5   |    12.5     |  -5393.75  |  5393.75|


Here is a citation, {cite}`brodzik/etal:2012`


Here is an example of how to label a section:

(seasons)= 
### Seasons

The  sea-ice drift CDR has global coverage and thus cover all sea ice in
the Northern Hemisphere (NH) and Southern Hemisphere (SH). The quality
of the drift estimates vary with season, and it is convenient to refer
to winter, summer, and transition periods. The definition of these
periods are in .

 |         |  Northern Hemisphere |  Southern Hemisphere|
 | --------| ---------------------| ---------------------|
 | Winter   |      Nov - Apr       |     Apr - Sept |
 | Spring   |         May        |           Oct |
 | Summer   |     Jun - Sept     |        Nov - Feb |
 | Autumn   |         Oct        |           Mar|


Here is an example of how to insert and label images:



```{figure} inv_params_nh_2013-2020_jul.jpg
---
name: inv_params_nh
---
Figure caption here!
```

```{figure} inv_params_sh_2012-2019_dec.jpg
---
name: inv_params_sh
---
Second figure caption
```

These maps of parameters and residuals are saved in a monthly parameter
file. In Figures {numref}`inv_params_nh` and {numref}`inv_params_sh`
examples of these parameters are shown.


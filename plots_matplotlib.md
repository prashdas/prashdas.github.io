## Matplotlib 

Matplotlib is a python library for generating appealing plots that are ready to go into your presentations/articles. I used it extensively during my PhD and postdocs and keep returning to it as I work on data science / ML projects. I hope I can sell it to you (*if you don't use it already, that is*) with a sample plot.

<img src="python_matplotlib/sample_streams.png?raw=true" width="250" title = "Streamlines showing the formation of multiple vortices in the presence of flexible flaps">
<br><br>

This is a plot of an experimentally measured velocity field of a two-dimensional starting jet. The two thick black lines represent bendable flaps that move and deform based on the fluid forces. The plot shows streamlines of the velocity field which are laid on top of the colored contours of velocity magnitude. Now, it is clear from the swirling streamlines that there are at least two large vortices in the flow. 

The data required to plot these streamlines and velocity contours are in the form of a matrix organized as [x, y, u, v]. Here x,y are the Cartesian coordinates and u,v are the two corresponding components of velocity. 

```
import numpy as np
import matplotlib.pyplot as plt
from scipy.interpolate import griddata

file_Vel= 'Vel_%d.dat' % (i)
file_Vort= 'Vort_%d.dat' % (i)
u,v = np.loadtxt(file_Vel, usecols=(2,3), unpack=True)
x,y,u,w = np.loadtxt(file_Vort, usecols=(0,1,2,3), unpack=True)

```



I was very impressed when I first came across matplotlib (or Python for that matter). As a novice grad student I would laboriously make plots and implement changes using different gui based plotting software. Sure, there was MATLAB to take care of programming needs, but I could never take work 'home', so to speak. Due to reasons I wouldn't want to delve in here, I realized running Python on my mediocre-performance laptop was the thing that I needed in my life. 


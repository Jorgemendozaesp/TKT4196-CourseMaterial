---
layout: default
title: INDEX
---

# TKT 4196

- [About the course](about)
- [Teaching team](team)
- [Autumn 2020 semester](fall2020)
- [Getting started with Python](py_guide)


# NEWS
## Week 43

I see that many groups are struggling with the 3D plots. I write here a hint to help this part. Assuming that you have a function f1 which outputs the reliability index and inputs as first argument the diameter and as second argument the height, a code to plot the reliability index as a function of the diameter and height is as follows:

```
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

PHI = np.linspace(0.2,1,15)
H = np.linspace(5,20,15)

pp,hh = np.meshgrid(PHI,H)
BETA = np.zeros_like(pp)

for idx_p in range(len(PHI)):
    for idx_h in range(len(H)):
        BETA[idx_p,idx_h] = obj.f1(pp[idx_p,idx_h],hh[idx_p,idx_h])
        
fig = plt.figure()
ax1 = fig.add_subplot(111, projection='3d')
surf = ax1.plot_surface(pp, hh, BETA,cmap=plt.cm.coolwarm)
ax1.set_xlabel('$\phi$')
ax1.set_xlim(PHI[0],PHI[-1])
ax1.set_ylabel('$h$')
ax1.set_ylim(H[0],H[-1])
ax1.set_zlabel(r'$\beta$')
plt.tight_layout()
plt.show()
```

| Compend. | Type |     Topic                                                 |	Lecturer |	Date       | Location |
|----------|------|-----------------------------------------------------------|----------|-------------|----------|
| CE2/CE3  | E    |Solution and discussion CE2/Introduction to CE3 (Code calibration)|	  M 	   | ti. 20.10	 |  S4      |
|  CE3     | P    |     Self study / Q&A Sessions                             |   M      | on. 21.10	 |  KJL1    |
|  Ch5     | T    |  Engineering Uncertainty Modelling I                      |   K      | fr. 23.10   |	KJL1    |

# UnderGradSolidState
Last year I got the chance grading the undegrad solid state physics at the University of Chicago. When preparing the solutions to the homeworks I realized that students might get more feelings if the some of the statements could be visualized. In particular, there's a fair amount of random knowledge most students (after taking undergrad quantum mechanics) did not master. In this repo I collected and uploaded some plots I prepared for the course.


### Density of States of simple tight-binding model

![plotting the density of states](https://github.com/whhsiao/UnderGradSolidState/blob/master/PlotOfDos.png)

### Effective mass of Kronig-Penney model
The Kronig-Penney model is a single-particle quantum mechanical problem that gives rise to the band structure. In a word, it describes a single quantum particle running in a periodic potential profile. Usually the potential is modeled by an array of Dirac delta function. Details can be found in the following Wiki page.

<https://en.wikipedia.org/wiki/Particle_in_a_one-dimensional_lattice>

To solve the energy, very often we have to solve a transcendental equation. In this case it's the following


![energy equation for Kronig Penney](https://github.com/whhsiao/UnderGradSolidState/blob/master/KronigPenneyEqn.png)

Given a value of _P_ (strength of the potential) and a quantum number (quasi momentum ) _k_, one can solve the value of the energy _E_. The curvature of dispersion is usually characterized by the effective mass defined as follows.  

![inverse of meff](https://github.com/whhsiao/UnderGradSolidState/blob/master/meff.png)

This effective mass is usually evaluated at the bottom of the top of the band. In this case, _k_ = 0 or _k_ = pi. We present the explicit equations to solve.

At _k_ = 0,

![k equal 0](https://github.com/whhsiao/UnderGradSolidState/blob/master/kEqZero.png)

At _k_ = pi,

![k equal pi](https://github.com/whhsiao/UnderGradSolidState/blob/master/kEqPi.png)

Solving these equations numerically and plugging the solutions into the expressions of effective mass, we can plot the effective masses as functions of potential strength. The code for this plot is given in the effectivemass.nb.

![plotting the inverse of meff](https://github.com/whhsiao/UnderGradSolidState/blob/master/PlotOfMeff.png)

### Chern number of Qi-Wu-Zhang model


![plotting the Chern number ](https://github.com/whhsiao/UnderGradSolidState/blob/master/PlotOfChern.png)

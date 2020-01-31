# UnderGradSolidState
Last year I got the chance grading the undegrad solid state physics at the University of Chicago. When preparing the solutions to the homeworks I realized that students might get more feelings if the some of the statements could be visualized. In particular, there's a fair amount of random knowledge most students (after taking undergrad quantum mechanics) did not master. In this repo I collected and uploaded some plots I prepared for the course.


### Density of States of simple tight-binding model
One of the fundamental feature of quantum physics is that a system cannot possess arbitrary energy. Given proper quantization conditions, a system can only take specific values of energy. Conversely, we can also quantify the number of the states (per unit volume) within a range of energy. This is the notion of density of states. Formally, it is given by the following equation

![Equation of Density of State](https://github.com/whhsiao/UnderGradSolidState/blob/master/densityOfState.png)

where the sum is taken over allowed energy levels. In the notebook we plot the density of states for a 2-dimensional lattice tight-binding model. For this particular model, the sum over nu can be replaced by a integral over Brillouin zone. More explicitly,

![integral representation of density of state](https://github.com/whhsiao/UnderGradSolidState/blob/master/ExDOS.png)

To perform the integral involving Dirac delta function, we use the following approximation sequence. 


![Dirac delta function](https://github.com/whhsiao/UnderGradSolidState/blob/master/DeltaMeasure.png)

Schematically, we use the notebook to plot 

![the integral we plot](https://github.com/whhsiao/UnderGradSolidState/blob/master/NumerIntegral.png)

The plot here is generated with epsilon = 0.01

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

Chern number is a quantity that characterizes phases of insulators. In the context of material science insulators are considered boring. However, they can be boring in different manners. Since the inception of the era of topological materials, scientists strive to look for those insulators that are boring in some non-trivial ways. One of the indicator is the Chern number of an insulator model. 

In this question, we consider the famous Qi-Wu-Zhang model and compute the Chern number as a function of chemical potential.

![plotting the Chern number ](https://github.com/whhsiao/UnderGradSolidState/blob/master/PlotOfChern.png)

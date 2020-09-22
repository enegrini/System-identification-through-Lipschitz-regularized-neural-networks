# System Identification with Lipschitz Regularized Neural Networks

### Problem Statement and Solution Approach
We use neural networks to learn governing equations from data. Specifically
we reconstruct the right-hand side of a system of ODEs <img src="https://render.githubusercontent.com/render/math?math=\dot{x}(t)=f(t, x(t))"> directly
from observed uniformly time-sampled data using a neural network. In contrast with
other neural network based approaches to this problem, we add a Lipschitz regularization
term to our loss function. In the synthetic examples we observed empirically that
this regularization results in a smoother approximating function and better generalization
properties when compared with non-regularized models, both on trajectory and
non-trajectory data, especially in presence of noise. In contrast with sparse regression
approaches, since neural networks are universal approximators, we don’t need any prior
knowledge on the ODE system. Since the model is applied component wise, it can
handle systems of any dimension, making it usable for real-world data.

### Some Experimental Results
We report here some results obtained when recovering the non-autonomousODE <a href="https://www.codecogs.com/eqnedit.php?latex=\dot{x}(t)&space;=&space;e^{-x}\log(t)&space;-&space;t^2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\dot{x}(t)&space;=&space;e^{-x}\log(t)&space;-&space;t^2" title="\dot{x}(t) = e^{-x}\log(t) - t^2" /></a> with 1% noise in the data. For a fixed training Mean Squared Error (MSE), regularized networks always attain a better test error than the non-regularized one (Table). 

This can be clearly seen in the error plots where the test error for the non-regularized network (left figure) is compared with the one from best regularized network (right figure). Darker gray level represents lower error.

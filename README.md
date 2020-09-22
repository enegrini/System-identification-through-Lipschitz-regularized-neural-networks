# System Identification with Lipschitz Regularized Neural Networks
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

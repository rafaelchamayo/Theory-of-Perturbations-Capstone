## Introduction


This project will explore the formal quantum mechanical derivation of Miller's rule using a 1D Morse potential. We move from the classical Lorentz model to show how second order nonlinear susceptibilities can be expressed as a produce of linear susceptibilities.

We:
1. implement a numerical solver for the TDSE to verify that the Miller delta $\delta$ remains frequency independent when the adiabatic switch on parameter $\gamma$ is scalled according to the susceptibility orders.
2. Do a formal, mathematical derivation of Miller's rule for the case of a 1D (or possibly more dimensions!) Morse potential.


## Hamiltonian

Modeltthe system as aparticle of mass $m$ and charge $q$ 

$$ H(t) = \frac{p^2}{2m} + V_{morse}(x) - qxE(t) $$

Where

$$ V_{morse}(x) = D_e(1-e^{-a(x-x_e)})^2 $$

for equilibrium position $x_e$, well depth $D_e$, and width $a$. To establish the Miller relation via perturbation theory, we consider the taylor expansion of the morse potential around the equilibrium position $x_e$. TO introduce broadening without the classical "phenomenological" damping, we use the adiabatic switch on:

$$E(t) = E_0 \cos(\omega t) e^{\gamma t}$$

for ${\gamma > 0 }$, and the limit ${\gamma \rightarrow 0}$ is taken to recover the steady state response (and monochromatic).


## Using UV python package manager


Clone the repository 

``` bash
git clone git@github.com:rafaelchamayo/Theory-of-Perturbations-Capstone.git
cd Theory-of-Perturbations-Capstone
uv sync
```

`uv sync` will update your python environment with the dependencies (python packages you will use) specified in your pyproject.toml. If you would like to add more dependencies, run `uv add <python package name>`.

Then to run any python scripts you write inside this uv managed python environment, use

``` bash
uv run <path to python script> # for example uv run python/main.py
```



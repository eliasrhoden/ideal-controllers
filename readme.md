# Ideal controllers for simple systems

For linear control design, a powerful technique is to compute the *ideal controller* by model inversion.

Given a plant $G(s)$ and a desired closed loop response, a *reference model* $M(s)$ (that have the same relative degree as the plant)

$$
\dfrac{C(s)G(s)}{1 + C(s)G(s)} = M(s)
$$

solving for the controller $C(s)$ we get

$$
C(s) = \dfrac{M(s)}{1 - M(s)} G^{-1}(s)
$$

Note that this requires that $G(s)$ is invertible!

For PT1 and PT2 systems, these ideal controllers are PI and PID controllers, in the jupyter notebook I've gatered the equations for:

* First order system (PT1) - PI Controller
* Second order system (PT2) - PID Controller

This can be usefull for adaptive control, inital parameters for numerical optimization, or maybe a simple autotuner. 

Often when you design and optimize the control parameters you perform a numerical optimization in relation with a nonlinear simulation or nonlinear objective. These optimizations require an intial guess of the parameters.


## Controller structure - PI controller

$$
C_{PI}(s) = K_p(1 + \dfrac{1}{sT_i})
$$

## Controller structure - PID controller
Including filter on derivative term, $T_f$.

$$
C_{PID}(s) = K_p(1 + \dfrac{1}{sT_i} + \dfrac{sT_d}{sT_f + 1})
$$



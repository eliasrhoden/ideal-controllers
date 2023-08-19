# Ideal controllers for simple systems

Often when you design and optimize the control parameters you perform an optimization in relation with a nonlinear simulation or nonlinear objective.

These methods often require an *inital guess* of the *optimial* control gains. Here are a solution for 

* First order system (PT1) - PI Controller
* Second order system (PT2) - PID Controller

## Controller structure - PI controller

$$
C_{PI}(s) = K_p(1 + \dfrac{1}{sT_i})
$$

## Controller structure - PID controller
Including filter on derivative term, $T_f$.

$$
C_{PID}(s) = K_p(1 + \dfrac{1}{sT_i} + \dfrac{sT_d}{sT_f + 1})
$$



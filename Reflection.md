# PID Control Project Reflection - Braulio Chavez

P stands for Proportional. The "Proportional" section of the algorithm
is `-Tau_P * CTE` (CTE: Crosstrack Error). This section alone only
accomplishes a marginally stable steering angle. Which means the
steering angle will go up and down without converging causing the car to
oscillate which can cause the user to get very seasick. I chose a
`Tau_P` coefficient of 0.2 doing manual tuning.

I stands for Integral. This section is represented by `-Tau_I *
Sum(CTE)`. Takes into consideration all the crosstrack errors across
time and compensates for bias (ie. bias in wheels angles). In this
project I chose a `Tau_I` coefficient of 0, because our car has no bias.

D stands for Differential. This portion of the algorithm is `-Tau_D *
differential(CTE)`. The differential helps the algorithm converge and
aids the car to oscillate less. I chose `Tau_D` coefficient of 3.0 doing
manual tuning.

Here's a video of the PID Control in action in a simulated environment
[PID Control Video](https://youtu.be/re-q_VnME6I)

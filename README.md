# University of Washington Husky Satellite Lab (HSL) Multiplicative Extended Kalman Filter (MEKF)

The system/state combination we have picked to filter is a CubeSat and its attitude. The rotation dyanmics of a satellite is commonly represented by a quaternion due to its avoidance of gimbal lock and easy normalization of the attitude representation.

Quaternions are, by nature, nonlinear in their dynamics/update equation. This means that at least an Extended Kalman Filter (EKF) is required to model the system effectively. However, since quaternions are groups, not vectors, the "vector addition" attempted by the posterior state correction does not represent a valid rotation.

Renormalization can work, but the more elegant solution is a Multiplicative Extended Kalman Filter (MEKF).

## References

[1] The Multiplicative Extended Kalman Filter, https://matthewhampsey.github.io/blog/2020/07/18/mekf

[2] https://apps.dtic.mil/sti/tr/pdf/ADA588831.pdf

# Double chirp paper simulation data

All figures in the paper are generated using the mass ratio 3 run (`q3/`). We have also included data for mass ratios 2, 5, 6, and 10 in the directories `q2/`, `q5/`, `q6/`, and `q10/`, respectively. Each simulation contains the following data files:

- `psi4analysis_r75.00.asc`: ASCII timeseries data for total radiated energy, momentum, and angular momentum as well as their time derivatives. Calculated using a spherical extraction surface at $r = 75.00 M$.
- `Psi4.xy.h5`: 2D HDF5 data for the real and imaginary parts of $\Psi_4$ in the orbital plane of the binary.
    - `WEYLSCAL4::Psi4i*` datasets: Imaginary part of $\Psi_4$.
    - `WEYLSCAL4::Psi4r*` datasets: Real part of $\Psi_4$.
- `horizons/VAR.t*.ah{123}.gp`: Values of VAR (see below) at every point on each horizon for a given iteration. The `t*` portion of the file name specifies the iteration (timestep) at which the horizon was found. The `ah{123}` portion specifies which horizon the data is for (`ah1` and `ah2` are the individual horizons and `ah3` the common horizon).
    - `h`: The cartesian coordinates of each point on the horizon.
    - `s_{ij}`: Components of the induced metric on the horizon $s_{ij} = \gamma_{ij} - n_i n_j$.
    - `mean_curvature`: The mean curvature on the horizon $H = \nabla_i n^i$.

## Relevant iterations for each figure
- Figure 3
    - Panel `t1`: 24864
    - Panel `t2`: 28032
    - Panel `t3`: 32448
    - Panel `t4`: 36192
- Figure 4: 26368

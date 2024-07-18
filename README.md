# Julia-MCRTE

A Julia implementation of the Monte Carlo simulation method to solve the radiative transfer equation. There are two Jupyter notebooks in this repository.
1. ``MC-Julia`` solves the radiatve transfer equation in a semi-infinite half space, $z > 0$, composed of a uniform absorbing and scattering medium. The only source of light is an infinitessimally narrow pencil beam incident normally on the boundary $z = 0$. Scattering is governed by the Henyey-Greenstein phase function. Included is the data set ``MCMLdata.Rr`` computed using the pre-compiled PC version of ``MCML`` available at https://omlc.org/software/mc/. The input file used ``halfspace.mci`` is also included here.
2. ``MC-rescaledRTE`` solves rescaled radiative transfer equation that is used to derive the asymptotic behavior of the reflectance due to a narrow beam where the beam width is the smallest length scale in the problem. Included in this Jupyter notebook is the computation of the influence integral and the asymptotic approximation for the reflectance. That result is plotted with the Monte Carlo simulations result for comparison.

These codes make use of the following Julia libraries.
* ``Dates``
* ``DelimitedFiles``
* ``SpecialFunctions``
* ``FastGaussQuadrature``
* ``PyPlot``
* ``LaTeXStrings``

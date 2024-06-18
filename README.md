# Results of the fits of MW globular clusters using GCfit

- `clusters/`
  + `NGC*/`
    * Output files from all sampling runs, for each cluster (see below)
    * Parameter posteriors, marginal distributions, black hole probability distributions, kinematic profiles, cumulative mass profiles and mass function confidence intervals, for each cluster
    * Core collapsed clusters are also shown without BHs under `no_BHs/`

- `parameters/`
  + Summary (machine-readable) table of all best-fitting parameters with statistical uncertainties
  + All figures represent the final sample of clusters as used in paperI (i.e. including ω-cen, with bad fits removed and with fixed core-collapsed clusters), after refits for paperII. See the papers (or `paper{I,II}_figures/`) for cleaner plots.
  + `comparisons/`
    * Distance, remnant fraction, mass, half-mass radius and BH mass comparisons with various literature values
  + `distributions/`
    * Violin plots of distributions of all parameters, for all clusters
  + `relations/`
    * Relationships between all parameters, and all parameters with dynamical age, remaining mass fraction, and orbital parameters

- `thesis_figures/`
  + All figures from the MSc thesis corresponding to this work
  + These are most likely out of date, but shown here for posterity

- `paperI_figures/`
  + All figures from paperI (Multimass modelling of Milky Way globular clusters I. Implications on their stellar initial mass function above 1 Msun)
  
- `Gaia_profiles`
  + All extracted Gaia EDR3 proper motion dispersion profiles


## Using sampler output files

The sampler outputs from all of the fitting runs, including parameter chains,
likelihoods, priors, nested bounds, etc., are available for each cluster,
as HDF5 files (`clusters/NGC*_sampler.hdf`).

For more instructions and information on using these outputs and recreating the
models, see the [GCfit documentation](https://gcfit.readthedocs.io/en/develop/usage/analysis_usage.html#fitting-results).

# Gaia radial proper motion dispersion profiles

Contains the profiles of radial and tangential proper motion dispersions
extracted from Gaia EDR3 data, binned radially, for all clusters in our sample.

Profiles are contained in an HDF5 file, with datasets:

- `R`, `eR`: Median and standard deviation of the cluster-centric radius of all stars in each bin
- `pmr`, `epmr`: Best-fitting radial PM dispersion (mean and 1σ) for each bin
- `pmt`, `epmt`: Best-fitting tangential PM dispersion (mean and 1σ) for each bin

Units on all radii are "arcmin" and on all proper motions are "mas/yr".

### See paperI for more details.

Profiles can easily be extracted in Python using `h5py`:
```
import h5py

f = h5py.File('NGC0104_profiles.hdf', 'r')
r, μ_R, μ_T = f['R'], f['pmr'], f['pmt']

# Units are stored as attributes on each dataset
import astropy.units as u
r = f['R'] << u.Unit(f['R'].attrs['unit'])

# Metadata surrounding the dispersion fitting stored as attributes on the file
stars_per_bin = f.attrs['Nstars']
min_membership_prob = f.attrs['memberprob']


f.close()
```

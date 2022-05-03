# honeyShrinkage

A python implementation of:

```plain
O. Ledoit and M. Wolf, 
“Honey, I Shrunk the Sample Covariance Matrix,” 
JPM, vol. 30, no. 4, pp. 110–119, Jul. 2004, 
doi: 10.3905/jpm.2004.110.
```

Usually, Ledoit-Wolf shirnkage is implemented to shrink towards a common variance [1],
this code however follows the proposed shrinkage target implemented in [0] and shrinks
towards a constant correlation.

The difference is inclusion of the rho-factor (see publication and code).

## Attribution

This code is a translation of the authors original code `covcor.m` from Matlab to Python and thus derived work.
The original code, and the derived code in this repository, are BSD 2-clause license licensed.

Original code accessed on 31.01.2022 from [here](https://www.econ.uzh.ch/en/people/faculty/wolf/publications.html#programming_code), [direct link](https://www.econ.uzh.ch/dam/jcr:ffffffff-935a-b0d6-ffff-ffffde5e2d4e/covCor.m.zip) also see the [paper](https://www.econ.uzh.ch/dam/jcr:ffffffff-935a-b0d6-ffff-ffffb4762fbf/honey.pdf).

## Installation - from this Repo

```terminal
pip install git+https://github.com/jkschluesener/honeyshrinkage@v1.0
```

## Usage

```python
from honeyShrinkage import covCor

n_samples, n_features = my_data_array.shape

sigma, shrinkage = covCor(my_data_array)
```

## References

```plain
[0]: O. Ledoit and M. Wolf, 
     “Honey, I Shrunk the Sample Covariance Matrix,” 
     JPM, vol. 30, no. 4, pp. 110–119, Jul. 2004, 
     doi: 10.3905/jpm.2004.110.
[1]: O. Ledoit and M. Wolf, 
     “A well-conditioned estimator for large-dimensional covariance matrices,” 
     Journal of Multivariate Analysis, vol. 88, no. 2, pp. 365–411, Feb. 2004, 
     doi: 10.1016/S0047-259X(03)00096-4.
```

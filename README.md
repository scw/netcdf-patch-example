# netcdf-patch-example

An example package illustrating [the issue](https://github.com/conda/conda-build/issues/2307) using the `patch` anaconda package as-is with a diff generated patch file.

Instructions to reproduce on Windows:

```
# first, install miniconda, activate root environment.
conda install conda-build patch
git clone https://github.com/scw/netcdf-patch-example
conda build --python=3.6 netcdf-patch-example
```

The simple solution is to instead install the msys2 `patch`:
```
conda remove patch
conda install m2-patch
```

# Sparse Matrix

## Exercise

I implemented
* BiCG and BiCGstab
* CRS method(CSR)
for understaning the mechanism.

## Future plan
* Multi Color ordering
* Cuthill_Mckee method


## Fortran magic

You can use Fortran code in Jupyter notebook if you install fortran-magic through python-pip.

```shell:
pip3 install -U fortran-magic
```

In jupyter notebook, 

```python:
%load_ext fortranmagic  # activating fortran-magic
```

```python:
In[1] %%fortran
       subroutine solve(x, y, z)
            real, intent(in) :: x(:), y(:)
            real, intent(out) :: z(size(x))
            z(:) = sin(x(:) + y(:))
       end subroutine solve
       
 In[2] solve([1, 2, 3], [4, 5, 6])
 array([-0.9589243,  0.6569866,  0.4121185], dtype=float32)
```
[fortran-magic example](http://arogozhnikov.github.io/2015/11/29/using-fortran-from-python.html)
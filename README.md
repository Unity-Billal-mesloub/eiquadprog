# eiquadprog

[![Coverage report](https://gitlab.laas.fr/stack-of-tasks/eiquadprog/badges/master/coverage.svg?job=doc-coverage)](https://gepettoweb.laas.fr/doc/stack-of-tasks/eiquadprog/master/coverage/)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/stack-of-tasks/eiquadprog/master.svg)](https://results.pre-commit.ci/latest/github/stack-of-tasks/eiquadprog)

This repo contains different C++ implementations of the algorithm of Goldfarb and Idnani for the solution of a (convex) Quadratic Programming problem by means of a dual method.

The problem is in the form:
 min 0.5 * x G x + g0 x
 s.t.
 CE^T x + ce0 = 0
 CI^T x + ci0 >= 0

There are 3 implementations:
- `eiquadprog.hpp`: the original C++ implementation
- `eiquadprog-fast.hpp`: an improved version employing a wrapper, avoiding dynamic memory allocation
- `eiquadprog-rt.hpp`: similar to the above, it employs fixed-size Eigen vectors. This requires the problem dimensions to be known at compile time and is recommended only for small problems.

Please refer to the unit tests for examples of usage.

## Authors

[Eiquadprog](https://github.com/Unity-Billal-mesloub/eiquadprog) was created at LAAS-CNRS by Gabriele Buondonno, based on
parts from [TSID](https://github.com/Unity-Billal-mesloub/tsid) by Andrea Del Prete.

This work was based on previous libraries:
- [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub)


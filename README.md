# mccs OCaml library

mccs (which stands for Multi Criteria CUDF Solver) is a CUDF problem solver
developed at UNS during the European MANCOOSI project.

This repository contains a stripped-down version of the
[mccs solver](http://www.i3s.unice.fr/~cpjm/misc/mccs.html), taken from snapshot
1.1, with a binding as an OCaml library, and building with `jbuilder`.

The binding enables interoperation with binary CUDF data from
[the OCaml CUDF library](https://gforge.inria.fr/projects/cudf/), and removes
the native C++ parsers and printers.

While mccs itself natively supports a wide array of underlying solvers (integer
programming or pseudo-boolean), at the moment, the build system is set to link
with [glpk](https://www.gnu.org/software/glpk/) only. It will also advertise as
much static linking as possible, in order to generate portable executables.

Build using `opam install .` (opam 2.0), or `jbuilder build`.

Note: this depends on a C++ compiler, and was only tested with g++.

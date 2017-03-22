# Build It PureScript

Bips is a PureScript build tool that wraps Pulp.

Running `bips build` or `bips test` will:

 1. Run `make -f prepare.make all` in all `purescript-*` Bower dependencies, as
    well as in the working directory.
 2. Invoke `pulp build` or `pulp test`, respectively.

The `all` tasks in the `prepare.make` files should put PureScript source files
in a directory called `gen`. Bips will pass these `gen` directories to Pulp
using the Pulp `-I` option.
